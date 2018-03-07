---
layout: single
title: Blocks, Procs & Lambdas
---
Ruby has a ton of methods readily available for you to use right off of the bat and there are some methods that can be passed a piece of code as an argument (sometimes it's even required.) These little snippets of code are what we call blocks in Ruby (they are also known as closures in some other languages if you happen to recognize the name from another language you know.) While all of the names and terminology can get a little confusing, I will try and help to clarify with some examples. Here is a really basic example of a block:

```
number_array = [1, 2, 3, 4]
number_array.map { |number| number += 1} # <-- the part with the {} is the block

#=> [2, 3, 4, 5]
```

As you can see in the example above, we created an array of numbers and used the .map method to create a new array of those numbers incremented by 1. That snippet of code in the curly brackets {} is what we call a block. Now we move onto procs which is where it gets a little interesting (and confusing).

So the simplest way to explain a proc is that it is a block that has been "objectified" or basically turned into an object so Ruby can manipulate it in the same way it does the rest of its objects. Creating a proc is pretty simple as it is created with the same basic instantiation syntax in which you could create arrays or classes. Check it out below to see how a proc is created:

```
my_proc = Proc.new { puts "I'm a proc!"}
my_proc.call

#=> I'm a proc!
```

So you see in the example above that we pass in a block to the `Proc.new` call and what Ruby does when it sees this is take that snippet of code in the block, creates a proc and saves that in the variable `my_proc`. Then we can call that proc with the `.call` method because it is an object now and voila! You have just created and called your very own proc. Now obviously this is a very basic use of a proc but it gives you an idea of how they are created. One great more in-depth use of procs is using them as closures which is best described for me in the *Well Grounded Rubyist*:

> "Creating a closure is like packing a suitcase: wherever you open the suitcase, it contains what you put in when you packed it."

So basically you can create a code snippet that does something and whenever you return to that object in your code, it will be just the way you left it, no matter what you did in the code prior to that. Also, you can see that procs are dependent on blocks and thus interrelated. Now onto lambdas which are also dependent on blocks. Another interesting aspect of procs is that they don't care about the number of arguments passed in so you won't get an ArgumentError if you happen to pass in too many or too few. Let me show you an example of how this works:

```
my_proc = Proc.new { |string| puts string }
my_proc.call("Hello World!", "Supercalifragilisticexpialidocious")

#=> Hello World!
```

Normally this would throw an error in other circumstances but in the case of this proc, it takes the first argument passed in an ignores the rest of them and runs the code block with the first argument. Neat!

Lambdas are actually a fancy version of procs that have a few more constraints but they are created similarly to procs. Here are some of the things that differentiate lambdas from procs:

* Lambdas have to be created explicitly. There are ways Ruby creates procs implicitly (check out the &block syntax) but these are regular proc and not lambdas. They must always be created with the lambda assignment</li>
* Lambdas and procs treat the `return` keyword differently. If you use `return` in a proc, it ends the code running inside of the containing object. However with lambdas, when `return` is used, Ruby ends the code in the block of the lambda and continues on with the code following the lambda</li>
* Thirdly, lambdas do care about the number of arguments provided unlike procs.</li>

Let me show you how you can create a lambda:

```
my_lambda = lambda {puts "Hey there. I'm a lambda!"}
my_lambda.call

#=> Hey there. I'm a lambda!
```

Hopefully, this has helped to shed a little light on blocks, procs, and lambdas and now you can better understand when to use them in your code. I know it seems a little cryptic because they are all so interdependent but the more time you spend with them, the clearer it will become.
