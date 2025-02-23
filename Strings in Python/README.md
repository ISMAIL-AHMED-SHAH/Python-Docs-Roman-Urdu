# **🐍 Python Strings!** 🚀  

Python mein **strings** ek **sequence of characters** hoti hain jo quotes (`' '`, `" "`, `''' '''`) mein likhi jati hain.  
✅ **Strings immutable hoti hain (badli nahi ja sakti hain)**  
✅ **Bohot saare built-in methods hote hain jo strings ko manipulate karne ke kaam aate hain.**  

---

## **🔹 1. Creating Strings in Python**
Python mein **4 tareeqe** hain strings likhne ke:  
| **Type** | **Example** | **Use Case** |
|----------|------------|-------------|
| **Single Quotes (`' '`)** | `'Hello'` | Simple Strings |
| **Double Quotes (`" "`)** | `"Hello"` | Jab string ke andar `'` ho |
| **Triple Quotes (`''' '''`)** | `'''Hello'''` | Multi-line strings |
| **Raw Strings (`r' '` or `r" "`)** | `r'Hello\tWorld'` | Escape sequences ko ignore karne ke liye |

### **✅ Example: Creating Strings**
```python
# Single & Double Quotes
str1 = 'Hello'
str2 = "Hello, World!"

# Multi-line String
str3 = '''Hello,
Python!'''

# Raw String (Escape characters ko ignore karega)
str4 = r'Hello\tPython\nWorld!'

print(str1)
print(str2)
print(str3)
print(str4)
```
🔹 **Output:**  
```
Hello
Hello, World!
Hello,
Python!
Hello\tPython\nWorld!
```
📌 **`r' '` ka use escape characters ko ignore karne ke liye hota hai.** ✅  

---

## **🔹 2. Escape Sequences in Strings**
👉 **Escape sequences wo special characters hain jo backslash (`\`) ke saath likhe jate hain.**  

| **Escape Sequence** | **Meaning** | **Example** | **Output** |
|------------------|-----------|---------|---------|
| `\n` | New Line | `"Hello\nWorld!"` | Hello <br> World! |
| `\t` | Tab | `"Hello\tWorld!"` | Hello   World! |
| `\\` | Backslash | `"Hello\\World!"` | Hello\World! |
| `\"` | Double Quote | `"Hello \"World\"!"` | Hello "World"! |
| `\'` | Single Quote | `'Hello \'World\'!'` | Hello 'World'! |

### **✅ Example: Escape Sequences**
```python
print("Hello,\tPython!")  # Tab
print("Hello,\nPython!")  # New Line
print("Hello, \"Python\"!")  # Double Quotes
print("Hello,\\Python!")  # Backslash
```
📌 **Escape sequences se special formatting aur special characters likhna asaan ho jata hai!** ✅  

---

## **🔹 3. String Operations**
### **✅ a) Concatenation (Strings ko jodna)**
```python
str1 = "Hello, "
str2 = "World!"
result = str1 + str2
print(result)  # Output: Hello, World!
```

### **✅ b) Indexing (String ke kisi ek character ko access karna)**
```python
text = "Python"
print(text[0])  # Output: P
print(text[-1])  # Output: n (Last character)
```

### **✅ c) Slicing (String ke kisi part ko nikalna)**
```python
print(text[0:4])  # Output: Pyth (index 0 se 3 tak)
print(text[2:])   # Output: thon (index 2 se end tak)
print(text[:3])   # Output: Pyt (start se index 2 tak)
```

### **✅ d) String Length (Kitne characters hain)**
```python
print(len(" Hello, World! "))  # Output: 15
```

📌 **Indexing `0` se start hoti hai, aur negative indexing bhi use ki ja sakti hai!** ✅  

---

## **🔹 4. Common String Methods**
Python mein **bohot saare built-in methods** hote hain jo strings ko manipulate karne ke liye kaam aate hain.  

### **✅ a) Case Conversion**
```python
text = "Hello, Python!"
print(text.upper())  # HELLO, PYTHON!
print(text.lower())  # hello, python!
print(text.title())  # Hello, Python!
```

### **✅ b) `split()` (String ko list mein todna)**
```python
sentence = "Hello, World!"
words = sentence.split()  # Default space se split karega
print(words)  # Output: ['Hello,', 'World!']

words = sentence.split("o")  # 'o' ke basis par split karega
print(words)  # Output: ['Hell', ', W', 'rld!']
```

### **✅ c) `join()` (List ko string mein convert karna)**
```python
words = ['Pakistan', 'USA', 'Canada']
result = ', '.join(words)
print(result)  # Output: Pakistan, USA, Canada
```

### **✅ d) `replace()` (String ke ek part ko doosre se replace karna)**
```python
text = "Hello, World! Hello, Python!"
new_text = text.replace("Hello", "Salam Walikum")
print(new_text)  # Salam Walikum, World! Salam Walikum, Python!
```

### **✅ e) `find()` aur `index()` (Substring ka index dhoondhna)**
```python
text = "Hello, World! Hello, Python!"
print(text.find("World"))  # Output: 7
print(text.index("Hello"))  # Output: 0
```

📌 **`find()` agar substring nahi mile to `-1` return karega, jabke `index()` error dega.** ✅  

---

## **🔹 5. String Formatting (Python 3+)**
Python mein **3 tareeqe** hain string formatting ke:  

| **Method** | **Example** |
|------------|------------|
| `% Operator` | `"My name is %s and I am %d years old" % ("John", 20)` |
| `.format()` | `"My name is {} and I am {} years old".format("John", 20)` |
| `f-String` | `f"My name is {name} and I am {age} years old"` |

### **✅ a) `% Operator` (Old Method)**
```python
name, age = "Safaid Khan", 20
print("My name is %s and I am %d years old" % (name, age))
```

### **✅ b) `.format()` (Modern Method)**
```python
print("My name is {} and I am {} years old".format(name, age))
print("My name is {1} and I am {0} years old".format(age, name))  # Indexing bhi possible hai
```

### **✅ c) `f-String` (Recommended)**
```python
print(f"My name is {name} and I am {age} years old")
```
📌 **f-Strings fastest aur recommended method hai!** ✅  

---

## **🚀 Summary Table**
| **Concept** | **Example** | **Description** |
|--------------|------------|----------------|
| **Creating Strings** | `'Hello'`, `"World"` | Strings ko define karna |
| **Escape Sequences** | `\n`, `\t`, `\\` | Special characters add karna |
| **String Operations** | `+`, `*`, `text[0]`, `text[1:5]` | Concatenation, Indexing, Slicing |
| **String Methods** | `upper()`, `lower()`, `split()`, `join()` | Strings ko modify karna |
| **Search & Replace** | `find()`, `replace()`, `count()` | Substrings dhoondhna ya replace karna |
| **Formatting** | `%`, `.format()`, `f"{}"` | Strings format karna |

---

## **🎯 Conclusion**
Python mein **strings bohot powerful hoti hain**, aur unko manipulate karne ke **bohot saare methods** hote hain.  
✅ **Escape sequences aur raw strings ka use kar ke special formatting ki ja sakti hai.**  
✅ **Slicing, concatenation, indexing, aur length ka use string manipulation ke liye hota hai.**  
✅ **f-Strings best aur recommended method hai formatting ke liye.**  
