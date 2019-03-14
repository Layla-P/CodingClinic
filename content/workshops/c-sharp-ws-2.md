---
author: "Layla Porter"
date: 2019-03-10
bgimage: images/workshops/bloom-blossom-flora.jpg
image: images/workshops/bloom-blossom-flora.jpg
linktitle: C# Workshop One
prev: /workshops/c-sharp-ws-1
next: /workshops/c-sharp-ws-3
title: Learning C# - Workshop Two
type: workshop
description: "In this workshop, we will create a basic application called a console application. This is an app that runs on the console, sometimes known as the terminal or command line."
---

In our first workshop, we installed everything we needed to run C# on our computer.  We even got our first program up and running!
In this workshop, we will start to edit our "Hello World" program.

Open up Visual Studio Code, the code editor we installed in the first workshop.
The welcome page will give you an option to "open a folder" rather than a file. Click this and then find your "HelloWorld" folder that we created inside "Repos".

This will open the directory containing our application.  There should be two files, `HelloWorld.csproj` and `Program.cs`, and one folder called `obj`.

Open the `Program.cs` file; this is the entry point of our application and it will look like this:

```csharp
using System;

namespace HelloWorld
{
   class Program
   {
       static void Main(string[] args)
       {
           Console.WriteLine("Hello World!");
       }
   }
}
```
It has a `Program` class with a `Main` method inside it. Don't worry about what a class or a method is as yet, we'll get to that later.

There is some code in this `Program.cs` file that is just not important at the moment, so let's get rid of it.  You code should look like this now:

```csharp
using System;
 class Program
{
   static void Main(string[] args)
   {
        Console.WriteLine("Hello World!");
    }
}
```

The `Console.WriteLine("Hello World!");` is what printed "Hello World!" inside our console.  Change the contents of the quote marks to say `"Hello, Milton Keynes."` as shown below.

```csharp
static void Main(string[] args)
{
   Console.WriteLine("Hello, Milton Keynes.");
}
```
Now if we run the project from the console, using `>dotnet run` again, you should see that our update is printed to the console instead.

## What's going on?
.NET comes with a whole load of ready-made code for us to use in the form of *libraries*. See the `using System` at the top of the `Program.cs` file? That's us saying that we want to use the System library, which is provided by Microsoft. Inside these libraries, we have methods or functions that we can use or call. `Console.WriteLine` is one of these methods.

Update your `Main` method inside your `Program` class to the following:

```csharp
static void Main(string[] args)
{
   var hello = "Hello";
   var name = "your name";
   Console.WriteLine(hello + name);
}
```

Now we have created two *variables* called `hello` and `name` and given them the values of "Hello" and "your name", respectively.
We have then added our two *variables* together using the `+` sign and put them in the `Console.WriteLine`.
The above will combine our two sentences and output them to the console.
But if you run this you may see that there is no space between our words where they join.
You have to add the space yourself if it's needed. Below is one way you could do it, see if you can find another

```csharp
Console.WriteLine(hello + " " + name);
```

We can also take input from the console using `Console.ReadLine()`.  Let's ask a question this time.  Update the code to the following.

```csharp
static void Main(string[] args)
{
   Console.WriteLine("Hello, what is your name?");
   var name = Console.ReadLine();
   Console.WriteLine("Your name is " + name);
}
```
<br/><br/>

In this code, we set the value of the user input to be equal to the *variable* `name`.

We then use another call to `Console.Writeline()`, this time passing in some text and our variable using the `+` sign to combine these.

<br/>
So in this workshop, we have learned to take input from a user, assign that to a variable and then combine that input some text, outputting that to the screen!

If you are happy with these concepts, perhaps have a play with `Console.Write()` instead of `Console.WriteLine()` and see what happens.