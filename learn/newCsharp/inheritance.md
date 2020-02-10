---
title: Inheritance
date: '2-7-2020'
module: newCsharp
order: 15
---

## Why

Inheritance, together with encapsulation, abstraction, and polymorphism, is one of the four pillars or primary characteristics of object-oriented programming. Inheritance enables you to create new classes that reuse, extend, and modify the behavior that is defined in other classes.

## What

The class whose members are inherited from is called the base class, and the class that inherits those members is called the derived class. This is done by using a colon “:” after the derived class and then typing the name of the base class. When you define a class to derive from another class, the derived class implicitly gains all the members of the base class, except for its constructors and finalizers. The derived class can thereby reuse the code in the base class without having to re-implement it. In the derived class, you can add more members. In this manner, the derived class extends the functionality of the base class. Examples in the “How”.

Inheritance allows us to define a class based on another class. This makes creating and maintaining an application easy.

![Inheritance](../images/inheritanceEx0.png "Inheritance")

The class whose properties are inherited by another class is called the Base class.

The class which inherits the properties is called the Derived class.

For example, base class **Animal** can be used to derive **Cat** and **Dog** classes.
The derived class inherits all the features from the base class, and can have its own additional features.

***Inheritance allows us to define a class based on another class.***

```csharp
class Animal
{
  public int Legs {get; set;}
  public int Age {get; set;}
}

class Dog : Animal
{
  public Dog()
  {
  Legs = 4;
  }
}

class Labrador : Dog
{

}
```

Inheritance allows the derived class to reuse the code in the base class without having to rewrite it. And the derived class can be customized by adding more members. In this manner, the derived class extends the functionality of the base class.

C# does not support multiple inheritance, so you cannot inherit from multiple classes.

However, you can use interfaces to implement multiple inheritance. To put it another way, a class can conform to multiple interfaces

Moreover, the ***derived class cannot inherit the constructor of the base class*** because constructors are not the members of the class

## How

* First we create a base class called "BankAccount"

![BankAccount Class](../images/inheritanceEx1.png "BankAccount Class")

* Then we give it members that all derived bank accounts would need

![Add members](../images/inheritanceEx2.png "Add members")

* Then create a derived class called “CheckingAccount” and set it to inherit from our base class, since a checking account will need all of the same members of a standard bank account. Then we give it members specific to a Checking Account

![CheckingAccount Class](../images/inheritanceEx3.png "CheckingAccount Class")

* Now when we access our class through the instance we create, we can also assign values to the inherited members as well as it non-inherited members

![Add members](../images/inheritanceEx4.png "Add members")

![Assign Values](../images/inheritanceEx5.png "Assign Values")

## Exercise

* First, fork the repository from <https://github.com/nrice41593/InheritanceExercise>

* Add me as a collaborator

* Then, clone the repo onto your personal machine and follow the instructions in the Project.

* When finished, push your project back up to GitHub and mark the assignment as complete in Google Classroom.  When the students finish, their code should look like:

## Quiz

<https://docs.google.com/forms/d/1H4K3G4ZTprsMvGDbePJTtkJcGwh0XYTfv2xH2OtlyMo/edit>
