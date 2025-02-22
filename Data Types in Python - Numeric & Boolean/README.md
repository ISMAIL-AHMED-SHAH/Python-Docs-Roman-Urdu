### **🐍 Python Data Types – Numeric & Boolean!**  

Python mein **bohot saare data types** hote hain, lekin **Numeric** aur **Boolean** types ka bohot zyada use hota hai. Aayiye ise **simple aur easy examples** ke saath samajhte hain! 🚀  

---

## **🔹 1. Numeric Types (Numbers in Python)**
Python mein **3 types ke numbers** hote hain:  
1️⃣ **Integer (`int`)** – Whole numbers (poore numbers)  
2️⃣ **Floating-Point (`float`)** – Decimal numbers  
3️⃣ **Complex (`complex`)** – Real + Imaginary numbers  

---

### **✅ a) Integer (`int`) – Poore Numbers**
👉 **Integer woh numbers hain jinmein decimal point nahi hota** (jaise `-10`, `0`, `42`).  

#### **📌 Example: Integer in Python**
```python
num_int: int = 42
print(type(num_int), " num_int =", num_int)
```
🔹 **Output:**  
```
<class 'int'>  num_int = 42
```
➡ **Integer ko hum directly likh sakte hain, bina kisi extra notation ke!** ✅  

---

### **✅ b) Floating-Point (`float`) – Decimal Numbers**
👉 **Float wo numbers hain jisme decimal point hota hai** (jaise `3.14`, `0.5`, `-2.75`).  

#### **📌 Example: Float in Python**
```python
num_float: float = 3.14
print(type(num_float), " num_float =", num_float)
```
🔹 **Output:**  
```
<class 'float'>  num_float = 3.14
```

🔹 **Zero ke bina bhi likh sakte hain:**  
```python
num_float: float = .14  # Python automatically 0.14 bana dega!
print(type(num_float), " num_float =", num_float)
```
📌 **Output:**  
```
<class 'float'>  num_float = 0.14
```
➡ **Matlab `.14` likhne ka matlab `0.14` hi hoga!** ✅  

---

### **✅ c) Complex (`complex`) – Real + Imaginary Numbers**
👉 **Complex numbers wo hote hain jo ek real aur ek imaginary part ko combine karte hain.**  
👉 **Python mein imaginary part ke liye `j` use hota hai.**  

#### **📌 Example: Complex Number in Python**
```python
num_complex: complex = 2 + 3j
print(type(num_complex), " num_complex =", num_complex)
```
🔹 **Output:**  
```
<class 'complex'>  num_complex = (2+3j)
```
📌 **Yahan `2` real part hai aur `3j` imaginary part hai!** ✅  

---

## **🔹 2. Boolean (`bool`) – True or False**
👉 **Boolean type sirf do values accept karta hai: `True` ya `False`.**  
👉 **Ye mostly conditions aur comparisons mein use hota hai.**  

#### **📌 Example: Boolean in Python**
```python
is_python_fun: bool = True  # ya False
print(type(is_python_fun), " is_python_fun =", is_python_fun)
```
🔹 **Output:**  
```
<class 'bool'>  is_python_fun = True
```
📌 **Matlab, `True` aur `False` bhi Python mein ek type hain!** ✅  

---

## **🚀 Summary Table**
| **Data Type** | **Description** | **Example** |
|--------------|----------------|------------|
| ✅ **Integer (`int`)** | Whole numbers (positive/negative) | `42`, `-5`, `1000` |
| ✅ **Float (`float`)** | Decimal numbers | `3.14`, `0.5`, `-2.75` |
| ✅ **Complex (`complex`)** | Numbers with real + imaginary part | `2 + 3j`, `-1.5 + 4j` |
| ✅ **Boolean (`bool`)** | `True` or `False` values | `True`, `False` |

---

## **🎯 Conclusion**
Python mein **numbers aur boolean** ka use bohot zyada hota hai.  
✅ **Integer (`int`)** simple numbers ke liye.  
✅ **Float (`float`)** decimal values ke liye.  
✅ **Complex (`complex`)** special scientific calculations ke liye.  
✅ **Boolean (`bool`)** conditions aur logic ke liye.  


