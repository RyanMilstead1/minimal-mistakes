---
layout: single
title: 'A Map of `.map`'
---
So one of the beautiful things about the Ruby programming language is it's plethora or useful enumerable methods that aid us in transforming and sorting collections. I'm sure you have heard or used some of these before: `.each, .sort., .collect, and .count`. What I want to give you an overview of today however is the `.map` method and how it sets itself apart in the long list of enumerable methods.

If you read a decent amount of information on the internet about `.map`, you will find that some people compare it somewhat to the .each method which is valid. You normally want to use the .each method if you want to take some collection of data and do something to each of the elements in that collection. `.map` takes the each method a little further though. Let me show you in an example below:

If you had an array of numbers and wanted to add 5 to each of those numbers you could use an each method that would look something like this

```
numbers = [7, 8, 29, 282]
numbers.each {|num| num + 5}
#=> [7, 8, 29, 282]
```

And you would think this would return all of the numbers in the array incremented by 5 but you would be wrong. The each method executes the block that you specify but then doesn't really do anything with the return value unless you specify in the code. This is where `.map` differs from the .each method.

``.map`` takes the `.each` method a step further by running the block that you pass in and taking the return value of each iteration and assigning it to a new object (in the instance of this example a new array) Check out the example below to see how the output differs from the .each method.

```
numbers = [7, 8, 29, 282]
numbers.map {|num| num + 5}
#=> [12, 13, 34, 287]
```

So as you can see from this example, using the `.map` method will automatically return an array with the altered elements so it helps you to create DRYer code (Don't Repeat Yourself.) If you have an array and you want to create a new array of altered elements then the `.map` method is the method for you. It will help to take a line or two out of your code because you can just assign the use of the `.map` method to a new variable and move on to the next step of your code.

As you can see, the `.map` method is not a very deep method but it can be very useful in the correct situations so I hope this has helped shed a little light for you and hopefully you will know when the `.map` method is right for you from now on.
