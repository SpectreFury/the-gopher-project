---
layout: "../../../layouts/MarkdownLayout.astro"
title: "Calculator"
subtitle: "The Basics"
backlink: "/roadmap#the-beginning"
---

## Introduction

It is time to make our first project with the knowledge of everything we have learnt from the previous lessons. We are going to make a simple CLI calculator application. It's going to wonderful learning opportunity and a stepping stone to move on to more complex Go applications.

## Guide

1. Make a github repository for your application. We are not going to tell you how to do that just because it's not within the scope of our lessons, but there's a lot of resources available. You can call it whatever you want, it doesn't matter but a name like `calculator-cli` works.

2. Clone the repostory and initialize a new `go.mod` file in it. If you don't remember the terminal command for it, just reference the previous lessons. Make sure you initialize it with your github url in mind.

3. Create a `main.go` file. We are going to everything inside a single file for now. We will move on to proper directory structure later on.

4. Write the main function and use the print function in go and run it with `go run .` to test if your application is running. Now, we're good to go.

5. We want this to be really basic, just get two number from the user and ask them for which operator they want to do e.g. multiply, divide.

6. After the user adds their inputs, you want to show the result of the operations.

7. Right now, our application will terminal when we get the answer which is as expect, but if you wanna do your own research, which I highly suggest, figure out a way to again ask till you exit the application manually. We will work on this if you decide not to do it.
