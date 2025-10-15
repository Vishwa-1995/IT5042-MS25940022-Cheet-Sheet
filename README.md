### 🧩 Python Sets

A **set** in Python is an **unordered, mutable collection** of **unique elements**.  
Sets are useful for membership testing, mathematical operations, and eliminating duplicates.

#### 🔹 Key Characteristics
- **Unordered:** The items have no defined order.
- **Mutable:** You can add or remove elements after creation.
- **No Duplicates:** Automatically removes repeated items.
- **Unindexed:** Elements cannot be accessed by index.

#### 🔹 Creating Sets
```python
# Creating sets
my_set = {1, 2, 3}
empty_set = set()  # not {}
```

#### 🔹 Common Set Methods
| Method                   | Description                                    | Example                  |
| ------------------------ | ---------------------------------------------- | ------------------------ |
| `add(x)`                 | Adds an element to the set                     | `s.add(4)`               |
| `remove(x)`              | Removes an element (raises error if not found) | `s.remove(3)`            |
| `discard(x)`             | Removes an element (no error if missing)       | `s.discard(5)`           |
| `pop()`                  | Removes a random element                       | `s.pop()`                |
| `clear()`                | Removes all elements                           | `s.clear()`              |
| `union()`                | Combines sets (no duplicates)                  | `a.union(b)` or `a \| b` |
| `intersection()`         | Elements common to both sets                   | `a & b`                  |
| `difference()`           | Elements in `a` but not in `b`                 | `a - b`                  |
| `symmetric_difference()` | Elements not shared by both                    | `a ^ b`                  |

#### 🔹 Set Operations Example
```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a | b)  # Union → {1, 2, 3, 4, 5, 6}
print(a & b)  # Intersection → {3, 4}
print(a - b)  # Difference → {1, 2}
print(a ^ b)  # Symmetric Difference → {1, 2, 5, 6}
```

#### 🔹 Set Comprehensions
```python
squares = {x**2 for x in range(6)}
print(squares)  # {0, 1, 4, 9, 16, 25}
```

#### 🔹 Frozen Sets
A frozenset is an immutable version of a set — once created, it cannot be changed.
```python
fs = frozenset([1, 2, 3])
print(fs)
```


### 🧩 Python Strings

#### 🔹Creation and Access
```python
# String indexing
s = "Artificial"
print(s[0])        # 'A' - first character
print(s[-1])       # 'l' - last character
print(s[0:3])      # 'Art' - slicing
print(s[::-1])     # 'lacifitrA' - reversed string
```

#### 🔹Case Conversion
```python
text = "hello World"

print(text.upper())        # "HELLO WORLD"
print(text.lower())        # "hello world"
print(text.capitalize())   # "Hello world"
print(text.title())        # "Hello World"
print(text.swapcase())     # "HELLO wORLD"

# Example usage
name = "john doe"
formatted_name = name.title()  # "John Doe"
```

#### 🔹Search and Replace
```python
text = "Hello World, Welcome to Python World"

# Finding substrings
print(text.find("World"))        # 6 - first occurrence
print(text.rfind("World"))       # 28 - last occurrence
print(text.find("Java"))         # -1 - not found
print(text.index("World"))       # 6 - similar to find but raises ValueError if not found

# Checking content
print(text.startswith("Hello"))  # True
print(text.endswith("World"))    # True
print("World" in text)          # True

# Replacement
print(text.replace("World", "Earth"))  # "Hello Earth, Welcome to Python Earth"
print(text.replace("World", "Earth", 1))  # "Hello Earth, Welcome to Python World" - replace only first occurrence
```

#### 🔹Splitting and Joining
```python
# Splitting strings
text = "apple,banana,cherry,date"
fruits = text.split(",")
print(fruits)  # ['apple', 'banana', 'cherry', 'date']

csv_data = "John,25,Engineer"
name, age, profession = csv_data.split(",")
print(f"Name: {name}, Age: {age}, Profession: {profession}")
```

#### 🔹String Formatting
```python
# Old style formatting
name = "John"
age = 25
print("Hello, %s! You are %d years old." % (name, age))

# str.format() method
print("Hello, {}! You are {} years old.".format(name, age))
print("Hello, {0}! You are {1} years old.".format(name, age))
print("Hello, {name}! You are {age} years old.".format(name=name, age=age))

# f-strings (Python 3.6+)
print(f"Hello, {name}! You are {age} years old.")
print(f"Next year you'll be {age + 1} years old.")

# Formatting numbers
price = 49.9876
print(f"Price: ${price:.2f}")  # Price: $49.99
```