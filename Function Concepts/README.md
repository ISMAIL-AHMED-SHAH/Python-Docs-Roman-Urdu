### **Fibonacci Sequence aur Recursive Functions – Roman Urdu Guide! 🚀**  

Recursion aik aisi technique hai jisme **function apne aap ko dobara call karta hai** jab tak ek **base case** na mil jaye. Yeh method bohat useful hoti hai **mathematical problems (jaise factorial, Fibonacci)** aur **tree traversal algorithms** ke liye.  

---

## **🔹 Fibonacci Sequence – Recursive Approach**
Fibonacci sequence aik **series of numbers** hoti hai jisme har number **pichlay do numbers ka sum** hota hai.  

✅ **Fibonacci Numbers:**  
`0, 1, 1, 2, 3, 5, 8, 13, ...`  

✅ **Recursive Formula:**  
\[
F(n) = F(n-1) + F(n-2)
\]
Jab tak **base case** na mil jaye:  
\[
F(0) = 0, \quad F(1) = 1
\]

### **💻 Recursive Function Example**
```python
def fibonacci(n):
    # Base cases
    if n == 0:
        return 0
    elif n == 1:
        return 1
    # Recursive case
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Example usage
print(fibonacci(6))  # Output: 8
```
📌 **Kaise Kaam Karta Hai?**  
1. **fibonacci(6)** ko call kiya gaya  
2. Yeh call karta hai: `fibonacci(5) + fibonacci(4)`  
3. **fibonacci(5)** call karega `fibonacci(4) + fibonacci(3)`  
4. Yeh process continue hota hai jab tak `fibonacci(1) = 1` aur `fibonacci(0) = 0` return ho jaye  
5. Sab results **sum** hote hain aur final answer `8` milta hai  

---

## **🔹 Advantages of Recursive Functions**
✔ **Code Simple hota hai:** Badi problems ko **choti aur samajhne laayak** bana deta hai.  
✔ **Elegant Solution:** Recursive algorithms **tree traversal, sorting, aur mathematical calculations** ke liye best hain.  
✔ **Divide and Conquer Approach:** Problem ko chhoti chhoti subproblems me todna easy hota hai.  

## **🔹 Disadvantages of Recursive Functions**
❌ **Stack Overflow:** Agar **base case na ho** ya function **bohat zyada calls** kare to stack overflow ho sakta hai.  
❌ **Performance Issues:** Har call ke liye **extra memory aur execution time** lagta hai.  
❌ **Debugging Complex Hoti Hai:** Recursive functions ko debug karna **difficult hota hai**.  

📌 **Solution:** **Memoization** ya **Iterative Approach** ka use karke recursion ka **alternative** bana sakte hain.  

---

# **Factorial Using Recursion**
Factorial `n!` ka formula:  
\[
n! = n \times (n-1)!
\]
\[
5! = 5 × 4 × 3 × 2 × 1 = 120
\]

✅ **Recursive Function for Factorial**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

number = 5
result = factorial(number)
print(f"The factorial of {number} is {result}")  # Output: 120
```
📌 **Kaise Kaam Karta Hai?**  
1. **factorial(5)** call karega `5 * factorial(4)`  
2. **factorial(4)** call karega `4 * factorial(3)`  
3. Jab tak `factorial(0) = 1` na mil jaye  
4. Phir values multiply hoti hain aur **final result** aata hai!  

---

# **🔹 Multi-Type Return in Function**
Python me ek function **multiple types ka data return** kar sakta hai **Tuple, List, ya Dictionary** ki form me. Yeh bohat useful hota hai **agar function ko multiple values return karni ho**.

✅ **Example – Function Returning Tuple**
```python
from typing import Tuple, List, Dict

def example_function(a: int, b: int = 0, *args: float, **kwargs: str) -> Tuple[int, List[float], Dict[str, str]]:
    """Function jo int, list, aur dictionary return karta hai"""
    sum_ab = a + b
    args_list = list(args)  # Convert tuple to a list
    return sum_ab, args_list, kwargs

# Example usage
result = example_function(1, 2, 3.14, 2.71, name="Alice", city="New York")
print(result)

result = example_function(10, *[1.0, 2.0, 3.0], **{"country": "USA", "language": "English"})
print(result)
```
📌 **Kaise Kaam Karta Hai?**  
✅ `a + b` ka sum return karega  
✅ `*args` ko list me convert karega  
✅ `**kwargs` ko dictionary me return karega  

📌 **Output:**  
```
(3, [3.14, 2.71], {'name': 'Alice', 'city': 'New York'})
(11, [1.0, 2.0, 3.0], {'country': 'USA', 'language': 'English'})
```
✅ **Faida:** Multiple values ko **ek saath return kar sakte hain** bina kisi complex structure ke.

---

## **🔹 Function Arguments ka Order (Important)**
Agar hum function likhte hain to arguments ka ek **specific order** hota hai:

1. **Positional Arguments** – Pehle specify hote hain  
2. **Default Arguments** – Default values wale arguments  
3. **Variable-length Arguments (`*args`)** – Multiple positional values store karne ke liye  
4. **Keyword Arguments (`**kwargs`)** – Named values store karne ke liye  

✅ **Example**
```python
def function_example(pos1, pos2, default1="default", *args, **kwargs):
    print("Positional:", pos1, pos2)
    print("Default:", default1)
    print("Args:", args)
    print("Kwargs:", kwargs)

function_example(1, 2, "Custom Default", 3, 4, 5, key1="value1", key2="value2")
```
📌 **Order:**  
✅ **Positional arguments:** `1, 2`  
✅ **Default argument:** `"Custom Default"`  
✅ **`*args` (Tuple me values):** `(3, 4, 5)`  
✅ **`**kwargs` (Dictionary me values):** `{'key1': 'value1', 'key2': 'value2'}`  

📌 **Output:**
```
Positional: 1 2
Default: Custom Default
Args: (3, 4, 5)
Kwargs: {'key1': 'value1', 'key2': 'value2'}
```

---

## **🎯 Recap – Key Takeaways**
✅ **Recursive Functions:** Jab function **khud ko dobara call kare**  
✅ **Fibonacci aur Factorial Examples:** Recursion ka practical use  
✅ **Multi-Type Return:** Function ek saath multiple values return kar sakta hai  
✅ **Function Arguments ka Order:** Pehle positional, phir default, phir `*args`, aur akhir me `**kwargs`  
