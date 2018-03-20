---
title: Interfaces
date: '2018-03-19T19:00:56-05:00'
module: csharp
order: 8
---

## Fundamentals

An Interface is like a blueprint. It defines some data and functionality that should exist within a type that implements the interface. An interface does not care about the implementation. It merely requires that it is implemented.

C# naming convention dictates that an interface start with a capital `I`, for interface.

Here's an example interface:

```csharp
interface ISampleInterface
{
    void SampleMethod();
}

interface IOtherInterface
{
    string OtherMethod();
}
```

Unlike inheritance, a class can conform to multiple interfaces:

```csharp
class SampleClass : ISampleInterface, IOtherInterface
{
    // ISampleInterface member implementation
    void SampleMethod()
    {
        // Method implementation
    }

    // IOtherInterface member implementation
    string OtherMethod()
    {
        // Other implementation
        return "Message";
    }
}
```

Later in code, you can create an instance of the `SampleClass` as an instance of the `ISampleInterface`:

```csharp
ISampleInterface sample = new SampleClass();
sample.SampleMethod();
```

You can also have an interface inherit from another interface.

Let's create a Hawk class and a Penguin class. Both are animals. Both are birds, even. But, only one can fly.

Using Interfaces, we can accomplish this functionality is a clear, concise, and readable way:

```csharp
class Animal {}

public interface IBird // For all birds
{
    void CleanFeathers();
}

public interface IFlyingBird : IBird // For all flying birds
{
    void Fly();
}

class Hawk : Animal, IFlyingBird
{
    public void CleanFeathers() {}
    public void Fly() {}
}

class Penguin : Animal, IBird
{
    public void CleanFeathers() {}
}
```

Let's look at an example that shows the benefit of interchangeable code using Interfaces. We'll use the `IBird` interface with a method:

```csharp
public void CleanBird(IBird bird)
{
    bird.CleanFeathers();
}
```

We've created a method that accepts any bird in a type-safe fashion. Later, we can create an instance of the `Hawk` class and the `Penguin` class. Both of these instances are different types, but both implement the `IBird` interface:

```csharp
var hawk = new Hawk();
CleanBird(hawk); // this works

var penguin = new Penguin();
CleanBird(penguin); // this also works
```

Let's look at another example. We'll use the `IEnumerable` interface:

```csharp
// Here we have an array of strings
var emailArray = new [] { "a@me.com", "b@me.com" };

// Here we have a list of strings
var emailList = new List<string> { "a@me.com", "b@me.com" };
```

Both these variables are different types, but both implement the `IEnumerable` interface. So, let's create a method:

```csharp
public void SendEmails(IEnumerable<string> emailAddresses)
{
    foreach(var emailAddress in emailAddresses)
    {
        //do something with the email
    }
}
```

Later in your code, you can call your `SendEmails` method using either your `emailArray` or `emailList` variables:

```csharp
SendEmails(emailArray); // this works
SendEmails(emailList); // this also works
```

We've created a method that accepts either an Array or a List in a type-safe fashion.
