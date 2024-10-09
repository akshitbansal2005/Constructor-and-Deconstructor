# Constructor-and-Deconstructor
### Experiment_12

#### Contents
- Aim
- Software Used
- Theory
  - Definition
  - Properties
  - Advantages
  - Types
  - Algorithms
- Conclusion

---

### **Aim:**
To study and implement Constructors and Destructors in C++.

---

### **Software Used:**
- VS Code  
- Dev C++

---

### **Theory:**

#### **Constructors Definition:**
A constructor in C++ is a special method that is invoked automatically when an object of a class is created. It is used to initialize the data members of objects and has the same name as the class. Since it provides initial values for the object, it is referred to as a constructor.

##### **Syntax of Constructors in C++:**
```cpp
className() {
   // constructor body
}
```

#### **Properties of Constructors:**
- The name of the constructor is the same as the class name.
- Constructors are typically declared in the public section of the class, though they can also be private.
- Constructors do not return values and do not have a return type.
- They are called automatically when an object is created.
- Constructors can be overloaded, allowing multiple constructors with different parameter lists.
- If no constructor is defined, the compiler provides a default constructor that initializes data members to default values.
- A special constructor, known as a copy constructor, initializes an object using another object of the same class (usually for deep copying).
- Constructors can take parameters for custom initialization of objects.

---

### **Advantages of Constructors:**
- **Automatic Initialization:** Ensures that objects are initialized to valid states.
- **Encapsulation of Initialization Logic:** Centralizes initialization logic, making code cleaner and more maintainable.
- **Support for Overloading:** Flexibility in object creation by overloading constructors.
- **Complex Object Initialization:** Handles dynamic memory allocation and complex object setups.
- **Consistency:** Ensures objects are initialized in a well-defined state.
- **Resource Management:** Handles resource allocation (memory, file handles) upon object creation.
- **Class Hierarchy Compatibility:** Inherited class constructors are called automatically in the proper sequence.
- **Avoiding Redundant Code:** Centralizes initialization, avoiding repetitive code in various parts of the program.

---

### **Types of Constructors:**

1. **Default Constructor:**
   A constructor with no parameters, automatically provided by the compiler if not defined.
   ```cpp
   className() {
      // constructor body
   }
   ```

2. **Parameterized Constructor:**
   A constructor that accepts parameters, allowing custom object initialization.
   ```cpp
   className(parameters...) {
      // constructor body
   }
   ```

3. **Copy Constructor:**
   A constructor that initializes a new object using an existing object of the same class.
   ```cpp
   className(const className &obj) {
      // constructor body
   }
   ```

---

### **Algorithms:**

#### **Algorithm for Date Class:**
1. Define `Date` class with members: `int d` (day), `int m` (month), `int y` (year).
2. Create a constructor `Date()` that initializes `d`, `m`, and `y`.
3. Create a method `display()` to print the date.
4. In `main()`, create a `Date` object. The constructor will be called automatically, and the `display()` method will show the initialized date.

#### **Algorithm for Student Class:**
1. Define `Student` class with members: `int rno` (roll number), `char name[50]` (name), `double fee` (fee).
2. Create a constructor `Student()` that prompts for input and initializes the members.
3. Create a method `display()` to print the details.
4. In `main()`, create a `Student` object, and call `display()` to print the initialized values.

#### **Algorithm for Construct Class (Parameterized Constructor):**
1. Define `Construct` class with members: `int a`, `int b`.
2. Create a constructor `Construct(int m, int n)` to initialize `a` and `b`.
3. Create a method `display()` to print the values of `a` and `b`.
4. In `main()`, create a `Construct` object with parameters, and call `display()` to print the initialized values.

#### **Algorithm for Wall Class (Copy Constructor):**
1. Define `Wall` class with members: `double length`, `double height`.
2. Create a constructor `Wall(double len, double hgt)` to initialize `length` and `height`.
3. Create a copy constructor `Wall(const Wall &obj)` to copy another `Wall` object.
4. Create a method `calculateArea()` to calculate the wall's area.
5. In `main()`, create a `Wall` object using the parameterized constructor, then create another using the copy constructor. Call `calculateArea()` for both.

#### **Algorithm for Object Count in Student Class:**
1. Declare a global variable `count` initialized to `0` to track the number of objects.
2. In `Student` class, increment `count` in the constructor and decrement in the destructor.
3. Create several objects in `main()` to observe the count's behavior, especially when objects go out of scope.

---

### **Conclusion:**
This experiment demonstrated the use of constructors and destructors in C++. Various types of constructors, including default, parameterized, and copy constructors, were explored, along with their application in different scenarios.

---
