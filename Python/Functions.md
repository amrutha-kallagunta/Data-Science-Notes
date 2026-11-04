# Python Functions

# What is a Function?

A **function** is a reusable block of code that performs a specific task.

Instead of writing the same code multiple times, we write it once inside a function and call it whenever needed.

## Why Use Functions?

Functions help us:

- Reduce code duplication.
- Improve code readability.
- Make programs easier to maintain.
- Break large problems into smaller parts.
- Reuse logic multiple times.

### Without Function

```python
print("Welcome")
print("Welcome")
print("Welcome")
```

### With Function

```python
def greet():
    print("Welcome")

greet()
greet()
greet()
```

---

# Defining a Function

Functions are created using the `def` keyword.

## Syntax

```python
def function_name():
    # function body
```

## Example

```python
def greet():
    print("Hello User")

greet()
```

### Output

```python
Hello User
```

### Explanation

- `def` creates the function.
- `greet` is the function name.
- Code inside the function runs only when the function is called.
- `greet()` calls the function.

---

# Calling a Function

After defining a function, use its name followed by parentheses.

## Example

```python
def greet():
    print("Hello")

greet()
```

### Output

```python
Hello
```

---

# Functions are First-Class Objects

In Python, functions can be assigned to variables.

## Example

```python
def greet():
    print("Hello")

msg = greet

msg()
```

### Output

```python
Hello
```

Here, `msg` refers to the same function as `greet`.

---

# Function Arguments

Arguments are values passed to a function.

They allow functions to work with different inputs.

## Syntax

```python
def function_name(parameter):
    # code
```

### Parameter vs Argument

| Term | Meaning |
|--------|----------|
| Parameter | Variable in function definition |
| Argument | Actual value passed while calling |

---

## Example

```python
def square(num):
    return num * num

print(square(5))
```

### Output

```python
25
```

### Explanation

- `num` is a parameter.
- `5` is an argument.
- Function calculates and returns the square.

---

# Types of Function Arguments

Python supports multiple argument types.

---

# 1. Positional Arguments

Values are assigned according to their order.

## Example

```python
def student(name, age):
    print(name, age)

student("John", 25)
```

### Output

```python
John 25
```

### Wrong Order

```python
student(25, "John")
```

### Output

```python
25 John
```

Order matters in positional arguments.

---

# 2. Keyword Arguments

Arguments are passed using parameter names.

Order does not matter.

## Example

```python
def student(name, age):
    print(name, age)

student(age=25, name="John")
```

### Output

```python
John 25
```

### Advantages

- More readable.
- Order can change safely.

---

# 3. Default Arguments

Default values are assigned if no argument is provided.

## Example

```python
def greet(name="Guest"):
    print("Hello", name)

greet()
greet("John")
```

### Output

```python
Hello Guest
Hello John
```

### Explanation

- If value is not given, default value is used.
- If value is provided, it overrides the default.

---

# 4. Arbitrary Positional Arguments (*args)

Used when the number of arguments is unknown.

## Example

```python
def add(*args):
    print(args)

add(1, 2, 3, 4)
```

### Output

```python
(1, 2, 3, 4)
```

### Important

`*args` stores values as a tuple.

---

## Example: Sum All Numbers

```python
def add(*args):
    total = 0

    for num in args:
        total += num

    return total

print(add(10, 20, 30))
```

### Output

```python
60
```

---

# 5. Arbitrary Keyword Arguments (**kwargs)

Used when the number of keyword arguments is unknown.

## Example

```python
def display(**kwargs):
    print(kwargs)

display(name="John", age=25)
```

### Output

```python
{'name': 'John', 'age': 25}
```

### Important

`**kwargs` stores values as a dictionary.

---

## Example

```python
def display(**kwargs):
    for key, value in kwargs.items():
        print(key, value)

display(name="John", age=25)
```

### Output

```python
name John
age 25
```

---

# Return Statement

`return` sends a value back to the caller.

## Syntax

```python
return value
```

---

## Example

```python
def square(n):
    return n * n

result = square(4)

print(result)
```

### Output

```python
16
```

---

# Difference Between print() and return

## Using print()

```python
def square(n):
    print(n*n)

square(5)
```

Output:

```python
25
```

Cannot reuse the result later.

---

## Using return

```python
def square(n):
    return n*n

result = square(5) + 10

print(result)
```

Output:

```python
35
```

`return` is generally more useful.

---

# Returning Multiple Values

Python can return multiple values.

## Example

```python
def calc(a, b):
    return a+b, a-b

x, y = calc(10, 5)

print(x)
print(y)
```

### Output

```python
15
5
```

Actually Python returns a tuple.

---

# Nested Functions (Function Inside Function)

A function can be defined inside another function.

## Example

```python
def outer():

    def inner():
        print("Inside Inner Function")

    inner()

outer()
```

### Output

```python
Inside Inner Function
```

---

# Why Use Nested Functions?

- Better code organization.
- Hide internal logic.
- Used in closures and decorators.

---

# Scope of Variables

Scope determines where a variable can be accessed.

---

# Local Variable

Defined inside a function.

```python
def test():
    x = 10
    print(x)

test()
```

### Output

```python
10
```

Outside the function, `x` is not available.

---

# Global Variable

Defined outside all functions.

```python
x = 100

def show():
    print(x)

show()
```

### Output

```python
100
```

---

# Modifying Global Variable

```python
x = 100

def change():
    global x
    x = 200

change()

print(x)
```

### Output

```python
200
```

---

# Pass by Object Reference

Python does not strictly use pass-by-value or pass-by-reference.

It uses **pass-by-object-reference**.

The function receives a reference to the object.

---

# Mutable Objects

Mutable objects can be changed.

Examples:

- List
- Dictionary
- Set

## Example

```python
def modify(lst):
    lst[0] = 99

nums = [1, 2, 3]

modify(nums)

print(nums)
```

### Output

```python
[99, 2, 3]
```

The original list changes.

---

# Immutable Objects

Cannot be modified.

Examples:

- int
- float
- str
- tuple

## Example

```python
def modify(x):
    x = 50

a = 10

modify(a)

print(a)
```

### Output

```python
10
```

Original value remains unchanged.

---

# Lambda Functions

Small anonymous functions created using `lambda`.

## Syntax

```python
lambda arguments: expression
```

## Example

```python
square = lambda x: x * x

print(square(5))
```

### Output

```python
25
```

Equivalent to:

```python
def square(x):
    return x * x
```

---

# Recursive Functions

A function calling itself is called recursion.

## Example

```python
def countdown(n):

    if n == 0:
        return

    print(n)

    countdown(n-1)

countdown(5)
```

### Output

```python
5
4
3
2
1
```

---

# Built-in Functions

Python provides many ready-made functions.

Examples:

```python
len()
sum()
max()
min()
type()
print()
input()
round()
sorted()
```

Example:

```python
nums = [10, 20, 30]

print(sum(nums))
```

Output:

```python
60
```

---

# Advantages of Functions

1. Code reusability.
2. Better readability.
3. Easier debugging.
4. Modular programming.
5. Less code duplication.
6. Easier maintenance.

---

# Common Mistakes

## Forgetting Parentheses

Wrong:

```python
greet
```

Correct:

```python
greet()
```

---

## Missing Return

```python
def add(a, b):
    a + b
```

Returns:

```python
None
```

Correct:

```python
def add(a, b):
    return a + b
```

---

## Changing Argument Order

```python
student("John", 25)
```

and

```python
student(25, "John")
```

produce different results with positional arguments.

---
