# **🐍 Python Naming Conventions & Variable Management!** 🚀  

Python mein **naming conventions** kaafi important hote hain, taake code **readable, maintainable aur error-free** rahe.  
Aaj hum **Camel Case, Pascal Case, Snake Case, Constants, Private Variables** aur **Variable Management** ko **simple examples** ke saath samjhenge! 😊  

---

## **🔹 1. Naming Conventions in Python**
Python ke **PEP 8 (Python Enhancement Proposal 8)** style guide mein recommended naming conventions diye gaye hain.  
👉 **Ye conventions code ko readable aur maintainable banate hain!**  

### **📌 Common Naming Styles**
| **Convention** | **Used For** | **Example** |
|--------------|------------|------------|
| **snake_case** | Variables, functions | `user_name`, `total_price` |
| **PascalCase** (CapWords) | Classes | `BankAccount`, `DataScienceModel` |
| **UPPER_CASE** | Constants | `MAX_SPEED`, `PI` |
| **_single_underscore** | Private variable (by convention) | `_config` |
| **__double_underscore** | Name mangling (avoid external access) | `__password` |
| **__dunder__** | Special methods | `__init__`, `__str__` |

📌 **Python mein naming conventions follow karne se code professional aur readable banta hai!** ✅  

---

## **🔹 2. Special Naming Cases**
Python mein kuch **special naming cases** bhi hote hain jo code organization aur security ke liye use hote hain.  

### **✅ Example: Special Naming Cases**
```python
# Regular variable
total_cost = 1000  # snake_case

# Constant
PI = 3.14159  # UPPER_CASE (by convention)

# Class Name
class BankAccount:  # PascalCase
    pass

# Private Variable (by convention)
_password = "mypassword"  # _single_underscore

# Name Mangling (avoid accidental override)
class Secure:
    __secret_key = "12345"  # __double_underscore

# Special method (dunder method)
class MyClass:
    def __init__(self, name):
        self.name = name
```
📌 **`_single_underscore` ka use private variables ke liye hota hai, lekin Python isse enforce nahi karta.** ✅  

---

## **🔹 3. Assigning Multiple Values to Variables**
Python mein ek hi line mein multiple variables ko assign kiya ja sakta hai.  

### **✅ Example: Assigning Multiple Values**
```python
x, y, z = 1, 2.5, "Python"
print(x, y, z)  # Output: 1 2.5 Python
```
📌 **Ek hi line mein alag alag types ki values assign ki ja sakti hain.** ✅  

### **❌ Incorrect: Type Hints with Multiple Assignments**
```python
# x: int, y: float, z: str = 1, 2.5, "Python"  # ❌ Syntax Error
```
📌 **Type hints alag se likhne chahiye, ek hi line mein nahi.** ✅  

---

## **🔹 4. `del` Keyword – Variable Delete Karna**
👉 **Python mein `del` keyword ka use kisi variable ko delete karne ke liye hota hai.**  
👉 **Ye variable ko memory se hata deta hai, aur uske baad uska access possible nahi hota.**  

### **✅ Example: Deleting a Variable**
```python
# Variable assign karna
x = 10
print("Before deletion:", x)  # Output: 10

# Variable delete karna
del x

# Variable ko access karne ki koshish (Error!)
# print(x)  # ❌ NameError: name 'x' is not defined
```
📌 **`del x` variable ko memory se hata deta hai, aur uske baad use access nahi kiya ja sakta.** ✅  

---

## **🚀 Summary Table**
| **Concept** | **Description** | **Example** |
|------------|---------------|------------|
| **snake_case** | Variables & functions | `user_name`, `total_price` |
| **PascalCase** | Class names | `BankAccount`, `DataScienceModel` |
| **UPPER_CASE** | Constants | `MAX_SPEED`, `PI` |
| **_single_underscore** | Private variable (by convention) | `_config` |
| **__double_underscore** | Name mangling (avoid external access) | `__password` |
| **__dunder__** | Special methods | `__init__`, `__str__` |
| **Multiple Assignments** | Ek hi line mein multiple values assign karna | `x, y, z = 1, 2.5, "Python"` |
| **Deleting Variable** | `del` se variable delete karna | `del x` |

---

## **🎯 Conclusion**
Python mein **naming conventions aur variable management** **best coding practices** ke liye zaroori hain.  
✅ **Naming conventions (snake_case, PascalCase, UPPER_CASE) follow karna readability badhata hai.**  
✅ **Ek hi line mein multiple variables assign kar sakte hain.**  
✅ **`del` keyword se variables ko memory se delete kiya ja sakta hai.**  

