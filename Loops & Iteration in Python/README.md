# **🐍 Loops & Iteration in Python!** 🚀  

Python mein **loops** ka use **repetitive tasks** ko execute karne ke liye hota hai.  
✅ **`for` loop** – Jab **sequence (list, string, range)** par iterate karna ho.  
✅ **`while` loop** – Jab **condition True rahe tab tak code execute karna ho**.  

---

## **🔹 1. Loops Ka Use Kab Karte Hain?**
| **Scenario** | **Loop Type** | **Example** |
|--------------|-------------|------------|
| **Fixed Iterations** | `for` loop | Student grades calculate karna |
| **Unknown Iterations (Until Condition is Met)** | `while` loop | Gas tank fill karna jab tak full na ho |

📌 **For Loop Example:** *Ek list mein har student ke marks ko process karna.*  
📌 **While Loop Example:** *Ek machine tab tak chale jab tak task complete na ho.*  

---

## **🔹 2. `for` Loop**
👉 **Jab kisi sequence (list, string, range) par iterate karna ho.**  

### **✅ Example 1: List ke Har Element Ko Print Karna**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
🔹 **Output:**  
```
apple
banana
cherry
```

### **✅ Example 2: String Ke Har Character Ko Print Karna**
```python
word = "Python"
for letter in word:
    print(letter)
```
🔹 **Output:**  
```
P
y
t
h
o
n
```

### **✅ Example 3: `range()` Ka Use**
```python
for i in range(5):  # 0 se 4 tak numbers print karega
    print(i)
```
🔹 **Output:**  
```
0
1
2
3
4
```

---

## **🔹 3. `while` Loop**
👉 **Jab tak condition True ho tab tak loop chalega.**  

### **✅ Example: `while` Loop Se Counting**
```python
count = 1
while count <= 5:
    print(count)
    count += 1  # Count ko har baar 1 se badhate raho
```
🔹 **Output:**  
```
1
2
3
4
5
```

---

## **🔹 4. Loops Ko Control Karna (`break` & `continue`)**
👉 **Loops ko manage karne ke liye `break` aur `continue` ka use hota hai.**  

### **✅ `break` – Loop Ko Rok Dena**
```python
for i in range(10):
    if i == 5:
        break  # Jaise hi i == 5 hoga, loop ruk jayega
    print(i)
```
🔹 **Output:**  
```
0
1
2
3
4
```

### **✅ `continue` – Current Iteration Skip Karna**
```python
for i in range(5):
    if i == 3:
        continue  # Jab i == 3 hoga, print nahi karega
    print(i)
```
🔹 **Output:**  
```
0
1
2
4
```

---

## **🔹 5. Nested Loops (Loops Ke Andar Loop)**
👉 **Jab ek loop ke andar doosra loop chalayen.**  

### **✅ Example: Multiplication Table (Nested Loop)**
```python
for outer in range(1, 4):  # Outer loop 1 se 3 tak chalega
    print(f"Table of {outer}:")
    for inner in range(1, 6):  # Inner loop 1 se 5 tak chalega
        print(f"{outer} x {inner} = {outer * inner}")
    print()  # Har table ke baad ek blank line
```
🔹 **Output:**  
```
Table of 1:
1 x 1 = 1
1 x 2 = 2
1 x 3 = 3
1 x 4 = 4
1 x 5 = 5

Table of 2:
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10

Table of 3:
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
```

📌 **Nested loops ka use tab hota hai jab hume kisi matrix ya table par kaam karna ho.** ✅  

---

## **🔹 6. Practical Examples**
### **✅ Example 1: 1 Se 100 Tak Numbers Ka Sum**
```python
total = 0
for i in range(1, 101):  # 1 se 100 tak add karega
    total += i
print("Sum of numbers from 1 to 100:", total)
```
🔹 **Output:**  
```
Sum of numbers from 1 to 100: 5050
```

### **✅ Example 2: Kisi Number Ke Factors Dhoondhna**
```python
num = 24
factors = []
for i in range(1, num + 1):
    if num % i == 0:
        factors.append(i)
print(f"Factors of {num}:", factors)
```
🔹 **Output:**  
```
Factors of 24: [1, 2, 3, 4, 6, 8, 12, 24]
```

---

## **🚀 Summary Table**
| **Concept** | **Example** | **Use Case** |
|------------|------------|------------|
| `for` loop | `for i in range(5):` | Jab fixed iterations ho |
| `while` loop | `while count <= 5:` | Jab tak condition True ho |
| `break` | `if i == 5: break` | Loop ko rokna |
| `continue` | `if i == 3: continue` | Current iteration skip karna |
| Nested Loops | `for i in range(3): for j in range(3):` | Multiplication tables, matrix operations |

---

## **🎯 Conclusion**
✅ **Loops se repetitive tasks automate ho jate hain.**  
✅ **`for` loop ka use tab hota hai jab sequence par iterate karna ho.**  
✅ **`while` loop ka use tab hota hai jab condition satisfy hone tak loop chalana ho.**  
✅ **`break` aur `continue` loop control karne ke liye use hote hain.**  
✅ **Nested loops complex tasks jaise **tables**, **matrices**, aur **data processing** ke liye kaam aate hain.**  

