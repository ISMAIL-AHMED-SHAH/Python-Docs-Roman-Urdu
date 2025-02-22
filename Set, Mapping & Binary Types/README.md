# **🐍 Python Data Types – Set, Mapping & Binary Types Asaan Lafzon Mein!**  

Python mein **data types** kaafi flexible hain, jo alag alag tarike se data store aur manipulate karne ke liye use hote hain.  
Aaj hum **Set, Dictionary aur Binary Types** ko **mazedaar examples** ke saath samajhne wale hain! 🚀  

---

## **🔹 4. Set Types – Unique Elements Collection**
Set ek **unordered collection** hota hai jo **sirf unique values** store karta hai.  

### **✅ a) Set (`set`) – Mutable, Unordered, Unique Values**
👉 **Set ke andar duplicate values nahi hoti.**  
👉 **Set unordered hota hai, iska koi fixed order nahi hota.**  
👉 **Mutable hota hai, iska data change kiya ja sakta hai.**  

#### **📌 Example: Set in Python**
```python
my_set: set = {1, 2, 33, 4, 4, 5}  # Duplicate `4` remove ho jayega!
print(type(my_set), "my_set =", my_set)
```
🔹 **Output:**  
```
<class 'set'> my_set = {1, 2, 33, 4, 5}
```
📌 **Key Features:**  
✅ Duplicate values **automatically remove** ho jati hain.  
✅ **Unordered hota hai** (iska koi fixed index nahi hota).  
✅ **Mutable hota hai** (hum isme naye elements add/remove kar sakte hain).  

---

### **✅ b) Frozen Set (`frozenset`) – Immutable Set**
👉 **Ye ek set ka immutable version hota hai, jo modify nahi kiya ja sakta.**  
👉 **Jo values add kar di, bas wahi rahengi, naye elements nahi add ho sakte!**  

#### **📌 Example: Frozen Set in Python**
```python
frozen_set = frozenset([11, 2, 3, 4, 4, 5])  # Duplicate 4 remove ho jayega
print(type(frozen_set), " frozen_set =", frozen_set)
```
🔹 **Output:**  
```
<class 'frozenset'>  frozen_set = frozenset({2, 3, 4, 5, 11})
```
📌 **Key Features:**  
✅ **Immutable hota hai** (iska data change nahi hota).  
✅ **Unique values hi store hoti hain** (duplicate values remove ho jati hain).  

---

## **🔹 5. Mapping Type – Dictionary (`dict`)**
👉 **Dictionary ek "key-value pair" storage hai.**  
👉 **Har key ka ek unique value hota hai.**  
👉 **Fast searching aur data retrieval ke liye best hota hai!**  

#### **✅ Example: Dictionary in Python**
```python
my_dict: dict = {"name": "Alice", "age": 25, "language": "Python"}
print(type(my_dict), " my_dict =", my_dict)
```
🔹 **Output:**  
```
<class 'dict'>  my_dict = {'name': 'Alice', 'age': 25, 'language': 'Python'}
```
📌 **Key Features:**  
✅ **Key-value pairs store karta hai.**  
✅ **Keys unique hoti hain, values repeat ho sakti hain.**  
✅ **Fast searching aur lookup ke liye efficient hota hai.**  

---

## **🔹 6. Binary Types – Bytes, Bytearray & Memoryview**
👉 **Binary types ko binary data store aur manipulate karne ke liye use kiya jata hai.**  
👉 **Mostly file handling, network programming aur low-level memory management ke liye useful hain.**  

### **✅ a) Bytes (`bytes`) – Immutable Binary Data**
👉 **Immutable binary sequence hota hai.**  
👉 **Mostly files ya network communication ke liye use hota hai.**  

#### **📌 Example: Bytes in Python**
```python
byte_data: bytes = b"Hello"
print(type(byte_data), " byte_data =", byte_data)
```
🔹 **Output:**  
```
<class 'bytes'>  byte_data = b'Hello'
```
📌 **Key Features:**  
✅ **Immutable hota hai (change nahi ho sakta).**  
✅ **Fixed binary data store karne ke liye useful hai.**  

---

### **✅ b) Bytearray (`bytearray`) – Mutable Binary Data**
👉 **Ye `bytes` ka ek mutable version hota hai, jo modify kiya ja sakta hai!**  

#### **📌 Example: Bytearray in Python**
```python
byte_array: bytearray = bytearray([65, 66, 67, 69])  # 65=A, 66=B, etc.
print(type(byte_array), " byte_array =", byte_array)
```
🔹 **Output:**  
```
<class 'bytearray'>  byte_array = bytearray(b'ABCE')
```
📌 **Key Features:**  
✅ **Mutable hota hai (modify kiya ja sakta hai).**  
✅ **Binary data manipulation ke liye useful hota hai.**  

#### **📌 Example: Modifying a Bytearray**
```python
ba: bytearray = bytearray(b"hello")
print("Before: ba =", ba)

# Modifying the bytearray
ba[0] = 72  # ASCII value of 'H'

print("After: ba =", ba)  # Output: bytearray(b'Hello')
```
🔹 **Output:**  
```
Before: ba = bytearray(b'hello')
After: ba = bytearray(b'Hello')
```
📌 **Yahan humne `hello` ko `Hello` bana diya by changing `h` → `H`.**  

---

### **✅ c) Memoryview (`memoryview`) – Efficient Binary Handling**
👉 **Ye ek efficient tarika hai binary data ko access karne ka bina uski copy banaye.**  

#### **📌 Example: Memoryview in Python**
```python
mem_view: memoryview = memoryview(b"Operation Badar")
print(type(mem_view), " mem_view =", mem_view)

print(bytes(mem_view[0:5]))  # First 5 bytes ko access karna
print(mem_view[6:11])  # Cast to bytes otherwise it will show memory address
```
🔹 **Output:**  
```
<class 'memoryview'>  mem_view = <memory at 0x7d294da28b80>
b'Opera'
<memory at 0x7d294da28f40>
```
📌 **Key Features:**  
✅ **Binary data efficiently handle karne ke liye use hota hai.**  
✅ **Bina extra copy banaye binary data ko access karta hai.**  

---

## **🚀 Summary Table**
| **Data Type** | **Description** | **Example** |
|--------------|----------------|------------|
| ✅ **Set (`set`)** | Unordered, mutable, unique values | `{1, 2, 3, 4, 5}` |
| ✅ **Frozen Set (`frozenset`)** | Immutable set | `frozenset({1, 2, 3})` |
| ✅ **Dictionary (`dict`)** | Key-value pair storage | `{"name": "Alice", "age": 25}` |
| ✅ **Bytes (`bytes`)** | Immutable binary data | `b'Hello'` |
| ✅ **Bytearray (`bytearray`)** | Mutable binary data | `bytearray(b'ABCE')` |
| ✅ **Memoryview (`memoryview`)** | Efficient binary data access | `memoryview(b'Python')` |

---

## **🎯 Conclusion**
Python ke **Set, Dictionary aur Binary types** powerful tools hain jo alag alag situations mein kaam aate hain.  
✅ **Sets unique values store karte hain.**  
✅ **Dictionaries fast key-value lookup ke liye use hoti hain.**  
✅ **Binary types data ko efficiently store aur manipulate karne ke liye use hote hain.**  

