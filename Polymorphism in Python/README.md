### **🐍 Polymorphism in Python – Asaan Lafzon Mein Samajhte Hain!**  

Computer science mein **"poly"** ka matlab **"many"** (zyada) aur **"morph"** ka matlab **"forms"** (shaklein) hota hai.  

👉 **Polymorphism** ka matlab hai **"ek cheez ka bohot saari shaklein lena"**. 🎭  
Matlab, ek **method, function, ya operator** alag alag types ke objects ke saath **different tareeke se behave** kar sakta hai.  

Aayiye ise **mazedaar examples** ke saath samajhte hain! 😊🚀  

---

## **🔹 Types of Polymorphism in Python**  

### **1️⃣ Method Overriding (Runtime Polymorphism)**
👉 **Jab ek subclass apne parent class ke method ko override kar deta hai** (matlab naya behavior de deta hai), to isse **runtime polymorphism** kehte hain.  

#### **✅ Example: Method Overriding**
```python
class Animal:
    def speak(self):
        return "Some sound"

class Dog(Animal):
    def speak(self):  # Overriding the parent method
        return "Bark!"

class Cat(Animal):
    def speak(self):  # Overriding the parent method
        return "Meow!"

# Function jo kisi bhi Animal object ke saath kaam karega
def animal_sound(animal):
    print(animal.speak())

# Objects create karte hain
dog = Dog()
cat = Cat()

animal_sound(dog)  # Output: Bark!
animal_sound(cat)  # Output: Meow!
```
📌 **Yahan `Dog` aur `Cat` class ne `speak()` method ko override kar diya, jo `Animal` class mein defined tha.**  

---

### **2️⃣ Method Overloading (Not Native in Python)**
👉 **Python Java ya C++ ki tarah direct method overloading support nahi karta**, lekin hum **default parameters** ya `*args` use karke ye behavior achieve kar sakte hain.  

#### **✅ Example: Default Parameters Se Method Overloading**
```python
class MathOperations:
    def add(self, a, b=0, c=0):
        return a + b + c

math = MathOperations()
print(math.add(5))       # Output: 5
print(math.add(5, 10))   # Output: 15
print(math.add(5, 10, 15))  # Output: 30
```
📌 **Yahan `add()` function ko alag alag tareeke se call kiya, aur har bar alag result mila!**  

---

### **3️⃣ Operator Overloading**
👉 Python mein **operators** (`+`, `-`, `*`, `/` etc.) ko **override** karne ki facility hoti hai jise **operator overloading** kehte hain.  
Matlab, aap kisi operator ka **custom behavior define** kar sakte hain.  

#### **✅ Example: `+` Operator Overloading**
```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):  # Overloading `+` operator
        return Point(self.x + other.x, self.y + other.y)

    def __str__(self):
        return f"({self.x}, {self.y})"

p1 = Point(2, 3)
p2 = Point(4, 5)
p3 = p1 + p2  # Custom `+` operator call hoga

print(p3)  # Output: (6, 8)
```
📌 **Yahan `+` operator ka custom behavior define kiya using `__add__()` method!**  

---

### **4️⃣ Duck Typing (Subtype Polymorphism)**
👉 **Duck Typing ka concept hai:**  
**"Agar koi cheez batakh ki tarah chalti hai aur batakh ki tarah awaaz nikalti hai, to wo batakh hi hai!"**  

Matlab, **Python object ka type check nahi karta, bas ye dekhta hai ke required method exist karta hai ya nahi.**  

#### **✅ Example: Duck Typing**
```python
class Human:
    def speak(self):
        print("Human: Hello!")

class Parrot:
    def speak(self):
        print("Parrot: Polly wants a cracker!")

class Robot:
    def speak(self):
        print("Robot: Beep boop!")

def have_conversation(entity):
    entity.speak()  # Bas method existence check hota hai, type nahi!

# Alag alag objects pass karte hain
have_conversation(Human())  # Output: Hello!
have_conversation(Parrot())  # Output: Polly wants a cracker!
have_conversation(Robot())  # Output: Beep boop!
```
📌 **Yahan `have_conversation()` function ko koi fark nahi padta ke object kis type ka hai. Jab tak `speak()` method hai, function kaam karega!**  

---

## **🔹 Why is Polymorphism Important?**
✅ **Code Reusability:** Same function ya method alag alag types ke saath kaam kar sakta hai.  
✅ **Scalability:** Naye classes add karne ke liye existing code ko change karne ki zaroorat nahi.  
✅ **Flexibility:** Methods aur functions dynamically alag alag object types ko handle kar sakte hain.  

---

## **🚀 Summary of Polymorphism in Python**
| **Type** | **Explanation** | **Example** |
|----------|---------------|------------|
| ✅ **Method Overriding** | Subclass apne parent method ka naya version banata hai | `Dog().speak()` overrides `Animal.speak()` |
| ✅ **Method Overloading** | Same method different parameters accept kar sakta hai (Python mein default arguments se achieve hota hai) | `add(a)`, `add(a, b)`, `add(a, b, c)` |
| ✅ **Operator Overloading** | Operators (`+`, `-`, `*`, etc.) ka custom behavior define kiya jata hai | `Point(2,3) + Point(4,5) -> (6,8)` |
| ✅ **Duck Typing** | Object ka type check nahi hota, bas usme required method ya attribute hai ya nahi ye dekha jata hai | `have_conversation(Human())` works with any class having `speak()` |

---

## **🎯 Conclusion**
Polymorphism Python ka ek **powerful concept** hai jo **flexibility, reusability aur scalability** provide karta hai.  
👉 **Ek function ya method alag alag types ke objects ke saath alag tareeke se behave kar sakta hai.**  
👉 **Python isko multiple tareekon se implement karta hai, jaise Method Overriding, Operator Overloading, aur Duck Typing!**  



