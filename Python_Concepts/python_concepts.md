# Core Python Concepts

## Data Types

### Numeric

* int
* float
* complex
* bool

### Sequence Types

* list
* tuple
* string
* range

### Mapping

* dictionary

### Set

* Unique unordered elements

---

## Mutability

| Type   | Mutable |
| ------ | ------- |
| list   | Yes     |
| dict   | Yes     |
| set    | Yes     |
| tuple  | No      |
| string | No      |

---

## Control Statements

### If-Else

```
if condition:
    ...
elif condition:
    ...
else:
    ...
```

### Loops

**While Loop**

1. Initialization
2. Condition
3. Increment/Decrement

**For Loop**

```
for i in range(start, end, step):
```

### Loop Controls

* `break`
* `continue`
* `pass`

---

## Functions

```
def func(a, b):
    return a + b
```

### Types of Arguments

* Positional
* Keyword
* Default
* Variable length `*args`
* Keyword variable `**kwargs`

---

## Scope

* Local variable
* Global variable

```
global x
globals()['x']
```

---

## Recursion

* Function calling itself

```
import sys
sys.getrecursionlimit()
sys.setrecursionlimit(n)
```

---

## Exception Handling

```
try:
    ...
except:
    ...
finally:
    ...
```

---

## Modules

```
import math
math.sqrt()
math.floor()
math.ceil()
math.pow()
```

Alias:

```
import math as m
```

---

## Bitwise Operators

| Operator | Meaning     |
| -------- | ----------- |
| &        | AND         |
| |        | OR          |
| ^        | XOR         |
| ~        | Complement  |
| <<       | Left shift  |
| >>       | Right shift |

---

## Number Systems

```
bin(x)
oct(x)
hex(x)
```
