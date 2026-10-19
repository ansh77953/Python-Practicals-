# Python-Practicals-
Python Practicals 
# Index
| S.No | Practical | 
| :--- | :--- |
| 1 | Write a program to find the roots of a quadratic equation. |
| 2 | Write a program to accept a number 'n' and <br /> a. Check if 'n' is prime <br /> b. Generate all prime numbers till 'n' <br /> c. Generate first 'n' prime numbers |
| 3 | Write a program to create a pyramid of the character '*' and a reverse pyramid |
| 4 | Write a program that accepts a character and performs the following: <be /> a. print whether the character is a letter or numeric digit or a special character. <br /> b. if the character is a letter, print whether the letter is uppercase or lowercase <be /> c. if the character is a numeric digit, prints its name in text |
| 5 | Write a program to perform the following operations on a string <br /> a. Find the frequency of a character in a string. <br /> b. Replace a character by another character in a string. <br /> c. Remove the first occurrence of a character from a string. <br /> d. Remove all occurrences of a character from a string |
| 6 | Write a program to swap the first n characters of two strings. |
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
Write a program to find the roots of a quadratic equation

```
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

