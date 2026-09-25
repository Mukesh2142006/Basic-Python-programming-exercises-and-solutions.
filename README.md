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






## Date:25/09/2026
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

