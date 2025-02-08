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

SESSION 2 HW
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


AI is a branch of computer science that focuses on creating intelligent systems capable of reasoning, learning, and decision-making.Artificial Intelligence (AI) is a field of computer science that enables machines to simulate human intelligence, including reasoning, learning, and decision-making. Key AI techniques include Machine Learning (ML), which allows machines to learn from data, and Natural Language Processing (NLP), which helps computers understand human language. AI is also used in automation, robotics, and machine vision for improving efficiency and productivity. Its applications span various fields, including astronomy, healthcare, gaming, finance, and cybersecurity. AI enhances medical diagnoses, automates financial processes, and strengthens data security. However, challenges such as ethical concerns, the complexity of human language, and security risks remain. Despite its limitations, AI continues to transform industries, making processes smarter and more efficient.

Chat GPT provides an insightful and useful analysis coming straight to the point without external disturbances and summarized everything by dividing into sectors and defining it in a line which saves time and is easy to understand.Other AI reponses were not that satisfactory because they seemed complex and external information was included .The missing points are it fails to justify or provide examples.



BROKEN CODE


import numpy as np
import pandas as pd
import random

def generate_random_number(min_num, max_num):
    num = random.randint(min_num, max_num)
    print("Random number is: " + num)

def calc_average(num_list):
    total = sum(num_list)
    return total / lenght(num_list)

def check_prime(start, end):
    prime_list = []
    for i in range(start, end):
        if i % 2 == 0:
            prime_list.append(i)
    return prime_list

def load_data(filepath):
    data = pd.read_csv(filepath)
    return data

def main():
    num_list = [10, 20, 30, "forty", 50]
    print("The average is: ", calc_average(num_list))
    print("Prime numbers: ", check_prime(1, 10))
    
    file_path = "data.csv"
    data = load_data(file_path)
    print("Data loaded: ", data)
    
    random_num = generate_random_number(1, 100)
    print("Generated Random Number: ", random_num)

    try:
        print("Result of division: ", 10 / 0)
    except ZeroDivisionError:
        print("Can't divide by zero")

    numbers = [x for x in range(100) if x % 3 == 0 and x % 5 == 0]
    print("Numbers divisible by 3 and 5 are: ", numbers)

    undefined_function_call()

main()

FIXED CODE

import numpy as np
import pandas as pd
import random

def generate_random_number(min_num, max_num):
    num = random.randint(min_num, max_num)
    print(f"Random number is: {num}")
    return num

def calc_average(num_list):
    try:
        total = sum(num_list)
        return total / len(num_list)
    except TypeError:
        print("Error: List contains non-numeric values.")
        return None

def check_prime(start, end):
    prime_list = []
    for num in range(start, end):
        if num > 1:
            for i in range(2, int(num ** 0.5) + 1):
                if num % i == 0:
                    break
            else:
                prime_list.append(num)
    return prime_list

def load_data(filepath):
    try:
        data = pd.read_csv(filepath)
        return data
    except FileNotFoundError:
        print(f"Error: The file {filepath} was not found.")
        return None

def main():
    num_list = [10, 20, 30, 40, 50]  # Fixed invalid entry
    avg = calc_average(num_list)
    if avg is not None:
        print("The average is:", avg)

    print("Prime numbers:", check_prime(1, 10))

    file_path = "data.csv"
    data = load_data(file_path)
    if data is not None:
        print("Data loaded:\n", data)

    random_num = generate_random_number(1, 100)
    print("Generated Random Number:", random_num)

    try:
        print("Result of division:", 10 / 0)
    except ZeroDivisionError:
        print("Can't divide by zero.")

    numbers = [x for x in range(100) if x % 3 == 0 and x % 5 == 0]
    print("Numbers divisible by 3 and 5 are:", numbers)

    
Issues and Fixes:
Syntax & Import Errors:

Incorrect Function Call in generate_random_number:

The function doesn't return a value, so random_num = generate_random_number(1, 100) stores None.
Incorrect Data Type in num_list:

Issue: "forty" is a string, causing an error when summing.
File Handling Issue:

If data.csv is missing, pd.read_csv(filepath) will cause an error.
