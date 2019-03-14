---
author: "Layla Porter"
date: 2019-03-13
bgimage: images/workshops/blank-conifers-crossroad-1578750.jpg
image: images/workshops/blank-conifers-crossroad-1578750.jpg
linktitle: C# Workshop Three
next: /workshops/c-sharp-ws-4
prev: /workshops/c-sharp-ws-2
title: Learning C# - Workshop Three
type: workshop
description: "Now we have the basics we can start to layer in some more ideas. In this workshop we will learn how to use conditional statements"
---

A lot about what computer programs do is based on decision making.  Computers can't make those decisions so we need a way to program this and we can use something called a *conditional statement*.

There are several different types of *conditional statement*but before we look at those, we just need to understand comparisons first.

### Comparisons

We can compare the value of a variable with another variable or value.  To do this we use a double equals sign, as shown below.   adding this to your code and see the result.

```csharp
static void Main(string[] args)
{
   var myColourVariable = "blue";
   Console.WriteLine(myColourVariable == "red");
}

```
In this code, we are doing a check to see if the value of `myColourVariable` has the value of "red". In this case, the value is "blue" so the program will write `false` to the console.

We can also compare two variables, as shown below:

```csharp
var myColourVariable = "blue";
var myOtherColourVariable = "red";
Console.WriteLine(myColourVariable == myOtherColourVariable);
```
It's important to note that "Red" would not be equal to "red" as comparisons are case sensitive.

Comparisons are really key for understanding how conditional statements work. Let's look at the most common conditional statement, the if/else statement.

## if/else statements

An if/else statement* is a very powerful concept in programming. It allows the computer to perform different actions depending on certain conditions. 

Let's add an if/else statement to our "HelloWorld" application by asking a question and doing something based on the answer.

Let's update our program with the following code.

```csharp
static void Main(string[] args)
{
   Console.WriteLine("Do you prefer green or blue?");
   var colour = Console.ReadLine();
}
```

So we now know what colour our user prefers, let's do something based on that, but first, we will need to compare their result against the options.

```csharp
static void Main(string[] args)
{
   Console.WriteLine("Do you prefer green or blue?");
   var colour = Console.ReadLine();

   if(colour == "green"){
   Console.WriteLine("Grass is green");
   }
   else{
   Console.WriteLine("The sky is blue");
   }
}
```
Try typing "red" into your program and see what happens.
Now in the above code, if our use wrote anything other than "green" the program will write whatever is in the `else` part of the statement.

We can build on our statement, by adding in an `else if` like so:
```csharp
static void Main(string[] args)
{
   Console.WriteLine("Do you prefer green or blue?");
   var colour = Console.ReadLine();

   if(colour == "green"){
   Console.WriteLine("Grass is green");
   }
   else if(colour == "blue"){
   Console.WriteLine("The sky is blue");
   }
   else{
   Console.WriteLine("You didn't answer my question!");
   }
}
```
There are several other types of conditional statement. If you feel like it, you could research some of the others and have a play with them.
