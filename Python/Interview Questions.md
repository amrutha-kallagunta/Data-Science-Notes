# Interview Quick Revision

## One-Line Definitions

### Function

Reusable block of code that performs a specific task.

### Parameter

Variable defined in a function definition.

### Argument

Actual value passed during a function call.

### Return

Sends value back to the caller.

### Lambda Function

Anonymous one-line function.

### Recursion

A function calling itself.

### *args

Accepts multiple positional arguments as a tuple.

### **kwargs

Accepts multiple keyword arguments as a dictionary.

### Nested Function

Function defined inside another function.

### Scope

Region where a variable is accessible.

---

# Frequently Asked Interview Questions

## Q1. What is a function in Python?

A reusable block of code used to perform a specific task.

---

## Q2. Difference between parameter and argument?

- Parameter → Variable in function definition.
- Argument → Actual value passed during function call.

Example:

```python
def greet(name):  # parameter
    print(name)

greet("John")     # argument
```

---

## Q3. Difference between print() and return?

| print() | return |
|----------|----------|
| Displays output | Sends value back |
| Cannot be reused easily | Can be reused |
| Returns None | Returns actual value |

---

## Q4. What is *args?

Used to accept multiple positional arguments.

```python
def fun(*args):
    print(args)
```

---

## Q5. What is **kwargs?

Used to accept multiple keyword arguments.

```python
def fun(**kwargs):
    print(kwargs)
```

---

## Q6. What is recursion?

A function calling itself.

---

## Q7. What is a lambda function?

A small anonymous function written in one line.

```python
lambda x: x*x
```

---

## Q8. What does a function return if there is no return statement?

```python
None
```

---

## Q9. What are mutable and immutable objects?

### Mutable

Can be modified.

```python
list
dict
set
```

### Immutable

Cannot be modified.

```python
int
float
str
tuple
```

---

## Q10. Does Python use pass-by-value or pass-by-reference?

Neither exactly.

Python uses:

```text
Pass-by-Object-Reference
```

---
