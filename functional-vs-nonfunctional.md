# Functional vs Non-Functional Requirements

System requirements define **what** a system should do (functional) and **how** it should behave (non-functional). These help ensure that developers, stakeholders, and testers all share a clear understanding of project goals.

---

## 1. Functional Requirements

**Definition**:  
Describe the actions a system must perform to fulfill business needs.

### Examples:
- The system must allow users to make payments.
- Employee leave request data must be entered before proceeding to the approval/reject screen.

### Common Functional Requirements Cover:
- Screen operations
- Data input and validation
- Workflow or process logic
- Output generation (e.g., reports)

---

## 2. Non-Functional Requirements

**Definition**:  
Define how the system should perform — quality standards, technical constraints, and regulatory expectations.

### Common Categories:
- **Usability**: Easy to use and understand
- **Reliability**: Minimal failure rates
- **Performance**: Response within 2 seconds under normal load
- **Security**: Password encryption, secure login
- **Availability**: Must be online 24/7
- **Recoverability**: Restore after crash within 10 minutes
- **Data Integrity**: Data must remain consistent across systems

---

## 3. Constraints

Constraints are system limitations defined by:
- Platform requirements: e.g., must work on iPhone, iPad, and Android
- Tools or languages to be used
- Regulatory or compliance boundaries

---

## 4. Writing Requirements Properly

| Requirement Type | Writing Guidelines |
|------------------|--------------------|
| **Functional**   | Focus on "what" the system does |
| **Non-Functional** | Focus on performance or quality of service |
| **Constraints**  | Define limitations for technology or environment |

### Format:
- Use **“shall”** for mandatory requirements  
  - *Example:* The system shall store accident claims.
- Use **“should”** for desirable but optional features  
  - *Example:* The interface should support light and dark modes.

Requirements should always be:
- **Testable**
- **Consistent**
- **Measurable**

---

## 5. Summary

| Type                | Focus                   | Example |
|---------------------|--------------------------|---------|
| Functional          | System behavior           | “Shall process orders” |
| Non-Functional      | System quality/attributes | “Should load within 2 sec” |
| Constraint          | System limits             | “Must run on iOS + Android” |

Both types of requirements must be considered carefully to ensure project success and user satisfaction.

