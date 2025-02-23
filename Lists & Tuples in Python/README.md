# **🐍 Lists & Tuples in Python** 🚀  

Python mein **lists aur tuples** ka use **data store karne aur manage karne** ke liye hota hai.  
✅ **Lists** – **Ordered, mutable (changeable), aur dynamic** hoti hain.  
✅ **Tuples** – **Ordered, immutable (unchangeable), aur memory-efficient** hoti hain.  

---

## **🔹 1. Lists in Python**
### ✅ **Lists Ki Khaas Baatain**
- **Ordered** – Har element ka ek fixed order hota hai.
- **Mutable** – Elements ko **add, remove, ya modify** kar sakte hain.
- **Indexed** – Har element ek index se access kiya jata hai.
- **Heterogeneous** – List mein **different types** ke elements ho sakte hain.
- **Duplicates Allowed** – Same value multiple times store ki ja sakti hai.

---

## **🔹 2. List Banana & Access Karna**
### ✅ **List Create Karna**
```python
fruits: list  = ["apple", "banana", "cherry"]
numbers: list = [10, 20, 30, 40]
mixed: list   = ["hello", 42, 3.14, True]

print("fruits  = ", fruits)
print("numbers = ", numbers)
print("mixed   = ", mixed)
```

### ✅ **List Elements Ko Access Karna (`Indexing`)**
```python
fruits: list = ["apple", "banana", "cherry"]
fruits[-3] = "watermelon" # replacing "apple" with "watermelon"
print(fruits)  # Output: ['watermelon', 'banana', 'cherry']
```

---

## **🔹 3. List Ko Modify Karna**
### ✅ **List Ka Element Change Karna**
```python
fruits[0] = "watermelon"
print(fruits)  # ['watermelon', 'banana', 'cherry']
```

### ✅ **List Slicing (Multiple Elements Ko Extract Karna)**
```python
print(fruits[0:2])  # Output: ['watermelon', 'banana']
```

---

## **🔹 4. List Methods (Important Operations)**
### ✅ **List Mein Element Add Karna**
```python
fruits.append("mango")  # Akhri position par add karega
print(fruits)  # ['watermelon', 'banana', 'cherry', 'mango']

fruits.extend(["grape", "kiwi"])  # Multiple elements add karega
print(fruits)  # ['watermelon', 'banana', 'cherry', 'mango', 'grape', 'kiwi']
```

### ✅ **List Se Element Remove Karna**
```python
fruits.remove("banana")  # Pehli occurrence remove karega
print(fruits)  # ['watermelon', 'cherry', 'mango', 'grape', 'kiwi']

deleted = fruits.pop(1)  # Index 1 wala element remove karega
print("Deleted element:", deleted)  # Output: 'cherry'
print(fruits)  # ['watermelon', 'mango', 'grape', 'kiwi']
```

### ✅ **List Ko Sort Aur Reverse Karna**
```python
numbers: list[int] = [3, 1, 4, 1, 5, 9]
numbers.sort()  # Ascending order
print(numbers)  # [1, 1, 3, 4, 5, 9]

numbers.reverse()  # Descending order
print(numbers)  # [9, 5, 4, 3, 1, 1]
```

---

## **🔹 5. Lists Par Iteration (Loop Chalana)**
### ✅ **For Loop Se List Print Karna**
```python
for fruit in fruits:
    print(fruit)
```

### ✅ **List Comprehension (Short Form of Loops)**
```python
squared = [x**2 for x in [1, 2, 3, 4, 5] if x > 3]
print(squared)  # Output: [16, 25]
```

---

## **🔹 6. Tuples in Python**
### ✅ **Tuple Ki Khaas Baatain**
- **Ordered** – Sequence maintain hoti hai.
- **Immutable** – Modify nahi kiya ja sakta.
- **Fast & Memory-Efficient** – Lists se zyada optimized hoti hain.
- **Duplicate Allowed** – Repeated values store ho sakti hain.

### ✅ **Tuple Create Karna**
```python
tuple1: tuple = tuple(["apple", "banana", "cherry"]) # cast a list into tuple
tuple2: tuple = (10, 20, 30) # tuple
mixed_tuple: tuple = ("hello", 42, 3.14, True) # tuple

print("tuple1      =", tuple1)
print("tuple2      =", tuple2)
print("mixed_tuple =", mixed_tuple)
```

### ✅ **Tuple Ke Elements Ko Access Karna**
```python
print(tuple1[0])  # Output: apple
print(tuple1[-1])  # Output: cherry
```

---

## **🔹 7. Tuples Ki Properties**
### ✅ **Tuple Ki Memory Allocation (Different Instances Ban Sakte Hain)**
```python
tuple_1: tuple = (10, 20, 30) # tuple
tuple_2: tuple = (10, 20, 30) # tuple

print(id(tuple_1))  # Unique memory address
print(id(tuple_2))  # Different memory address
print(tuple_1 == tuple_2)  # True (value same hai)
```

### ✅ **Tuple Immutable Kyun Hota Hai?**
- **Memory Efficient** – Single memory block allocate hota hai.
- **Thread Safe** – Multi-threading mein safe hota hai.
- **Hashable** – Dictionaries mein keys ke tor par use ho sakta hai.

📌 **Tuples Ko Modify Karne Ki Koshish Error De Gi!**
```python
tuple1[0] = "watermelon"  # ❌ TypeError: 'tuple' object does not support item assignment
```

---

## **🔹 8. Important Tuple Operations**
### ✅ **Tuple Length**
```python
print(len(tuple1))  # Output: 3
```

### ✅ **Tuple Concatenation**
```python
tuple3: tuple = tuple1 + tuple2
print(tuple3)  # ('apple', 'banana', 'cherry', 10, 20, 30)
```

### ✅ **Tuple Repetition**
```python
tuple4: tuple = tuple2 * 2
print(tuple4)  # (10, 20, 30, 10, 20, 30)
```

### ✅ **Tuple Unpacking**
```python
a, b, c = tuple1
print(a, b, c)  # Output: apple banana cherry
```

### ✅ **Tuple Methods (`count()` & `index()`)**
```python
print(tuple1.count("apple"))  # Output: 1
print(tuple1.index("apple"))  # Output: 0
```

📌 **Tuple Par `sort()`, `append()`, `remove()` Jaise Methods Work Nahi Karte!**

---

```python
# prompt: generate a example of ['count', 'index'] in tuple

tuple1: tuple = tuple(["apple", "banana", "cherry"])
print(tuple1.count("apple"))  # Output: 1
print(tuple1.index("apple"))  # Output: 0
example_tuple: tuple = ('count', 'index')
print(example_tuple) # Output: ('count', 'index')
```


## **🚀 Summary Table**
| **Concept** | **Lists** | **Tuples** |
|------------|------------|------------|
| **Mutable?** | ✅ Haan (Change ho sakti hai) | ❌ Nahi (Change nahi hoti) |
| **Ordered?** | ✅ Haan | ✅ Haan |
| **Duplicate Allowed?** | ✅ Haan | ✅ Haan |
| **Faster?** | ❌ Nahi | ✅ Haan |
| **Memory Efficient?** | ❌ Nahi | ✅ Haan |
| **Methods** | `append()`, `remove()`, `sort()`, `pop()` | `count()`, `index()` |

---

## **🎯 Conclusion**
✅ **Lists aur Tuples Python ke sabse important data structures hain.**  
✅ **Lists mutable hoti hain, jab ke Tuples immutable hote hain.**  
✅ **List me elements ko add, remove aur modify kiya ja sakta hai, jab ke Tuples fix hote hain.**  
✅ **Lists zyada flexible hoti hain, jab ke Tuples performance aur memory optimization ke liye best hain.**  

