---
layout: single
title: Don't Inject My SQL Bro
---
My first introduction to hacking was when I stumbled upon the wonderful feature film **Hackers** starring Angelina Jolie and Jonny Lee Miller. This was a delightfully 90s movie about some grungy hackers who stumble upon this greedy corporate cyber security employee who plans to release a horrible computer virus. As the good hearted hackers that they are, they decide to stop this guy through all of their tricks of the trade:

![hackers.gif](https://media.giphy.com/media/Q2W4hziDOyzu0/giphy.gif)

Awesome right? Well now obviously hacking has become a lot more mainstream and even pretty popular in the media since the huge Target and Home Depot hacks that occurred recently. One method of accessing data that those pesky hackers use is going to be the topic today and that topic is SQL injection.

Other than sounding like some shot that you get to prevent a nasty disease, SQL injection is a method that is used by hackers to access information that is stored in database servers. These servers store all of the pertinent user information for whatever website the hacker is trying to access. So they could potentially find personal information, bank account and credit card numbers, even social security numbers. So obviously you can see the danger in something like this being possible within your website. How this works essentially is that hackers can use different inputs on login pages or any place that accepts user input (rather than a login name they would use a portion of SQL code) and that will trick the database servers into divulging whatever information the hacker wants. Here is an example of what a potential SQL injection would look like:

![sqli.png]({{ site.baseurl }}/assets/images/SQLi-min.png)

Basically when you type in your login name on a website, the application will check to see if the login you entered exists in the user database and if it returned as true, the website will log in that particular user. When you pass in code like the example above, it will evaluate to true and since the application doesn't know which user to choose, it will choose the first user in the database and log him or her in. Scary stuff, but it is preventable and that is what we will discuss next.

SQL injection is a pretty well know method of accessing sensitive information nowadays so people have had lots of experience in preventing it. You just have to educate yourself with that information to make sure no one can get to all of the information in your website.

* The first thing you can do is use input validation for your login information which will check the data that is submitted for a login against a defined set of rules for length, type, and syntax. Basically this will make sure that data that is passed in by a user will be within a certain set of rules so it is unlikely that the website will accept something that isn't a proper input.
* Secondly, you can encrypt the sensitive data in your databases which would render anything that hackers could access completely useless as they couldn't understand it.
* Also, part of the way hackers access information is through SQL error messages so you can format your error messages to divulge as little information as possible.
* Finally, if you have users that have permission to access sensitive data, make sure that they have the least privileges which will make it very difficult for the data to be accessed without proper authentication.

As you can see, SQL injection is a big issue with internet security and it is one of the bigger ways that sensitive data is stolen in this day and age. However there are ways to stop it so when you are designing your website, make sure to think about how to prevent SQL injection and keep all of your precious data safe!
