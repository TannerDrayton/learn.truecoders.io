---
title: Methods
date: '2018-03-19T19:00:56-05:00'
module: csharp
order: 4
---

## Fundamentals

A method, sometimes called a function, is a block of code that contains a collection of code to execute. You can execute this code by calling the method. In C#, a method consists of a few things:

* Modifiers: an optional list of keywords that give certain qualities to the method
* Return Type: the type returned by the method, or `void` when not returning anything
* Name: a descriptive method name
* Parameters: an optional list of parameters to be passed into the method
* Scope: the block of code to be executed when the method is called

## Modifiers and Return Types

Here's a `public` method with a `void` return type.

The modifier is `public`, meaning any place in the code can call your method. It's not `private` or `internal`.

The return type is `void`. You can think of `void` as similar to `null`. It's a keyword that represents the absence of a return type.

```csharp
public void MyMethod()
{
    // Code to execute goes here when MyMethod() is called
    // Return type is void, so no need to return anything
}
```

Here's a `public` method with a `string` return type:

```csharp
public string MyMessage()
{
    // Code to execute goes here when MyMessage() is called
    // Return type is string, so we must return a string
    return "This is the message";
}
```

Later in your code, you can call your methods:

```csharp
MyMethod(); // executes any code in your MyMethod() method

var message = MyMessage(); // executes any code in MyMessage() and returns a string
```

## Parameters

Below, we have a method called `SendEmail`. The return type is `bool`, in this case, if the email sent with success. The method has one parameter: `string emailAddress`.

```csharp
public bool SendEmail(string emailAddress)
{
    if (emailAddress == "cwinton@truecoders.io")
    {
        // Send the email and return true, for success
        return true;
    }
    else
    {
        // Don't send the email and return false, for failure
        return false;
    }
}
```

Later in your code, you can call your methods:

```csharp
var didSendFirst = SendEmail("cwinton@truecoders.io"); // This call will return true

var didSendSecond = SendEmail("dwalsh@truecoders.io"); // This call will return false
```
