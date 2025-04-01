
1. **What is a package?**  
   A **package** is a namespace that organizes a set of related classes and interfaces in Java.

2. **How to import packages? (Syntax example)**  
   ```java
   import packageName.ClassName;
   ```

3. **Purpose of import.**  
   The **import** statement allows access to classes and interfaces from other packages in the current class.

4. **What is an interface?**  
   An **interface** is a reference type in Java, with abstract methods that a class can implement.

5. **Can you implement multiple interfaces? (Yes, with example)**  
   Yes, a class can implement multiple interfaces:  
   ```java
   interface A {
       void methodA();
   }
   interface B {
       void methodB();
   }
   class C implements A, B {
       public void methodA() { System.out.println("Method A"); }
       public void methodB() { System.out.println("Method B"); }
   }
   ```

6. **What is an abstract class?**  
   An **abstract class** is a class that cannot be instantiated and may have abstract methods that need to be implemented by subclasses.

7. **Default Constructor vs Parameterized Constructor**  
   - **Default Constructor**: A constructor that **does not take any parameters** and initializes objects with default values.
   - **Parameterized Constructor**: A constructor that **takes parameters** to initialize an object with specific values.
   
   Example of **Default Constructor**:
   ```java
   class Car {
       int speed;
       String color;

       // Default constructor
       Car() {
           speed = 0;
           color = "Unknown";
       }
   }
   ```
   
   Example of **Parameterized Constructor**:
   ```java
   class Car {
       int speed;
       String color;

       // Parameterized constructor
       Car(int speed, String color) {
           this.speed = speed;
           this.color = color;
       }
   }
   ```

8. **Static Method**  
   A **static method** is a method that belongs to the class rather than instances of the class, and can be called without creating an object.
   ```java
   class Utility {
       static void display() {
           System.out.println("Static Method Called");
       }
   }
   Utility.display();  // No object creation needed
   ```

9. **Purpose of `final` keyword**  
   The `final` keyword is used to **restrict modification**: it can be applied to variables (to make them constants), methods (to prevent overriding), and classes (to prevent inheritance).

10. **Using `super` Keyword with Methods**  
    The `super` keyword is used to call a **parent class method** from a child class, especially when the method is overridden.
    ```java
    class Parent {
        void display() {
            System.out.println("Parent Method");
        }
    }
    class Child extends Parent {
        void display() {
            super.display();  // Calls Parent's method
            System.out.println("Child Method");
        }
    }
    ```

11. **Constructor Chaining**  
    Constructor chaining is the process of **calling one constructor from another** in the same class or between a parent and child class using `this()` or `super()`.

    - **Within the Same Class**:  
      ```java
      class A {
          A() {  
              this(10);  // Calls parameterized constructor
              System.out.println("Default Constructor");
          }
          A(int x) {  
              System.out.println("Parameterized Constructor: " + x);
          }
      }
      ```

    - **Between Parent and Child Class**:  
      ```java
      class Parent {
          Parent() {  
              System.out.println("Parent Constructor");
          }
      }
      class Child extends Parent {
          Child() {  
              super();  // Calls Parent class constructor
              System.out.println("Child Constructor");
          }
      }
      ```

12. **Class Loader**  
    A **ClassLoader** in Java is responsible for loading class files into memory during runtime. There are three main types of ClassLoaders:  
    - **Bootstrap ClassLoader**  
    - **Extension ClassLoader**  
    - **Application ClassLoader**

13. **Heap, Class Area, Stack, Method Area, Native Area**  
    - **Heap**: Objects are created here.  
    - **Class Area**: Stores class definitions and static variables.  
    - **Stack**: Stores method calls and local variables.  
    - **Method Area**: Stores method definitions and runtime constants.  
    - **Native Area**: Used for native code (JNI) execution.

14. **Purpose of `static` Keyword**  
    The `static` keyword is used for **memory management** and allows members to belong to the **class** rather than individual objects.

15. **Difference Between Method Execution and Method Implementation**  
    - **Method Execution**: The process of running a method, where the JVM handles the execution stack.  
    - **Method Implementation**: The actual code inside the method.

16. **Constructor**  
    A **constructor** is a special method used to initialize objects, automatically called when an instance of a class is created.

17. **Abstraction**  
    Abstraction in Java is achieved by **abstract classes** and **interfaces** to hide implementation details and show only essential features.

18. **Final vs Parameterized Constructors**  
    - **Final Constructor**: Once assigned a value, the variable cannot be changed.  
    - **Parameterized Constructor**: A constructor that takes parameters to initialize an object with specific values at the time of creation.

---
