### 🧩 Python Sets – Theory

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