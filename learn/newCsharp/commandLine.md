---
title: Intro to C# with Command Line
date: '2-2-2020'
module: newCsharp
order: 0
---

## Why

The .NET Core **command-line interface (CLI)** is a new cross-platform toolchain for developing .NET applications. The CLI is a foundation upon which higher-level tools, such as Integrated Development Environments (IDEs), editors, and build orchestrators, can rest.  

We teach this topic because it is important to know that we can do everything that our IDE (Visual Studio) does on the command line.  So if we are experiencing issues with Visual Studio, we can always fall back on our command line skills.

## What

**Solution file (.sln)** - a solution is a container used by Visual Studio to organize one or more related projects.  When you open a solution in Visual Studio, it automatically loads all the projects the solution contains

**Project file (.csproj)** – contains all the source code that are compiled.  It also contains compiler settings and other configuration files

* **Structure:**
  * Solution files contain
    * Project files which contain
      * source code

![Solutions](../images/commandLineEx0.png "Solutions")

