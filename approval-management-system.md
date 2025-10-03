# 📝 Request Approval Workflow

## Problem Statement
You are tasked with designing a **Request Approval Workflow System** for a company.  

Whenever an employee submits a purchase request, it must be approved based on the **amount of money requested**:
- If the request is **up to $1,000**, the **Team Lead** can approve.  
- If the request is **up to $5,000**, the **Manager** can approve.  
- If the request is **up to $20,000**, the **Director** can approve.  
- Anything above $20,000 must be escalated to the **CEO**.  

The key requirement is that the system should be **extensible**. If the company later introduces a new role (e.g., VP), we should be able to add that role into the approval workflow **without modifying the existing code**.  

This problem is ideal for applying the **Chain of Responsibility Pattern**.  

---

## Requirements
1. **Approval Chain**
   - Define roles: Team Lead, Manager, Director, CEO.
   - Each role decides whether to approve or pass the request along.

2. **Request**
   - A request has: ID, Amount, and Description.

3. **Extensibility**
   - New approvers (e.g., VP) should be easy to add into the chain.

4. **Notification (Optional)**
   - Print or log who approved the request.

---

## Deliverables
- A console-based or simple implementation of the workflow.
- Documentation explaining:
  - Why **Chain of Responsibility** was used.
  - The trade-offs (e.g., flexibility vs. request tracing complexity).
- A few test cases showing:
  - Requests at different amounts being approved by the right person.
  - A request being escalated through the chain.

---

## Evaluation Criteria
- **Correctness**: Requests get approved at the correct level.
- **Design Quality**: Proper implementation of Chain of Responsibility.
- **Extensibility**: Easy to add new approvers without changing existing code.
- **Clarity**: Code and documentation are well-structured and easy to understand.
