
# Python Interview Questions and Answers

### 1. What are Python’s key features?
- **Answer**: Interpreted, dynamically-typed, object-oriented, high-level, and has extensive libraries.

### 2. What is PEP 8?
- **Answer**: PEP 8 is the Python style guide that dictates how code should be formatted for better readability.

### 3. How does Python handle memory management?
- **Answer**: Python uses reference counting and a cyclic garbage collector to manage memory.

### 4. What is a lambda function in Python?
- **Answer**: A lambda is an anonymous function in Python, defined with the `lambda` keyword. Example: `lambda x: x + 1`.

### 5. What’s the difference between `deepcopy()` and `copy()`?
- **Answer**: `copy()` creates a shallow copy (copies references), while `deepcopy()` creates a full copy (recursively copies objects).

### 6. Explain Python’s GIL (Global Interpreter Lock).
- **Answer**: GIL is a mutex in Python that protects access to Python objects, limiting the execution of multiple threads at a time in CPython.

### 7. What’s the difference between a list and a tuple?
- **Answer**: Lists are mutable (can change), while tuples are immutable (cannot change).

### 8. What are Python decorators?
- **Answer**: Decorators are functions that modify the behavior of other functions or methods. They are defined with the `@decorator` syntax.

### 9. How does exception handling work in Python?
- **Answer**: Use `try`, `except`, `finally` to handle exceptions. Example:
   ```python
   try:
       x = 1 / 0
   except ZeroDivisionError:
       print("Cannot divide by zero")
   finally:
       print("Done")
   ```

### 10. What are Python’s built-in data types?
- **Answer**: Lists, tuples, sets, dictionaries, strings, integers, floats, booleans.

### 11. What is a generator in Python?
- **Answer**: Generators are iterators that generate values lazily (one at a time) using the `yield` keyword.

### 12. How does list comprehension work in Python?
- **Answer**: It’s a concise way to create lists. Example:
   ```python
   squares = [x ** 2 for x in range(10)]
   ```

### 13. What is the `with` statement used for?
- **Answer**: It simplifies resource management, such as file handling, by automatically managing the setup and teardown of resources.

   Example:
   ```python
   with open('file.txt', 'r') as file:
       data = file.read()
   ```

### 14. What’s the difference between `==` and `is`?
- **Answer**: `==` checks for value equality, while `is` checks for identity (whether two objects are the same in memory).

### 15. How are Python functions passed—by reference or value?
- **Answer**: Python passes arguments by reference (object reference), but immutable types like strings and tuples behave as if passed by value.

- Here are more Python interview questions with concise answers to enhance your preparation:

### 11. What are lambda functions in Python?
**Answer:** Lambda functions are anonymous functions defined using the `lambda` keyword. They can take any number of arguments but can only have one expression. They're often used for short, throwaway functions.
```python
add = lambda x, y: x + y
```

### 12. Explain the difference between `==` and `is`.
**Answer:** 
- **`==`** checks for value equality, meaning it evaluates whether the values of two objects are the same.
- **`is`** checks for identity, meaning it evaluates whether two references point to the same object in memory.
```python
a = [1, 2, 3]
b = a
c = a[:]
print(a == c)  # True (values are equal)
print(a is b)   # True (same object)
print(a is c)   # False (different objects)
```

### 13. What are Python's built-in types for handling text?
**Answer:** Python provides several built-in types for handling text, primarily:
- **`str`**: Immutable sequences of Unicode characters.
- **`bytes`**: Immutable sequences of bytes (used for binary data).
- **`bytearray`**: Mutable sequences of bytes.

### 14. What is the Global Interpreter Lock (GIL)?
**Answer:** The GIL is a mutex that protects access to Python objects, preventing multiple threads from executing Python bytecode simultaneously. This can limit the performance of CPU-bound multithreaded programs but allows for safe memory management.

### 15. How do you create a virtual environment in Python?
**Answer:** You can create a virtual environment using the `venv` module. Here’s how:
```bash
# Create a virtual environment named 'venv'
python -m venv venv

# Activate the virtual environment (Windows)
venv\Scripts\activate

# Activate the virtual environment (macOS/Linux)
source venv/bin/activate
```

### 16. What is the purpose of the `with` statement in Python?
**Answer:** The `with` statement is used for resource management and exception handling. It simplifies the use of try/finally blocks by ensuring that resources are properly cleaned up, like closing files.
```python
with open('file.txt', 'r') as file:
    content = file.read()
```

### 17. Explain the difference between a list and a tuple.
**Answer:** 
- **List:** Mutable, can be modified after creation, allows duplicate elements, defined with square brackets `[]`.
- **Tuple:** Immutable, cannot be modified after creation, allows duplicate elements, defined with parentheses `()`.

### 18. What are Python's built-in functions for data type conversion?
**Answer:** Common data type conversion functions include:
- **`int()`**: Converts a value to an integer.
- **`float()`**: Converts a value to a float.
- **`str()`**: Converts a value to a string.
- **`list()`**: Converts a value to a list.
- **`tuple()`**: Converts a value to a tuple.

### 19. How do you read and write files in Python?
**Answer:** You can read and write files using the built-in `open()` function with modes such as `'r'` for reading and `'w'` for writing.
```python
# Writing to a file
with open('file.txt', 'w') as f:
    f.write("Hello, World!")

# Reading from a file
with open('file.txt', 'r') as f:
    content = f.read()
```

### 20. What is a Python module and how do you create one?
**Answer:** A module is a file containing Python code (functions, classes, variables) that can be imported and reused in other scripts. To create a module, simply save Python code in a `.py` file.
```python
# example_module.py
def greet(name):
    return f"Hello, {name}!"
```

### 21. What is the difference between `input()` and `raw_input()`?
**Answer:** 
- **`input()`**: In Python 3, reads a line from input and evaluates it as a Python expression. 
- **`raw_input()`**: In Python 2, reads input as a string without evaluation. (In Python 3, `raw_input()` is removed.)

### 22. How do you implement a singleton pattern in Python?
**Answer:** The singleton pattern ensures a class has only one instance and provides a global point of access to it. Here's a simple implementation:
```python
class Singleton:
    _instance = None

    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(Singleton, cls).__new__(cls)
        return cls._instance
```

### 23. What are context managers and how do you create one?
**Answer:** Context managers allow you to allocate and release resources precisely when you want to. You can create a context manager using the `with` statement or by defining a class with `__enter__` and `__exit__` methods.
```python
class MyContext:
    def __enter__(self):
        print("Entering context")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Exiting context")

with MyContext() as context:
    print("Inside context")
```

### 24. What is the difference between `append()` and `extend()` in lists?
**Answer:** 
- **`append()`**: Adds a single element to the end of the list.
- **`extend()`**: Adds elements from an iterable (like a list or tuple) to the end of the list.
```python
lst = [1, 2, 3]
lst.append([4, 5])  # Result: [1, 2, 3, [4, 5]]
lst.extend([6, 7])  # Result: [1, 2, 3, [4, 5], 6, 7]
```

### 25. How do you handle command-line arguments in Python?
**Answer:** You can handle command-line arguments using the `sys` module or the `argparse` module. `argparse` is more powerful and user-friendly.
```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('echo', help='Echo the string you use here')
args = parser.parse_args()
print(args.echo)
```
