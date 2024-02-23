---
title: OOP Puzzles
layout: Assignment
order: 7
---
## Submission
This is two mini-projects. Upload 1 .cs file for each to brightspace.

Include your name as a comment at the top of each file. 

*Note: In ‘real’ projects we write one class per file, because Unity requires this for components, and because it’s good practice.
The C# compiler doesn’t actually care. It ignores file and folder structures completely (This is why namespaces are a thing, to replace folders as a disambiguation system).
Code written as a single file is still perfectly valid C# code. Neat. More importantly, it’s convenient for me to grade. In “real” projects that have to actually run, we will stick to one class per file.*

## Puzzle 1
Create an arbitrary set of classes that have a hierarchy that could be diagrammed as follows:

![(A->((b),(c->((d),(e)))))](/assignmentInfo/oop1.png)

Do not call your classes “A”, “B”, etc; but **invent an example using appropriate names**.

Since the classes do not need to actually do anything, they can just be empty. Write all the classes in the same file, and upload that single file to Brightspace.

## Puzzle 2
Given the following script, reverse engineer a possible class hierarchy.

Write out the classes (with appropriate variables and functions) that would coherently satisfy this script.

While you need to write functions, the functions don’t need to do anything, they can just be empty.
The classes do not need to inherit from MonoBehaviour, or have anything to do with Unity.

When you’re done, compile all of the classes into a single file and upload just that one file. 

![A screenshot of code](/assignmentInfo/oop2.png)

## Resources
- [Object Oriented Syntax](https://guidebook.hdyar.com/docs/programming/advanced/object-oriented-syntax/)
- [Polymorphism](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/object-oriented/polymorphism)
- [Inheritance](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/inheritance)
- [OOP Guidebook page](https://guidebook.hdyar.com/docs/programming/advanced/object-oriented-programming/)
