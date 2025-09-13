# Python OOP Assignment 🏗️🎭

This project demonstrates **Object-Oriented Programming (OOP)** concepts in Python using two activities:

1. **Assignment 1: Design Your Own Class**  
   - Create a `Smartphone` class with attributes and methods.  
   - Use constructors (`__init__`) to initialize unique objects.  
   - Apply **inheritance** from a base `Device` class.  
   - Demonstrates **encapsulation** and class behaviors.  

2. **Activity 2: Polymorphism Challenge**  
   - Create multiple vehicle classes (`Car`, `Plane`, `Boat`) with the same method `move()`.  
   - Show how polymorphism allows different behaviors for the same method.  

---

## Assignment 1: Smartphone Example 📱

### Code Summary
```python
# Base class
class Device:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def info(self):
        return f"{self.brand} {self.model}"

# Child class
class Smartphone(Device):
    def __init__(self, brand, model, storage, battery):
        super().__init__(brand, model)
        self.storage = storage
        self.battery = battery

    def call(self, number):
        print(f"📞 Calling {number} from {self.info()}...")

    def charge(self, percent):
        self.battery = min(100, self.battery + percent)
        print(f"🔋 {self.info()} charged to {self.battery}%")

    def phone_info(self):
        return f"{self.info()} | Storage: {self.storage}GB | Battery: {self.battery}%"
