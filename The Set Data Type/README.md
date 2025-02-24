# **🐍 Python Sets** 🚀  

Python mein **Set (`set`)** ek **unordered collection** hai jo **unique elements** store karta hai.  
✅ **Duplicate values allow nahi karta**  
✅ **Mutable hai (values add/remove ki ja sakti hain)**  
✅ **Unordered hota hai (insertion order maintain nahi hota)**  
✅ **Indexing aur slicing allow nahi hoti**  

---

## **🔹 1. Set Create Karna**
### ✅ **Method 1: Curly Braces `{}` Ka Use Kar Ke**
```python
my_set = {123, 452, 5, 6}
print(my_set)
# Output: {123, 452, 5, 6}
```

### ✅ **Method 2: `set()` Constructor Ka Use Kar Ke**
```python
my_set2 = set([123, 452, 5, 6])
print(my_set2)
# Output: {123, 452, 5, 6}
```

### ✅ **Multiple Data Types Store Karna**
```python
multi_type_set = {7, 9.0, False, True, "Hello!", (1, 5, 9)}
print(multi_type_set)
# Output: {False, True, 7, 9.0, 'Hello!', (1, 5, 9)}
```

📌 **🚫 Mutable Objects (Lists, Dictionaries) Sets Mein Store Nahi Ho Sakte!**  
```python
my_set = {[123, 452, 5, 6]}  # ❌ TypeError: unhashable type: 'list'
```

---

## **🔹 2. Set Properties**
### ✅ **Unordered**
Set ke elements ka **order fix nahi hota**, har execution pe different order ho sakta hai.

```python
set2 = {'Java', 'Python', 'JavaScript', 'java'}
print(set2)
# Output: {'Java', 'java', 'Python', 'JavaScript'}  (order unpredictable)
```

### ✅ **Unchangeable (Immutable)**
Set ke elements modify nahi ho sakte, sirf **add ya remove** kar sakte hain.

```python
my_set = {1, 2, 3, 4, 5}
my_set[0] = 10  # ❌ TypeError: 'set' object does not support item assignment
```

---

## **🔹 3. Set Mein Data Add Aur Remove Karna**
### ✅ **Element Add Karna (`add()`)**
```python
my_set = {1, 2, 3}
my_set.add(4)
print(my_set)
# Output: {1, 2, 3, 4}
```

### ✅ **Multiple Elements Add Karna (`update()`)**
```python
my_set.update([5, 6, 7])
print(my_set)
# Output: {1, 2, 3, 4, 5, 6, 7}
```

### ✅ **Element Remove Karna (`remove()` & `discard()`)**
```python
my_set.remove(3)  # Agar element exist na kare to error dega
my_set.discard(100)  # Agar element exist na kare to error nahi dega
```

### ✅ **Random Element Remove Karna (`pop()`)**
```python
my_set = {1, 2, 3, 4, 5}
print("Before:", my_set)

my_set.pop()  # Koi bhi random element remove karega
print("After:", my_set)
```

### ✅ **Multiple Elements Remove Karna (`difference_update()`)**
```python
my_set = {1, 2, 3, 4, 5, 'A', 'a'}
print("Before:", my_set)

my_set.difference_update({1, 3, 'A'})  # Ye elements remove ho jayenge
print("After:", my_set)
# Output: Before: {1, 2, 3, 4, 5, 'A', 'a'}
#         After: {2, 4, 5, 'a'}
```

---

## **🔹 4. Set Operations**
### ✅ **Union (`union()` ya `|`)**
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

union_set = set1.union(set2)
print(union_set)
# Output: {1, 2, 3, 4, 5}

union_set = set1 | set2  # Shortcut
print(union_set)
```

### ✅ **Intersection (`intersection()` ya `&`)**
```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

intersection_set = set1.intersection(set2)
print(intersection_set)
# Output: {2, 3}

intersection_set = set1 & set2  # Shortcut
print(intersection_set)
```

### ✅ **Difference (`difference()` ya `-`)**
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5}

diff_set = set1.difference(set2)
print(diff_set)
# Output: {1, 2}

diff_set = set1 - set2  # Shortcut
print(diff_set)
```

### ✅ **Symmetric Difference (`symmetric_difference()` ya `^`)**
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

sym_diff = set1.symmetric_difference(set2)
print(sym_diff)
# Output: {1, 2, 5, 6}

sym_diff = set1 ^ set2  # Shortcut
print(sym_diff)
```

---

## **🔹 5. Subset, Superset, and Disjoint Sets**
### ✅ **Subset Check (`issubset()`)**
```python
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4, 5}

print(set1.issubset(set2))  # Output: True
```

### ✅ **Superset Check (`issuperset()`)**
```python
print(set2.issuperset(set1))  # Output: True
```

### ✅ **Disjoint Check (`isdisjoint()`)**
```python
set1 = {1, 2, 3}
set2 = {4, 5, 6}

print(set1.isdisjoint(set2))  # Output: True
```

---

## **🔹 6. Set Iteration (Loop)**
```python
my_set = {"apple", "banana", "cherry"}
for item in my_set:
    print(item)
```

---

## **🔹 7. Set Length (`len()`)**
```python
my_set = {1, 2, 3, 4, 5}
print(len(my_set))  # Output: 5
```

---

## **🔹 8. Set Copy (`copy()`)**
```python
original_set = {1, 2, 3}
copy_set = original_set.copy()
print(copy_set)  # Output: {1, 2, 3}
```

---

## **🔹 9. Frozen Set (`frozenset()`)**
📌 **Frozenset ek immutable set hota hai, ismein add/remove nahi kar sakte.**  
```python
frozen = frozenset({1, 2, 3})
print(frozen)
# Output: frozenset({1, 2, 3})

# frozen.add(4)  # ❌ AttributeError: 'frozenset' object has no attribute 'add'
```

---

## **🔹 10. Set Hashing & Internal Working (Advanced)**
### ✅ **Hashing Example**
```python
print(hash("Hello"))  # Output: e.g. 9090330697819382555
print(hash(123))      # Output: e.g. 123
```

🚀 **Sets internally hash values store karte hain, is wajah se order unpredictable hota hai.**  

---

## **🎯 Summary**
| **Concept**  | **Set (`set`)** |
|-------------|----------------|
| **Ordered?**  | ❌ Nahi |
| **Mutable?**  | ✅ Haan |
| **Duplicate Allowed?** | ❌ Nahi |
| **Indexing Allowed?** | ❌ Nahi |
| **Methods?** | `.add()`, `.remove()`, `.union()`, `.intersection()`, `.difference()` |

---

## **🎯 Conclusion**
✅ **Sets fast hoti hain aur duplicate values remove karne ke liye best option hain.**  
✅ **Mathematical operations jaise union, intersection, difference ke liye sets best hain.**  
✅ **Agar order maintain karna hai to `list` use karein, warna sets best choice hain!** 🚀🔥  
