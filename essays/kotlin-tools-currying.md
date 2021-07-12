---
layout: essay
type: essay
title: Kotlin tools - Currying
# All dates must be YYYY-MM-DD format!
date: 2021-07-12
labels:
  - Software Engineering
  - Learning
---

`Currying` a function allows us to reduce the number of parameters that a function requires. We can do this by returning a function that has some of the original information embedded within it. This is a functional programming technique called creating a `closure`. 

You can see kotlin currying in action here:
<script src="https://gist.github.com/patbeagan1/b293048084617a1071d73baa33166e06.js"></script>

Notice how each step requires one fewer argument than the one before it. 
- The first function call requires 2 arguments. 
- `b` requires 1 argument, because we are calling a function that has the first parameter stored in a closure. 
- `c` requires no arguments because we have curried the original function twice, removing both of its parameters.

This can be useful in practice to encourage code reuse and simplification, in a way that is easy to refactor later. Currying a function reduces its dimensionality, and allows us to prepare a generic function to be called for similar tasks later. 

One very practical way to use this, is to create a curried function that writes to a database. By injecting the database instance into the original function and currying it, we remain decoupled (we can always inject a different instance into the original function), while at the same time guaranteeing that the same injected instance is used throughout the file. 