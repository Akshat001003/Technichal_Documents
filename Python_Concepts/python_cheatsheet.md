# Python Cheatsheet

## Basic Operators

| Operator | Meaning             |
| -------- | ------------------- |
| +        | Addition            |
| -        | Subtraction         |
| *        | Multiplication      |
| /        | Float Division      |
| //       | Integer Division    |
| %        | Modulus (remainder) |
| **       | Power               |

## Strings

* `' '` or `" "` → String
* `\` → Escape character
* `\n` → New line
* `r"string"` → Raw string (ignores escape sequences)

## Variables

* Variables store values.
* Python is dynamically typed.
* `_` stores last output (in interactive mode).

## Indexing & Slicing

* Index starts from **0**
* Last index = **-1**

```
var[x]
var[x:y]
var[x:]
var[:y]
```

## Input

```
input()          # string
int(input())     # integer
eval(input())    # evaluate expression
```

## Type Checking

```
type(var)
id(var)
```

## Range

```
range(10)
range(start, end, step)
list(range(2,11,2))
```
