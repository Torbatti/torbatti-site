---
weight: 3
title: "Var Const Let"
draft: false
---
## Var Const Let
### Var
* The var statement declares a new local or global variable.
```nim
var x, y: int
```
```nim
var
  x, y: int
  a, b, c: string
```
```nim
var x = "abc" # Declares `x` and assigns a value to it
x = "xyz"
```

### Const
* Constants are symbols which are bound to a value.
* The constant's value cannot change.
* The compiler must be able to evaluate the expression in a constant declaration at compile time.
```nim
const x = "abc"
```
```nim
const
  x = 1
  y = 2
  z = y + 5
```
### Let
* The let statement works like the var statement but the declared symbols are single assignment variables: After the initialization their value cannot chang
```nim
let x = "abc" # Declares `x` and assigns a value to it
x = "xyz"     # Illegal: assignment to `x`
```
* The difference between let and const is: let introduces a variable that can not be re-assigned, const means "enforce compile time evaluation and put it into a data section"
```nim
const input = readLine(stdin) # Error: constant expression expected
```
```nim
let input = readLine(stdin)   # works
```
