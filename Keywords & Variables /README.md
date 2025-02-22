
# **🐍 Python Keywords & Variables** 🚀  

Python mein **keywords aur variables** programming ka basic foundation hain.  
Aaj hum **keywords, variable naming rules aur best practices** ko **simple examples** ke saath samjhenge! 😊  

---

## **🔹 1. Python Keywords – Reserved Words**
👉 **Keywords wo words hain jo Python ke andar special meaning rakhte hain.**  
👉 **Inko hum variable, function ya class ke naam ke tor par use nahi kar sakte.**  

### **✅ Example: Python Keywords List**
```python
import keyword

print("Python Keywords List:")
print(keyword.kwlist)  # Sab keywords print honge
```
🔹 **Output:**
```
Python Keywords List:
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 
'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 
'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 
'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```
📌 **Keywords ka use special Python functionalities ke liye hota hai, aur inhe variable names ke tor par use nahi kar sakte.**  

### **❌ Example: Keywords as Variable Names (Invalid)**
```python
# and = True  # ❌ Error: "and" ek keyword hai, variable nahi ho sakta!
# class = "CS101"  # ❌ Error: "class" ek reserved keyword hai!
```
📌 **Agar aap kisi keyword ko variable banane ki koshish karenge, to Python error dega!** ✅  

---

## **🔹 2. Python Variables – Data Store Karne Ka Tareeka**
👉 **Variables program execution ke dauraan values ko store aur manipulate karne ke liye use hote hain.**  
👉 **Python dynamically type assign karta hai (hume `int`, `str`, `float` likhne ki zaroorat nahi hoti).**  

### **✅ Example: Creating Variables**
```python
name = "Ali"   # String
age = 25         # Integer
salary = 50000.5 # Float
is_python_fun = True  # Boolean

print("Name:", name)
print("Age:", age)
print("Salary:", salary)
print("Is Python Fun?", is_python_fun)
```
🔹 **Output:**
```
Name: Ali
Age: 25
Salary: 50000.5
Is Python Fun? True
```
📌 **Python automatically detect kar leta hai ke variable kis type ka hai!** ✅  

---

## **🔹 3. Rules for Naming Variables**
✅ **Valid Variable Names:**  
✔ Letters (`a-z`, `A-Z`), digits (`0-9`), aur underscore (`_`) use kar sakte hain.  
✔ Case-sensitive hote hain (`myVar` aur `myvar` alag hain).  

❌ **Invalid Variable Names:**  
❌ Digit se start nahi ho sakte (`2name = "Bob"` **Error**).  
❌ Special characters nahi ho sakte (`my-variable = "Error"` **Error**).  
❌ Keywords nahi ho sakte (`class = "CS101"` **Error**).  

### **✅ Example: Valid & Invalid Variables**
```python
# ✅ Valid variables
user_name = "John"
_age = 30
salary2024 = 55000

# ❌ Invalid variables (Uncomment to see errors)
# 2name = "Bob"        # ❌ Starts with a digit
# my-variable = "Error" # ❌ Contains a hyphen (-)
# class = "CS101"      # ❌ Uses a reserved keyword
```
📌 **Python variables ka naam meaningful aur readable hona chahiye!** ✅  

---

## **🔹 4. Best Practices for Naming Variables**
✅ **Descriptive names use karein (meaningful variables likhein).**  
✅ **Snake case (`my_variable_name`) ya camel case (`myVariableName`) follow karein.**  
✅ **Lowercase letters (`name`, `age`, `salary`) use karein (except constants).**  
✅ **Keywords avoid karein (`class`, `def`, `if` as variable names mat likhein).**  

---

## **🚀 Summary Table**
| **Concept** | **Explanation** | **Example** |
|------------|---------------|------------|
| ✅ **Keywords** | Reserved words, special meaning in Python | `if`, `for`, `while`, `def` |
| ✅ **Variables** | Data store karne ke liye use hote hain | `name = "Alice"` |
| ✅ **Valid Names** | Letters, digits, `_` allowed, case-sensitive | `_age`, `salary2024` |
| ❌ **Invalid Names** | Digits start nahi ho sakte, special chars nahi ho sakte | `2name`, `my-variable` |
| ✅ **Best Practices** | Meaningful names, snake/camel case use karein | `user_name`, `totalSalary` |

---

## **🎯 Conclusion**
Python **keywords aur variables** programming ke basic blocks hain.  
✅ **Keywords reserved hote hain, inhe variable names ke tor par use nahi kar sakte.**  
✅ **Variables values ko store karte hain, aur Python dynamically types assign karta hai.**  
✅ **Good practices follow karne se code readable aur maintainable hota hai.**  

