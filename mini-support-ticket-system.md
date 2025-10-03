# 🎫 Mini Support Ticket System

## Problem Statement
You need to design a **lightweight Support Ticket System** where customers can raise tickets, and support agents can manage them.  
The focus is not on building a full application but on practicing **design patterns** to make the system flexible and extensible.

The system should allow creating tickets with different **types** (e.g., Technical, Billing, General Inquiry) and **priorities** (Low, Medium, High).  
When the ticket’s status changes, the customer should automatically be notified.

This problem helps practice:
- **Factory Method** → for creating different ticket types.
- **Observer Pattern** → for sending notifications when ticket status changes.
- **Strategy Pattern (Optional)** → for ticket assignment rules.

---

## Requirements
1. **Ticket Creation**
   - Support creation of different ticket types (Technical, Billing, General Inquiry).
   - Each ticket should have: ID, Type, Priority, Status, and Customer Info.

2. **Ticket Status**
   - Tickets can move through statuses: `Open → In Progress → Resolved`.
   - Notifications should be sent to customers when status changes.

3. **Notifications**
   - Customers should get a message like:  
     *“Your ticket #123 status changed to Resolved”*.

4. **Extensibility**
   - Should be easy to add new ticket types or notification channels (e.g., Email, SMS) without rewriting the core system.

---

## Deliverables
- A small implementation (no UI required, console-based or simple code).
- Documentation explaining:
  - Which design patterns you used and why.
  - How the system can be extended with new ticket types or notification channels.
- A few test cases showing:
  - Ticket creation.
  - Status change and notification delivery.

---

## Evaluation Criteria
- **Correctness**: Tickets can be created and moved through statuses, with notifications sent.
- **Design Quality**: Proper use of Factory and Observer patterns.
- **Simplicity**: Lightweight and doable in a few hours.
- **Extensibility**: Easy to add new ticket types or notification methods.
