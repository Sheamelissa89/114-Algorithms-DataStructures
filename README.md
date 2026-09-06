# Course 114: Algorithms and Data Structures

This repository contains my coursework for **Course 114: Algorithms and Data Structures**. The projects were completed in Python using Jupyter Notebooks and demonstrate Python fundamentals, object-oriented programming, stacks, queues, sorting algorithms, linked lists, recursion, and Big O notation.

## Technologies Used

- Python 3
- Jupyter Notebook
- Visual Studio Code
- Git and GitHub
- Python virtual environment (`venv`)

## Course Topics

- Python functions, loops, and conditional statements
- Classes and object-oriented programming
- Big O notation and algorithm complexity
- Recursive functions and base cases
- Sorting algorithms, including Quick Sort and Quick Sort 3
- Singly and doubly linked lists
- Stacks using LIFO behavior
- Queues using FIFO behavior
- Creating custom data structures

## Assignment 1: Count Even Numbers

This assignment uses a function, loop, and modulo operator to count the values in a list that are evenly divisible by two.

```python
def count_even_numbers(numbers):
    count = 0

    for number in numbers:
        if number % 2 == 0:
            count += 1

    return count


numbers = [3, 5, 27, 20, 6, 3.5, 60]

print(count_even_numbers(numbers))
```

### Expected Output

```text
3
```

## Assignment 2: Calculator Class

This assignment demonstrates object-oriented programming by creating a `Calculator` class with two attributes.

The class contains methods for:

- Addition
- Subtraction
- Multiplication
- Division
- Displaying the object using `__str__()`

```python
class Calculator:
    def __init__(self, number1, number2):
        self.number1 = number1
        self.number2 = number2

    def add(self):
        return self.number1 + self.number2

    def subtract(self):
        return self.number1 - self.number2

    def multiply(self):
        return self.number1 * self.number2

    def divide(self):
        if self.number2 == 0:
            return "Cannot divide by zero"

        return self.number1 / self.number2

    def __str__(self):
        return f"Calculator({self.number1}, {self.number2})"


c1 = Calculator(5, 2)

print(c1)
print(c1.add())
print(c1.subtract())
print(c1.multiply())
print(c1.divide())
```

## Assignment 3: Reverse a String Using a Stack

This assignment uses the provided `CustomStack` class to reverse a string.

Each character is pushed onto the stack and then popped from the stack in reverse order. This demonstrates the stack principle of **LIFO: Last In, First Out**.

```python
def reverse_string(value):
    stack = CustomStack()

    for character in value:
        stack.push(character)

    reversed_value = ""

    while not stack.is_empty():
        reversed_value += stack.pop()

    return reversed_value


print(reverse_string("Rafael"))
print(reverse_string("stars"))
print(reverse_string("cool"))
```

### Expected Output

```text
leafaR
srats
looc
```

## Final Project: CustomQueue

The final project completes and expands a custom queue class.

A queue follows **FIFO: First In, First Out**, meaning the first item added to the queue is the first item removed.

The completed queue includes:

- `enqueue()` to add an item
- `dequeue()` to remove the front item
- `is_empty()` to check whether the queue is empty
- `size()` to return the number of items
- `peek()` to view the front item without removing it
- `__str__()` to display the queue clearly

```python
class CustomQueue:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0

    def enqueue(self, item):
        self.items.append(item)

    def dequeue(self):
        if self.is_empty():
            return None

        return self.items.pop(0)

    def size(self):
        return len(self.items)

    def peek(self):
        if self.is_empty():
            return None

        return self.items[0]

    def __str__(self):
        values = ", ".join(str(item) for item in self.items)

        return f"CustomQueue -> [{values}]"


queue = CustomQueue()

queue.enqueue("A")
queue.enqueue("B")
queue.enqueue("C")

print(queue)
print(queue.peek())
print(queue.size())
```

### Expected Output

```text
CustomQueue -> [A, B, C]
A
3
```

## Stack vs. Queue

| Data Structure | Order | Description |
| --- | --- | --- |
| Stack | LIFO | The last item added is the first item removed. |
| Queue | FIFO | The first item added is the first item removed. |

## Algorithm Complexity

Big O notation describes how the running time or memory usage of an algorithm grows as its input increases.

Complexities covered in this course include:

- `O(1)` — Constant time
- `O(n)` — Linear time
- `O(n log n)` — Linearithmic time
- `O(n²)` — Quadratic time

## Recursion

A recursive function calls itself until it reaches a base case. The base case prevents the function from continuing indefinitely.

## Linked Lists

### Singly Linked List

A singly linked list stores a reference to the next node and allows forward traversal.

### Doubly Linked List

A doubly linked list stores references to both the next and previous nodes, allowing traversal in either direction.

## Repository Contents

- `Class_1.ipynb` — Python functions and Assignment 1
- `Class_2.ipynb` — Classes and the Calculator assignment
- `Class_3.ipynb` — Stacks and string reversal
- `class_4.ipynb` — Queues and the CustomQueue final project
- `.gitignore` — Excludes the virtual environment and generated files
- `README.md` — Course and repository documentation

## Running the Notebooks

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code.
3. Activate the Python virtual environment.
4. Install Jupyter if necessary:

```bash
pip install jupyter
```

5. Open the desired `.ipynb` notebook.
6. Select the Python interpreter from the virtual environment.
7. Click **Run All** to execute the notebook.

## Author

**Shea Mullin**

Full-Stack Development Student