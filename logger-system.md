# Logger System Problem (with Platform-Level Configuration)

## Problem Statement
We need to design and implement a **flexible and extensible logging system**.  
The system should be able to log messages to multiple platforms simultaneously (e.g., Console, File, Database, External Logging Services). Unlike a typical logger that logs to only one platform, this system must log to **all configured platforms at the same time**.  

Additionally, each platform should be configurable to **accept only specific log levels**. For example:  
- Console may receive **all log levels** (Info, Warning, Error).  
- File may store only **Warning and Error** logs.  
- Database may store only **Error** logs.  

This ensures fine-grained control while still maintaining extensibility for future platforms.

The solution must follow **SOLID principles** and use appropriate **design patterns** so that new logging platforms or configurations can be added in the future without modifying existing code.

---

## Requirements
1. The logger should:
   - Accept log messages of different levels (Info, Warning, Error, etc.).
   - Write logs to multiple platforms at once (e.g., Console + File + Database).
   - Allow configuration of which log levels each platform should handle.

2. The system must be **extensible**:
   - Adding a new logging platform (e.g., CloudWatch, Elasticsearch, Splunk) should not require changes to existing logic.
   - Adding new log levels should also be supported with minimal effort.

3. Each logging platform must follow:
   - **Single Responsibility Principle (SRP):** Each platform is responsible only for writing logs in its own way.
   - **Open/Closed Principle (OCP):** New platforms or log levels can be added without modifying existing logic.
   - **Dependency Inversion Principle (DIP):** The logger should depend on abstractions, not specific implementations.

4. Design pattern usage:
   - **Composite Pattern** (or a variation of Strategy + Aggregator) to combine multiple loggers into one unified logger.
   - **Factory Pattern** for creating different platform loggers.
   - Optional: **Chain of Responsibility** if log-level filtering per platform is implemented as a chain.

---

## Deliverables
- A working logging system that:
  - Supports multiple log levels (at least Info, Warning, Error).
  - Logs messages to all configured platforms.
  - Allows per-platform configuration for supported log levels.
  - Can easily extend to new platforms or log levels without modifying core logic.

- Documentation covering:
  - Why the chosen design pattern(s) were used.
  - Trade-offs considered (e.g., performance vs. configurability).
  - How SOLID principles are applied.

---

## Evaluation Criteria
- **Correctness:** Logs are written to all configured platforms according to their allowed log levels.
- **Design Quality:** Proper use of design patterns and adherence to SOLID principles.
- **Extensibility:** Ability to add new platforms or log levels without modifying existing code.
- **Configurability:** Each platform correctly filters logs by the configured log levels.
- **Clarity:** Code and documentation are well-structured and easy to follow.
- **Trade-off Explanation:** The developer explains chosen design patterns and the impact of per-platform filtering.
