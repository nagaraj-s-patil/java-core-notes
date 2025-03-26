# Chapter 1: Introduction  

## What is Java?  
Java is an **object-oriented** programming language similar to C++, but easier and more advanced. It is **free to access** and runs on **all platforms**.  

## Key Features:  
- **Write Once, Run Anywhere (WORA)**  
- **Platform Independent**  
- **Robust, Scalable, and Portable**  
- **Supports Integration with Technologies** like Spring, Node.js, Android, Hadoop, J2EE  
- **Promotes Testing & CI/CD** using tools like Selenium  

## History of Java:  
- Developed by **James Gosling** and team at **Sun Microsystems** in the early 1990s  
- Initially called **Project Oak**  
- Renamed **Java** after an espresso bean  
- **First release:** Java 1.0 in **1995**  
- **Oracle acquired Sun Microsystems** on **January 27, 2010**  
- The latest version (as of 2019) is **Java 12**  

## Real-World Example:  
Java is like a universal remote control, working on any device without modification.

# Creating a Markdown file with the Features of Java content

java_features_content = """\
# Features of Java

## 1. Simple  
Java removes complexities like pointers and operator overloading seen in C++, making it easier to use.  

## 2. Portable  
Java is **platform-independent**, meaning applications written on one platform can be easily moved to another.  

## 3. Object-Oriented  
Everything in Java is treated as an **object** with state and behavior, allowing for modular and reusable code.  

## 4. Dynamic  
Java supports **dynamic memory allocation**, reducing memory wastage and improving performance.  

## 5. Robust  
Java has strong **memory management** and eliminates errors through compile-time and runtime checking.  

## 6. Interpreted  
Java is compiled into **bytecode**, which is interpreted by the Java Runtime Environment (JRE).  

## 7. Multithreaded  
Java allows multiple **threads** to run concurrently, making applications more interactive and responsive.  

## 8. Platform Independent  
Java code is compiled into **bytecode**, which can run on any system with a Java Virtual Machine (JVM).  
Thus, Java follows the principle: **"Write Once, Run Anywhere"**.  

## 9. Secure  
Java has built-in **security features** like static type-checking and runtime security management to prevent unauthorized access.  
"""

# Creating a Markdown file with the Software and Program content

software_content = """\
# 1.1 Software  

Software is an **automated version** of manual work. It provides **solutions** for real-world problems.  
Software typically contains **Programs, UI Components, and Storage Components**.  

## 1.1.1 Program  
A **program** is a set of instructions given to **hardware or a platform** for execution.  

### Platform  
A **platform** is a combination of a **processor** and an **operating system**.  
**Examples:** Windows, Linux, Android, etc.  

## Java and Platform Independence  
Java is **platform-independent**, meaning that applications or programs developed using Java can work on different platforms without modification.  
"""

# Save content to a Markdown file
software_file_path = "/mnt/data/Java_Software.md"
with open(software_file_path, "w") as file:
    file.write(software_content)

# Provide the file path for download
software_file_path
 ![image](https://github.com/user-attachments/assets/8428f8e8-04ce-4079-b08f-d1060ae75bfb)

 # 1.3 Object Orientation  

## Object  
An **Object** is a real-world physical entity.  
Anything with a physical presence or appearance is considered an **Object**.  
An Object has **States** and **Behavior**.  

### 1.3.1 State  
The **State** of an Object represents its properties, features, or data that describe what an Object is.  

**State → Information / Data → Variable (Data-Member)**  

### 1.3.2 Behavior  
The **Behavior** of an Object represents the actions or work performed by an Object.  

**Behavior → Action / Work → Method**  

#### Example: **Mobile Object**  
- **States**: Model, Color, Price, RAM, Storage, etc.  
- **Behavior**: `call()`, `sendSms()`  

In programming, the **State** of an Object is called a **Variable (Data Member)**, and the **Behavior** is called a **Method**.  

---

# 1.4 Class  

A **Class** is a logical entity or blueprint used to create multiple Objects.  

- We **cannot** create an Object without a Class.  
- **Step 1**: Create a Class → **Step 2**: Create Objects from it.  
- Multiple Objects created using the same Class are called **Similar Objects** or **Identical Objects**.  
- Each Object works **independently**; modifying or destroying one Object does not affect another.  

# 1.5 Keywords or Reserved Words  

Java has predefined **keywords** (also called **reserved words**) that have special meanings and cannot be used as identifiers.  

### Common Java Keywords:  
`class`, `interface`, `abstract`, `import`, `package`, `static`, `public`, `private`, `protected`, `default`, `super`,  
`this`, `extends`, `implements`, `try`, `catch`, `finally`, `break`, `continue`, `int`, `double`, `float`, `if`, `else`,  
`switch`, etc.  

### Example for `class`:  

#### **Bike.java**  
```java
class Bike {  
}  
```
# 1.6 Identifiers  

An **Identifier** is a name used to identify a class, method, variable, or other elements in Java.  

### **Key Point:**  
- A **class name** is an **Identifier** because it is used to identify a class.  

### **Example:**  
```java
class Bike {  
}
```

![image](https://github.com/user-attachments/assets/ed7d5df4-e451-4bb4-8bef-8a1843469097)
# Good Practice / Coding Standards / Naming Convention for Class  

### **Class Naming Rules:**  
- **Use Camel Case** → The first letter of each word should be capitalized.  
- **Use Singular Form** → Class names should be singular.  
- **Use Nouns** → Class names should represent an entity or object.  

### **Examples:**  
✅ ```class Student { }``` (Correct)  
✅ `class EmployeeDetails { }` (Correct)  
❌ `class students { }` (Incorrect - Plural)  
❌ `class emp_details { }` (Incorrect - Not Camel Case)  
# Example  

```java
class Pen {  
}  

class BlackDog {  
}  
```

# 1.7 Association (Has-A Relationship)  

**Association** is an Object-Oriented concept also known as **Has-A Relationship**.  
It represents the process of one or multiple objects being associated with another object.  

## **Types of Association:**  
1. **Composition**  
2. **Aggregation**  

---

## **1.7.1 Composition**  

**Composition** is a special form of association where the associated object **cannot exist independently** without the owner object.  

- If the **owner object is destroyed**, the **associated object is also destroyed**.  
- This is known as a **Strong Has-A Relationship**.  

### **Example:**  

```java
class Engine {  
    void start() {  
        System.out.println("Engine started");  
    }  
}  

class Car {  
    private Engine engine;  

    Car() {  
        engine = new Engine();  // Engine object is created inside Car  
    }  

    void startCar() {  
        engine.start();  
        System.out.println("Car started");  
    }  
}  

public class Main {  
    public static void main(String[] args) {  
        Car myCar = new Car();  
        myCar.startCar();  
    }  
}  
```
![image](https://github.com/user-attachments/assets/8ca93949-0b91-4093-aa1f-149dcc906857)

# 1.7.2 Aggregation  

**Aggregation** is a special form of association where the associated object **can exist independently** even if the owner object is destroyed.  

- If the **owner object is destroyed**, the **associated object still exists**.  
- This is called a **Weak Has-A Relationship**.  

### **Example:**  

```java
class College {  
    String name;  

    College(String name) {  
        this.name = name;  
    }  

    void displayCollege() {  
        System.out.println("College: " + name);  
    }  
}  

class Student {  
    String studentName;  
    College college;  // Aggregation (Student has a College)  

    Student(String studentName, College college) {  
        this.studentName = studentName;  
        this.college = college;  
    }  

    void displayStudent() {  
        System.out.println("Student: " + studentName);  
        college.displayCollege();  
    }  
}  

public class Main {  
    public static void main(String[] args) {  
        College college = new College("ABC University");  
        Student student = new Student("John", college);  
        student.displayStudent();  
    }  
}  
![image](https://github.com/user-attachments/assets/9c49f910-14f6-4af9-9a4d-2acc5ad48e31)

# 1.8 Java Compilation  

Java compilation happens in **2 steps**:  

1. **Check Syntax** – The compiler checks if the program is written correctly.  
2. **Generate Bytecode** – If there are no errors, the compiler creates a **.class file (bytecode)**.  

### **Important Note:**  
- If there are **syntax errors**, the compiler **does not** generate bytecode.  
- Instead, it shows an **error message**.  

### **Example:**  

✅ **Correct Program (Compiles Successfully)**  
```java
class Hello {  
    public static void main(String[] args) {  
        System.out.println("Hello, Java!");  
    }  
}  
```
![image](https://github.com/user-attachments/assets/1c6d0221-2aca-40e8-a8c9-eecc3853ef05)

# 1.9 WORA Architecture (Write Once, Run Anywhere)  


![image](https://github.com/user-attachments/assets/a436aa5c-ca2f-492f-98d2-0634efee6856)


Java programs can run on **any platform** as long as the platform has **JVM (Java Virtual Machine)**.  

### **How It Works?**  
1. **Java Code → Compiled → Bytecode (.class file)**  
2. The **JVM** interprets the **bytecode** and runs the program on any system with JVM.  

### **Why is Java WORA?**  
- **Write Once, Run Anywhere (WORA)** means Java code written on one system **can run on any system** with JVM **without modification**.  
- This is possible because Java **does not compile directly to machine code**, but instead generates **bytecode**, which JVM executes.  

### **Comparison with C & C++**  
| Feature         | C/C++                            | Java (WORA)                     |
|---------------|--------------------------------|--------------------------------|
| Compilation   | Converts code into **machine-specific binary** | Converts code into **bytecode** |
| Portability   | **Not portable** (recompilation needed for different systems) | **Portable** (runs on any JVM) |
| Execution     | **Directly executed by CPU**  | **Interpreted by JVM** |

### **Example:**  
1. Write and compile Java code on **Windows**  
2. Run the same **bytecode (.class file)** on **Linux** or **Mac** without changes  

### **Conclusion:**  
Java achieves **platform independence** because of the JVM, making it truly **Write Once, Run Anywhere**.  

# JVM, JRE, and JDK  

## **1. JVM (Java Virtual Machine)**  
- JVM is an **abstract machine** (it does not physically exist).  
- It provides a **runtime environment** to execute Java **bytecode**.  
- JVM can also run programs written in other languages if compiled to bytecode.  
- **Java is platform-independent, but JVM is platform-dependent.**  

### **JVM Performs 4 Main Tasks:**  
1. **Loads code**  
2. **Verifies code**  
3. **Executes code**  
4. **Provides a runtime environment**  

---

## **2. JRE (Java Runtime Environment)**  
- JRE stands for **Java Runtime Environment**.  
- It provides the **runtime environment** required to run Java applications.  
- JRE = **JVM + Libraries + Other Files**  
- JRE **physically exists**.  

### **Key Point:**  
- **JRE does NOT contain development tools** like a compiler. It is used **only to run Java applications**.  

---

## **3. JDK (Java Development Kit)**  
- JDK stands for **Java Development Kit**.  
- It is used for **developing** Java applications.  
- JDK = **JRE + Development Tools**  

### **JDK Includes:**  
- **JVM** (Java Virtual Machine)  
- **JRE** (Java Runtime Environment)  
- **Compiler (`javac`)** – Converts Java code into bytecode  
- **Interpreter (`java`)** – Runs Java programs  
- **Jar Tool (`jar`)** – Used to package Java applications  
- **Documentation Generator (`Javadoc`)**  

### **JDK Editions by Oracle:**  
1. **Java SE (Standard Edition)** – General-purpose applications  
2. **Java EE (Enterprise Edition)** – Web & enterprise applications  
3. **Java ME (Micro Edition)** – Mobile & embedded systems  

---

## **Comparison Table**  

| Feature | JVM | JRE | JDK |
|---------|-----|-----|-----|
| Purpose | Runs Java bytecode | Provides runtime environment | Develops and runs Java applications |
| Contains | Just the Java Virtual Machine | JVM + Libraries | JRE + Development Tools |
| Required for | Running Java programs | Running Java programs | Developing and Running Java programs |
| Includes Compiler? | ❌ No | ❌ No | ✅ Yes |

---

### **Conclusion:**  
- **JVM** runs Java programs.  
- **JRE** provides the required libraries and files.  
- **JDK** is needed for developing Java applications.  




