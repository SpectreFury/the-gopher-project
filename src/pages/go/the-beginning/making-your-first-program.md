---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Making Your First Program"
subtitle: "The Beginning"
backlink: "/roadmap#the-beginning"
---

## Hello World

We are going to start off very simple and write what's called a "Hello World" program. It's like a initiation ceremony and after you write this, you can be called a Go programmer.

### Creating our first module

We will create our first go module in this tutorial. A Go module can be a collection of one or more go files along with other non-go files (we'll talk more about this). Let's assume we want to make a calculator project where each go file will be an operation i.e adding, subtraction. It makes sense to make a calculator project and let all the operations be individual go files which may or may not interact with each other.

It's easier to understand once you do this yourself, so let's make a simple go project. Assuming you have properly done the last lesson and have a successfully installed go compiler, we can use the Go CLI to make a project.

The first thing we're going to do is make a directory where you're gonna do all the tutorials or anything related to The Gopher Project. It can be anywhere of your computer.

Open your terminal and navigate to wherever you want the directory to be and then type the following.

```bash
mkdir thegopherproject
```

This will create the directory "thegopherproject" at your preferred location.

Now let's get inside this directory. For that, type:

```bash
cd thegopherproject
```

Once you do that, your terminal will probably say something like

```bash
thegopherproject -> ~
```

Now we can finally start with our first Go module.

### Go Modules

Let's start by making a hello_world module by writing the following command:

```bash
go mod init example/hello_world
```

Once you run this successfully, you'll get this message:

```bash
go: creating new go.mod: module example/hello_world
go: to add module requirements and sums:
        go mod tidy
```

This means that the command worked and if you just look inside your directory, you will find a neat `go.mod` file.

Let's talk more about what that file is.

Go mod file usually contains all the metadata relating to your project. Think of all the dependencies relating to your project like the go version is stored inside this file. You can relate this file to the package.json file that's usually found in the Node.js ecosystem.

What I want you to do is just open that file we just implicitly created, you can just simply show the content of that file inside your terminal using the command:

```bash
cat go.mod
```

You should see something similar to this:

```go
module example/hello_world

go 1.24.2
```

The first line is the module path we gave while we were initializing the module. Usually, this path is the path to the online repository. For example, `go mod init github.com/SpectreFury/the-gopher-project` could be a module that refers to this project on the Github website.

The next line is the minimum version of Go required for our module. This is likely going to be different for you if you're seeing this lesson in the future.

## Assignment

This is time for your first assignment. Some of these are going to just be things that you have to read (boring, I know,) and the others, you'll have to do yourself. I suggest you do both, as it will be a great opportunity to learn from official resources as well as the ones we provide.

1. Check out the Go [Wikipedia](<https://en.wikipedia.org/wiki/Go_(programming_language)>). You don't have to read absolutely everything, just get an idea about the language.
