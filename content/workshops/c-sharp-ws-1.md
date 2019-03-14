---
author: "Layla Porter"
date: 2019-03-10
bgimage: images/workshops/asphalt-dark-dawn-531321.jpg
image: images/workshops/asphalt-dark-dawn-531321.jpg
linktitle: C# Workshop One
next: /workshops/c-sharp-ws-2
title: Learning C# - Workshop One
type: workshop
description: "In this workshop, we will create a basic application called a console application. This is an app that runs on the console, sometimes known as the terminal or command line."
---

## Introduction
If you would like to know why learning C# (see-sharp) is a good thing, then check this [blog post](http://www.bestprogramminglanguagefor.me/why-learn-c-sharp).
In this workshop, we will create a basic application called a console application. This is an app that runs on the console as opposed to a website or a phone app. It's sometimes known as the terminal or command line. A console is the simplest type of program we can make.
On a Windows machine, we can use the cmd or Powershell as our console.
On Linux, it's the terminal.
And on macOS, it's also terminal or you can download iTerm and use that instead.

We will also be using the command line to create and run our application.

## Setting up our development environment.

To get started with C# we will need to download a [Software Development Kit](https://dotnet.microsoft.com/download), or SDK. C# runs on a framework called .NET (dot net) and we will download the .NET SDK here. We will specifically be using the .NET Core framework as it works on Windows, Mac and Linux - known as cross-platform.
Choose the correct download for your operating system, e.g. Windows, and follow the installation instructions.

We will also need a code editor to enable us to edit our code.  [Visual Studio Code](https://code.visualstudio.com/download) is a free and very versatile editor, so let's download that one, again, choosing the right download for your operating system.

To check if the .NET SDK installed correctly, open the console and type in `dotnet` and press enter.
You should see something similar to this
<br/><br/>
![image showing dotnet in the console](/images/workshops/dotnet-check.png)
<br/><br/>
Now that we know the SDK is installed correctly we can make our first application.
When you open the command line it will most likely open in a certain folder or directory on your computer.
If you type in `ls` on Mac/Linux and `dir` on Windows and press enter, you should see a list of all the folders and files in the current directory.
<br/><br/>
We need to create a new directory for our code to live in.
To make a new directory we will use the following command:

```
>mkdir MyCode
```
</br>
This will create a folder called `MyCode` on your computer.
If you type in `ls` again, you should see we now have a new directory called MyCode.
We now need to change directory (cd) so that our command line is inside our new folder.

```
>cd MyCode
```
</br>
Now we are in the right folder, let's create a new .NET project.

```
>dotnet new
```
<br/><br/>
![image showing dotnet new in the console](/images/workshops/dotnet-new.png)
<br/><br/>
The above command will bring up all the available templates projects that came with the SDK.  We want to build a console app, so enter the following command:
</br>
```
>dotnet new console -n HelloWorld
```
</br>
This command will create a new Directory called `HelloWorld` and add a new console application inside it.
If you cd into the `HelloWorld` directory and list all of the files we will see there are 2 files called `Program.cs` and `HelloWorld.csproj`.
<br/><br/>
![image showing contents of new console app](/images/workshops/ls-console.png)
<br/><br/>
We now have a basic application that we can run.
Type in the following command:
```
>dotnet run
```
</br>
And we should see that "Hello World!" is printed in the console.

We have made our first program!
</br></br>
[Let's go edit our program!](/workshops/c-sharp-ws-2)