# **🐍 Python Dictionaries** 🚀  

Python mein **Dictionaries (`dict`)** ek **powerful aur flexible data structure** hai jo **key-value pairs** ko store karne ke liye use hoti hai.  
✅ **Ordered** (Python 3.7+ mein insertion order maintain hota hai).  
✅ **Mutable** (Values ko modify, delete aur add kiya ja sakta hai).  
✅ **Unique Keys** (Ek key ek hi dafa exist karegi, duplicate keys nahi hoti).  
✅ **Unindexed** (Keys ka use kar ke values ko access kiya jata hai, index nahi hota).  

---

## **🔹 1. Dictionary Create Karna**
### ✅ **Method 1: Curly Braces `{}` Ka Use Kar Ke**
```python
person = {
    "name": "Ali",
    "age": 25,
    "city": "New York"
}
print(person)
# Output: {'name': 'Ali', 'age': 25, 'city': 'New York'}
```

### ✅ **Method 2: `dict()` Constructor Ka Use Kar Ke**
```python
thisdict = dict(name="Safaid Khan", age=36, country="Norway")
print(thisdict)
# Output: {'name': 'Safaid Khan', 'age': 36, 'country': 'Norway'}
```

---

## **🔹 2. Dictionary Mein Data Access Karna**
### ✅ **Method 1: Square Brackets `[]` Ka Use**
```python
print(person["name"])  # Output: Ali
```

📌 **Agar key exist na kare to error aayegi:**
```python
print(person["gender"])  # ❌ KeyError: 'gender'
```

### ✅ **Method 2: `get()` Function Ka Use**
```python
print(person.get("age", "Not Found"))  # Output: 25
print(person.get("gender", "Not Found"))  # Output: Not Found
```

---

## **🔹 3. Dictionary Ko Modify Karna**
### ✅ **New Key-Value Pair Add Karna**
```python
person["email"] = "ali@example.com"
print(person)
# Output: {'name': 'Ali', 'age': 25, 'city': 'New York', 'email': 'ali@example.com'}
```

### ✅ **Existing Value Update Karna**
```python
person["age"] = 26
print(person)
# Output: {'name': 'Ali', 'age': 26, 'city': 'New York', 'email': 'ali@example.com'}
```

---

## **🔹 4. Dictionary Se Data Delete Karna**
### ✅ **Method 1: `del` Keyword Ka Use**
```python
del person["city"]
print(person)
# Output: {'name': 'Ali', 'age': 26, 'email': 'ali@example.com'}
```

### ✅ **Method 2: `pop()` Function Ka Use**
```python
removed_age = person.pop("age", 0)
print("Removed age:", removed_age)
print(person)
# Output: Removed age: 26
#         {'name': 'Ali', 'email': 'ali@example.com'}
```

📌 **Agar key exist na kare to default value return hogi:**
```python
print(person.pop("age", "Not Found"))  # Output: Not Found
```

### ✅ **Method 3: `clear()` Function Ka Use (Poora Dictionary Empty Karna)**
```python
person.clear()
print(person)  # Output: {}
```

---

## **🔹 5. Dictionary Methods**
| **Method**  | **Description**  |
|-------------|----------------|
| `.keys()`   | Sabhi keys return karta hai. |
| `.values()` | Sabhi values return karta hai. |
| `.items()`  | (key, value) pairs return karta hai. |
| `.update()` | Do dictionary ko merge karta hai. |
| `.pop()`    | Ek key-value pair ko remove kar ke uski value return karta hai. |
| `.clear()`  | Poora dictionary empty kar deta hai. |

```python
person = {"name": "Ali", "age": 25, "email": "ali@example.com"}

print(person.keys())   # Output: dict_keys(['name', 'age', 'email'])
print(person.values()) # Output: dict_values(['Ali', 25, 'ali@example.com'])
print(person.items())  # Output: dict_items([('name', 'Ali'), ('age', 25), ('email', 'ali@example.com')])

# Update Dictionary
person.update({"city": "Los Angeles", "age": 27})
print(person)  
# Output: {'name': 'Ali', 'age': 27, 'email': 'ali@example.com', 'city': 'Los Angeles'}
```

---

## **🔹 6. Iterating Over a Dictionary**
### ✅ **Loop Through Keys**
```python
for key in person:
    print(key)
# Output:
# name
# age
# email
# city
```

### ✅ **Loop Through Keys & Values (Tuple Format)**
```python
for key, value in person.items():
    print(key, ":", value)
# Output:
# name : Ali
# age : 27
# email : ali@example.com
# city : Los Angeles
```

---

## **🔹 7. Dictionary Mein Key Check Karna (`in` Operator)**
```python
if "name" in person:
    print("Key exists!")
else:
    print("Key does not exist.")
# Output: Key exists!
```

---

## **🔹 8. Dictionary Se Data Sorting**
### ✅ **Keys Ke Basis Par Sorting**
```python
sorted_dict = dict(sorted(person.items()))
print(sorted_dict)
```

### ✅ **Values Ke Basis Par Sorting**
```python
sorted_by_values = dict(sorted(person.items(), key=lambda item: item[1]))
print(sorted_by_values)
```

---

## **🔹 9. Dictionary Use Kar Ke Phonebook Banayein**
```python
phonebook: dict = {
    "Alpha": "123-456-7890",
    "Bravo": "987-654-3210",
    "Charlie": "555-555-5555"
}

name: str = input("Enter a name to search: ")
if name in phonebook:
    print(f"{name}'s phone number is {phonebook[name]}.")
else:
    print(f"{name} is not in the phonebook.")
```

📌 **Example Output**
```
Enter a name to search: Bravo
Bob's phone number is 987-654-3210.
```

---

## **🔹 10. Word Frequency Counter**
```python
sentence = "AI is the future. AI is changing the world."

word_count = {}
words: list = sentence.split()

for word in words:
    word = word.lower().strip(".,")  # Convert to lowercase & remove punctuation
    word_count[word] = word_count.get(word, 0) + 1

print(word_count)
# Output: {'ai': 2, 'is': 2, 'the': 1, 'future': 1, 'changing': 1, 'world': 1}
```

---

## **🔹 11. Nested Dictionary (Dictionary Ke Andar Dictionary)**
```python
students = {
    "student1": {"name": "Ali", "age": 25},
    "student2": {"name": "Bilal", "age": 30}
}

print(students["student1"]["name"])  # Output: Ali
```

---

## **🚀 Summary Table**
| **Concept**  | **Dictionary (`dict`)** |
|-------------|----------------|
| **Ordered?**  | ✅ (Python 3.7+ mein) |
| **Mutable?**  | ✅ Haan |
| **Unique Keys?** | ✅ Haan |
| **Duplicates Allowed?** | ✅ Values duplicate ho sakti hain, par keys nahi |
| **Indexed?** | ❌ Nahi, indexing ka use nahi hota |
| **Methods?** | `.keys()`, `.values()`, `.items()`, `.update()`, `.pop()` |

---

## **🎯 Conclusion**
✅ **Dictionaries ek flexible aur efficient data structure hai jo key-value pairs store karne ke liye use hota hai.**  
✅ **Keys unique hoti hain, values duplicate ho sakti hain.**  
✅ **Dictionaries ko loop ke zariye iterate kar sakte hain aur keys ya values extract kar sakte hain.**  
✅ **Dictionaries real-world applications jaise phonebooks, word frequency counters, aur nested data store karne ke liye use hote hain.**  

