[laba2.py](https://github.com/user-attachments/files/32804198/laba2.py)
# Задача 1
```
def convert_types(data):
    result = []
    for item in data:
        # bool является подклассом int в Python, поэтому проверяем его первым
        if isinstance(item, bool):
            result.append(str(item))
        elif isinstance(item, (int, float)):
            result.append(str(item))
        elif isinstance(item, str):
            try:
                result.append(int(item))
            except ValueError:
                try:
                    result.append(float(item))
                except ValueError:
                    result.append(item)
        else:
            result.append(str(item))
    return result

```
```
# Задача 2
def swap_values(a, b):
    a, b = b, a
    return (a, b)

```
```
# Задача 3
def bool_transform(value):
    if value:
        return True
    else:
        return False

```
```
# Задача 4
def compound_operations(a, b):
    return [
        a + b,
        a - b,
        a * b,
        a / b,
        a // b,
        a % b,
        a ** b
    ]

```
```
# Задача 5
def check_type(value, expected_type):
    return type(value).__name__ == expected_type

```
```
# Задача 6
def logical_and(a, b, c):
    if a:
        if b:
            if c:
                return True
    return False

```
```
# Задача 7
def logical_or(a, b, c):
    if a:
        return True
    if b:
        return True
    if c:
        return True
    return False

```
```
# Задача 8
def is_between(value, low, high):
    if low <= value <= high:
        return True
    return False

```
```
# Задача 9
def print_even_numbers(n):
    for i in range(2, n + 1, 2):
        print(i)

```
```
# Задача 10
def countdown_while(n):
    while n >= 1:
        print(n)
        n -= 1

```
```
# Задача 11
def skip_multiples(n, multiple):
    for i in range(1, n + 1):
        if i % multiple == 0:
            continue
        print(i)

```
```
# Задача 12
def if_elif_else_chain(x):
    if x > 0:
        return "positive"
    elif x < 0:
        return "negative"
    else:
        return "zero"

```
```
# Задача 13
def abs_value(x):
    if x < 0:
        return -x
    return x

```
```
# Задача 14
def binary_representation(n):
    if n == 0:
        return "0"
    result = ""
    num = n
    while num > 0:
        result = str(num % 2) + result
        num //= 2
    return result

```
```
# Задача 15
def custom_round(number, ndigits):
    multiplier = 10 ** ndigits
    if number >= 0:
        return int(number * multiplier + 0.5) / multiplier
    else:
        return int(number * multiplier - 0.5) / multiplier

```
```
# Задача 16
def find_max_min(numbers):
    if not numbers:
        return None
    max_val = numbers[0]
    min_val = numbers[0]
    for num in numbers:
        if num > max_val:
            max_val = num
        if num < min_val:
            min_val = num
    return (max_val, min_val)

```
```
# Задача 17
def all_true(iterable):
    for item in iterable:
        if not item:
            return False
    return True

```
```
# Задача 18
def any_true(iterable):
    for item in iterable:
        if item:
            return True
    return False
```
```
# Задача 19
def custom_enumerate(sequence, start=0):
    result = []
    index = start
    for item in sequence:
        result.append((index, item))
        index += 1
    return result

```
```
# Задача 20
def custom_filter(func, iterable):
    result = []
    for item in iterable:
        if func(item):
            result.append(item)
    return result

```
```
# Задача 21
def custom_map(func, iterable):
    result = []
    for item in iterable:
        result.append(func(item))
    return result

```
```
# Задача 22
def custom_zip(list1, list2):
    result = []
    length = len(list1) if len(list1) < len(list2) else len(list2)
    for i in range(length):
        result.append((list1[i], list2[i]))
    return result

```
```
# Задача 23
def custom_reversed(sequence):
    result = []
    for i in range(len(sequence) - 1, -1, -1):
        result.append(sequence[i])
    return result

```
```
# Задача 24
def custom_sorted(iterable, reverse=False):
    result = list(iterable)
    n = len(result)
    for i in range(n):
        for j in range(0, n - i - 1):
            if (not reverse and result[j] > result[j + 1]) or (reverse and result[j] < result[j + 1]):
                result[j], result[j + 1] = result[j + 1], result[j]
    return result

```
```
# Задача 25
def sum_digits(n):
    n = abs(n)
    total = 0
    while n > 0:
        total += n % 10
        n //= 10
    return total

```
```
# Задача 26
def count_vowels(text):
    vowels = 'aeiouAEIOU'
    count = 0
    for char in text:
        if char in vowels:
            count += 1
    return count

```
```
# Задача 27
def power(base, exp):
    if exp == 0:
        return 1
    result = 1
    for _ in range(exp):
        result *= base
    return result

```
```
# Задача 28
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

```
```
# Задача 29
def factorial(n):
    if n == 0 or n == 1:
        return 1
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result

```
```
# Задача 30
def fibonacci(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b
```
