# 📈 Stock Market Listener Problem

## Problem Statement
We need to design and implement a **stock market notification system** where consumers (listeners) can subscribe to specific stocks.  
When the price of a subscribed stock changes, all registered listeners should automatically receive a notification.  

Additionally, each listener should be able to configure **price thresholds**. For example:  
- "Notify me if Tesla (TSLA) goes above $300"  
- "Notify me if Apple (AAPL) drops below $150"  

This ensures users receive alerts only when their conditions are met, instead of on every price change.  

The solution should demonstrate the use of **design patterns** (Observer Pattern is strongly recommended) and must follow **SOLID principles** to allow easy extensibility (e.g., adding new types of listeners, notification channels, or threshold conditions).

---

## Requirements
1. The system should:
   - Allow consumers to **subscribe** to one or more stocks.  
   - Allow consumers to **unsubscribe** from a stock at any time.  
   - Notify only the relevant subscribers when a stock price changes.  
   - Support **price threshold alerts** (greater than, less than, equal to conditions).  
   - Support multiple notification types (e.g., console message, email, push notification).  

2. The system must be **extensible**:
   - Adding new notification channels (e.g., SMS, Webhook, Mobile Push) should not require changes to the stock or listener management code.  
   - Adding new stock types (e.g., crypto, bonds) should require minimal effort.  
   - Supporting new threshold conditions (e.g., percentage changes, time-based alerts) should be easy to add.  

3. The design must follow:
   - **Single Responsibility Principle (SRP):** Stock management, listener management, and notification handling should be separated.  
   - **Open/Closed Principle (OCP):** New notification channels, stock types, or alert conditions should be added without modifying existing logic.  
   - **Dependency Inversion Principle (DIP):** The stock market system should rely on abstractions (interfaces) for listeners and conditions.  

4. Recommended design pattern:
   - **Observer Pattern:** For managing subscriptions and notifying listeners about stock changes.  
   - **Strategy Pattern:** For handling different threshold conditions (e.g., >, <, =).  
   - Optional: **Factory Pattern** for creating listeners or conditions dynamically.  

---

## Deliverables
- A working stock market system that:  
  - Allows users to subscribe/unsubscribe to specific stocks.  
  - Notifies subscribers whenever their subscribed stock meets their threshold condition.  
  - Supports at least two types of listeners (e.g., ConsoleListener, EmailListener).  
  - Implements at least two threshold types (greater than, less than).  
  - Is easily extendable for new notification channels, stock types, or threshold conditions.  

- Documentation covering:  
  - Why the chosen design pattern(s) were used.  
  - Trade-offs considered (e.g., performance with many subscribers and frequent stock updates).  
  - How SOLID principles are applied in the design.  

---

## Evaluation Criteria
- **Correctness:** Subscribers only receive updates when their threshold conditions are met.  
- **Design Quality:** Use of Observer and Strategy Patterns with SOLID compliance.  
- **Extensibility:** Ability to add new stock types, threshold conditions, or notification channels without modifying existing code.  
- **Scalability:** The design can handle many subscribers and high-frequency stock updates efficiently.  
- **Clarity:** Code and documentation are clear and easy to follow.  
- **Trade-off Explanation:** Developer explains chosen design patterns and challenges (e.g., performance, memory usage, or delayed notifications).  
