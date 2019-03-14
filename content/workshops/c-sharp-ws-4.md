---
author: "Layla Porter"
date: 2019-03-14
bgimage: images/workshops/blank-business-card-697059.jpg
image: images/workshops/blank-business-card-697059.jpg
linktitle: C# Workshop Four
prev: /workshops/c-sharp-ws-3
title: Learning C# - Workshop Four
type: workshop
description: "Things are going well, so let's introduce a key concept - data-types"
---
Now we have the basics we can start to layer in some more ideas.

Let's continue to update our "HelloWorld" application.

In workshop 2 we learned how to add two variables together with the following code.

```csharp
static void Main(string[] args)
{
    var hello = "Hello";
    var name = "your name";
    Console.WriteLine(hello + name);
}
```
What if my variables only have numbers in it? What happens when we add them together?

Let's update our code now to the following 
```csharp
static void Main(string[] args)
{
    var numberOne = "7";
    var numberTwo = "3";
    Console.WriteLine(numberOne + numberTwo);
}
```
Even if *variables* only contain numbers, the program will still treat them like text and not numbers.  So if we add the above two strings we will get the output of `"73"` and not `"10"` like we may want.

This is a really good time to return to *types*.

## Data Types

A data type or type is a particular kind of data item, as defined by the values it can take, the programming language used, or the operations that can be performed on it.
What does that mean exactly?
### Data type: "strings"
Up until now we have been working with data type known as a *string*. It treats all of it's values as text.  A string looks like the following examples: 

```csharp
var someText = "This is a string of text";
string moreText = "More text";
```
You may have noticed that on the second *variable*, `string` was used instead of `var` in front of the variable name. This is known as *explicitly* typing a variable. When we use `var` the computer program makes a guess at what the type will be based on the value set. More on this later.

We know that we can add two strings together like so:

```csharp
var combinedText = someText + moreText;
```
The above will combine our two sentences, but you have to add the space yourself if it's needed like so:
```csharp
var combinedText = someText + " " + moreText;
``` 
Now, earlier we saw that adding two numbers together, didn't work as we might expect.
```csharp
var someText = "27";
var moreText = "13";
```
Even if your string only contains numbers, the datatype will still be a string.  So if we add the above two strings we will get the output of `"2713"` and not `"40"`.
We can try and turn these strings into a different data type, such as an *int* which is an integer data type.

### Data type: "ints"

An *int* data type can only have values that are integers or whole numbers.

```csharp
var someInt = 27;
var anotherInt = 13;
```
Note that we no longer surround our numbers with `"`. This means that the computer will *infer* the data type is an *int*. If we wanted to be explicit we could use the following, telling the computer that we want the *variable* to be an *int*:

```csharp
int someInt = 27;
int anotherInt = 13;
```

If we were to add these two variables together like so:
```csharp
var combinedInt = someInt + anotherInt;
```
We would get the expected result of `40`.

So how do we make a *string* into an *int*?

We can try and *parse* it using the following code.

```csharp
var someText = "27";
int myInt;
int.TryParse(someText, out myInt);
Console.WriteLine(myInt);
```
This is using the `TryParse` method provided for us in `System`, the library of methods that Microsoft provide us within the SDK. There are a few extra things about this method like `out` but don't worry about that now.

If `someText` can be turned into an integer, the method will assign the variable `myInt` with the value,  in this case,  `27`. 

If the method can't change the string into an integer, it will set the value of `age` as `0`. So in the code below, `"twenty-seven"` cannot be made into an integer, so `myInt` will be given a value of `0`.
```csharp
var someText = "Twenty-Seven";
int myInt;
int.TryParse(someText, out myInt);
Console.WriteLine(myInt);
```
There are many different data types available, you can even create your own.
But don't worry if this seems strange or complicated.  As we start to use these types, it will start to make more sense.

If you are happy with the above concepts, you can try and cobine the above code with an if/else statement, which we learned about in workshop 3.

Start with the code below and see what you can do.


```csharp
Console.WriteLine("What is your favourite number?");
var numberString = Console.ReadLine();
int number;
int.TryParse(numberString, out number);

//write you if/else statement here
```

You may have noticed the line above starting with two slashes.  This is a comment. Comments allow you to make notes in your code that are ignored by your computer. There are two types:

* Single line comments (denoted with //)

```csharp
// example single line comment
```
* Multiline comments (prefixed with /* and suffixed with */)

```csharp

/* This is a multi line comment
  it can span over a number of lines.
  Anything between the prefix and the suffix.
*/

/************************
* Sometimes people add an asterix on each line
* to make things stand out (e.g. headings etc..).
* These are also just multi line comments.
************************/

```

## Coding Challeng Time!!!

If you are happy with all of the concepts we have covered, have a go at making a new project and building a text adventure game!
