# **Python Functions aur Advanced Concepts – Roman Urdu Guide! 🚀**  

Python me **functions aur arguments** bohat important concepts hain jo **code reuse, efficiency, aur readability** ko improve karte hain. Yahaan hum **pass by reference vs pass by value**, **function arguments**, **lambda functions**, **recursion**, aur **generators** ko **roman urdu** me samjhenge!  

---

## **🔹 Pass by Reference vs Pass by Value – Farq Kya Hai?**
Python me **pass by object reference** hota hai. Iska matlab hai ke **immutable objects (jaise integers)** unchanged rehte hain, magar **mutable objects (jaise lists)** modify ho jate hain.  

### **✅ Immutable Example (Integer) – Value Change Nahi Hoti**
```python
def modify_value(x):
    x = 10
    print("Function ke andar:", x)

x = 5
print("Original:", x)
modify_value(x)
print("Function ke baad:", x)
```
📌 **Output:** `x` same rahta hai kyunki integer **immutable** hai.

---

### **✅ Mutable Example (List) – Value Change Ho Jati Hai**
```python
def modify_list(lst):
    lst.append(4)
    print("Function ke andar:", lst, " - ID:", id(lst))

lst = [1, 2, 3]
print("Original:", lst, " - ID:", id(lst))
modify_list(lst)
print("Function ke baad:", lst, " - ID:", id(lst))
```
📌 **Output:** `lst` modify ho jata hai kyunki **list mutable hoti hai**.

---

## **🔹 Function Arguments – Function me Values Pass Karna**
Python me **function arguments** wo values hain jo function ko call karte waqt pass ki jati hain.

```python
def greetings(name):
   print("Hello, {}".format(name))

greetings("Ali")  # Output: Hello, Ali
greetings("Omar")  # Output: Hello, Omar
```

---

## **🔹 Keyword Arguments – Arguments Ko Naam Se Pass Karna**
Agar hum function call karte waqt **arguments ka naam likh dein**, to order ki koi tension nahi hoti.  

```python
def printinfo(name, age):
    print("Name:", name)
    print("Age:", age)

printinfo(age=50, name="Arif")  # Order different hai, lekin output same hoga
```

---

## **🔹 Default Arguments – Agar Koi Value Na Ho To Default Set Karna**
Agar function me koi **default value** set ki ho, to agar koi argument pass na ho tab bhi function theek kaam karega.

```python
def printinfo(name, age=35):
    print("Name:", name)
    print("Age:", age)

printinfo(name="Arif")  # Default age 35 use hogi
printinfo(name="Ali", age=50)  # Age overwrite ho jayegi
```

---

## **🔹 `*args` – Multiple Values Ko Function Me Pass Karna**
Agar hume nahi pata ke kitne **arguments pass honge**, to hum `*args` ka use kar sakte hain.

```python
def my_sum(*nums):
    return sum(nums)

print(my_sum(1, 2, 3, 4, 5))  # Output: 15
print(my_sum(*[1, 2, 3, 4, 5]))  # List unpacking
```
📌 **Faida:** Multiple values pass karne ke liye **ek hi parameter kaafi hai**!

---

## **🔹 `**kwargs` – Multiple Named Arguments**
Agar hum **multiple key-value pairs** pass karna chahte hain to `**kwargs` ka use karte hain.

```python
def student_info(**info):
    for key, value in info.items():
        print(key, ":", value)

student_info(name="Ali", age=20, course="Python 101")
```
📌 **Faida:** Multiple **named arguments** pass kar sakte hain **dictionary ki tarah**.

---

## **🔹 `lambda` Functions – Chhoti aur Fast Functions**
Lambda functions ek **single-line function** hota hai jo jaldi likhne ke liye use hota hai.

```python
add = lambda x, y: x + y
print(add(5, 3))  # Output: 8
```

✅ **Lambda with `map()`**
```python
numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # Output: [1, 4, 9, 16]
```

✅ **Lambda with `filter()`**
```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4, 6]
```

---

## **🔹 Recursive Functions – Function Jo Khud Ko Call Kare**
Agar aik function **khud ko dobara call kare**, to usay **recursive function** kehte hain.

✅ **Factorial (5! = 5 × 4 × 3 × 2 × 1)**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```
📌 **Base Case:** Jab `n == 0`, function recursion stop kar dega.  

---

✅ **Fibonacci Series (0, 1, 1, 2, 3, 5, 8, ...)**
```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(6))  # Output: 8
```
📌 **Recursive case:** Function apne aap ko `n-1` aur `n-2` ke liye call karega.

---

## **🔹 Generator Functions – Memory Efficient Functions**
Normal functions **poori list memory me store karte hain**, magar **generators aik aik value return karte hain**. Yeh **kam memory consume** karte hain.

✅ **Simple Generator**
```python
def my_generator():
    yield 1
    yield 2
    yield 3

gen = my_generator()

for value in gen:
    print(value)
```
📌 **`yield` ka faida:** Memory me **poori list store nahi hoti**, bas **jo chahiye wahi generate hota hai**.

---

✅ **Infinite Number Generator**
```python
def infinite_numbers():
    num = 0
    while True:
        yield num
        num += 1

gen = infinite_numbers()

for _ in range(5):
    print(next(gen))  # 0, 1, 2, 3, 4
```
📌 **Iska faida:** Yeh **infinite numbers generate** kar sakta hai bina memory overflow ke.

---

## **🎯 Summary**
✅ **Pass by Reference vs Pass by Value** – Integers change nahi hote, Lists modify ho jati hain.  
✅ **`*args` & `**kwargs`** – Multiple values ya named arguments pass karne ke liye.  
✅ **Lambda Functions** – Short aur fast functions.  
✅ **Recursive Functions** – Jab function **khud ko call kare**.  
✅ **Generators** – **Kam memory consume** karne wale special functions.  

