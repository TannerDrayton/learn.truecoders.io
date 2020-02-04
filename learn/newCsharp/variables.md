---
title: Variables
date: '2-2-2020'
module: newCsharp
order: 2
---

## Why

At the end of the 16th century, François Viète introduced the idea of representing known and unknown numbers by letters, nowadays called variables, and of computing with them as if they were numbers, in order to obtain the result by a simple replacement. In reference to programming, values being used in the program are able to be remembered more easily.

Essentially, variables play an important role as they allow us as programmers to write flexible programs. Instead of entering data directly into a program, a programmer can use variables to represent the data. ... The opposite of a variable is a constant. **Constants** are values that never change.

## What

Variables keep track of the data throughout the program. It is like a container to store the information. It is used to store, retrieve, and modify changeable data.

Variables consist of a data-type, a variable name and a value (initialized by providing a value:

```csharp
datatype variableName; <---- Declaration
```

Variables are always assigned with a data-type, meaning it holds the value of a specific type, such as string, bool, int and so on. C-sharp is **strongly-typed** meaning once a variable has a type, that type cannot change. C-sharp is also **statically-typed** meaning every variable must have a type.

***C# Variable Naming Conventions:***

You can’t just choose any sequence of characters as a variable name. Instead, C# has some rules regarding variable names that are to be followed:

* camelCase for local variables, such as cost, firstName, dateOfBirth, and petName.
* A meaningful or descriptive name that is neither too long nor too short to identify the information stored in a variable just by looking at it.
* Can contain the letters a–z and A–Z, numbers 0–9, and the underscore (_) character..other symbols are not allowed.
* Cannot have spaces and cannot start with a number.
* Cannot use a word reserved by C# language—keywords such as namespace, class, using, and so on...

***Invalid Names:***

* 1 (number)
* class, while, if, protected(key words)
* 1order, 1name (starts with a number)

## How

Create a variable by declaring its type and then giving it a name using the syntax below.

When you **declare** a variable, the computer knows that it has to reserve a place in its memory for this variable.

```csharp
datatype variableName; //declaration syntax
```

To **initialize** a variable, you need to assign it a value. This is done by naming the variable followed by an equal sign (=) and then the value.

```csharp
variableName = variableValue; // initialization syntax
```

**Note:** The term initialize means to assign an initial value.

**Variable Declaration and Initialization Syntax Combined on a Single Line.**

While you can declare a variable and assign it a value in two separate steps, it is also possible to do both of them at the same time on a single line:

```csharp
datatype variableName = variableValue; // syntax
```

Here, datatype must be one of the valid data types, and variableName is the identifier used for the variable. This is an explicitly typed local variable where the type is explicitly defined.

1. string name;
2. int age;
3. int weight;
4. bool isMarried;

## Exercise

Step 1: Declare and initialize variables for the following types:

1. string
2. int
3. char
4. bool
5. double

Step 2: Concatenate these variables in a Console.Writeline();

Step 3: Analyze any errors you might incur, if any, and research how to fix it. This is a prime opportunity to exemplify self-learning.

## Quiz

<https://docs.google.com/forms/d/1_GzjkIYHc199V05HIHZFfF6hjHf2hTiot9AdFOnvZxo/edit>
