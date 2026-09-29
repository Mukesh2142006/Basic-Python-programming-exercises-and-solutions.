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






# Date:25/09/2026
## 1. Student Attendance Analysis
A college maintains the daily attendance details of its students in the form of a list containing student IDs. Some students may have attended multiple sessions on the same day. The administration wants to identify the longest continuous sequence of sessions in which no student ID is repeated. Develop a solution that determines the maximum length of such a sequence.

```
a = input("Enter numbers: ").split()
longest = 0
for i in range(len(a)):
    x = []
    for j in range(i, len(a)):
        if a[j] in x:
            break
        x.append(a[j])
    if len(x) > longest:
        longest = len(x)
print("Longest length:", longest)

```
## output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bdab5525-df74-4a6f-9883-e18e728f9d03" />


## 2. Online Shopping Price Analysis
An online shopping application stores the prices of products viewed by a customer during a browsing session. The customer wants to identify a continuous range of products that provides the maximum possible total discount value. Given the discount values, determine the maximum value that can be obtained from any continuous range.

```

a = input("Enter numbers: ").split()

max_sum = 0
sum = 0

for i in a:
    sum = sum + int(i)

    if sum > max_sum:
        max_sum = sum

    if sum < 0:
        sum = 0

print("Maximum sum:", max_sum)
```

## Output :
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/21401778-9676-4152-bda7-69a29e67fb34" />


## 3. Rainwater Collection System
A city installs buildings of different heights along a straight road. During rainfall, water gets collected between taller buildings. The engineering team needs to calculate the total amount of water that can remain trapped after heavy rainfall based on the heights of the buildings.

```
a = input("Enter building heights: ").split()

a = [int(x) for x in a]

water = 0

for i in range(1, len(a) - 1):
    left = max(a[:i])
    right = max(a[i+1:])

    height = min(left, right)

    if height > a[i]:
        water = water + height - a[i]

print("Water trapped:", water)

```
## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/af348ff1-79b1-4ed6-869f-8cd74d1e30b0" />




## 4. Employee Performance Analysis
A company stores the monthly performance scores of an employee for several months. The scores may contain both positive and negative values depending on the employee's performance. Management wants to identify the continuous period during which the employee achieved the highest overall performance.

```
a = input("Enter scores: ").split()

max_sum = 0
sum = 0

for i in a:
    sum = sum + int(i)

    if sum > max_sum:
        max_sum = sum

    if sum < 0:
        sum = 0

print("Maximum performance:", max_sum)
```

## Output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0d96127b-1ec5-4670-b8c2-824ae50be57d" />


## 5. Product Sales Analysis
A retail company stores the daily sales quantity of a product for several consecutive days. Due to seasonal changes, some days may have negative adjustments. The company wants to identify the period that produced the highest multiplication of sales-related values. Develop a solution to determine this maximum product.

```
a = input("Enter numbers: ").split()

max_product = int(a[0])
product = 1

for i in a:
    product = product * int(i)

    if product > max_product:
        max_product = product

    if product == 0:
        product = 1

print("Maximum product:", max_product)
```
## output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/241f2d4e-6d90-49e1-92ec-44bdc524bf94" />




## 6. Customer Purchase History
An e-commerce application stores the product IDs purchased by a customer in chronological order. The same product may appear multiple times. The system needs to determine the longest sequence of consecutive purchases in which every product ID is unique.

```
a = input("Enter product IDs: ").split()

longest = 0

for i in range(len(a)):
    x = []

    for j in range(i, len(a)):
        if a[j] in x:
            break

        x.append(a[j])

    if len(x) > longest:
        longest = len(x)

print("Longest length:", longest)
```
## output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8096962c-07c3-42da-8177-e38fb3a84f93" />


## 7. Bank Transaction Analysis
A bank stores transaction amounts for a customer's account. A continuous group of transactions may add up to a specific target amount. The auditing system needs to determine how many different continuous transaction groups produce exactly the specified amount.

```
a = input("Enter transactions: ").split()
target = int(input("Enter target: "))

count = 0

for i in range(len(a)):
    sum = 0

    for j in range(i, len(a)):
        sum = sum + int(a[j])

        if sum == target:
            count = count + 1

print("Number of groups:", count)

```
## output:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2b16a1a0-7d3d-4726-beb1-63f30d244477" />


## 8. Employee Skill Grouping
A company receives a list of employee skill codes represented as strings. Employees having the same set of characters in their skill codes belong to the same skill category, even if the characters appear in a different order. The HR system needs to organize employees into appropriate skill groups.

```
a = input("Enter words: ").split()

groups = {}

for word in a:
    key = ''.join(sorted(word))

    if key not in groups:
        groups[key] = []

    groups[key].append(word)

for group in groups.values():
    print(group)
```

## Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/300f2d90-6bac-4f7f-b8b6-e61372b16cd2" />


## 9. Network Packet Analysis
A network monitoring system receives packet identifiers in chronological order. The system must determine the longest sequence of consecutive packets whose identifiers form a continuous numerical sequence, regardless of their original order in the incoming data.

```
a = input("Enter numbers: ").split()

a.sort()

longest = 1
count = 1

for i in range(1, len(a)):
    if int(a[i]) == int(a[i-1]) + 1:
        count = count + 1
    else:
        count = 1

    if count > longest:
        longest = count

print("Longest sequence:", longest)
```
## output

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/25343334-92fd-487d-82d6-cd9df522da06" />


## 10. Hospital Appointment Scheduling
A hospital receives appointment requests represented by starting and ending times. Some appointments overlap with each other. The scheduling system needs to combine overlapping appointment periods so that the final schedule contains only non-overlapping time ranges.
```
a = input("Enter intervals: ").split()

intervals = []

for i in range(0, len(a), 2):
    intervals.append([int(a[i]), int(a[i+1])])

intervals.sort()

result = []

for x in intervals:
    if not result or x[0] > result[-1][1]:
        result.append(x)
    else:
        result[-1][1] = max(result[-1][1], x[1])

print("Merged intervals:", result)
```

## output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/46b4e452-cc0a-4e57-9eef-025ff03ac64e" />

# 29/9/2026


## 1. Print All Prime Numbers Between a Range

**Question:**
Print all prime numbers between the given input range.

**Example Input:**

```text
20 50
```

**Code:**

```python
a, b = map(int, input().split())

for n in range(a, b + 1):
    if n < 2:
        continue

    prime = True

    for i in range(2, n):
        if n % i == 0:
            prime = False
            break

    if prime:
        print(n)
```

**Output:**

<img width="560" height="321" alt="image" src="https://github.com/user-attachments/assets/2964533d-6901-40cd-8134-4385dfa7def2" />


---

## 2. Factorial Using Recursion

**Question:**
Find the factorial of a number using recursion.

**Example Input:**

```text
5
```

**Code:**

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)


n = int(input())

print(factorial(n))
```

**Output:**
<img width="452" height="399" alt="image" src="https://github.com/user-attachments/assets/5b097169-a6bc-40b6-9c76-536345d8592f" />




---

## 3. Square of Numbers Using Lambda

**Question:**
Find the square of each number using a lambda function.

**Example Input:**

```text
2 3 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

square = lambda x: x * x

for n in numbers:
    print(square(n))
```

**Output:**

<img width="510" height="241" alt="image" src="https://github.com/user-attachments/assets/1e2476ad-1bf2-4970-8a20-27f66e530c20" />


---

## 4. Find the Second Largest Element in a List

**Question:**
Find the second largest element in a list.

**Example Input:**

```text
10 5 20 8 20 15
```

**Code:**

```python
numbers = list(map(int, input().split()))

numbers = list(set(numbers))
numbers.sort()

print(numbers[-2])
```

**Output:**

<img width="544" height="323" alt="image" src="https://github.com/user-attachments/assets/c4b27511-d132-4e04-ab4b-ab846eb9b747" />


---

## 5. Count Frequency of Characters in a String

**Question:**
Count the frequency of each character in a string.

**Example Input:**

```text
banana
```

**Code:**

```python
s = input()

freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

**Output:**

<img width="551" height="389" alt="image" src="https://github.com/user-attachments/assets/4072528f-6b80-4ccb-958b-d6303f54bccf" />


---

## 6. Calculate Area of a Circle Using Math Library

**Question:**
Calculate the area of a circle using the `math` library.

**Example Input:**

```text
5
```

**Code:**

```python
import math

r = float(input())

area = math.pi * r * r

print(area)
```

**Output:**

<img width="615" height="206" alt="image" src="https://github.com/user-attachments/assets/49937cf3-4b2e-4202-a5d5-61763bc22d2c" />


---

## 7. Reverse a String Without Using Built-in Reverse

**Question:**
Reverse a string without using the built-in `reverse()` function.

**Example Input:**

```text
python
```

**Code:**

```python
s = input()

result = ""

for i in range(len(s) - 1, -1, -1):
    result += s[i]

print(result)
```

**Output:**

<img width="550" height="269" alt="image" src="https://github.com/user-attachments/assets/4fe84d35-a1c5-4441-952d-085acdcf047e" />


---

## 8. Remove Duplicates from a List

**Question:**
Remove duplicate elements from a list.

**Example Input:**

```text
1 2 2 3 4 4 5
```

**Code:**

```python
numbers = list(map(int, input().split()))

result = []

for n in numbers:
    if n not in result:
        result.append(n)

print(result)
```

**Output:**

<img width="610" height="310" alt="image" src="https://github.com/user-attachments/assets/830a1c32-92a8-4241-9533-0b7ab1ab15ca" />


---

## 9. Merge Two Dictionaries

**Question:**
Merge two dictionaries into a single dictionary.

**Code:**

```python
d1 = {'a': 10, 'b': 20}
d2 = {'c': 30, 'd': 40}

d1.update(d2)

print(d1)
```

**Output:**

<img width="578" height="332" alt="image" src="https://github.com/user-attachments/assets/27477010-a010-4bb9-b9f4-6a51442e7793" />


---

## 10. Fibonacci Series Using Recursion

**Question:**
Print the Fibonacci series using recursion.

**Example Input:**

```text
7
```

**Code:**

```python
def fibonacci(n):
    if n <= 1:
        return n

    return fibonacci(n - 1) + fibonacci(n - 2)


n = int(input())

for i in range(n):
    print(fibonacci(i), end=" ")
```

**Output:**

<img width="588" height="378" alt="image" src="https://github.com/user-attachments/assets/103fa28b-02fe-425b-ab5b-39f5560a3a3c" />




# NUMPY_CODING

## 1. Student Marks Array

**Question:**
Create a NumPy array using the marks `[78, 65, 89, 56, 92]` and display the array along with its basic properties.

**Code:**

```python
import numpy as np

marks = np.array([78, 65, 89, 56, 92])

print("Array:", marks)
print("Dimension:", marks.ndim)
print("Shape:", marks.shape)
print("Size:", marks.size)
print("Data Type:", marks.dtype)
```

**Output:**

<img width="803" height="409" alt="image" src="https://github.com/user-attachments/assets/d5ece809-1609-4a4a-98c9-7c2749eca6b7" />


---

## 2. Student Marks Access

**Question:**
Access and display specific student marks using NumPy indexing and slicing.

**Code:**

```python
import numpy as np

marks = np.array([72, 85, 64, 90, 76])

print("First student:", marks[0])
print("Third student:", marks[2])
print("First three students:", marks[:3])
print("Last two students:", marks[-2:])
```

**Output:**

<img width="804" height="343" alt="image" src="https://github.com/user-attachments/assets/7f2fa810-fc3b-4950-aa11-11341874b1d6" />


---

## 3. Subject-wise Marks

**Question:**
Create a NumPy array for the given marks and reshape it into a matrix representing 5 students and 3 subjects.

**Code:**

```python
import numpy as np

marks = np.array([
    78, 85, 90,
    65, 72, 80,
    88, 91, 84,
    56, 62, 70,
    95, 89, 92
])

matrix = marks.reshape(5, 3)

print(matrix)
```

**Output:**

<img width="787" height="363" alt="image" src="https://github.com/user-attachments/assets/dc40d241-1988-4112-88e7-79f17600286a" />


---

## 4. Internal and External Marks

**Question:**
Calculate the final marks of five students using internal and external examination marks.

**Code:**

```python
import numpy as np

internal = np.array([25, 28, 24, 27, 30])
external = np.array([60, 55, 65, 58, 62])

final = internal + external

print("Internal Marks:", internal)
print("External Marks:", external)
print("Final Marks:", final)
```

**Output:**

<img width="811" height="353" alt="image" src="https://github.com/user-attachments/assets/b91751ac-175f-44df-a6dd-91ca9b458b01" />


---

## 5. Pass Percentage Analysis

**Question:**
Using NumPy Boolean masking, identify students who have secured 50 marks or above.

**Code:**

```python
import numpy as np

marks = np.array([45, 78, 56, 32, 91])

passed = marks[marks >= 50]

print("Marks:", marks)
print("Students with 50 or above:", passed)
```

**Output:**

<img width="810" height="382" alt="image" src="https://github.com/user-attachments/assets/041e2e9c-c105-4108-89b4-48d35bb4d8d6" />


---

## 6. Average Marks

**Question:**
Calculate the average marks of each student in three subjects.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

average = np.mean(marks, axis=1)

print("Average Marks:", average)
```

**Output:**

<img width="826" height="422" alt="image" src="https://github.com/user-attachments/assets/c2031cb2-80ed-4ce6-847c-45bbd2ae0e5b" />


---

## 7. Class Performance Statistics

**Question:**
Find the total, average, highest, lowest, and standard deviation of the marks `[67, 82, 91, 74, 58]`.

**Code:**

```python
import numpy as np

marks = np.array([67, 82, 91, 74, 58])

print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
print("Standard Deviation:", np.std(marks))
```

**Output:**

<img width="837" height="420" alt="image" src="https://github.com/user-attachments/assets/9821b2bc-ea89-4db3-9a16-729b0afa7318" />


---

## 8. Subject-wise Performance

**Question:**
Calculate the total marks obtained in each subject using an appropriate axis operation.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

subject_total = np.sum(marks, axis=0)

print("Subject-wise Total:", subject_total)
```

**Output:**

<img width="826" height="429" alt="image" src="https://github.com/user-attachments/assets/a51fb6ac-eb3b-4c15-b38b-61862ff706e9" />


---

## 9. Student-wise Performance

**Question:**
Calculate the total marks obtained by each student using an appropriate axis operation.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

student_total = np.sum(marks, axis=1)

print("Student-wise Total:", student_total)
```

**Output:**

<img width="788" height="431" alt="image" src="https://github.com/user-attachments/assets/041ed90c-0d17-4cc8-93ac-f2a91eb5d04e" />


---

## 10. Student Ranking

**Question:**
Arrange the total marks `[245, 278, 219, 290, 256]` in order and determine the ranking of the students.

**Code:**

```python
import numpy as np

marks = np.array([245, 278, 219, 290, 256])

sorted_marks = np.sort(marks)
ranking = np.argsort(marks)[::-1]

print("Sorted Marks:", sorted_marks)
print("Student Ranking:", ranking + 1)
```

**Output:**

<img width="809" height="438" alt="image" src="https://github.com/user-attachments/assets/c76c1b98-7fa2-4f0b-9973-4a9637ced780" />


---

## 11. Duplicate Marks Analysis

**Question:**
Identify the unique marks obtained by the students.

**Code:**

```python
import numpy as np

marks = np.array([85, 92, 85, 76, 92])

unique_marks = np.unique(marks)

print("Marks:", marks)
print("Unique Marks:", unique_marks)
```

**Output:**
<img width="807" height="343" alt="image" src="https://github.com/user-attachments/assets/c4ebce13-06f6-4c5d-a38c-d18676bdaf5c" />


---

## 12. Missing Marks

**Question:**
Calculate the average marks without considering the missing value represented by `np.nan`.

**Code:**

```python
import numpy as np

marks = np.array([78, 85, np.nan, 92, 67])

average = np.nanmean(marks)

print("Marks:", marks)
print("Average:", average)
```

**Output:**

<img width="783" height="332" alt="image" src="https://github.com/user-attachments/assets/04a8a2a6-dbd9-45b8-abbc-1b26041c96de" />


---

## 13. Grade Classification

**Question:**
Classify the students into grades based on their marks.

**Grade Criteria:**

```text
90 and above → A
80–89        → B
70–79        → C
60–69        → D
Below 60     → F
```

**Code:**

```python
import numpy as np

marks = np.array([95, 82, 74, 61, 45])

grades = np.select(
    [
        marks >= 90,
        marks >= 80,
        marks >= 70,
        marks >= 60
    ],
    [
        'A',
        'B',
        'C',
        'D'
    ],
    default='F'
)

print("Marks:", marks)
print("Grades:", grades)
```

**Output:**

<img width="777" height="463" alt="image" src="https://github.com/user-attachments/assets/efef1864-d650-406f-8227-9ede545c6385" />


---

## 14. Random Marks Generation

**Question:**
Generate marks for five students using NumPy's random number generation functionality and perform basic statistical analysis.

**Code:**

```python
import numpy as np

np.random.seed(10)

marks = np.random.randint(0, 101, 5)

print("Generated Marks:", marks)
print("Total:", np.sum(marks))
print("Average:", np.mean(marks))
print("Highest:", np.max(marks))
print("Lowest:", np.min(marks))
```

**Output:**

<img width="774" height="366" alt="image" src="https://github.com/user-attachments/assets/9550466f-51d0-4bb5-a15f-f1178cf3ffb1" />


---

## 15. Student Performance Analysis

**Question:**
Perform a complete student performance analysis by calculating total marks, average marks, highest marks, lowest marks, and identifying students who perform above the class average.

**Code:**

```python
import numpy as np

marks = np.array([
    [78, 85, 90],
    [65, 72, 80],
    [88, 91, 84],
    [56, 62, 70],
    [95, 89, 92]
])

total = np.sum(marks, axis=1)
average = np.mean(marks, axis=1)

class_average = np.mean(average)

highest = np.max(marks, axis=1)
lowest = np.min(marks, axis=1)

above_average = np.where(average > class_average)[0] + 1

print("Total Marks:", total)
print("Average Marks:", average)
print("Highest Marks:", highest)
print("Lowest Marks:", lowest)
print("Class Average:", class_average)
print("Students Above Class Average:", above_average)
```

**Output:**

<img width="848" height="459" alt="image" src="https://github.com/user-attachments/assets/03306038-652b-49b8-9171-9db50dd67abd" />



## PYTHON_FUNCTIONS_CODING

## 1. Calculator Using Function

**Question:**
Write a function `calculate(a, b, operation)` that performs addition, subtraction, multiplication, or division based on the supplied operation.

**Example Input:**

```text
10
5
+
```

**Code:**

```python
def calculate(a, b, operation):
    if operation == "+":
        return a + b

    elif operation == "-":
        return a - b

    elif operation == "*":
        return a * b

    elif operation == "/":
        return a / b

    else:
        return "Invalid operation"


a = int(input())
b = int(input())
operation = input()

print(calculate(a, b, operation))
```

**Output:**

<img width="439" height="531" alt="image" src="https://github.com/user-attachments/assets/e4dab559-8c0b-426f-b903-c8e11632bd12" />



---

## 2. Sum of Numbers Using `*args`

**Question:**
Write a function `sum_numbers(*args)` that accepts any number of arguments and returns their sum.

**Example Input:**

```text
10 20 30 40
```

**Code:**

```python
def sum_numbers(*args):
    total = 0
    for num in args:
        total += num
    return total
print(sum_numbers(10, 20, 30))
```

**Output:**

<img width="469" height="263" alt="image" src="https://github.com/user-attachments/assets/f4b752bc-7869-48e7-806f-5fcad29350f7" />



---

## 3. Employee Information Using `**kwargs`

**Question:**
Write a function `employee(**args)` that accepts employee information such as name, ID, department and salary, then displays the information.

**Code:**

```python
def employee(**args):
    for key, value in args.items():
        print(key, ":", value)
employee(
    name="Mukesh ",
    ID=101,
    department="AIDS",
    salary=30000
)
```

**Output:**


<img width="492" height="454" alt="image" src="https://github.com/user-attachments/assets/6439a63b-7828-47c9-a34b-1d8c953f03a5" />



---

## 4. Remove Duplicates While Preserving Order

**Question:**
Write a function `remove_duplicates(lst)` that returns a list containing only unique elements while preserving their original order.

**Example Input:**

```text
1 2 2 3 4 3 5 1
```

**Code:**

```python
def remove_duplicates(lst):
    result = []

    for item in lst:
        if item not in result:
            result.append(item)

    return result


numbers = list(map(int, input().split()))

print(remove_duplicates(numbers))
```

**Output:**

<img width="532" height="332" alt="image" src="https://github.com/user-attachments/assets/cbaea014-7543-4788-a69a-acd85e7e54f2" />



---

## 5. Sort List of Tuples Using Lambda

**Question:**
Using a lambda function, sort a list of tuples based on the second element.

**Example Input:**

```text
[(1, 5), (2, 3), (4, 1)]
```

**Code:**

```python
numbers = [(1, 5), (2, 3), (4, 1)]

result = sorted(numbers, key=lambda x: x[1])

print(result)
```

**Output:**

<img width="605" height="186" alt="image" src="https://github.com/user-attachments/assets/c3c006f2-c478-4dd2-a7e7-6bd72ea13a2d" />

