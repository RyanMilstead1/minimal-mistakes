---
layout: single
title: Class is in Session
---
Ruby is just one of the many object-oriented languages out there in the world but it has become so popular because it does what it does so well. At the base level, Ruby has most of the basic objects that you would expect in a language: strings, integers, floats, symbols, and the list goes on. While all of these things are considered objects each of them are also specific "classes" of objects.

Now, what is a class you ask? Well, essentially a class is just a specific collection of rules, parameters, and methods that apply to a particular object. If you create a "string" in your code that string is part of the String class and has specific things that it can and cannot do.

But let's say that you want to create some objects that don't exist in the normal library of Ruby classes? Well, you can create your very own class pretty easily. Let me show you how...

Let's say that you are a big comic book fan (as I am) and you want to create a way to keep information about your big catalog of comics contained neatly on your computer. This can be done very easily with a ruby Class. In the example below, I will create a new class and a method for that class that is pretty common with classes called an initialize method. What this does basically is create an instance of what information you want to store and allocates room for that info in the memory of your computer. It will look a little something like this:

```
class ComicBook
  def initialize(title, issue_num, condition)
    @comic_title = title
    @comic_issue_num = issue_num
    @comic_condition = condition
  end
end
```

Now I know what you're thinking. Why do those variable names have that weird @ sign in front of them? Well, those are magical little things called instance variables. These are better than typical local variables in a few ways that make them important to classes:

* They are created inside every instance of an object that you create and they are completely isolated to that sole object
* They are accessible by every other method that you create inside of the class, unlike local variables who are only available inside the method in which they are created
* Instance methods are inaccessible outside of the class unless you create a particular method that will allow you to view or edit those variables

So now we have created a new class that takes in some information about all of our classes. How would we create an instance of our new ComicBook class? Take a look below.

```
comic = ComicBook.new("The Incredible Hulk", 18, "mint")
```

All we have to do is assign a new instance of the ComicBook class to a variable and pass in the info as arguments. Easy as pie. Now you can take that variable and store it in an array to keep your catalog nice and neat and you are on your way.

But it doesn't have to be as simple as that. You can do countless things to your class to make them more interesting, accessible, and useful. Let's take a look at a little method that will take our comic book info and print it out to the console.

```
def info
  puts "Your comic, #{@comic_title}, is the #{@comic_issue_num} issue and is in
  #{@comic_condition} condition.}"
end
```

As you can probably tell, this method would take all of the info that you stored in the instance variable of your particular class object and display it all in a nice string to your console. So calling the method and its output would look like this:

```
comic.info

#=> Your comic, The Incredible Hulk, is the 18 issue and is in mint condition.
```

So hopefully that has helped you to understand the basics of classes a little more and if you build an awesome comic book collection with this you should totally let me come over check it out sometime.
