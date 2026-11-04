# Python Functions - Quick Revision

## Function
Definition: Reusable block of code.

Syntax:
```python
def function_name():
    pass
```

Example:
```python
def greet():
    print("Hello")
```

---

## Parameter
Definition: Variable in function definition.

Syntax:
```python
def greet(name):
```

Example:
```python
def greet(name):
    print(name)
```

---

## Argument
Definition: Actual value passed to function.

Example:
```python
greet("John")
```

---

## Return
Definition: Sends value back to caller.

Syntax:
```python
return value
```

Example:
```python
return a + b
```

---

## Default Argument
Definition: Uses default value if not provided.

Syntax:
```python
def fun(x=10):
```

Example:
```python
def fun(x=10):
    print(x)
```

---

## Positional Argument
Definition: Arguments matched by position.

Example:
```python
fun(10, 20)
```

---

## Keyword Argument
Definition: Arguments matched by parameter name.

Example:
```python
fun(y=20, x=10)
```

---

## *args
Definition: Multiple positional arguments.

Syntax:
```python
def fun(*args):
```

Example:
```python
fun*1, 2, 3)
*``

---

## **kwargs
Definition: M*ltiple keyword arguments.

Syntax:*```python
def fun***kwargs):
```

Example:
```python****(name="John", age=25)
``***---

## Nested Function
Definiti*** Function inside***other function.

Syntax:
```pyth***def outer():
    def inner():
``***---

## Lambda Function
Definiti*** Anonymous one-line function.

***tax:
```python
lambda arguments***xpression
```

Example***``python
lambda x: x*x
***

---

## Recursion
Definition: ***ction***lling itself.

Example:
```pytho***ef fun***
    fun()
```

---

## Mutable ***ects
Examples:
```python
list, d***, set
```

---

## Immutable Obj***s
Examples***``python
int, float, str,***ple
```

---

## Python***gument Passing
```text
Pass-by-***ect-Reference
``***
