# **🐍 Python Control Flow & Decision Making** 🚀  

Python mein **Control Flow** ka matlab hai **program ka execution kis order mein hoga**.  
✅ **`if`, `elif`, `else` ka use decision making ke liye hota hai.**  
✅ **Comparison aur Logical operators ka use conditions check karne ke liye hota hai.**  

---

## **🔹 1. Comparison Operators (Conditions Check Karna)**
👉 **Comparison operators True ya False return karte hain.**  

| **Operator** | **Meaning** | **Example** | **Output** |
|------------|-------------|---------|--------|
| `==` | Equal to | `x == y` | `True/False` |
| `!=` | Not equal to | `x != y` | `True/False` |
| `>` | Greater than | `x > y` | `True/False` |
| `<` | Less than | `x < y` | `True/False` |
| `>=` | Greater than or equal to | `x >= y` | `True/False` |
| `<=` | Less than or equal to | `x <= y` | `True/False` |

### **✅ Example: Comparison Operators**
```python
x = 10
y = 20

print("x == y:", x == y)  # False
print("x != y:", x != y)  # True
print("x > y:", x > y)    # False
print("x < y:", x < y)    # True
print("x >= y:", x >= y)  # False
print("x <= y:", x <= y)  # True
```

---

## **🔹 2. Logical Operators**
👉 **Multiple conditions ko combine karne ke liye use hotay hain.**  

| **Operator** | **Meaning** | **Example** | **Output** |
|------------|-------------|---------|--------|
| `and` | Dono conditions True ho | `(x > 5 and x < 20)` | `True` |
| `or` | Ek bhi condition True ho | `(x > 5 or x < 3)` | `True` |
| `not` | Condition ka result opposite ho | `not(x > 5)` | `False` |

### **✅ Example: Logical Operators**
```python
age = 25
is_student = True

if age > 18 and is_student:
    print("You are eligible for a student discount.")

if age < 12 or age > 60:
    print("You qualify for a special discount.")

if not is_student:
    print("You are not a student.")
```
🔹 **Output:**  
```
You are eligible for a student discount.
```

---

## **🔹 3. `if` Statement (Condition True Ho to Execute Karega)**
👉 **Agar condition True ho, to code execute hoga.**  

### **✅ Example: `if` Statement**
```python
num = 10

if num > 0:
    print("The number is positive.")
```
🔹 **Output:**  
```
The number is positive.
```

---

## **🔹 4. `else` Statement (Agar `if` False Ho to Execute Karega)**
👉 **Jab `if` condition False ho, tab `else` execute hoga.**  

### **✅ Example: `else` Statement**
```python
num = -5

if num > 0:
    print("The number is positive.")
else:
    print("The number is not positive.")
```
🔹 **Output:**  
```
The number is not positive.
```

---

## **🔹 5. `elif` Statement (Multiple Conditions Check Karne Ke Liye)**
👉 **Agar pehli condition False ho, to `elif` ka check hoga.**  

### **✅ Example: `elif` Statement**
```python
num = 0

if num > 0:
    print("The number is positive.")
elif num < 0:
    print("The number is negative.")
else:
    print("The number is zero.")
```
🔹 **Output:**  
```
The number is zero.
```

---

## **🔹 6. Nested `if` (Ek `if` ke andar doosra `if`)**
👉 **Jab ek condition ke andar aur ek condition check karni ho.**  

### **✅ Example: Nested `if`**
```python
num = 10

if num > 0:
    if num % 2 == 0:
        print("The number is positive and even.")
    else:
        print("The number is positive and odd.")
else:
    print("The number is negative.")
```
🔹 **Output:**  
```
The number is positive and even.
```

---

## **🔹 7. Practical Examples**
### **✅ Example 1: Simple Calculator**
```python
operation = input("Enter operation (+, -, *, /): ")
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

if operation == '+':
    result = num1 + num2
elif operation == '-':
    result = num1 - num2
elif operation == '*':
    result = num1 * num2
elif operation == '/':
    if num2 != 0:
        result = num1 / num2
    else:
        result = "Error: Division by zero."
else:
    result = "Invalid operation."

print("Result:", result)
```
🔹 **Output (Example Input: `/`, `10`, `2`)**  
```
Enter operation: /
Enter first number: 10
Enter second number: 2
Result: 5.0
```

---

### **✅ Example 2: Advanced Calculator (With More Operators)**
```python
def calculator():
    while True:
        operation = input("Enter operation (+, -, *, /, %, //, ** or 'q' to quit): ")
        if operation.lower() == 'q':
            break
        if operation not in ('+', '-', '*', '/', '%', '//', '**'):
            print("Invalid operation.")
            continue

        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
        except ValueError:
            print("Invalid input. Enter numbers only.")
            continue

        if operation == '+':
            result = num1 + num2
        elif operation == '-':
            result = num1 - num2
        elif operation == '*':
            result = num1 * num2
        elif operation == '/':
            result = num1 / num2 if num2 != 0 else "Error: Division by zero."
        elif operation == '%':
            result = num1 % num2
        elif operation == '//':
            result = num1 // num2 if num2 != 0 else "Error: Division by zero."
        elif operation == '**':
            result = num1 ** num2

        print("Result:", result)

calculator()
```

---

### **✅ Example 3: Grading System**
```python
def grading_system(marks):
    if marks >= 90:
        grade = "A+"
    elif marks >= 80:
        grade = "A"
    elif marks >= 70:
        grade = "B"
    elif marks >= 60:
        grade = "C"
    elif marks >= 50:
        grade = "D"
    else:
        grade = "F"

    return grade

marks = float(input("Enter the marks: "))
print(f"The grade for {marks} marks is: {grading_system(marks)}")
```
🔹 **Example Output:**  
```
Enter the marks: 96
The grade for 96.0 marks is: A+
```

---

## **🚀 Summary Table**
| **Concept** | **Example** | **Description** |
|------------|------------|----------------|
| `if` | `if x > 10:` | Jab condition True ho |
| `else` | `else:` | Jab `if` condition False ho |
| `elif` | `elif x == 5:` | Multiple conditions check karna |
| Nested `if` | `if x > 0: if x % 2 == 0:` | `if` ke andar `if` |
| Logical Operators | `and`, `or`, `not` | Multiple conditions ko combine karna |

---

## **🎯 Conclusion**
✅ **Python ka `if-else` aur logical operators program decision making ke liye bohot zaroori hain.**  
✅ **Grading system, calculator jaise programs control flow ka best example hain.**  
