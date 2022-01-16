### Introduction to Recursion

Recursion is when a function calls itself . Recursion is an alternative to looping.
* Any problem that can be solved by a for loop can also be solved by recursion and vice versa
* Isn't necessarily better, just different
* Recursive functions must stop calling themselves at some point or they will create an infinite loop

### Structure of recursive functions

Recursive functions must have a condition to determine when it should stop calling itself
* Recursive case - if true function will continue to call itself
* Base case - if true function will not call itself

Each recursive call will work on the problem being solved by breaking it down into a smaller, simpler one until it reaches the smallest version of the problem. The base case will then solve the problem without further recursion. A recursive function must have at least one recursive case and one base case.