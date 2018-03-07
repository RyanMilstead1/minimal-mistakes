---
layout: single
title: 'Classes vs. IDs: The Battle of the Century'
---

When Joe Schmo decides to write an HTML file even the most basic of files will be filled with what we call tags. If you take a look at the example below, everything you see that is surrounded by <> is a tag:

```
<!DOCTYPE html>
<html>
<body>

  <h1>My First Heading</h1>

  <p>My First Paragraph</p>

</body>
</html>
```

Then when Joe wants to make off of his elements in his HTML page look nice and shiny this is where CSS comes in. CSS stands for Cascading Style Sheet and is an external file that styles all of the HTML elements. The CSS file will be filled with selectors that directly relate to the tags in the HTML and will style the content accordingly. Take a look below at the connected CSS styling.

```
body: {
  background-color: #d0e4fe;
}

h1: {
  color: orange;
  text-align: center;
}

p: {
  font-family: "Times New Roman";
  font-size: 20px;
}
```

Classes and IDs are two of the many versions of HTML selectors that can be used to selectively style your HTML elements in CSS. You might think these two selectors are pretty similar syntax wise (which they are) but they serve two very different purposes when you use them.

So let's say you are designing a blog post and you have several different headers assigned to your different paragraphs. You could just use the basic header tag selector in CSS and it would style all of those headers the exact same way. But wait! I want more control! I want to make all of my headers look different. This is where IDs come in.

To use an ID, you have to assign it in the HTML file. Inside of the tag, for example a h1 tag, you would follow the h1 with id="id-name". Now I know what you're thinking. "id-name" is a really boring name and I completely agree. That's the beauty of IDs. You can name them literally anything that your heart desires. You want a "princess-popcorn" ID. Done. "fresh-prince-of-bel-air" ID? You got it. While these ID names may not be the most concise names in the world, they are all your own. Your shiny new id can then easily be styled in CSS by using the id name in the CSS file in the same way you would use any CSS selector but the name must be preceded by a # to work properly. Then whatever styling you apply will be put on **only** that element. I think using the Miami font on that fresh-prince-of-bel-air id is a great idea too.

One thing you have to remember though, ID names can only be used once otherwise you could create a rift in the space-time continuum. Check out the CSS below to see how you would use ID styling in CSS:

```
#para1: {
  text-align: center;
  color: red;
}
```

But lets throw out another situation. Say that you are working on the same blog post with various paragraphs and headers and you want to style several different headers in one way and the rest of the headers in another way. Now you could apply specific IDs to each and every one of those headers but that seems a little silly doesn't it? Surely there is a better way of doing this. Classes to the rescue!

Classes are utilized very similarly to IDs. They are assigned in HTML after the tag name with `class="class-name"` and just like IDs, you can name them anything your little brain can think up. They beautiful thing about classes though, is that you can apply the same class to multiple elements and they will all be styled the same way. This also makes the styling in CSS a lot easier since you only need one selector and styling section as opposed to individual sections for each ID. Inside the CSS file instead of preceding the class-name with a # like you would with an ID, you use a "." Check out the CSS syntax below to see how classes are used:

```
.center: {
  text-align: center;
  color: red;
}
```

So as you can see, IDs and Classes are written and styled in a similar way but they are used in completely different circumstances. I am a strong advocate of learning by getting your hands dirty so get out there and experiment with classes and IDs and find out for yourself the best times to use one or the other but remember: IDs for individuals and Classes for groups.
