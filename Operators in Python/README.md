# **🐍 Python Operators!** 🚀  

Python mein **operators** ka use **variables aur values par operations** perform karne ke liye hota hai.  
Aaj hum **Arithmetic, Comparison, Logical, Assignment, Identity, Membership** aur **Bitwise Operators** ko **simple examples** ke saath samjhenge! 😊  

---

## **🔹 1. Arithmetic Operators (Math Operations)**
👉 **Math calculations ke liye use hotay hain.**  

| **Operator** | **Name** | **Example** | **Output** |
|------------|---------|---------|--------|
| `+` | Addition | `5 + 2` | `7` |
| `-` | Subtraction | `5 - 2` | `3` |
| `*` | Multiplication | `5 * 2` | `10` |
| `/` | Division (float) | `5 / 2` | `2.5` |
| `//` | Floor Division | `5 // 2` | `2` |
| `%` | Modulus (remainder) | `5 % 2` | `1` |
| `**` | Exponentiation | `5 ** 2` | `25` |

### **✅ Example: Arithmetic Operators**
```python
a, b = 10, 3
print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulus:", a % b)
print("Exponentiation:", a ** b)
```
🔹 **Output:**  
```
Addition: 13
Subtraction: 7
Multiplication: 30
Division: 3.3333333333333335
Floor Division: 3
Modulus: 1
Exponentiation: 1000
```
📌 **`//` ka result hamesha integer hota hai!**  

---

## **🔹 2. Comparison (Relational) Operators**
👉 **Do values ko compare karne ke liye use hotay hain.**  

| **Operator** | **Name** | **Example** | **Output** |
|------------|---------|---------|--------|
| `==` | Equal to | `5 == 5` | `True` |
| `!=` | Not equal to | `5 != 3` | `True` |
| `>` | Greater than | `5 > 3` | `True` |
| `<` | Less than | `5 < 3` | `False` |
| `>=` | Greater than or equal to | `5 >= 5` | `True` |
| `<=` | Less than or equal to | `5 <= 3` | `False` |

### **✅ Example: Comparison Operators**
```python
x, y = 10, 5
print("x == y:", x == y)
print("x != y:", x != y)
print("x > y:", x > y)
print("x < y:", x < y)
print("x >= y:", x >= y)
print("x <= y:", x <= y)
```
📌 **Comparison operators ka result `True` ya `False` hota hai!** ✅  

---

## **🔹 3. Logical Operators**
👉 **Multiple conditions ko combine karne ke liye use hotay hain.**  

| **Operator** | **Name** | **Example** | **Output** |
|------------|---------|---------|--------|
| `and` | Logical AND | `(5 > 3 and 10 > 5)` | `True` |
| `or` | Logical OR | `(5 > 3 or 10 < 5)` | `True` |
| `not` | Logical NOT | `not(5 > 3)` | `False` |

### **✅ Example: Logical Operators**
```python
x, y = True, False
print("x and y:", x and y)
print("x or y:", x or y)
print("not x:", not x)
```
📌 **`and` tabhi `True` hoga jab dono conditions `True` hongi.** ✅  

---

## **🔹 4. Assignment Operators**
👉 **Variables ko values assign karne ke liye use hotay hain.**  

| **Operator** | **Example** | **Equivalent To** |
|------------|---------|---------|
| `=` | `x = 5` | `x = 5` |
| `+=` | `x += 3` | `x = x + 3` |
| `-=` | `x -= 3` | `x = x - 3` |
| `*=` | `x *= 3` | `x = x * 3` |
| `/=` | `x /= 3` | `x = x / 3` |
| `//=` | `x //= 3` | `x = x // 3` |

### **✅ Example: Assignment Operators**
```python
x = 5
x += 3
print("Addition Assignment:", x)
x -= 3
print("Subtraction Assignment:", x)
x *= 3
print("Multiplication Assignment:", x)
```
📌 **Short-hand notation se code readable hota hai!** ✅  

---

## **🔹 5. Identity Operators**
👉 **Do objects ki memory location compare karne ke liye use hotay hain.**  

| **Operator** | **Name** | **Example** |
|------------|---------|---------|
| `is` | Same memory location | `x is y` |
| `is not` | Different memory location | `x is not y` |

### **✅ Example: Identity Operators**
```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print("a is c:", a is c)  # True (Same object)
print("a is b:", a is b)  # False (Different objects)
print("a == b:", a == b)  # True (Same values)
```
📌 **`is` memory location compare karta hai, `==` values compare karta hai.** ✅  

---

## **🔹 6. Membership Operators**
👉 **Check karte hain ke koi value sequence (list, string, tuple, dictionary) mein hai ya nahi.**  

| **Operator** | **Name** | **Example** |
|------------|---------|---------|
| `in` | Value present hai | `x in list` |
| `not in` | Value present nahi hai | `x not in list` |

### **✅ Example: Membership Operators**
```python
my_list = [1, 2, 3, 4, 5]
print("3 in my_list:", 3 in my_list)  # True
print("10 not in my_list:", 10 not in my_list)  # True
```
📌 **`in` aur `not in` membership check karte hain.** ✅  

---

## **🚀 Summary Table**
| **Operator Type** | **Example** | **Description** |
|--------------|----------------|----------------|
| **Arithmetic** | `x + y`, `x - y`, `x * y`, `x / y` | Math operations |
| **Comparison** | `x > y`, `x == y`, `x != y` | Values compare karna |
| **Logical** | `x and y`, `x or y`, `not x` | Conditions ko combine karna |
| **Assignment** | `x += 3`, `x *= 2` | Values ko variables mein store karna |
| **Identity** | `x is y`, `x is not y` | Memory location compare karna |
| **Membership** | `x in list`, `x not in list` | List ya string mein value check karna |

---

## **🎯 Conclusion**
Python mein **operators programming ka essential part hain!**  
✅ **Arithmetic operations calculations ke liye use hote hain.**  
✅ **Comparison aur Logical operators conditions ke liye kaam aate hain.**  
✅ **Membership aur Identity operators object checking ke liye useful hain.**  



