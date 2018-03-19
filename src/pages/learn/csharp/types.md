---
title: C# Types
---

* [Value Types](#value-types)
  * [Boolean](#boolean)
  * [Character](#character)
  * [Integer](#integer)
  * [Decimal](#decimal)
  * [Enum](#enum)
  * [Additional Value Types](#additional-value-types)
* [Null and Nullables](#null-and-nullables)
* [Reference Types](#reference-types)
  * [String](#string)
  * [Array](#array)
* [Reference vs. Value Types](#reference-vs-value-types)

## Value Types

A value type is set based on the provided value. Assigning one value type variable to another copies the contained value. This differs from the assignment of reference type variables, which copies a reference to the object but not the object itself.

### Boolean

The Boolean type is defined with the keyword: `bool`. You can set the value be `true` or `false`:

```csharp
bool isBoolean = true;
isBoolean = false;
```

### Character

The Character type is defined with the keyword: `char`. You can set the value to any unicode character, surrounded by single quotes:

```csharp
char myCharacter = 'a';
myCharacter = '@';
```

### Integer

The Integer type is defined with the keyword: `int`. The `int` is a 32-bit signed integer that can be set to any integer between `-2,147,483,648` to `2,147,483,647`:

```csharp
int myInteger = 123;
myInteger = -456;
```

### Decimal

The Decimal type is defined with the keyword: `decimal`. You can set the value to be any decimal within the range of `(-7.9 x 1028 to 7.9 x 1028) / 100 to 28` and appended with an `m`;

```csharp
decimal myDecimal = 1234567890.234m;
myDecimal = -1234567890.234m;
```

### Enum

An Enum type is a distinct type used when you want to limit the value set to a fixed amount of options. This allows for very readable code and a delightful autocomplete experience within Visual Studio.

```csharp
// This enum defines every week day
public enum Day { Sun, Mon, Tue, Wed, Thu, Fri, Sat };

// Can only be set to a day of the week
var dayOfWeek = Day.Tue;
dayOfWeek = Day.Wed;
```

### Additional Value Types

Although you won't run into these types quite as often as the four above, we wanted to list them:

| Type     | Description             | Range/Precision                                            |
| -------- | ----------------------- | ---------------------------------------------------------- |
| `byte`   | 8-bit unsigned integer  | `0` - `255`                                                |
| `sbyte`  | 8-bit signed integer    | `-128` - `127`                                             |
| `short`  | 16-bit signed integer   | `-32,768` - `32,767`                                       |
| `uint`   | 32-bit unsigned integer | `0` - `4,294,967,295`                                      |
| `ushort` | 16-bit unsigned integer | `0` - `65,535`                                             |
| `long`   | 64-bit signed integer   | `-9,223,372,036,854,775,808` - `9,223,372,036,854,775,807` |
| `ulong`  | 64-bit unsigned integer | `0` - `18,446,744,073,709,551,615`                         |
| `double` | signed decimal          | `(+/-)5.0 x 10-324` - `(+/-)1.7 x 10308`                   |
| `float`  | signed decimal          | `-3.4 x 1038` - `+3.4 x 1038`                              |

## Null and Nullables

In C#, the keyword `null` represents the absence of value.

While [reference types](#reference-types) automacially support being set to `null`, value types require an actual value. When you need to assign `null` to a value type, you employ the "nullable" of that type. A value type, followed by a `?` is shorthand syntax for nullable:

```csharp
// Here's a nullable boolean value
bool? isBoolean = true;
isBoolean = null;

// You can do the same for other value types
int? myInteger = null;
myInteger = 0;

// Reference types support null automatically
string myString = "Hello World";
myString = null;
```

**Note:** `null` is not the same as `0` or an empty string: `""`

* `0` and `""` are actual values, stored in memory or to disk as `0` or `""`
* `null` represents the absence of value: nothing is stored in memory or to disk

## Reference Types

A reference type is set by storing the actual data (object) in memory and storing a reference to the object within the variable. Reference types in C# automatically support being set `null`.

### String

A String is a sequence of zero or more unicode characters, surrounded by double quotes.

```csharp
var myString = "Hello World!";
```

You can concatenate strings with the `+` symbol:

```csharp
var message = "What's " + "up?"; // message equals "What's up?"
```

You can split a single string into an [array](#array) of strings:

```csharp
// This splits `aString` using a separator `char` value
var aString = "1,2,3"; // the string to split
var numbers = aString.Split(','); // numbers equals { "1", "2", "3" };
```

### Array

Arrays allow you to combine multiple variables of the same type in a single variable. You declare an array type by specifying the type, followed by double square brackets `type[]`.

```csharp
// We've created an array that can hold up to 5 ints
int[] ints = new int[5];

// You can also use type inference when you provide the variables for the array to contain
var intsLiteral = new [] { 7, 58, 5 }; // Array with set values using curly bracket notation
```

Arrays are zero-based index, meaning that the first value is stored at index `0`. You can access a value using its index, along with square bracket notation.

```csharp
var intsLiteral = new [] { 7, 58, 5 };

int firstNumber = intsLiteral[0]; // Equals 7
int secondNumber = intsLiteral[1]; // Equals 58

intsLiteral[2] = 10; // Did change 5 to 10
```

You can join an array of [strings](#strings) into a single string:

```csharp
var numbers = new [] { "1", "2", "3" }; // the array to join
var allNums = string.Join(",", numbers); // allNums equals "1,2,3"
```

## Reference vs. Value Types

With a value type, when you copy a variable you create a clone of the actual value.

Let's see how this works with an [int](#integer)

```csharp
var a = 1; // value type int
var b = a; // clone the value of `a`

a = 2; // Change the contained value of `a`

// Now a equals 2 && b equals 1
```

With a reference type, when you copy a variable you create a clone of the reference to the same actual data value:

Let's see how this works with a [class](classes.markdown#classes) called `Animal`.

```csharp
var c = new Animal { Name = "Fido" }; // reference type Animal
var d = c; // copy of reference to same object

// currently c.Name equals "Fido" && d.Name equals "Fido", but let's change that:
c.Name = "Fluffy";

// You changed the property of the actual object
// So now c.Name equals "Fluffy" && d.Name equals "Fluffy"
```

**Previous:** [Variables](variables.markdown) |
**Next:** [Methods](methods.markdown)
