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

If the condition evaluates to `true`, the body will run and if it's `false`
