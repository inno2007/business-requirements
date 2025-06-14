# Entity-Relationship Diagram (ERD) Modeling

ERDs are used to visualize how entities (tables) in a database relate to one another. They help model data requirements during the early stages of system design.

---

## 1. Core Components

### Entities
- Represent real-world objects or concepts like Customer, Order, Product.
- Use singular nouns.
- Can be physical (e.g., Student) or conceptual (e.g., Payment).

### Attributes
Describe characteristics of an entity.

| Type              | Example / Description                          |
|-------------------|------------------------------------------------|
| **Required**      | Name, email (must be provided)                |
| **Optional**      | Middle name, secondary contact                |
| **Simple**        | Age, weight                                   |
| **Composite**     | Full Name → First Name + Last Name           |
| **Single-valued** | One value only (e.g., Date of Birth)          |
| **Multi-valued**  | Multiple values allowed (e.g., Phone Numbers) |
| **Stored**        | Saved directly in the DB (e.g., birth date)   |
| **Derived**       | Computed from stored data (e.g., age)         |

### Primary Key
- Uniquely identifies a record in an entity.
- Cannot be empty or duplicated.
- Example: `CustomerID`, `OrderID`

---

## 2. Relationships Between Entities

Relationships define how records in one table relate to records in another.

### Types of Relationships:

| Relationship Type | Description                        | Example                              |
|-------------------|------------------------------------|--------------------------------------|
| One-to-One (1:1)  | Each record in A relates to 1 in B | Each employee has one ID card        |
| One-to-Many (1:M) | One in A can relate to many in B   | One customer places many orders      |
| Many-to-Many (M:M)| Many in A relate to many in B      | Students enroll in many courses, and courses have many students |

---

## 3. Cardinality and Modality

Used to show how many instances are involved and whether the relationship is optional or required.

| Concept     | Description                             |
|-------------|-----------------------------------------|
| Cardinality | Maximum: 1 or many (1, *, 0..*, 1..*)    |
| Modality    | Minimum: optional or mandatory (0 or 1) |

### Crow's Foot Notation
- |—| = one  
- |< = many  
- 0..* = zero or many  
- 1..1 = exactly one

Example:
- One customer *can* place many orders → 1:M  
- One service *requires at least one* part → 1:1

---

## 4. Associative Entities (Join Tables)

Used to handle many-to-many relationships and store attributes relevant to the relationship.

### Example:
**Mechanic** ↔ **Service**  
We need to store "hours worked" per mechanic on each service.

Solution:
Create a new entity → `WorkLog`  
Attributes: `MechanicID`, `ServiceID`, `HoursWorked`

### Another Example:
**Employee** ↔ **Course**  
To track certifications:
- Associative entity: `Certificate`
- Attributes: `CertificateNo`, `DateCompleted`, `EmployeeID`, `CourseID`

---

## 5. Summary

| Concept            | Purpose                                           |
|--------------------|---------------------------------------------------|
| Entity             | A thing or object in the system                   |
| Attribute          | A property or field of an entity                  |
| Primary Key        | Uniquely identifies each record                   |
| Relationship       | Links between entities                            |
| Associative Entity | Handles many-to-many and stores relationship data |
| Cardinality        | Max number of linked records                      |
| Modality           | Min number (optional/required)                    |

