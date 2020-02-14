---
title: Var and Duck Typing
date: '2-6-2020'
module: javaScript
order: 0
---

## Why

[JavaScript is a programming language](https://www.fraudlabspro.com/resources/tutorials/add-fraudlabs-pro-agent-javascript-bigcommerce/) used primarily by Web browsers to create a dynamic and interactive experience for the user. Most of the functions and applications that make the Internet indispensable to modern life are coded in some form of JavaScript. In the past, Web pages were static, offering little user interaction beyond clicking links and loading new pages. For the first time, JavaScript enabled animation, adaptive content and form validation on the page. Initially, JavaScript compatibility was a major issue across the most common platforms.

Some of the dynamic website enhancements performed by JavaScript are:

* Autocomplete

* Loading new content or data onto the page without reloading the page

* Rollover effects and dropdown menus

* Animating page elements such as fading, resizing or relocating

* Playing [audio and video](https://www.bigcommerce.com/blog/product-video-marketing-examples/)

* Validating input from Webforms

* Repairing browser compatibility issues

Duck typing gives a programmer the ability to not worry about the type of an object rather perform the required operations. This allows a programmer to save time and optimize performance. It's been said that duck typing in general cuts down development time. There's less boilerplate code and gives programmers flexibility.

## What

Javascript is an Interpreted language, meaning the interpreter assigns variables a type based on the variable’s value at run-time.

Moreover, Interpreted languages are languages that are not compiled but are parsed on the fly.  Javascript and other languages fall into this category as you don’t have a compile step prior to running.  Simply save the script and refresh.

When referring to Duck Typing, many use the saying,

“If it quacks like a duck, walks like a duck...it’s a duck”

This can initially be confusing...

Duck Typing refers to a duck test program. You will test something, if it goes like a duck, and fly like a duck, it is a duck. If a method responds to any given object call, it passes the **“Duck Test”.**

**Duck Typing** is a feature in javascript where the variable attempts to behave in the manner it is used.  So if it’s used as a string it’s a string etc.

In C# or other statically typed languages, passing methods into objects is deemed suitable based on its type. With duck typing, however, objects are determined whether or not suitable based on what it does, not what it is. It doesn’t matter the type if both objects do the same thing or better yet, have the same capabilities. If the method responds to the object call, basically as long as the object responds **TYPE DOESN’T MATTER!**

Duck Typing is polymorphism w/o hierarchy, dynamic dispatch w/o inheritance hierarchy, and no explicit interfaces. Essentially checking for capability, not compatibility.  

Duck Typing is used in many programming languages, for example,  Ruby, Python,.. and it is really useful but sometimes it creates unwanted acts in application because the rules of  Duck Typing are too simple and can result in wrong conclusions. You can understand this warning more in examples.
