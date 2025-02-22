# **🐍 Sequence Types in Python – Asaan Lafzon Mein!**  

Python mein **Sequence Types** ka use **multiple values ko ordered way mein store karne** ke liye hota hai.  
✅ **Sequence types mein data ko ek specific order mein store kiya jata hai.**  

**Python ke major sequence types:**  
1️⃣ **String (`str`)** – Characters ka sequence  
2️⃣ **List (`list`)** – Ordered, mutable collection  
3️⃣ **Tuple (`tuple`)** – Ordered, immutable collection  
4️⃣ **Range (`range`)** – Number sequences ke liye  

Chaliye ise **mazedaar examples ke saath samajhte hain!** 😊🚀  

---

## **🔹 1. String (`str`) – Character Sequence**
👉 **String ek sequence hai jo characters ka collection hota hai.**  
👉 **Hamesha quotes (`""`, `''`, `'''` ya `"""`) ke andar likha jata hai.**  

### **✅ Example: Strings in Python**
```python
text_double: str  = "Hello, Python!"  # Double Quotes
text_single: str  = 'Hello, Python!'  # Single Quotes
text_multi: str   = '''Hello, Python!'''  # Triple Single Quotes
text_multi_1: str = """Hello, Python!"""  # Triple Double Quotes

print(type(text_double), " text_double   = ", text_double)
print(type(text_single), " text_single   = ", text_single)
print(type(text_multi), " text_multi    = ", text_multi)
print(type(text_multi_1), " text_multi_1  = ", text_multi_1)
```
🔹 **Output:**  
```
<class 'str'>  text_double   =  Hello, Python!
<class 'str'>  text_single   =  Hello, Python!
<class 'str'>  text_multi    =  Hello, Python!
<class 'str'>  text_multi_1  =  Hello, Python!
```
### **📌 Key Takeaways**
✅ **Double Quotes (`" "`):** Jab string ke andar **single quote (`'`)** ho.  
✅ **Single Quotes (`' '`):** Jab string ke andar **double quote (`"`)** ho.  
✅ **Triple Quotes (`'''` ya `"""`):** **Multi-line strings** ya **docstrings** ke liye.  

---

## **🔹 2. List (`list`) – Ordered, Mutable Collection**
👉 **List ek ordered collection hoti hai jo change (modify) ki ja sakti hai.**  
👉 **Har type ka data store kar sakti hai (`int`, `str`, `float`, `bool`, etc.).**  

### **✅ Example: Lists in Python**
```python
my_list_1: list = [1, 2, 3, "Java", 3.14, True]
my_list: list = [1, 2, 3, "Python", 3.14, 3+2j]  # Mixed data types

print(type(my_list_1), " my_list_1 = ", my_list_1)
print(type(my_list), " my_list   = ", my_list)
```
🔹 **Output:**  
```
<class 'list'>  my_list_1 =  [1, 2, 3, 'Java', 3.14, True]
<class 'list'>  my_list   =  [1, 2, 3, 'Python', 3.14, (3+2j)]
```
📌 **Lists:**  
✅ **Ordered hoti hain (har item ka index hota hai).**  
✅ **Mutable hoti hain (change ki ja sakti hain).**  
✅ **Mixed data types store kar sakti hain.**  

---

## **🔹 3. Tuple (`tuple`) – Ordered, Immutable Collection**
👉 **Tuple bhi ek ordered collection hoti hai, lekin immutable hoti hai (change nahi ki ja sakti).**  
👉 **Har type ka data store kar sakti hai.**  

### **✅ Example: Tuples in Python**
```python
my_tuple: tuple = (1, 2, 3, "AI", 2.71, False, .3 , 3+2j)
print(type(my_tuple), " my_tuple = ", my_tuple)
```
🔹 **Output:**  
```
<class 'tuple'>  my_tuple =  (1, 2, 3, 'AI', 2.71, False, 0.3, (3+2j))
```
📌 **Tuples:**  
✅ **Ordered hoti hain (har item ka index hota hai).**  
✅ **Immutable hoti hain (change nahi ki ja sakti).**  
✅ **Mixed data types store kar sakti hain.**  

---

## **🔹 4. Range (`range`) – Number Sequences**
👉 **Range ek sequence hai jo numbers generate karta hai.**  
👉 **Mostly loops ke saath use hota hai.**  

### **✅ Example: Range in Python**
```python
num_range: range = range(1, 10, 2)  # range(start, stop, step)
print(type(num_range), " num_range.step =", num_range.step)
```
🔹 **Output:**  
```
<class 'range'>  num_range.step = 2
```
### **✅ Example: Using `range()` in a Loop**
```python
for i in range(1, 10, 2):  # 1 se 10 tak, har bar 2 ka step
  print(i)
```
🔹 **Output:**  
```
1
3
5
7
9
```
📌 **Range:**  
✅ **Numbers ka sequence generate karta hai.**  
✅ **Looping mein zyada use hota hai.**  
✅ **Step parameter se custom sequence bana sakte hain.**  

---

## **🚀 Summary Table**
| **Data Type** | **Description** | **Example** |
|--------------|----------------|------------|
| ✅ **String (`str`)** | Ordered sequence of characters | `"Hello"`, `'Python'`, `'''Multi-line'''` |
| ✅ **List (`list`)** | Ordered, mutable collection | `[1, 2, "Python", 3.14]` |
| ✅ **Tuple (`tuple`)** | Ordered, immutable collection | `(1, 2, "AI", 2.71)` |
| ✅ **Range (`range`)** | Sequence of numbers | `range(1, 10, 2)` |

---

## **🎯 Conclusion**
Python ke **Sequence Types** data ko **ordered way mein store** karne ke liye use hote hain.  
✅ **Strings (`str`)** – Characters ka sequence  
✅ **Lists (`list`)** – Ordered, mutable collection  
✅ **Tuples (`tuple`)** – Ordered, immutable collection  
✅ **Ranges (`range`)** – Number sequences  
