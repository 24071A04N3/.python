# .python
Check if a number is prime
python
Copy code
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

print(is_prime(29))  # Example usage
2. Fibonacci sequence generator using recursion
python
Copy code
def fibonacci(n):
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    elif n == 2:
        return [0, 1]
    else:
        seq = fibonacci(n - 1)
        seq.append(seq[-1] + seq[-2])
        return seq

print(fibonacci(10))  # Example usage
3. Find GCD and LCM of two numbers
python
Copy code
import math

def gcd_lcm(a, b):
    gcd = math.gcd(a, b)
    lcm = (a * b) // gcd
    return gcd, lcm

print(gcd_lcm(12, 18))  # Example usage
4. Simple calculator using functions
python
Copy code
def calculator(a, b, operation):
    if operation == '+':
        return a + b
    elif operation == '-':
        return a - b
    elif operation == '*':
        return a * b
    elif operation == '/':
        return a / b if b != 0 else "Cannot divide by zero"
    else:
        return "Invalid operation"

print(calculator(10, 5, '+'))  # Example usage
5. Remove duplicates from a list
python
Copy code
def remove_duplicates(lst):
    return list(set(lst))

print(remove_duplicates([1, 2, 2, 3, 4, 4, 5]))  # Example usage
6. Create a dictionary and print key-value pairs
python
Copy code
my_dict = {"name": "Alice", "age": 25, "city": "New York", "job": "Engineer", "hobby": "Reading"}

for key, value in my_dict.items():
    print(f"{key}: {value}")
7. Use NumPy for basic matrix operations
python
Copy code
import numpy as np

matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])

sum_matrix = matrix1 + matrix2
product_matrix = np.dot(matrix1, matrix2)

print("Sum:\n", sum_matrix)
print("Product:\n", product_matrix)
8. Read a CSV file using pandas and display the first 5 rows
python
Copy code
import pandas as pd

df = pd.read_csv("sample.csv")  # Replace with actual CSV file path
print(df.head())
9. Find the most common word in a given text
python
Copy code
from collections import Counter

def most_common_word(text):
    words = text.split()
    counter = Counter(words)
    return counter.most_common(1)[0]

text = "apple banana apple orange banana apple"
print(most_common_word(text))  # Example usage
10. Generate a random password with uppercase, lowercase, digits, and special characters
python
Copy code
import random
import string

def generate_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

print(generate_password())


import numpy as np
arr=["1","2","3","4","5"]
a=np.array(arr)
print(a)

import numpy as np

a=np.zeros(3)
print(a)

a=np.identity(3)
print(a)

import numpy as np

array=np.array([1,2,3,4,5])
a=np.amax(array)
 
print(a)

import numpy as np

array=np.array([1,2,3,4,5])
a=np.amin(array)
 
print(a)

import numpy as np

array=np.array([1,2,3,4,5])
a=np.mean(array)
 
print(a)

import numpy as np

array=np.array([1,2,3,4,5])
a=np.unique(array)
 
print(a)
import numpy as np

array=np.random.random((5,5))
print(array)
import numpy as np

array=np.array([1,2,3,4,5])

print(array[1:2])
import pandas as pd 
data = [{'Geeks': 'dataframe', 'For': 'using', 'geeks': 'list'}, 
		{'Geeks':10, 'For': 20, 'geeks': 30}] 

df = pd.DataFrame.from_dict(data) 
print(df)
