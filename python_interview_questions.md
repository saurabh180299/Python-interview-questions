
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
