
## 1. OOP kya hota hai?
OOP ka matlab hai **Object-Oriented Programming**. Ye aik aisa programming style hai jisme hum apni coding ko **objects aur classes** ki madad se organize karte hain – functions aur logic ki bajaye.  

Ek **class** hoti hai blueprint (ya design) aur **object** uska real version.  
Jaise agar aap aik car simulator bana rahe hain to aap aik `Car` class banaenge, aur har gaari aik `object` hogi jiska apna `color`, `speed`, `model` waghera hoga – aur kaam jaise `accelerate()` ya `brake()` honge.

---

## OOP kyu use karein?

- **Modularity:** Badi problems ko choti-choti cheezon (objects) mein divide karna asaan hota hai.
- **Reusability:** Ek class ko dobara kisi aur code mein bhi use kiya ja sakta hai.
- **Maintainability:** Code easily update ya maintain hota hai kyunke sab kuch proper structure mein hota hai.
- **Scalability:** Asani se naye features add kiye ja sakte hain.
- **Real-world modeling:** OOP real-life cheezon jaise hota hai – is liye samajhna aur design karna easy hota hai.

---

## 🔑 OOP ke 4 Basic Principles

### 1. Encapsulation

Encapsulation ka matlab hai data aur methods ko aik class mein bundle karna, aur kuch cheezon ko hidden rakhna.

**Example:**

```python
class Car:
    def __init__(self, color, speed):
        self.color = color  # Public
        self.__speed = speed  # Private

    def accelerate(self):
        self.__speed += 10

    def get_speed(self):
        return self.__speed
````

**Test Code:**

```python
car = Car("red", 0)
print("Current speed: ", car.get_speed())

for i in range(10):
    car.accelerate()

print("Speed after acceleration: ", car.get_speed())
```

---

### 2. Abstraction

Abstraction ka matlab hai user ko sirf zaroori cheezein dikhana, aur internal details chhupa lena.

**Example:**

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
        self._engine_status = False
        self._idling_time = 0
        self._traffic_signal = None

    def drive(self):
        if self._engine_status and self._traffic_signal == "green":
            print(f"You are driving a {self.brand} {self.model}.")
        elif self._traffic_signal == "red":
            print(f"You stopped at the red light in a {self.brand} {self.model}.")
            self._idle_stop_engine()
        else:
            self._start_engine()
            print(f"You are driving a {self.brand} {self.model}.")

    def stop(self):
        if self._engine_status:
            print(f"You stopped the {self.brand} {self.model}.")
            self._idle_stop_engine()
        else:
            print(f"The {self.brand} {self.model} is already stopped.")

    def set_traffic_signal(self, signal):
        self._traffic_signal = signal
        if signal == "red":
            print(f"Traffic signal turned red. You stopped in a {self.brand} {self.model}.")
            self._idle_stop_engine()
        elif signal == "green":
            print(f"Traffic signal turned green. You can drive your {self.brand} {self.model}.")
            if not self._engine_status:
                self._start_engine()

    def _start_engine(self):
        self._engine_status = True
        self._idling_time = 0
        print("Engine started.")

    def _idle_stop_engine(self):
        import time
        print("Engine is idling...")
        for i in range(5):
            print(f"Idling time: {i+1} seconds")
            time.sleep(1)
            self._idling_time += 1
        if self._idling_time >= 5:
            self._engine_status = False
            print("Engine stopped (idle stop) to save fuel.")
```

**Abstraction Ka Faida:**

* User sirf `drive()`, `stop()` aur `set_traffic_signal()` use karta hai.
* `engine start/stop`, `idling logic` sab andar hidden hai.

---

### ❗ Note on Private Methods

```python
class ShoppingMall:
  def basement_parking():
    my_car = Car("Toyota", "Camry")
    my_car._start_engine()  # Ye internal method hai
```

In Python, underscore `_` se start hone wale methods private hote hain. Technically call kar sakte ho, lekin **recommended nahi** hai.

**Kyunkay:**

* **Encapsulation** break hoti hai
* **Abstraction** ka purpose fail ho jata hai
* **Future updates** se issues ho sakte hain

---

### 3. Inheritance

Inheritance ka matlab hai aik class doosri class ki properties aur methods ko inherit karti hai.

```python
class BMW(Car):
  def __init__(self, brand, model):
    super().__init__(brand, model)

  def start_engine(self):
    self._start_engine()

  def _start_engine(self):
    print("BMW engine started")
```

```python
bmw = BMW("BMW", "i5")
bmw.start_engine()
```

Output:

```
BMW engine started
```

Yahan `BMW` class ne `Car` ki functionality inherit ki aur `_start_engine()` method override kiya.

---

## 🎉 Conclusion

OOP se aapka code:

* Zyada organized hota hai
* Asani se samajh aata hai
* Reusable hota hai
* Real-world jaisa lagta hai

Happy Coding! 💻🚗✨

