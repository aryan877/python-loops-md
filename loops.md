# Python Loops

Loops in Python are used to repeatedly execute a block of code until a certain condition is met. There are two main types of loops in Python: `for` and `while`. Let's explore each one in detail.

## 1. For Loop

The `for` loop in Python is used to iterate over a sequence (such as a list, tuple, string, or range) and execute a block of code for each element in the sequence.

```python
for variable in sequence:
    # code to be executed 
```

Example:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

Output:

```
apple
banana
cherry
```

## 2. While Loop

The `while` loop is used to repeatedly execute a block of code as long as a specified condition is true.

```python
while condition:
    # code to be executed
```

Example:

```python
count = 0
while count < 3:
    print("Count is", count)
    count += 1
```

Output:

```bash
Count is 0
Count is 1
Count is 2
```

## Loop Control Statements

### 1. Break Statement

The `break` statement is used to exit the loop prematurely, regardless of whether the loop condition is true or false.

```python
for variable in sequence:
    if condition:
        break
```

Example:

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 3:
        break
    print(num)
```

Output:

```
1
2
```

### 2. Continue Statement

The `continue` statement is used to skip the rest of the code inside the loop for the current iteration and move to the next iteration.

```python
for variable in sequence:
    if condition:
        continue
    # code to be executed for non-matching condition 
```

Example:

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 3:
        continue
    print(num)
```

Output:

```
1
2
4
5
```

### 3. Else Clause with Loop

In Python, loops can have an `else` clause that is executed when the loop condition becomes false.

```python
for variable in sequence:
    # code to be executed
else:
    # code to be executed when loop condition is false
```

Example:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
else:
    print("No more fruits")
```

Output:

```
apple
banana
cherry
No more fruits
```

## The `range` Function

The `range` function is commonly used with `for` loops to generate a sequence of numbers. It can take one, two, or three arguments:

- `range(stop)`: Generates numbers from 0 to (stop - 1).
- `range(start, stop)`: Generates numbers from start to (stop - 1).
- `range(start, stop, step)`: Generates numbers from start to (stop - 1) with a specified step.

Example:
```python
for i in range(1, 6):
    print(i, end=" ")
```

Output:

```
1 2 3 4 5
```

## Challenges

### Challenge 1:

Write a program using a `for` loop to find the sum of all even numbers from 1 to 10.

**Answer:**

```python
sum_even = 0
for i in range(1, 11):
    if i % 2 == 0:
        sum_even += i
print("Sum of even numbers:", sum_even)
``` 

### Challenge 2:

Implement a `while` loop to print Fibonacci numbers up to the 10th term.

**Answer:**

```python
a, b = 0, 1
count = 0
while count < 10:
    print(a, end=" ")
    a, b = b, a + b
    count += 1
``` 

### Challenge 3:

Create a program that uses a `for` loop to iterate over a list of words and prints the length of each word.

**Answer:**

```python
words = ["apple", "banana", "cherry"]
for word in words:
    print(f"The length of {word} is {len(word)}") 
```

### Challenge 4:

Write a program using nested  `for`  loops to print the following pattern:

```
1
22
333
4444
55555

```

**Answer:**

```python
for i in range(1, 6):
    for j in range(i):
        print(i, end="")
    print()
```
This program uses nested loops to print a pattern of numbers where each line consists of the same digit repeated a number of times equal to the line number.