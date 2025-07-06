---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Variables and Constants"
subtitle: "The Basics"
backlink: "/roadmap#the-beginning"
---

It is time to finally learn Go in detail. Don't worry, we are going to go at an extremely slow pace initially and I'm gonna do my best to explain everything to you as if you are a 5 year old.

## Variables and Constants

If you have ever taken a math class in your life and the chances of that are pretty high, you must have heard about the concept of variables and constants. It mathematical terms, a _variable_ is something that does not have a fixed value and can be subject to change.


Similarly in Go, and almost every other programming language on the planet, we have the concepts of variables and constants. In Go, the variable is like a container that can have any value (not exactly, but we're going to learn more about that later.)

### Variables

To make a variable in Go is really easy. We need

```go
var greeting string = "Hello, World!";
```

Let's look at the various components of this expression.

1. First of all, we got the `var` keyword. It basically tells the compiler that the next thing that is going to come after it is going to be the name of the variable also called as an identifier in a lot of languages.

2. Next is the identifier `greeting` or the name of the variable we set. It can be anything we like as long as it's within the rules of variables.

3. After that comes the data type which we are setting as `string`. This is a really important topic in itself, so we are going to talk about it a bit later.

4. Next is the `=` operator. This just tells the compiler that whatever comes after this operator is going to be assigned to our variable.

5. Finally, we have our `"Hello, World!"` which is the value that we want the variable to contain.

That is generally how you write a variable in Go. It's a bit verbose if you are coming from dynamically typed languages, but being explicit with your types makes life easier in the long run.

However, this is not the only way you can create a variable in Go. Thanks to the lovely creators of Go, we have a shorthand syntax for creating variables, and it goes something like this:

```go
name := "Hello, World!";
```

I know, this looks way more elegant, but you may be asking yourself, where did all the keywords that we added earlier go? Well, we are technically declaring all the keywords, but it's happening implicitly rather than explicitly.

What's happening is that the compiler is smart enough to know that `"Hello, World!"` is a string, so it's assigning the name variable to be of the type `string`. This is how you would be mostly writing variables, but you know both the ways now so you can choose.

Let's try to change the value of the variable, after all, that's why we made it a variable.

```go
package main

import ("fmt")

func main() {
    var name string = "Hello, World!";
    fmt.Println("Before change: ", name);

    name = "Hello, Gophers!";
    fmt.Println("After change: ", name);
}
```

Let's run this program, remember how we did it in the last lesson?

```sh
go run .
```

Your output should be something like this:

```
Before change:  Hello, World!
Before change:  Hello, Gophers!
```

We have successfully changed the value inside the variable, let's go. This is a powerful technique used everywhere in programming, so make sure you remember this.

You might wonder if we can change the data type of a variable from `string` to an `int`. Is it still going to work?

How about we try going that, in our last program, let's make a little modification.

```go
package main

import ("fmt")

func main() {
    var name string = "Hello, World!";
    fmt.Println("Before change: ", name);

    name = 18;
    fmt.Println("After change: ", name);
}
```

You are going to see something interesting if you're writing this in a code editor that has a LSP for Go, you will immediately get an error. However, let's ignore that for educational purpose and try to build and run our project.

```sh
go run .
```

If all goes correctly, you're going to get this message:

```
# example/hello_world
.\main.go:12:9: cannot use 18 (untyped int constant) as string value in assignment
```

The compiler let's us know that you cannot assign a `int` to a `string` variable. This is actually amazing as we know at compile time that we're trying to assign a wrong data type to a varible.

Go is a statically typed language which means that you are not allowed to change the data type of a variable if it's already assigned to be something else.

### Constants

Constants in Go are very similar to variables, well, they are just variables with one caveat. You cannot change it's value. Let's look at a constant in action.

```go
package main

import ("fmt")

func main() {
    const NAME string = "Bruce Wayne";

    fmt.Println(NAME)
}
```
If you run our little program, we will get this:

```
Bruce Wayne
```

Let's try to modify the value of the constant, see what happens.

```go
package main

import ("fmt")

func main() {
    const NAME string = "Bruce Wayne";
    fmt.Println(NAME)

    NAME = "Jason Todd"
}
```

Your compiler is going to scream at you for doing that, but let's ignore it and try to run our application.

You should remember how to run the project by now, so let's see the result.

```bash
.\main.go:11:2: cannot assign to name (neither addressable nor a map index expression)
```

This is just as we expected, Constants value cannot be modified. If you try to modify the value, the compiler is going to scream at you and rightfully so. You must have seen that we are just all capital letter as the variable name. This is because of a convention to use all caps for constant variables.

So when should you use variables and when should you use constants? If you know during the declaration of the variable that it's value is going to change then use a variable, and if that's not the case, use constant. Other good way of doing this is just using const variables unless you need to change it.

## Operators

We can use operators to do different operations over the variables or constant we have. There are different types of operators, so let's discuss about them here. 

### Arithmetic

Arithmetic operators are used to do mathematical operations over values in Go. They usually require two or more values to work, but there are exception like the `-` operator.

Here are all the arithmetic operators in Go:

```go
package main

import ("fmt")

func main() {
    a := 90
    b := 10

    counter := 0

    fmt.Println("Addition: ", a + b);
    fmt.Println("Subtraction: ", a - b);
    fmt.Println("Multiplication: ", a * b);
    fmt.Println("Division (integer division): ", a / b);
    fmt.Println("Modulus (remainder division)", a % b);


// This will increase the value by 1 (can also be written as counter = counter + 1)
    counter++;

// This will decrease the value by 1 (can also be written as counter = counter - 1)
    counter--;

}
```

A important thing to note is that Go follows the order of operations just like any other programming language. You most likely have heard about PEMDAS or BODMAS.

```go
package main

import ("fmt")

func main() {
    // This should evaluate to 7
    fmt.Println((10 / 2) + 1 * 3 - 1);
}
```

### Relational

Relational operators are used to compare two or more values and give us either true or false according to the result of the conditions. Here's all of them:

- == (Is Equal To)
- != (Not Equals To)
- \> (Greater Than)
- < (Less Than)
- \>= (Greater Than or Equals to)
- <= (Less Than or Equals to)

```go
package main

import ("fmt")

func main() {
    fmt.Println("Is Equal To: ", 10 == 10)
    fmt.Println("Not Equals To: "10 != 1)
    fmt.Println("Greater Than: ", 11 > 10)
    fmt.Println("Less Than: ", 9 < 10)
    fmt.Println("Greater Than or Equals to: ", 10 >= 10)
    fmt.Println("Less Than or Equals to: ",  9 <= 10)
}

```

At this point, you know enough to make a simple CLI application and it's exactly what we're going to do next.

---

## Assignment

1. Do some basic math, try using basic
