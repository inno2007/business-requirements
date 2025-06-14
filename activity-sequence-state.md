# UML Behavioral Diagrams: Activity, Sequence, and Statechart

Behavioral UML diagrams show how the system behaves and interacts over time. This file summarizes the use, purpose, and construction of **Activity Diagrams**, **Sequence Diagrams**, and **Statechart Diagrams**.

---

## 1. Activity Diagram

Used to model **workflow or business processes** by showing the sequence of steps.

### Purpose:
- Visualize sequential, parallel, and conditional flows.
- Clarify complex use case flows.
- Communicate workflow to technical and non-technical audiences.

### Symbols Used:
| Symbol                    | Meaning                                |
|---------------------------|----------------------------------------|
| Rounded rectangle         | Activity (e.g., "Validate Order")      |
| Arrow                     | Transition between steps               |
| Diamond                   | Decision (e.g., Yes/No branch)         |
| Horizontal bar (thick)    | Fork (start parallel tasks) or Join    |
| Filled circle             | Start of process                       |
| Circle with border        | End of process                         |
| Swimlane                 | Organizes responsibilities by role     |

### Concurrent Activities:
- Use forks (`---||`) and joins to model tasks happening at the same time.
- Example: Payment and confirmation processing running in parallel.

---

## 2. Sequence Diagram

Used to model **object interactions** over time within a single use case.

### Purpose:
- Shows the order in which objects (or system components) interact.
- Focuses on **timing and flow of messages**.

### Key Elements:
| Element       | Description                                |
|---------------|--------------------------------------------|
| Actors        | Stick figures that trigger the scenario    |
| Objects       | Rectangles representing classes or systems |
| Lifeline      | Dashed vertical line showing object's life |
| Messages      | Solid arrows (calls), dashed (responses)   |
| Activation    | Narrow rectangles on lifelines (processing time) |

### Example:
ATM Sequence
1. Person inserts card.
2. ATM verifies card with bank server.
3. Requests PIN and processes transaction.
4. If valid → complete transaction.
5. If invalid → reject.

### Alternatives:
- Use **alt/else frames** to show different outcomes (e.g., valid vs invalid login).

---

## 3. Statechart Diagram (State Machine)

Used to model **object states** and how they transition over time.

### Purpose:
- Model **lifecycle of an object**.
- Show how the state of an object changes based on events and triggers.

### Key Elements:
| Element       | Description                                 |
|---------------|---------------------------------------------|
| Object        | The instance being tracked (e.g., Order)    |
| State         | Condition or status of object               |
| Transition    | Arrows showing movement between states      |
| Event         | What triggers the transition                |
| Guard         | Optional condition required to transition   |

### Example: Pizza Order Lifecycle
| State             | Trigger                                     |
|------------------|---------------------------------------------|
| Created           | Place Order button                         |
| Confirmed         | Payment completed                         |
| In Preparation    | Kitchen staff begins cooking               |
| Out for Delivery  | Driver picks up the pizza                  |
| Delivered         | Pizza delivered to customer                |

Objects can only be in **one state at a time**, but different objects can be in different states concurrently.

---

## Summary Table

| Diagram Type      | Focus                         | Usage Example                         |
|-------------------|-------------------------------|----------------------------------------|
| Activity Diagram   | Workflow/steps in a process   | Approving a purchase order             |
| Sequence Diagram   | Time-based interactions       | ATM transaction sequence               |
| Statechart Diagram | Object lifecycle over time    | Order goes from "Placed" to "Delivered"|

---

Each diagram provides a different but complementary view of system behavior:
- **Activity Diagram**: Overall flow of control
- **Sequence Diagram**: Interaction between objects in time
- **Statechart Diagram**: Lifecycle of a single object
