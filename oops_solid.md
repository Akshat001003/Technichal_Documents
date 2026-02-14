# OOP and SOLID Principles (Python)

This document contains Object-Oriented Programming (OOP) concepts and SOLID design principles with examples in Python. The content is based on handwritten notes and organized for quick reference and practical understanding.

---

# Object-Oriented Programming (OOP)

## What is a Class?

A **class** is a blueprint for creating objects.
It defines:

* Attributes (variables)
* Methods (functions)

Example:

```python
class Car:
    wheels = 4   # class variable

    def __init__(self, mileage):
        self.mileage = mileage   # instance variable
```

---

## What is an Object?

An **object** is an instance of a class.

```python
c1 = Car(10)
print(type(c1))
```

Built-in types like `int`, `str`, `list`, `dict` are also classes.

---

## Constructor (`__init__`)

* Automatically called when an object is created.
* Used to initialize instance variables.

```python
class Student:
    def __init__(self, name):
        self.name = name
```

---

## Types of Variables

### 1. Instance Variable

* Unique for each object
* Defined inside `__init__`

```python
self.mileage = 10
```

### 2. Class Variable (Static Variable)

* Shared among all objects

```python
class Car:
    wheels = 4
```

Change class variable:

```python
Car.wheels = 5
```

---

## Types of Methods

### 1. Instance Method

Works with instance variables.

```python
def show(self):
    print(self.mileage)
```

**Types:**

* Accessor (getter)
* Mutator (setter)

---

### 2. Class Method

Used to access class variables.

```python
@classmethod
def get_wheels(cls):
    return cls.wheels
```

---

### 3. Static Method

Utility method that does not depend on class or instance.

```python
@staticmethod
def info():
    print("This is a car class")
```

---

## Inner Class

A class defined inside another class.

```python
class Outer:
    class Inner:
        pass
```

---

## Inheritance

Child class inherits properties and methods from parent class.

```python
class A:
    def show(self):
        print("Parent")

class B(A):
    pass
```

---

## Constructor in Inheritance & super()

```python
class A:
    def __init__(self):
        print("Parent constructor")

class B(A):
    def __init__(self):
        super().__init__()
        print("Child constructor")
```

---

## Method Resolution Order (MRO)

Defines the order in which base classes are searched in multiple inheritance.

```python
print(B.__mro__)
```

---

## Polymorphism

### Types:

1. Duck Typing

```python
class PyCharm:
    def execute(self):
        print("Running")

class MyEditor:
    def execute(self):
        print("Executing")

def code(editor):
    editor.execute()
```

---

2. Operator Overloading

```python
a = 5
b = 6
print(a + b)
```

---

3. Method Overriding

```python
class A:
    def show(self):
        print("A")

class B(A):
    def show(self):
        print("B")
```

---

## Abstraction

Using `ABC` module:

```python
from abc import ABC, abstractmethod

class Computer(ABC):
    @abstractmethod
    def process(self):
        pass
```

---

## Encapsulation

Hiding internal details using private variables.

```python
class Student:
    def __init__(self):
        self.__marks = 0

    def set_marks(self, m):
        self.__marks = m

    def get_marks(self):
        return self.__marks
```

---

# SOLID Principles

SOLID helps in writing maintainable and scalable code.

---

## S – Single Responsibility Principle (SRP)

A class should have **only one reason to change**.

Example:

```python
class Report:
    def generate(self):
        print("Generating report")

class ReportPrinter:
    def print_report(self):
        print("Printing report")
```

Benefits:

* Better maintainability
* Less fragile code
* Easier testing

---

## O – Open/Closed Principle (OCP)

Software should be:

* Open for extension
* Closed for modification

Example:

```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        return 3.14 * 5 * 5
```

Add new shapes without modifying existing code.

---

## L – Liskov Substitution Principle (LSP)

Child class should be usable in place of parent class without breaking functionality.

---

## I – Interface Segregation Principle (ISP)

Clients should not depend on methods they do not use.

Instead of one large interface, create smaller ones.

---

## D – Dependency Inversion Principle (DIP)

Depend on **abstractions**, not concrete classes.

Example structure:

```
Client → Abstract Class → Concrete Implementation
```

Benefits:

* Loose coupling
* Easy testing
* Better scalability

---

# Advantages of SOLID

* Reduced code complexity
* Better readability
* Improved maintainability
* High reusability
* Better testability
* Loose coupling

---

