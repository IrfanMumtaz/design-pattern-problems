# Problem: Email Service Management  

## Problem Statement  
Your company uses multiple email services for different use cases. Currently, you have three providers:  

- **ServiceA** → Used for **Transactional Emails** (e.g., order confirmations, password resets).  
- **ServiceB** → Used for **Non-Transactional Emails** (e.g., promotional campaigns, marketing messages).  
- **ServiceC** → Used for **Subscription Emails** (e.g., newsletters, product updates).  

At present, every time a new email service or scenario is introduced, developers must modify existing code. This creates a maintenance challenge, makes the system error-prone, and violates the **Open/Closed Principle** of SOLID.  

You have been asked to design a **flexible email service system** where:  
1. Adding new email services does **not** require modifying existing code.  
2. Each email service has a **single responsibility** (SRP).  
3. The solution should demonstrate the use of an appropriate **design pattern**.  

---

## Requirements  
- Implement a basic project in any programming language.  
- Each email service (ServiceA, ServiceB, ServiceC, etc.) should be **independent** and handle only its own responsibility.  
- The main system should decide which service to use **without hardcoding service logic everywhere**.  
- New services (e.g., ServiceD for Survey Emails, ServiceE for Event Notifications) can be added later with minimal changes.  
- Follow **SOLID principles**, especially **SRP** and **OCP**.  
- Use at least one **Design Pattern** (Factory, Strategy, or another suitable one).  

---

## Deliverables  
1. **Code Implementation** in your chosen language.  
2. **Explanation Document** (short write-up) containing:  
   - Which design pattern(s) you used.  
   - Why this pattern was chosen.  
   - How SRP and OCP are applied in your design.  
   - Trade-offs of your chosen solution (e.g., complexity vs. flexibility).  
   - Any alternative pattern that could also work and why you did not choose it.  

---

## Evaluation Criteria  
- Does the solution cleanly separate each email service’s responsibility?  
- Does the system allow adding new services without changing existing code?  
- Is the design pattern applied appropriately (not forced)?  
- Are SOLID principles respected?  
- Is the reasoning clear and well explained?  
