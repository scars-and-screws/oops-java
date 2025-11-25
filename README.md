# OOP in Java - Learning Repository

A hands-on learning repository for understanding **Object-Oriented Programming (OOP)** concepts in Java.

---

## What is Object-Oriented Programming (OOP)?

**Object-Oriented Programming (OOP)** is a programming paradigm that organizes software design around **objects** rather than functions and logic. An object is a data field that has unique attributes and behavior.

In OOP, we model real-world entities as objects in our code. For example, a `Pen` has attributes like `color` and `type`, and behaviors like `write()`. This approach makes code more modular, reusable, and easier to maintain.

---

## The Four Pillars of OOP

### 1. Encapsulation

Encapsulation is the bundling of data (attributes) and methods (functions) that operate on the data into a single unit called a **class**. It restricts direct access to some of an object's components and protects the internal state of an object.

**Example from this repository:**
```java
class Pen {
    String color;
    String type; // ball, gel

    public void write() {
        System.out.println("Writing something...");
    }

    public void printColor() {
        System.out.println(this.color);
    }
}
```

Here, the `Pen` class encapsulates the properties (`color`, `type`) and behaviors (`write()`, `printColor()`) of a pen object.

---

### 2. Inheritance

Inheritance allows a new class to **inherit** properties and methods from an existing class. The existing class is called the **parent/super class**, and the new class is called the **child/sub class**. This promotes code reusability.

**Example from this repository:**
```java
class Shape {
    public void area() {
        System.out.println("displays area");
    }
}

class Triangle extends Shape {
    public void area(int l, int h) {
        System.out.println((1 / 2) * l * h);
    }
}

class EquilateralTriangle extends Triangle {
    public void area(int l, int h) {
        System.out.println((1 / 2) * l * h);
    }
}
```

- `Triangle` inherits from `Shape`
- `EquilateralTriangle` inherits from `Triangle` (Multi-level Inheritance)

---

### 3. Polymorphism

Polymorphism means "many forms". It allows objects to be treated as instances of their parent class. There are two types:

- **Compile-time Polymorphism (Method Overloading)**: Same method name with different parameters
- **Runtime Polymorphism (Method Overriding)**: Subclass provides a specific implementation of a method already defined in its parent class

**Method Overloading Example:**
```java
class Student {
    String name;
    int age;

    public void printInfo(String name) {
        System.out.println(name);
    }

    public void printInfo(int age) {
        System.out.println(age);
    }

    public void printInfo(String name, int age) {
        System.out.println(name + " " + age);
    }
}
```

The `printInfo` method is overloaded with three different parameter combinations.

---

### 4. Abstraction

Abstraction is the concept of hiding complex implementation details and showing only the necessary features of an object. In Java, this is achieved through **abstract classes** and **interfaces**.

While not explicitly shown in this repository, abstraction helps in:
- Reducing complexity
- Isolating the impact of changes
- Focusing on what an object does rather than how it does it

---

## Quick Reference: OOP Concepts in This Repository

| Concept | Example in Code |
|---------|-----------------|
| Class & Object | `Pen`, `Student`, `Shape` classes |
| Encapsulation | Attributes and methods bundled in classes |
| Inheritance | `Triangle extends Shape` |
| Method Overloading | Multiple `printInfo()` methods in `Student` |
| Method Overriding | `area()` method in `Triangle` and `EquilateralTriangle` |

---

## How to Run

1. Compile the Java file:
   ```bash
   javac oops.java
   ```

2. Run the compiled class:
   ```bash
   java oops
   ```

---

## Learning Resources

- [Oracle Java Documentation](https://docs.oracle.com/javase/tutorial/java/concepts/)
- [W3Schools Java OOP](https://www.w3schools.com/java/java_oop.asp)
- [GeeksforGeeks OOP Concepts](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)

---

## Contributing

Feel free to add more examples, fix bugs, or enhance the documentation!

---

**Happy Learning! 🚀**
