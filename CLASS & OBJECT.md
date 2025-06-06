


# **Class & Object in Java**  

## **1. Class**  
- A **class** is a **blueprint** used to create multiple objects.  
- **Objects cannot be created without a class**.  
- Objects created from the **same class** are called **similar or identical objects**.  
- Each object works **independently** (modifying one object does not affect another).  

### **Example of a Class:**  
```java
class Movie {  
    Movie() {  // Constructor (same name as class)  
        System.out.println("Movie Object Created");  
    }  
}
```

---

## **2. Object**  
- An **object** is a **real-world physical entity**.  
- Anything with **physical presence** is an object.  
- Objects have **state (data) and behavior (methods)**.  

### **Example of an Object:**  
```java
class Product {  
    Product() {  // Constructor  
        System.out.println("Product Object Created");  
    }  
}

public class Main {  
    public static void main(String[] args) {  
        Product p1 = new Product();  // Object creation  
    }  
}  
```
**Output:**  
```
Product Object Created
```

---

## **3. Memory Management in Java**  
- **Objects are stored in Heap Memory**.  
- **JVM manages memory allocation and deallocation automatically**.  
- Objects are created in **heap memory** using the `new` keyword.  

### **Example:**  
```java
Product p1 = new Product();  // JVM stores p1 in heap memory
```

### **Object Address:**  
- The memory address of an object is represented in **Hexadecimal format**.  

```java
System.out.println(p1);  // Prints memory address
```

---

## **4. Constructor in Java**  
- After compilation, **Java automatically generates a default constructor**.  
- A **constructor name must be the same as the class name**.  

### **Example of Constructor:**  
```java
class Car {  
    Car() {  // Constructor  
        System.out.println("Car Object Created");  
    }  
}
```

---

## **5. Key Points**  
✅ A **class** is a logical entity (blueprint).  
✅ An **object** is a real-world entity (instance of a class).  
✅ **Memory allocation & deallocation** is handled by JVM.  
✅ **Objects are created in Heap Memory** using the `new` keyword.  
✅ **Constructors have the same name as the class and initialize objects.**  


![image](https://github.com/user-attachments/assets/b7d56ce0-aaae-4eda-9f7a-132cc2b55af6)


# **2.1 Object Reference / Object Address**  

## **What is an Object Reference?**  
- An **Object Reference** stores the **address** of an object in **Heap Memory**.  
- The actual object exists in the **Heap Memory**, while the reference is used to access it.  
- Each object has a **unique memory address**.  

---

## **Heap Memory Representation**  

| Object Name | Memory Address |
|------------|----------------|
| Bike       | 13867C         |
| Car        | 1467FC         |
| Carrot     | 190FFD         |

---

## **Example of Object Reference in Java**  
```java
class Bike {  
    String model;  

    Bike(String model) {  
        this.model = model;  
    }  
}

public class Main {  
    public static void main(String[] args) {  
        Bike b1 = new Bike("Yamaha");  
        Bike b2 = new Bike("Honda");  

        System.out.println(b1);  // Prints memory address of b1  
        System.out.println(b2);  // Prints memory address of b2  
    }  
}  
```
**Output (Example memory addresses):**  
```
Bike@13867C  
Bike@1467FC  
```

---

## **Key Points**  
✅ **Object Reference** stores the **memory address** of an object.  
✅ **Objects are stored in Heap Memory**.  
✅ **Reference variables** are used to access objects.  
✅ JVM automatically assigns a **Hexadecimal memory address** to each object.  



![image](https://github.com/user-attachments/assets/3a6c64c9-ebf6-46b2-a927-919edc47e55f)


# **2.2 States**  

## **What is a State?**  
- The **state of an object** is its **property, information, or data** that describes the object.  
- A **data member** is a **data holder** that **stores** information.  

---

## **Types of Data Members**  
1. **Variable**  
   - Data **changes** over time.  
   - Non-final data members are called **Variables**.  
   
2. **Constant**  
   - Represents a **fixed value**.  
   - Declared using the `final` keyword.  

### **Example:**  
```java
final String name = "Spiders";  // Constant  
String name = "SRK";  // Variable  
```

---

## **States & Behaviors in a Class**  
- Since an **object is derived from a class**, its **states & behaviors** must be **declared inside the class**.  

### **Example:**  
```
class Pen {  
    String color = "green";  // State (Variable)  
    String type = "marker";  // State (Variable)  

    public static void main(String[] args) {  
        Pen p1 = new Pen();  
        Pen C1 = new Pen();  
        Pen C2 = new Pen();  
    }  
}  
```

![image](https://github.com/user-attachments/assets/d7514fb6-89bb-4b8e-886d-4752cb3bbddf)


# **2.3 Object Creation & Direct Initialization**  

### **Example:**  
```java
class Bike {  
    String color = "blue";  
    String name = "R15 V3";  

    Bike b1 = new Bike();  
    Bike b2 = new Bike();  
    Bike b3 = new Bike();  
}  
```

![image](https://github.com/user-attachments/assets/2b363c5b-bee6-40cb-b676-1778105d6084)

---

# **2.4 Object Creation & Initialization using Object Reference**  


![image](https://github.com/user-attachments/assets/b6cc6b0f-82cd-44b5-a4db-7195e5201ab3)

### **Example 1:**  
```java
class Bike {  
    String color = "blue";  
    String name = "R15 V3";  

    Bike b1 = new Bike();  
    Bike b2 = new Bike();  
    Bike b3 = new Bike();  
}  
```

### **Example 2:**  
```java
class Bike {  
    String color;  
    String name;  

    public static void main(String[] args) {  
        Bike b1 = new Bike();  
        b1.color = "Orange";  
        b1.name = "Duke";  

        Bike b2 = new Bike();  
        b2.color = "Red";  
        b2.name = "Pulsar";  

        Bike b3 = new Bike();  
        b3.color = "Blue";  
        b3.name = "R15 V3";  
    }  
}  
```




