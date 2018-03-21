---
title: Introduction
date: '2018-03-19T19:00:56-05:00'
module: java
order: 0
---

## Documentation and Resources

As we go into details of any programming language, you'll find that documentation is your best friend for learning and improving your language skill set:

* [Java Oracle Docs](https://docs.oracle.com/javase/9/)

## Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by a compiler and are just there to help us programmers understand the code better.

You'll use comments for documentation and explanation of your code. Anytime you see comments, just know it's there for clarity.

### Line Comment

Also known as single-line comment, line comment syntax is prepended with `//`

```java
// Example line comment
```

### Block Comment

Also known as multi-line comment, block comment syntax is surrounded with `/* */`. Also, though not required, this block comment syntax usually contains a `*` at the beginning of each new line.

```java
/* Example
 * block
 * comment
 */
```

## Source Code Line Termination

Unless otherwise specified, each line of source code in Java must be terminated with a `;`

```java
// Here is a simple variable assignment
String message = "Hello World";
```

## Case Sensitivity

Unless otherwise specified, the Java language *IS* case sensitive. `User` is distict from `user`.

## Output

When working with programming languages, at times you'll want to output something for your user or yourself. Also, at times, you'll want to read user input. In most languages, this is made available. Don't worry if this doesn't make total sense yet. We'll get there.

```java
// Write a message to the console
System.out.println("Message to write out");
```

Output:

```output
Message to write out
```
