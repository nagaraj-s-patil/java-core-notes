      <h1> *INSTANCE METHOD***</h1>
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

Here is your content in **Markdown (.md) format**, keeping it **easy, simple, and unchanged**:  

```md
# **Methods in Java**  

---

## **Example: Returning Objects from Methods**  
```java
class Money {  
}  

class Atm {  
    Money dispense() {  
        Money m = new Money();  
        return m;  
    }  
}  
```

---

## **Key Points about Methods:**  
- A **method executes only when invoked**.  
- A **method can be invoked multiple times**.  
- The **main method is not required for compilation**, but **it is required for execution**.  

---

## **Example: Method Invocation**  
```java
class Pen {  
    int price = 40;  
    String color = "Black";  

    void write() {  
        System.out.println("Pen writes");  
    }  

    public static void main(String[] args) {  
        System.out.println("Main starts");  
        Pen p = new Pen();  
        p.write(); // Invoking a method  
        p.write(); // Invoking a method  
        System.out.println("Main ends");  
    }  
}
# **Methods in Java**  

---

## **Example 1: Dance Class with Method Invocation**  
```java
class Dance {  
    int price = 40;  
    String color = "Black";  

    public static void main(String[] args) {  
        System.out.println("Main starts");  
        Dance d = new Dance();  
        d.dance(); // Invoking Method  
        d.dance(); // Invoking Method  
        System.out.println("Main ends");  
    }  

    void dance() {  
        String name = "Jackson";  
        System.out.println(name + " dances");  
    }  
}  
```

---

## **Example 2: Student Class with Multiple Methods**  
```java
class Student {  
    String name = "Arya";  
    String qualification = "B.E";  

    void study() {  
        System.out.println(name + " reads every day");  
    }  

    void sleep() {  
        System.out.println(name + " sleeps 8 hours");  
    }  

    public static void main(String[] args) {  
        System.out.println("Main starts");  
        Student s = new Student();  
        s.study();  
        s.sleep();  
        System.out.println("Main ends");  
    }  
}  
```



