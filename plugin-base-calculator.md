# 🧮 Calculator Problem

## Problem Statement
We need to design and implement a **flexible and extensible calculator system**.  
The calculator should initially support **addition, subtraction, multiplication, and division**. However, the design must allow developers to easily add new operations (e.g., modulus, power, square root) without modifying existing code.  

The solution should demonstrate adherence to **SOLID principles** and appropriate use of **design patterns** to ensure scalability and maintainability.

---

## Requirements
1. The calculator should:
   - Take two inputs and an operation type.
   - Perform the calculation using the appropriate logic.
   - Return the result.

2. The system must be **extensible**:
   - New operations can be added without changing existing classes.

3. Each operation must follow:
   - **Single Responsibility Principle (SRP):** Each operation encapsulated in its own class.
   - **Open/Closed Principle (OCP):** Existing code should not change when adding new operations.
   - **Dependency Inversion Principle (DIP):** The calculator should rely on abstractions, not concrete implementations.

---

## Deliverables
- A working calculator implementation that supports:
  - Addition
  - Subtraction
  - Multiplication
  - Division
- Extensibility for adding new operations (e.g., modulus, power).
- Documentation covering:
  - Why the chosen design pattern(s) were used.
  - The trade-offs considered.
  - How SOLID principles are applied in the solution.

---

## Evaluation Criteria
- **Correctness:** The calculator performs operations accurately.
- **Design Quality:** The solution demonstrates proper use of design patterns and SOLID principles.
- **Extensibility:** New operations can be added without modifying existing logic.
- **Clarity:** Code and documentation are easy to understand and well-structured.
- **Trade-off Explanation:** The developer explains why the chosen design pattern was selected and what alternatives were considered.
