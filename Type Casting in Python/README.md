# **🐍 Python Type Casting!** 🚀  

Python mein **Type Casting** ka matlab hai **ek data type ko doosre data type mein convert karna**.  
✅ **Python automatically kuch conversions kar leta hai (Implicit Casting).**  
✅ **Hum manually bhi data type convert kar sakte hain (Explicit Casting).**  

---

## **🔹 1. Implicit Type Casting (Automatic Conversion)**
Python **automatically** kuch data types ko doosre types mein convert kar leta hai jab **koi data loss na ho**.  

### **✅ Example 1: Integer → Float**
```python
num_int = 10
num_float = num_int + 5.5  # int + float → float
print(num_float, type(num_float))
```
🔹 **Output:**  
```
15.5 <class 'float'>
```
📌 **Python ne `int` ko `float` mein convert kar diya!** ✅  

---

### **✅ Example 2: Integer → Complex**
```python
num_int = 7
num_complex = num_int + 3j  # int + complex → complex
print(num_complex, type(num_complex))
```
🔹 **Output:**  
```
(7+3j) <class 'complex'>
```
📌 **Python automatically `int` ko `complex` mein promote kar deta hai!** ✅  

---

### **❌ Example 3: String & Integer ka Implicit Conversion Nahi Hota**
```python
num_str = "100"
num_int = 5

# print(num_str + num_int)  # ❌ TypeError (Implicit conversion nahi hoga)
```
📌 **Python automatically `str` ko `int` mein convert nahi karega!** ❌  
✅ **Hume manually convert karna padega:**  
```python
print(int(num_str) + num_int)  # ✅ String → Integer
print(num_str + str(num_int))  # ✅ Integer → String
```
🔹 **Output:**  
```
105
1005
```
📌 **Manually `int()` aur `str()` use karke convert karna padega!** ✅  

---

## **🔹 2. Explicit Type Casting (Manual Conversion)**
👉 **Python ke built-in functions ka use karke hum manually data type convert kar sakte hain.**  

| **Function** | **Description** |
|------------|----------------|
| `int(x)` | Integer mein convert karega |
| `float(x)` | Float mein convert karega |
| `complex(x)` | Complex number mein convert karega |
| `str(x)` | String mein convert karega |
| `bool(x)` | Boolean mein convert karega |
| `list(x)` | List mein convert karega |
| `tuple(x)` | Tuple mein convert karega |
| `set(x)` | Set mein convert karega |
| `dict(x)` | Dictionary mein convert karega |

---

## **🔹 3. Integer Conversion (`int()`)**
✅ **Float ko Integer mein Convert Karna (Decimal Remove Ho Jata Hai)**  
```python
num_float = 9.8
num_int = int(num_float)  # Decimal remove ho jayega
print(num_int, type(num_int))
```
🔹 **Output:**  
```
9 <class 'int'>
```
📌 **`int()` decimal part truncate kar deta hai (round nahi karta)!** ✅  

✅ **String → Integer (Sirf Valid Numbers Convert Honge)**  
```python
num_str = "123"
num_int = int(num_str)
print(num_int, type(num_int))
```
🔹 **Output:**  
```
123 <class 'int'>
```
📌 **Agar `num_str = "123abc"` ho, to `ValueError` aayega!** ❌  

✅ **Boolean → Integer (`True = 1`, `False = 0`)**  
```python
print(int(True))   # Output: 1
print(int(False))  # Output: 0
```

---

## **🔹 4. Float Conversion (`float()`)**
✅ **Integer → Float**  
```python
num_int = 5
num_float = float(num_int)
print(num_float, type(num_float))
```
🔹 **Output:**  
```
5.0 <class 'float'>
```

✅ **String → Float**  
```python
num_str = "3.14"
num_float = float(num_str)
print(num_float, type(num_float))
```
🔹 **Output:**  
```
3.14 <class 'float'>
```

---

## **🔹 5. String Conversion (`str()`)**
✅ **Number → String**  
```python
num = 100
num_str = str(num)
print(num_str, type(num_str))
```
🔹 **Output:**  
```
100 <class 'str'>
```

✅ **Boolean → String**  
```python
print(str(True))   # Output: "True"
print(str(False))  # Output: "False"
```

---

## **🔹 6. Boolean Conversion (`bool()`)**
✅ **Python mein koi bhi non-empty ya non-zero value `True` hoti hai, baaki `False`.**  
```python
print(bool(1))       # True
print(bool(0))       # False
print(bool(-10))     # True
print(bool(""))      # False
print(bool("Hello")) # True
print(bool([]))      # False
print(bool([1, 2]))  # True
```

---

## **🔹 7. List, Tuple, Set & Dictionary Conversions**
✅ **Tuple → List**  
```python
tup = (1, 2.7, 3, 'OB')
lst = list(tup)
print(lst, type(lst))
```
🔹 **Output:**  
```
[1, 2.7, 3, 'OB'] <class 'list'>
```

✅ **List → Set (Duplicates Remove Ho Jate Hain)**  
```python
lst = [1, 2, 2, 3, 4, 4, 5]
s = set(lst)
print(s, type(s))
```
🔹 **Output:**  
```
{1, 2, 3, 4, 5} <class 'set'>
```

✅ **List of Tuples → Dictionary**  
```python
lst = [("name", "Ali"), ("age", 25)]
d = dict(lst)
print(d, type(d))
```
🔹 **Output:**  
```
{'name': 'Ali', 'age': 25} <class 'dict'>
```

---

## **🔹 8. Complex Number Conversion (`complex()`)**
✅ **Integer → Complex Number**  
```python
num = 5
comp = complex(num)
print(comp, type(comp))
```
🔹 **Output:**  
```
(5+0j) <class 'complex'>
```
❌ **Complex Number ko Integer Mein Convert Nahi Kar Sakte**  
```python
# num = int(comp)  # ❌ TypeError: Complex number ko int mein convert nahi kar sakte
```

---

## **🚀 Summary Table**
| **Conversion** | **Function** | **Example** | **Output** |
|--------------|------------|------------|------------|
| **Integer** | `int(x)` | `int(5.7)` | `5` |
| **Float** | `float(x)` | `float("3.14")` | `3.14` |
| **String** | `str(x)` | `str(100)` | `"100"` |
| **Boolean** | `bool(x)` | `bool(0)`, `bool([])` | `False` |
| **List** | `list(x)` | `list((1,2,3))` | `[1, 2, 3]` |
| **Set** | `set(x)` | `set([1,1,2,3])` | `{1,2,3}` |
| **Dictionary** | `dict(x)` | `dict([("a",1),("b",2)])` | `{'a':1, 'b':2}` |

---

## **🎯 Conclusion**
✅ **Implicit Type Casting Automatically Hota Hai Jab Data Loss Nahi Hota.**  
✅ **Explicit Type Casting (`int()`, `float()`, `str()`) Manually Data Convert Karne Ke Liye Use Hota Hai.**  
✅ **String Conversion Carefully Karni Chahiye (Invalid Strings Error De Sakti Hain).**  

