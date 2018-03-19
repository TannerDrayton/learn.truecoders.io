---
title: C# Course Material and Resources
---

* [Documentation and Resources](#documentation-and-resources)
* [Source Code Comments](#source-code-comments)
  * [Line Comment](#line-comment)
  * [Block Comment](#block-comment)
* [Source Code Line Termination](#source-code-line-termination)
* [Case Sensitivity](#case-sensitivity)
* [Output](#output)
* [Material](#material)

## Documentation and Resources

As we go into details of any programming language, you'll find that documentation is your best friend for learning and improving your language skill set:

* [C# Microsoft Walkthrough](https://msdn.microsoft.com/en-us/library/jj153219.aspx)
* [C# Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/csharp/)

## Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by a compiler and are just there to help us programmers understand the code better.

You'll use comments for documentation and explanation of your code. Anytime you see comments, just know it's there for clarity.

### Line Comment

Also known as single-line comment, line comment syntax is prepended with `//`

```csharp
// Example line comment
```

### Block Comment

Also known as multi-line comment, block comment syntax is surrounded with `/* */`. Also, though not required, this block comment syntax usually contains a `*` at the beginning of each new line.

```csharp
/* Example
 * block
 * comment
 */
```

## Source Code Line Termination

Unless otherwise specified, each line of source code in C# must be terminated with a `;`

```csharp
// Here is a simple variable assignment
var message = "Hello World";
```

## Case Sensitivity

Unless otherwise specified, the C# language *IS* case sensitive. `User` is distict from `user`.

## Output

When working with programming languages, at times you'll want to output something for your user or yourself. Also, at times, you'll want to read user input. In most languages, this is made available. Don't worry if this doesn't make total sense yet. We'll get there.

```csharp
// Write a message to the console
Console.WriteLine("Message to write out");
```

Output:

```output
Message to write out
```

## Material

Awesome, let's get your [System Setup](system.markdown) and move onto our materials:

* [Variables](variables.markdown)
* [Types](types.markdown)
* [Methods](methods.markdown)
* [Operators](operators.markdown)
* [Statements](statements.markdown)
* [Classes](classes.markdown)
* [Interfaces](interfaces.markdown)
* [Syntax](syntax.markdown)
