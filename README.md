# Python
## NAME: Mukesh B

Basic Python programming exercises and solutions.

## 1. Binary Numbers Divisible by 5

Write a Python program which accepts a sequence of comma-separated 4-digit binary numbers and checks whether they are divisible by 5. The numbers that are divisible by 5 are printed in a comma-separated sequence.

**Example Input:**

```text
0100,0011,1010,1001
```

**Output:**

```text
1010
```

### Code

```python
numbers = input().split(',')
result = []

for num in numbers:
    if int(num, 2) % 5 == 0:
        result.append(num)

print(','.join(result))
```

### Output

<img width="1919" height="1077" alt="image" src="https://github.com/user-attachments/assets/f90504b5-d7d2-4157-b052-e8cfd6b289d9" />


---

## 2. Count Letters and Digits

Write a Python program that accepts a sentence and calculates the number of letters and digits.

**Example Input:**

```text
hello world! 123
```

**Expected Output:**

```text
LETTERS 10
DIGITS 3
```

### Code

```python
sentence = input()

letters = 0
digits = 0

for char in sentence:
    if char.isalpha():
        letters += 1
    elif char.isdigit():
        digits += 1

print("Letters:", letters)
print("Digits:", digits)
```

### Output

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/cf4a14a3-dc48-4bcc-aa3f-6033f3cfa896" />


---

## 3. Factorial of Numbers

Write a Python program that computes the factorial of given numbers. The results are printed in a comma-separated sequence on a single line.

**Example Input:**

```text
8
```

**Output:**

```text
40320
```

### Code

```python
numbers = input().split(',')
result = []

for n in numbers:
    n = int(n)
    fact = 1

    for i in range(1, n + 1):
        fact *= i

    result.append(str(fact))

print(','.join(result))
```

### Output


<img width="1910" height="1061" alt="image" src="https://github.com/user-attachments/assets/e06da347-18d8-4dc6-8566-4180b2bccd1a" />
