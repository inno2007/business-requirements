# UML Class Diagrams and Object-Oriented Relationships

Class diagrams are a core component of the Unified Modeling Language (UML). They allow developers and analysts to model the structure of an object-oriented system, showing the attributes, methods, and relationships between classes.

---

## 1. Key Concepts in Object-Oriented Design

| Concept     | Description |
|-------------|-------------|
| **Class**   | A blueprint or template used to create objects. |
| **Object**  | An instance of a class. Represents a real-world item (e.g., a Student or Product). |
| **Attribute** | Properties that describe the object (e.g., name, address). |
| **Method** | Actions that an object can perform (e.g., placeOrder()). |

Example:  
A `Customer` class may have attributes like `name`, `email`, and `phoneNumber`, and methods like `placeOrder()` and `cancelOrder()`.

---

## 2. UML Class Diagram

A class diagram includes:

- **Class Name**
- **Attributes**
- **Methods**
- **Relationships with other classes**

Notation:
```
+---------------------+
|      ClassName      |
+---------------------+
| - attribute1        |
| - attribute2        |
+---------------------+
| + method1()         |
| + method2()         |
+---------------------+
```

- `-` (minus) = private
- `+` (plus) = public

---

## 3. Class Relationships

| Type         | Description |
|--------------|-------------|
| **Association** | A basic connection between two classes (e.g., Customer places Order). |
| **Aggregation** | "Has-a" relationship where the part can exist independently (e.g., Department has Employees). |
| **Composition** | Stronger "part-of" relationship; parts die with the whole (e.g., House has Rooms). |
| **Generalization** | "Is-a" relationship. One class is a subtype of another (e.g., Car is a Vehicle). |
| **Dependency** | One class temporarily uses another (e.g., generates a report). |

### Association
- The simplest and most general relationship.
- Can be **unidirectional** or **bidirectional**.

### Aggregation
- Whole-part relationship.
- Parts can exist independently.
- Represented with a white diamond.

### Composition
- Whole-part relationship with stronger dependency.
- If the whole is deleted, so are its parts.
- Represented with a black diamond.

### Generalization / Inheritance
- The subclass inherits attributes and behaviors from the superclass.
- Encourages reusability.

Example:  
A `Vehicle` superclass can be generalized into `Car`, `Truck`, or `Motorcycle` subclasses.

---

## 4. Reflexive Associations

- An object in a class may relate to another object in the same class.
- Example: An `Employee` manages another `Employee`.

---

## 5. Collection

- Represents a group of objects.
- The group retains identity even as members change (weak association).
- Example: A `Library` contains many `Books`.

---

## 6. Summary

| Concept         | Description |
|------------------|-------------|
| Class Diagram    | Visual map of classes, attributes, methods |
| Association      | Basic link between two classes |
| Aggregation      | Whole-part, independent parts |
| Composition      | Whole-part, dependent parts |
| Generalization   | Inheritance from superclass to subclass |
| Reflexive Link   | Class linked to itself (e.g., manager relationship) |

