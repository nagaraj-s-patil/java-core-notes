
# **Methods in Java**  

A **method** is a collection of statements that **perform a specific task** and **return a result** to the caller.  
- A method can **return a value** or perform a task **without returning anything**.  
- Methods **save time** and help **reuse code** without retyping.  
- In Java, every method **must be part of a class**, unlike C, C++, and Python.  

---

## **Syntax:**  
```java
return_type MethodName() {  
    // Body of the Method / Logic / Implementation  
    return statement;  
}  
```

---

## **Examples:**  
### **Basic Method Examples**  
```java
class Horse {  
    void run() {  
        // Method logic  
    }  
}  
```
```java
class Tap {  
    Water open() {  
        return new Water();  
    }  
}  

class Water {  
}  
```
```java
class Conductor {  
    Ticket issue() {  
        return new Ticket();  
    }  
}  

class Ticket {  
}  
```
```java
class Shop {  
    Product sell() {  
        return new Product();  
    }  
}  

class Product {  
}  
```
```java
class Atm {  
    Money dispense() {  
        return new Money();  
    }  
}  

class Money {  
}  
```

---

# **4.1 Rules for Methods**  
- A method **must have either a return type or void**, but not both.  
- A **void method** cannot return any data.  
- A method **can have only one return type** and **one return statement**.  
- The **return type and returned value must match**.  
- The **return statement must be the last executable statement** in a method.  

---

# **Examples of Return Types**  
```java
int meth() {  
    return 40;  
}  
```
```java
void meth() {  
    return;  
}  
```
```java
String meth() {  
    String s = "Beast";  
    return s;  
}  
```
```java
double m1() {  
    return 10;  
}  
```
```java
int m2() {  
    return 30;  
}  
```
```java
boolean m1() {  
    return true;  
}  
```
```java
int m2() {  
    return 87;  
    System.out.println("Hello");  // Error: Unreachable statement  
}  
```

---

## **Example: Returning Objects from Methods**  
```java
class Ticket {  
}  

class Conductor {  
    Ticket issue() {  
        Ticket t = new Ticket();  
        return t;  
    }  
}  
```
- Here, **`t` is a local reference variable**.  

```java
class Product {  
}  

class Shop {  
    Product sell() {  
        Product p = new Product();  
        return p;  
    }  
}  
```
```  

This Markdown file keeps your **original content, examples, and format** unchanged while making it **easy and simple**. Let me know if you need any modifications!
