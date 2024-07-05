
>>>>>>>>> # Welcome to the Python Coding
-----------------------------------------------------------------
1) Accept two numbers and print the greatest between them

```python
a = input("Enter 1st number : ")
b = input("Enter your 2nd Number : ")

if a > b:
    print(f"{a} is greater than {b}")
elif b > a:
    print(f"{b} is greater than {a}")
else:
    print(f"{a} and {b} both are equal")
```

-----------------------------------------------------
2) Accept the gender from the user as char and print the respective greeting message

```python
gender = input("Enter Your Gender (Male/Female) : ")

if gender == "Male" or gender == "m":
    print("Good Morning, sir..!!")
elif gender == "Female" or gender == "f":
    print("Good Morning, mam..!!")
else:
    print("Wrong Text..!!")
```

--------------------------------------------
3) Accept an integer and check whether it is an even number or odd.

```python
num = int(input("Enter an integer : "))

if num % 2 == 0:
    print("Number is Even")
else:
    print("Number is odd")
```

------------------------------------------------
4) Accept name and age from the user. Check if the user is a valid voter or not.

```python
name = input("Enter Your Name : ")
age = int(input("Enter Your Age : "))

if age < 18:
    print("You are not valid for Vote..!!")
else:
    print("You are valid for Vote..!!")
```

-----------------------------------------------------
5) Accept a year and check if it is a leap year or not

```python
year = int(input("Enter any Year : "))

if year % 4 == 0 and year % 100 != 0:
    print(f"{year} is Leap Year..!!")
elif year % 100 == 0 and year % 400 == 0:
    print(f"{year} is Leap Year..!!")
else:
    print(f"{year} is not Leap Year..!!")
```

----------------------------------------------------------
6) Accept an English alphabet from user and check if it is a consonant or a vowel

```python
z = input("Enter any Alphabet : ")

if z in "aeiouAEIOU":
    print(f"{z} is a vowel..!!")
else:
    print(f"{z} is NOT a vowel..!!")
```



# Loops question
---

1) Print natural number up to n.

```python
n = int(input("Enter a number: "))
for i in range(0, n+1):
    print(i)
```
------------------------------------------------------------------------

 2) Reverse for loop. Print n to 1.
```python
n = int(input("Enter a number: "))
for i in range(n, 0, -1):
    print(i)
```
------------------------------------------------------------------------

3) Take a number as input and print its table
```python
n = int(input("Enter a number: "))
for i in range(1, 11):
    print(f"{n} * {i} = {n * i}")
```
------------------------------------------------------------------------

4) Factorial of a number.
```python
n = int(input("Enter a number: "))
fac = 1
for i in range(1, n+1):
    fac *= i
print(fac)
```
------------------------------------------------------------------------

5) Sum up to n terms.
```python
n = int(input("Enter a number: "))
sum = 0
for i in range(1, n+1):
    sum += i
print(sum)
```
------------------------------------------------------------------------

 6) print all factors of a given number:
```python
n = int(input("Enter a number : "))
print(f"All factors of {n} are: ")
for i in range(1, n+1):
    if n % i == 0:
        print(i)
```
------------------------------------------------------------------------

7) Accept a number and check if it a perfect number or not.
```python
n = int(input("Enter a number: "))
sum = 0
print(f"All factors of {n} are: ")
for i in range(1, n):
    if n % i == 0:
        sum += i
        print(i, end=" ")
print("\nSum of factors is:", sum)
if sum == n:
    print(f"{n} is a perfect number")
else:
    print(f"{n} is not a perfect number")
```
------------------------------------------------------------------------

8) Check if the number is Prime or not.
```python
# i> using count:
n = int(input("Enter a number : "))
count = 0
for i in range(1, n+1):
    if n % i == 0:
        count += 1
if count == 2:
    print(f"{n} is a prime number.")
else:
    print(f"{n} is not a prime number.")

# ii> using sum method:
n = int(input("Enter a number : "))
sum = 0
for i in range(1, n+1):
    if n % i == 0:
        sum += i
if sum == (1+n):
    print(f"{n} is a prime number.")
else:
    print(f"{n} is not a prime number.")
```
------------------------------------------------------------------------

9) Separate each digit of a number and print it on a new line
```python
n = 256
while n > 0:
    a = n % 10
    n = n // 10
    print(a)
```
------------------------------------------------------------------------

10) Accept a number and check if it is a palindromic number (If number and its reverse are equal)
```python
# a = int(input("Enter a number : "))
a = "121"
temp = a[::-1]
if temp == a:
    print("Yes")
else:
    print("No")

# Using loop method:
b = 121
c = b
p = 0
while b > 0:
    k = b % 10
    p = p * 10 + k
    b = b // 10
if c == p:
    print("Palindrome")
else:
    print("Not palindrome")
```
------------------------------------------------------------------------




# **User Define Functions:**

1) Check the Given number is odd or Even::

```python
def oddeven(a):
    if (a % 2) == 0:
        print(f"{a} is Even Number.")
    else:
        print(f"{a} is Odd Number.")

a = int(input("Enter a number : "))
oddeven(a)
```

> We can use “return” for getting value from the function, to where function call.

```python
def oddeven(a):
    if (a % 2) == 0:
        return "Even"
    else:
        return "Odd"

a = int(input("Enter a number : "))
print(oddeven(a))
n = oddeven(a)
print(n)
```

2) Write a Python function that takes an integer as input and determines the type of numbers present in it. The function should count the number of odd and even digits in the input number and print one of the following messages:

- "Even numbers" if all digits in the number are even.
- "Odd numbers" if all digits in the number are odd.
- "Mixed numbers" if the number contains a mix of odd and even digits.

```python
def oddeven(x):
    x = str(x)
    odd = 0
    even = 0
    for i in range(len(x)):
        if int(x[i]) % 2 == 0:
            even += 1
        else:
            odd += 1
    if odd == 0:
        print("All even numbers")
    elif even == 0:
        print("All odd numbers")
    else:
        print(f"Mixed numbers\nCount of odd numbers : {odd}\nCount of even numbers : {even}")

oddeven(123)
```

Output:
```
Mixed numbers
Count of odd numbers : 2
Count of even numbers : 1
```

```python
def oddeven(x):
    odd = 0
    even = 0
    for i in str(x):
        if int(i) % 2 == 0:
            even += 1
        else:
            odd += 1
    if odd == 0:
        print("All even numbers")
    elif even == 0:
        print("All odd numbers")
    else:
        print(f"Count of odd numbers : {odd}\nCount of even numbers : {even}")

a = int(input("Enter a number : "))
oddeven(a)
```

Output:
```
Enter a number : 12123
Count of odd numbers : 3
Count of even numbers : 2
```

# **::: Advance Level Questions :::** 

Strings ::
=========

—------------------------------------------------------------------------

1) Print string in reverse, its length, in uppercase, lowercase and copy into another string.

```python
a = "AjaY"

# Convert to uppercase
print(a.upper())
# Output : AJAY

# Convert to lowercase
print(a.lower())
# Output : ajay

# Print reverse string using slicing
print(a[::-1])
# Output : YajA

# Print reverse string using for loop
b = ""
for i in a[::-1]:
    b += i
print(b)
# Output : YajA

# Reverse a string without using slicing
c = ""
for i in range(len(a)-1, -1, -1):
    c += a[i]
print(c)
# Output : YajA

# Copy a string into another string using "="
b = a
print(b)
# Output : AjaY

# Find length of a
print("Length of a : ", len(a))
# Output : 4

# Merge / join / add / concatenate 2 string :
a = "Mango"
b = "Orange"
c = a + b  # using concatenation "+"
print(c)
d = " ".join([a, b])  # using .join Method
print(d)
```

—------------------------------------------------------------------------

2) Arrange string characters such that lowercase letters should come first in another string.

```python
a = "yoo BrotHER How Are You"
b = ""
c = ""
for i in a:
    if i.islower():  # .islower checks the case of element
        b += i
    elif i.isupper():
        c += i
d = b + c
print(d)
# Output : yoorotowreouBHERHAY
```

—------------------------------------------------------------------------

3) Count all letters, digits, and special symbols from a given string

```python
str1 = "P@#yn26at^&i5ve"
chars = ""
digits = ""
symbols = ""
for i in str1:
    if i.isalpha():
        chars += i
    elif i.isdigit():
        digits += i
    else:
        symbols += i

print("Chars : ", len(chars))
print("Digits : ", len(digits))
print("Symbols : ", len(symbols))
# Outputs:
# Chars : 8
# Digits : 3
# Symbols : 4
```

—------------------------------------------------------------------------

4) Count Vowels from given string

```python
str1 = "my name is Khan"
vowel = 0
const = 0
for i in str1:
    if i in "aeiouAEIOU":
        vowel += 1
    elif i == " ":
        pass
    else:
        const += 1

print(f"Vowel : {vowel} \nConsonant : {const}")
# Output : Vowel : 4
# Consonant : 8

# Using a function:
def vowelconst(x):
    vowel = 0
    const = 0
    for i in x:
        if i.lower() in "aeiou":
            vowel += 1
        elif i == " ":
            pass
        else:
            const += 1
    print(f"Vowel : {vowel} \nConsonant : {const}")

str1 = "my name is Khan"
vowelconst(str1)
# Output : Vowel : 4
# Consonant : 8
```

—------------------------------------------------------------------------

5) Check if a string is Palindrome or not

```python
def palindrome(x):
    b = ""
    for i in range(len(x)-1, -1, -1):
        b += x[i]
    if b == x:
        print(f"String '{x}' is a palindrome.")
    else:
        print(f"String '{x}' is not a palindrome.")

a = "naman"
palindrome(a)
# Output : String 'naman' is a palindrome.

def palindrome(x):
    a = x[::-1]
    if x == a:
        print(f"String '{x}' is a palindrome.")
    else:
        print(f"String '{x}' is not a palindrome.")

a = "naman"
palindrome(a)
# Output : String 'naman' is a palindrome.
```

—------------------------------------------------------------------------

# List ::
=========

1) Accept List elements and reprint it

```python
l = []
a = int(input("How many numbers you want in the list: "))
for i in range(a):
    z = input("Write an element and press Enter: ")
    l.append(z)
print(f"Your list with {a} elements: {l}")
```

Output:
```
How many numbers you want in the list: 5
Write an element and press Enter: 12
Write an element and press Enter: ada
Write an element and press Enter: asc
Write an element and press Enter: 55
Write an element and press Enter: 32
Your list with 5 elements: ['12', 'ada', 'asc', '55', '32']
```

—------------------------------------------------------------------------

2) Print List elements in reverse order

```python
l = []
a = int(input("How many numbers you want in the list: "))
for i in range(a):
    z = int(input("Write an element and press Enter: "))
    l.append(z)
k = l[::-1]
print(f"List with {a} elements in reverse order: {k}")
```

Output:
```
How many numbers you want in the list: 5
Write an element and press Enter: 1
Write an element and press Enter: 2
Write an element and press Enter: 3
Write an element and press Enter: 4
Write an element and press Enter: 5
List with 5 elements in reverse order: [5, 4, 3, 2, 1]

a = [1, 2, 3, 4, 5, 6]
b = []
for i in a[::-1]:  # We can use for i in range(len(a)-1, -1, -1):
    b.append(i)   # b.append(a[i])
print(f"List {a} in reverse order: {b}")
```

Output:
```
List [1, 2, 3, 4, 5, 6] in reverse order: [6, 5, 4, 3, 2, 1]
```

—------------------------------------------------------------------------

3) Print positive and negative elements of a List in separate lists

```python
a = [1, -2, -3, 4, -5, 6]
b = []
c = []
for i in a:
    if i >= 0:
        b.append(i)
    else:
        c.append(i)
print(f"List of positive integers: {b}\nList of negative integers: {c}")
```

Output:
```
List of positive integers: [1, 4, 6]
List of negative integers: [-2, -3, -5]
```

—------------------------------------------------------------------------

4) Find the greatest element and print its index too.

```python
l = [2, 96, 69, 77, 145, 20]
max_value = l[0]
index = 0
for i in range(len(l)):
    if l[i] > max_value:
        max_value = l[i]
        index = i
print(f"Greatest number in list {l} is {max_value} at index {index}")
```

Output:
```
Greatest number in list [2, 96, 69, 77, 145, 20] is 145 at index 4
```

We can use the `max()` method but it’s not recommended:

```python
a = max(l)
print(f"Greatest number in list {l} is {a}")
```

Output:
```
Greatest number in list [2, 96, 69, 77, 145, 20] is 145
```

—------------------------------------------------------------------------

5) Find the second greatest element and print its index too.

```python
l = [2, 96, 69, 77, 145, 20]
max_value = max2 = float('-inf')
index = index2 = 0

for i in range(len(l)):
    if l[i] > max_value:
        max2 = max_value
        index2 = index
        max_value = l[i]
        index = i
    elif l[i] > max2:
        max2 = l[i]
        index2 = i

print(f"Second greatest number in list {l} is {max2} at index {index2}")
```

Output:
```
Second greatest number in list [2, 96, 69, 77, 145, 20] is 96 at index 1
```

—------------------------------------------------------------------------

6) Check if List is sorted or not.

```python
l = [1, 2, 3, 4, 5, 6]
sorted_flag = True
for i in range(len(l)-1):
    if l[i] > l[i+1]:
        sorted_flag = False
        break

if sorted_flag:
    print("Your list is sorted")
else:
    print("Your list is not sorted")
```

Output:
```
Your list is sorted
```

—------------------------------------------------------------------------

7) Palindromic List - Write a program to check if elements of a List are the same from front to back

```python
def palindrome(x):
    a = x[::-1]
    if x == a:
        print(f"Your list {x} is palindrome")
    else:
        print(f"Your list {x} is not palindrome")

l = [1, 2, 1]
palindrome(l)
```

Output:
```
Your list [1, 2, 1] is palindrome
```

Another method:

```python
a = [1, 2, 3, 4, 3, 2, 1]
b = []
for i in range(len(a)-1, -1, -1):
    b.append(a[i])

if a == b:
    print("Your list is palindrome")
else:
    print("Your list is not palindrome")
```

Output:
```
Your list is palindrome
```

—------------------------------------------------------------------------

8) How many unique elements are there in the list excluding repetitions.

```python
a = [1, 2, 3, 4, 3, 2, 1]
b = set(a)
print(b)
```

Output:
```
{1, 2, 3, 4}
```

Certainly! Here's your text converted into Markdown format:


# Dictionary::
===========

1) Write a Python script to merge two Python dictionaries.

```python
a = {1: "Jay", 2: "Vijay"}
b = {3: "Ajay", 4: "Digvijay"}
c = a.copy()
c.update(b)
print(c)
```

Output:
```
{1: 'Jay', 2: 'Vijay', 3: 'Ajay', 4: 'Digvijay'}
```

2) Write a Python program to sum all the values in a dictionary.

```python
a ={1:5,2:15,3:25} 
sum = 0 
for i in a: 
sum = sum + a[i] 
print(f"The Sum of all values of {a} is {sum} ")
```

Output:
```
The Sum of all values of {1: 5, 2: 15, 3: 25} is 45
```
or
```python
a ={1:5,2:15,3:25} 
sum = 0 
for i in a.values(): 
sum += i 
print(f"The Sum of all values of {a} is {sum} ")
```

Output:
```
The Sum of all values of {1: 5, 2: 15, 3: 25} is 45
```


3) Count the frequency of each element in a list.

```python
a = [1, 2, 2, 3, 3, 4, 4, 5, 5, 5, 5, 5, 6, 1, 1, 2, 2, 3, 4, 5]
b = {}
for i in a:
    if i in b.keys():
        b[i] += 1
    else:
        b[i] = 1
print(b)
```

Output:
```
{1: 3, 2: 4, 3: 3, 4: 3, 5: 6, 6: 1}
```

—------------------------------------------------------------------------

4) Write a Python program to combine two dictionaries by adding values for common keys.

```python
a = {1: 10, 2: 20, 3: 40}
b = {3: 10, 1: 20, 4: 40}

for key in b:
    if key in a:
        a[key] += b[key]
    else:
        a[key] = b[key]

print(a)
```

Output:
```
{1: 30, 2: 20, 3: 50, 4: 40}
```

# ::: ULTIMATE CODING :::
=====================

# PALINDROME :

1) Check if the given string is palindrome or not!!

**Method 1:** using reverse string function `a[::-1]`

```python
def palindrome(x):
    a = x[::-1]
    if x == a:
        print("it's palindrome")
    else:
        print("it's not palindrome")

b = "nitin"
palindrome(b)
```

Output:
```
it's palindrome
```

—------------------------------------------------------------------------

**Method 2:** using INDEXING or length function (`len(a)`)

```python
def palindrome(b):
    for i in range(len(b)):
        if b[i] == b[len(b) - i - 1]:
            return "it's palindrome"
        else:
            return "it's not palindrome"

x = "12121"
print(palindrome(x))
```

Output:
```
it's palindrome
```

—------------------------------------------------------------------------

**Method 3:** using REVERSE (`reversed(x)`) and JOIN function (`"".join(y)`)

```python
def palindrome(x):
    z = reversed(x)
    y = "".join(z)
    if x == y:
        print("it's palindrome")
    else:
        print("it's not palindrome")

a = "nitin"
palindrome(a)
```

Output:
```
It's Palindrome
```

—------------------------------------------------------------------------

**Method 4:** using WHILE LOOP or CONDITIONAL LOOP

```python
def palindrome(x):
    f = 0
    l = len(x) - 1
    while f < l:
        if x[f] == x[l]:
            f += 1
            l -= 1
        else:
            return "It's not Palindrome"
    return "It's Palindrome"

p = "nitin"
print(palindrome(p))
```

Output:
```
It's Palindrome
```

—------------------------------------------------------------------------

2) Check if the Given NUMBER is palindrome or not!!

**Method 1:** NOT Preferred

```python
n = 12321
s = str(n)
r = s[::-1]
if s == r:
    print("The number is Palindrome")
else:
    print("The number is not Palindrome")
```

Output:
```
The number is palindrome
```

—------------------------------------------------------------------------

**Method 2:** Use WHILE LOOP: **MOST IMP**

```python
def palindrome(n):
    r = 0
    temp = n
    while temp > 0:
        digit = temp % 10
        temp = temp // 10
        r = r * 10 + digit
    if r == n:
        print("The number is palindrome")
    else:
        print("The number is not palindrome")

t = 121
palindrome(t)
```

Output:
```
The number is palindrome
```

—------------------------------------------------------------------------

# FIBONACCI : #

1) Finding Sum of Fibonacci numbers up to the given number:

```python
def Fibonacci(x):
    a = 0
    b = 1
    sum = 0
    total = 1
    
    if x == 0:
        print(a)
        total = 0
    else:
        print(a)
        print(b)
        total = 1
    
    for i in range(x - 2):
        sum = a + b
        a = b
        b = sum
        total = total + sum
        print(sum)
    
    print(f"Sum of first {x} Fibonacci numbers is {total}")
    
z = int(input("Enter a number to get Fibonacci numbers: "))
Fibonacci(z)
```

Output:
```
Enter a number to get Fibonacci numbers: 5
0
1
1
2
3
Sum of first 5 Fibonacci numbers is 7
```

—------------------------------------------------------------------------

**METHOD 2:** using only 2 variables

```python
def Fibonacci(x):
    a = 0
    b = 1
    print(a)
    while b < x - 1:
        print(b)
        a, b = b, a + b  # swapping method of python
    
z = int(input("Enter a number to get Fibonacci numbers: "))
Fibonacci(z)
```

Output:
```
Enter a number to get Fibonacci numbers: 5
0
1
1
2
3
```

—------------------------------------------------------------------------

**METHOD 3:** using RECURSION : **MOST IMP**

```python
def Fibonacci(n):
    if n <= 1:
        return n
    else:
        return Fibonacci(n - 1) + Fibonacci(n - 2)

n = int(input("Enter a number: "))
if n <= 0:
    print("Invalid input")
else:
    for i in range(n):
        print(Fibonacci(i))
```

Output:
```
Enter a number: 5
0
1
1
2
3
```

—------------------------------------------------------------------------

# COMPRESS STRING : #

1) Compress a given string:

**METHOD 1:** Use FOR LOOP

```python
def compress(x):
    new_s = ""
    count = 1
    
    for i in range(len(x) - 1):
        if x[i] == x[i + 1]:
            count += 1
        else:
            new_s = new_s + x[i] + str(count)
            count = 1
    
    new_s = new_s + x[len(x) - 1] + str(count)
    print(new_s)

a = str(input("Enter any string to compress: "))
compress(a)
```

Output:
```
Enter any string to compress: aabbbcceegg
a2b3c2e2g2
```

—------------------------------------------------------------------------

**METHOD 2:** Use WHILE LOOP

```python
def compress(x):
    new_s = ""
    i = 0
    
    while i < len(x) - 1:
        count = 1
        while i < len(x) - 1 and x[i] == x[i + 1]:
            count += 1
            i += 1
        i += 1
        new_s = new_s + x[i - 1] + str(count)
    
    print("Compressed string:", new_s)

z = str(input("Enter a string to compress: "))
compress(z)
```

Output:
```
Enter a string to compress: aaaavbbbvv
Compressed string: a4v1b3v2
```

—------------------------------------------------------------------------

# FizzBuzz Problem : #

1) Print Fizz, Buzz, FizzBuzz, or the number based on divisibility:

**METHOD 1:** Use FOR LOOP

```python
def fizzbuzz(i):
    for x in range(1, i + 1):
        if x % 15 == 0:
            print(f"{x} = FizzBuzz")
        elif x % 3 == 0:
            print(f"{x} = Fizz")
        elif x % 5 == 0:
            print(f"{x} = Buzz")
        else:
            print(f"{x} = {x}")

i = 20
fizzbuzz(i)
```

Output:
```
1 = 1
2 = 2
3 = Fizz
4 = 4
5 = Buzz
6 = Fizz
7 = 7
8 = 8
9 = Fizz
10 = Buzz
11 = 11
12 = Fizz
13 = 13
14 = 14
15 = FizzBuzz
16 = 16
17 = 17
18 = Fizz
19 = 19
20 = Buzz
```

—------------------------------------------------------------------------

**METHOD 2:** Use Dictionary

```python
def fizzbuzz(n):
    d = {3: "Fizz", 5: "Buzz"}
    for i in range(1, n + 1):
        result = ""
        for k in d.keys():
            if i % k == 0:
                result += d[k]
        if not result:
            result = i
        print(result)

s = 15
fizzbuzz(s)
```

Output:
```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

—------------------------------------------------------------------------

# Character Occurence : #

1. Least Repeating character in a string

**Method 1:** Using Dictionary

```python
def least_repeating_char(a):
    d = {}
    for i in a:
        if i in d:
            d[i] += 1
        else:
            d[i] = 1
    
    print(d)  # To Print Number Of Occurrences Of All Characters
    result = min(d, key=d.get)
    print("Minimum occurred Character is:", result)

b = str(input("Enter a string: "))
least_repeating_char(b)
```

Output:
```
Enter a string: ababa
{'a': 3, 'b': 2}
Minimum occurred Character is: b
```

—-----------------------------------------------------------------------

**Method 2:** Using Inbuilt Function `Counter` from `collections`

```python
from collections import Counter

a = "ababaa"
c = Counter(a)
print(c)
result = min(c, key=c.get)
print("Minimum occurred Character is:", result)
```

Output:
```
Counter({'a': 4, 'b': 2})
Minimum occurred Character is: b
```

—-----------------------------------------------------------------------

# Count Particular element : #

**Method 1:** Using inbuilt Method `.count`

```python
# count in string
s = "ababaa"
print(s.count("a"))  # Output: 4

# count in list of strings
l = ["a", "b", "a", "b", "a"]
print(l.count("a"))  # Output: 3

# count in list of integers
l2 = [1, 2, 3, 4, 1, 2, 3, 4, 2, 3]
print(l2.count(2))  # Output: 3
```

—-----------------------------------------------------------------------

**Method 2:** Without using inbuilt Method, using Dictionary

```python
def count_element(s, c):
    d = {}
    for i in s:
        if i in d:
            d[i] += 1
        else:
            d[i] = 1
    
    print(d)
    try:
        print(f"The count of '{c}' in '{s}' is", d[c])
    except KeyError:
        print(f"The count of '{c}' in '{s}' is 0")

z = str(input("Enter a string: "))
x = str(input("Enter an element you want to find: "))
count_element(z, x)
```

Output:
```
Enter a string: ababaa
Enter an element you want to find: a
{'a': 4, 'b': 2}
The count of 'a' in 'ababaa' is 4
```

—-----------------------------------------------------------------------

# Count all elements : #

```python
def count_all_elements(s):
    d = {}
    for i in s:
        if i in d:
            d[i] += 1
        else:
            d[i] = 1
    
    print("Count of all elements is:", d)

z = str(input("Enter a string: "))
count_all_elements(z)
```

Output:
```
Enter a string: ababa
Count of all elements is: {'a': 3, 'b': 2}
```

—-----------------------------------------------------------------------

# Prime Number : #

**Method 1:** Using FLAG

```python
def is_prime(n):
    flag = False
    if n > 1:
        for i in range(2, n):
            if n % i == 0:
                flag = True
                break
    if flag:
        print("It's not a prime number")
    else:
        print("It's a prime number")

a = 7
is_prime(a)
```

Output:
```
It's a prime number
```

—-----------------------------------------------------------------------

**Method 2:** Using For and Else

```python
def is_prime(n):
    if n > 1:
        for i in range(2, n):
            if n % i == 0:
                print("It's not a prime number")
                break
        else:
            print("It's a prime number")
    else:
        print("It's a prime number")

prime(12)
```

Output:
```
It's not a prime number
```

—-----------------------------------------------------------------------

# List of Prime Number : #

**Method 1:** Using For Else

```python
def prime(a, b):
    for n in range(a, b):
        if n > 1:
            for i in range(2, n):
                if n % i == 0:
                    break
            else:
                print(n)

prime(2, 10)
```

Output:
```
2
3
5
7
```

—-----------------------------------------------------------------------

**Method 2:** Using Flag

```python
def prime(a, b):
    for n in range(a, b):
        flag = False
        if n > 1:
            for i in range(2, n):
                if n % i == 0:
                    flag = True
                    break
            if not flag:
                print(n)

prime(1, 10)
```

—-----------------------------------------------------------------------

# Modify String Format : #

- Input = I_Am_Coder 
- Output = i.aM. a.cODER 

- Input = This_Is_A _Good_Morning 
- Output = tHIS.iS.a. gOOD.mORNING 

- first_upper_letter = first_lower_letter 
- remaining_lower_letter = remaining_upper_letter 

**Method 1:** Using list

```python
def modify_string(s):
    temp = s.split("_")
    l = []
    for i in temp:
        l.append(i[0].lower() + i[1:].upper())
    z = ".".join(l)
    print(z)

a = "This_Is_A_Good_Morning"
modify_string(a)
```

Output:
```
tHIS.iS.a. gOOD.mORNING
```

—-----------------------------------------------------------------------

**Method 2:** Using string manipulation

```python
def modify_string(s):
    temp = s.split("_")
    st = ""
    for i in temp:
        st = st + i[0].lower() + i[1:].upper() + "."
    st = st[:-1]
    print(st)

a = "This_Is_A_Good_Morning"
modify_string(a)
```

Output:
```
tHIS.iS.a. gOOD.mORNING
```
—-----------------------------------------------------------------------

# Armstrong Number / Modify String Format : #

```python
def is_armstrong(n):
    a = str(n)
    temp = n
    sum = 0
    while temp > 0:
        d = temp % 10
        sum += d ** (len(a))
        temp //= 10
    if sum == n:
        print(f"{n} is an Armstrong number")
    else:
        print(f"{n} is not an Armstrong number")

x = int(input("Enter a number: "))
is_armstrong(x)
```

Output:
```
Enter a number: 1634
1634 is an Armstrong number
```

# Strings are Anagram or Not : #

**Anagram strings:**
- An anagram of a string is another string that contains the same characters, only the order of characters can be different. For example, "abcd" and "dabc" are anagrams of each other.

```python
def anagram(s1, s2):
    if sorted(s1) == sorted(s2):
        print(f"strings {s1} and {s2} are anagram")
    else:
        print(f"strings {s1} and {s2} are not anagram")

a = input("Enter first string: ")
b = input("Enter second string: ")
anagram(a, b)
```

Output:
```
Enter first string: abcd
Enter second string: abdc
strings abcd and abdc are anagram
```

—-----------------------------------------------------------------------

# Unpack a Collection : #

If you have a collection of values in a list, tuple, etc., Python allows you to extract the values into variables. This is called unpacking.

```python
a = [1, 2, 3, 4, 5]
x, y, z, b, c = a
print(x, y, z, b, c, a)
```

Output:
```
1 2 3 4 5 [1, 2, 3, 4, 5]
```

—-----------------------------------------------------------------------

# Random Number #

If you want to generate a random number from a particular range, import "random" and print it according to the syntax:

```python
import random
print(random.randrange(1, 6))
```

Output:
```
5
```

—-----------------------------------------------------------------------

# Casting : #

Specify a Variable Type:

```python
a = int(2.5)
b = float(3)
c = str(25)
print(a, type(a))
print(b, type(b))
print(c, type(c))
```

Output:
```
2 <class 'int'>
3.0 <class 'float'>
25 <class 'str'>
```








