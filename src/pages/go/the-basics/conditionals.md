---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Conditionals"
subtitle: "The Basics"
backlink: "/roadmap#the-beginning"
---

You now know how to store data in variables and constants, amazing job. However, you won't be able to do much with it if there's no logical flow of the data.

This is where conditional statements shine, let's dig in.

### If Statements

There are times when you want to conditions do _something_. This is the best time to use if-statements. Let's see the syntax first and understand how they work as it's relatively straight forward.

```go
package main

import ("fmt")

func main() {
    isGopher := true

    if isGopher == true {
        fmt.Println("You sir, are a true gopher!")
    }
}
```

Let's understand the code a bit; Inside the main function, we are creating a boolean variable called `isGopher` and setting it's value to `true`.

Now comes the fun part, the if statement comprises of two parts. The **condition** and the **body**. The condition decides when the body is going to work.

If the condition evaluates to `true`, the body will run and if it's `false`, the body is not going to run. The condition part needs a true or a false value, which is also called as a `boolean`.

### Else Statement

We can do a lot with the if statement, however what if we want to do a different action if the conditions is not true. For example, we want to let somebody be able to buy alcohol if they are of the age 21 or higher, and not let anybody below that buy it.

This is a perfect use for an if-else statement. Let's do the same proper inside code.

```go
package main

import ("fmt")

func main() {
    var age int;

    fmt.Print("Enter your age: ")
    fmt.Scan(&age)

    if(age >= 21) {
        fmt.Println("Have a beer, my friend")
    } else {
        fmt.Println("Sorry, maybe in a few year")
    }
}
```

Woah, that's a lot of unseen stuff, what is `fmt.Print` and `fmt.Scan`. Well, these are just other function available to us inside the `fmt` library.

`fmt.Print` is a function that prints whatever we write without a newline, which is what I wanted in the above code.

`fmt.Scan` is also a function which is used to get user input when we run the program. the `&age` means that we want to save whatever the user types inside our age variable.

We will talk more about what functions are and what that `&` operator is later, right now, this amount of knowledge is going to suffice till we build our first project.

Now, try running the application and enter any value for the age and see what we get.

This is the result of running the application:

```
Enter your age: 21
Have a beer, my friend!
```

It works perfectly as we expected, but let's extend this using a new concept.

### Else if Statement

If you want to check multiple statements after the initial if statement, what you need is a else if statement.

```go
package main

import ("fmt")

func main() {
    var age int;

    fmt.Print("Enter your age: ")
    fmt.Scan(&age)

    if(age > 21) {
        fmt.Println("Have a beer, my friend")
    } else if(age == 21) {
        fmt.Println("You're the exact age for alcohol, good save")
    } else {
        fmt.Println("Sorry, maybe in a few year")
    }
}

```

These statements make the basics of control flow in any programming language

## Switch Statements

We also have something called as a switch statement in Go. It's really useful if want to go to different branches of execution based on a value.

Let's see an example.

```go
package main

import ("fmt")

func main() {
    var day string

    fmt.Println("Enter a day of the week: ")
    fmt.Scan(&day)

    switch(day) {
        case "Sunday":
            fmt.Println("Today is Sunday")
        case "Monday":
            fmt.Println("Today is Monday")
    }
}
```

The `switch(day)` refers to what value we will have the branching for, in this case, we want to print different lines for different days of the week.

The `case` keyword is going to run if the current value is equal to what's provide inside the switch statement. So, if day is equals to Sunday, then the `case "Sunday":` will work.

---

## Assignment
