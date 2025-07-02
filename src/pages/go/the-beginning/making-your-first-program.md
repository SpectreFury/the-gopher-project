---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Making Your First Program"
subtitle: "The Beginning"
backlink: "/roadmap#the-beginning"

---

## Preface

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

### Creating a Go file

Now we are ready to create our file go file. Open the project in your preferred code editor (I use neovim btw!) and create a `main.go` file inside `thegopherproject` directory that we previously created. Once you have created this file, the directory should contain two files, the go.mod and the main.go files.

```bash
ls
```

This command should give the following result

```bash
-a---           6/19/2025  7:37 PM             38 go.mod
-a---           6/19/2025  9:04 PM             82 main.go
```

Pat yourself on the back, you have created your go file.

Now we just gotta print hello world to the console, let's see how we can do that.

### Hello World

Open the main.go file in any code editor you like and type the following, I'm going to explain in details what's going on later but for now, we will get to see our long awaited hello world in the console.

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```

Good job, now all we gotta do is run our application.

Open your terminal inside our `thegopherproject` directory and type

```bash
go run .
```

This will compile and run our application and you will get to see the following

```
Hello World!
```

We finally have our hello world printed to the console. Well done fellow _Gophers_. Give yourself a pat on the back, that was a lot.

## Assignment

1. Try to modify the quotes inside the `fmt.println()` function and see what happens.
2. Can you print two things right below each other? Something like:

   ```
   SpectreFury
   I am learning Go!
   ```
