# Use Case Modeling

Use case modeling is a core tool in systems analysis. It helps identify, organize, and communicate system requirements from a user’s perspective — focusing on what the system must do, not how.

---

## 1. Purpose of Use Case Modeling

- Captures both functional and some non-functional requirements
- Helps identify data requirements and system interactions
- Aids communication among stakeholders, analysts, and developers
- Supports planning, testing, and documentation

---

## 2. Key Components of Use Case Modeling

| Element        | Description |
|----------------|-------------|
| **Actors**     | External users or systems that interact with the system |
| **Use Cases**  | Goals or services the system performs for the actors |
| **System**     | The boundary defining where the use cases live |
| **Relationships** | Connections between actors and use cases (include, extend) |

---

## 3. Use Case Diagram

A visual representation that includes:

- Actors (stick figures)
- Use cases (ovals)
- System boundary (a box around all use cases)
- Arrows indicating interaction or relationships

---

## 4. Use Case Description

A detailed text document that includes:

| Field             | Description |
|------------------|-------------|
| **Actor**         | The user or external system initiating the action |
| **Event**         | The trigger for the interaction |
| **System Action** | The system’s response |
| **Flow**          | Main and alternate flows |
| **Relationships** | Use of include/extend logic |

---

## 5. Relationship Types

| Type     | Description |
|----------|-------------|
| **Include** | Shared functionality reused by multiple use cases (like a subroutine) |
| **Extend**  | Optional or conditional functionality that adds to a base use case |

**Examples:**
- `Include`: Login is included in all access-related actions.
- `Extend`: "Reset Password" may extend "Login" only if login fails.

---

## 6. Steps to Create a Use Case Model

1. Review business specifications.
2. Identify actors (users, external systems).
3. Identify primary use cases triggered by the actors.
4. Group common behavior using **include** relationships.
5. Define optional flows using **extend** relationships.
6. Create detailed use case descriptions.

---

## 7. Benefits of Use Case Descriptions

- Easier to understand than technical specifications
- Helps uncover the real user needs early
- Useful for developers, testers, and non-technical stakeholders

---

## Summary

Use case modeling ensures system behavior aligns with user needs. Diagrams provide a high-level overview, while detailed use case descriptions document interactions step by step.

