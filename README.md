# Python-Practicals-
Python Practicals 
# Index
| S.No | Practical | 
| :--- | :--- |
| 1 | The roots of a quadratic equation. |
| 2 | Prime Numbers <br /> a-Check Prime numbers  <br /> b-Print All Prime numbers till 'n' <br /> c-First 'n' Prime numbers |
| 3 | Create a pyramid of '*' and a reverse pyramid. |
| 4 | Check Character |
| 5 | Basic String Operations |
| 6 | Swap the first n characters of two strings. |
| 7 | Write a function that accepts two strings and returns the indices of all the occurrences of the second string in the first string as a list. If the second string is not present in the first string then it should return -1. |
| 8 | Write a program to create a list of the cubes of only the even integers appearing in the input list (may have elements of other types also) using the following: <br /> a. 'for' loop <br /> b. list comprehension |
| 9 | Write a program to read a file and <br /> a. Print the total number of characters, words and lines in the file. <br /> b. Calculate the frequency of each character in the file. Use a variable of dictionary type to maintain the count. <br /> c. Print the words in reverse order. <br /> d. Copy even lines of the file to a file named 'Filel' and odd lines to another file named 'File2'. |
| 10 | Write a function that prints a dictionary where the keys are numbers between 1 and 5 and the values are cubes of the keys. |
| 11 | Consider a tuple t1=(1, 2, 5, 7, 9, 2, 4, 6, 8, 10). Write a program to perform following operations: <br /> a. Print half the values of the tuple in one line and the other half in the next line. <br /> b. Print another tuple whose values are even numbers in the given tuple. <br /> c. Concatenate a tuple t2=(11,13,15) with t1. <br /> d. Return maximum and minimum value from this tuple. |
| 12 | Define a class Employee that stores information about employees in the company. The class should contain the following: <br /> (i) data members- count (to keep a record of all the objects being created for this class) and for every employee: an employee number, Name, Dept, Basic, DA and HRA. <br /> (ii) function members: <br /> a._init_method to initialize and/or update the members. Add statements to ensure that the program is terminated if any of Basic, DA and HRA is set to a negative value. <br /> b. function salary, that returns salary as the sum of Basic, DA and HRA. <br /> _del_function to decrease the number of objects created for the class. <br /> d. str function to display the details of an employee along with the salary of an employee in a proper format. |
| 13 | Write a program to define a class "2DPoint" with coordinates x and y as attributes. Create relevant methods and print the objects. Also define a method distance to calculate the distance between any two point objects. |
| 14 | Inherit the above class to create a "3Dpoint" with additional attribute z. Override the method defined in "2DPoint" class, to calculate distance between two points of the "3DPoint" class. |
| 15 | Write a program to accept a name from a user. Raise and handle appropriate exception(s) if the text entered by the user contains digits and/or special characters. |

---
# Practical-1
#### The roots of a quadratic equation

```Python

import math

print("----- Q1 -----")
a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

if a == 0:
    print("Not a quadratic equation")
else:
    d = b * b - 4 * a * c
    if d > 0:
        r1 = (-b + math.sqrt(d)) / (2 * a)
        r2 = (-b - math.sqrt(d)) / (2 * a)
        print("Real and different roots:", r1, r2)
    elif d == 0:
        r = -b / (2 * a)
        print("Real and equal roots:", r, r)
    else:
        real = -b / (2 * a)
        imag = math.sqrt(-d) / (2 * a)
        print("Complex roots:", real, "+", imag, "i and", real, "-", imag, "i")


```
Trail Run <br /> Inputs: a=1, b=5, c=6

Output:
<img width="657" height="240" alt="Image" src="https://github.com/user-attachments/assets/43913bb4-c5bd-46a9-aed3-7a0f24411993" />

---
# Practical-2
#### Prime Numbers <br /> 1 - Check Prime numbers <br /> 2 - Print All Prime numbers till 'n' <br /> 3 - First 'n' Prime numbers 

```Python

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

def primes_till_n(n):
    result = []
    for i in range(2, n + 1):
        if is_prime(i):
            result.append(i)
    return result

def first_n_primes(n):
    result = []
    num = 2
    while len(result) < n:
        if is_prime(num):
            result.append(num)
        num += 1
    return result

n = int(input("Enter n: "))
if is_prime(n):
    print(n, "is prime")
else:
    print(n, "is not prime")
print("Primes till", n, ":", primes_till_n(n))
print("First", n, "primes:", first_n_primes(n))

```

Trail Run <br /> Inputs: a=5

Output:
<img width="1007" height="350" alt="Image" src="https://github.com/user-attachments/assets/6c8df528-622c-4385-8be6-d16cf2d28560" />

---
# Practical-3
#### Create a pyramid of '*' and a reverse pyramid

```Python

rows = int(input("Enter number of rows: "))

print("Pyramid:")
for i in range(1, rows + 1):
    print(" " * (rows - i) + "* " * i)

print("Reverse pyramid:")
for i in range(rows, 0, -1):
    print(" " * (rows - i) + "* " * i)

```

Trail Run <br /> Input: a=6

Output:
<img width="1080" height="842" alt="Image" src="https://github.com/user-attachments/assets/fdff5d90-a6a6-4a42-be25-4e0a71760fba" />

---
# Practical-4
#### Check Character

```Python

ch = input("Enter a single character: ")[0]
names = ["ZERO", "ONE", "TWO", "THREE", "FOUR", "FIVE", "SIX", "SEVEN", "EIGHT", "NINE"]

if ch.isalpha():
    print(ch, "is a letter")
    if ch.isupper():
        print("It is uppercase")
    else:
        print("It is lowercase")
elif ch.isdigit():
    print(ch, "is a numeric digit")
    print("Name:", names[int(ch)])
else:
    print(ch, "is a special character")

```

Trail Run <br /> Inputs: A, 7 

Output:
| <img width="982" height="303" alt="Image" src="https://github.com/user-attachments/assets/eceb4b4c-7d8a-428d-beeb-50b72292a7ae" /> | <img width="950" height="297" alt="Image" src="https://github.com/user-attachments/assets/7cee53a0-0fdf-4fac-be92-0cb01d4250ec" /> |
|:---:|:---:|

---
# Practical-5
#### String Operation 

```Python

s = input("Enter a string: ")
x = input("Enter a character: ")

# a. frequency
count = 0
for i in s:
    if i == x:
        count += 1
print("Frequency of", x, "=", count)

# b. replace a character by another
y = input("Enter the character to replace with: ")
new_s = ""
for i in s:
    if i == x:
        new_s += y
    else:
        new_s += i
print("After replacing:", new_s)

# c. remove first occurrence
new_s = ""
removed = False
for i in s:
    if i == x and not removed:
        removed = True
    else:
        new_s += i
print("After removing first occurrence:", new_s)

# d. remove all occurrences
new_s = ""
for i in s:
    if i != x:
        new_s += i
print("After removing all occurrences:", new_s)

```

Trail Run <br /> Inputs:

Output:
<img width="1080" height="494" alt="Image" src="https://github.com/user-attachments/assets/f072d883-78a6-462d-8dfa-93629f05457e" />

---
# Practical-6
#### Swap the first n characters of two strings.

```Python

s1 = input("Enter first string: ")
s2 = input("Enter second string: ")
n = int(input("Enter n: "))

new1 = s2[:n] + s1[n:]
new2 = s1[:n] + s2[n:]
print("After swapping:", new1, new2)

```

Trail Run <br /> Inputs:

Output:

