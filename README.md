# Hospital-Management-System

**PROBLEM DEFINITION **
Hospital operations involve managing patient records, doctor scheduling, appointment lifecycles, and billing. However, most existing Hospital Management Systems, especially in academic and small-scale implementations, act only as passive data storage systems. They store and retrieve data but do not enforce business rules, operational logic, or domain-driven behavior.
This leads to several issues. Patient medical histories are often overwritten instead of being versioned, preventing reconstruction of a complete clinical timeline. Doctor profiles lack scheduling constraints, allowing appointments to be booked outside available time slots. Appointment statuses are overly simplified and do not represent the real multi-stage hospital workflow, resulting in invalid state transitions. Billing is often handled manually, which increases the risk of errors, duplication, or missed invoices. Notification systems are also tightly coupled with booking processes, where failures can impact core operations.
The core problem this project addresses is the lack of a system that enforces real hospital operational rules within the software itself. The system should not only store data but also enforce rules, manage state transitions, respond to events, and maintain consistency across modules without tight coupling.

**OBJECTIVES **
•	To design and implement a Patient Profile Management module with append-only medical history revisions to preserve the complete clinical timeline, along with an auto-computed risk score based on structured health indicators for actionable patient classification.
•	To design and implement a Doctor Profile Management module that maintains weekly availability templates, validates appointment requests against these constraints, and provides a workload metric to support balanced physician scheduling.
•	To design and implement an Appointment Scheduling module with a six-state lifecycle state machine, atomic conflict detection (doctor availability, time overlap, and patient concurrency), and asynchronous notification handling using the transactional outbox pattern.
•	To design and implement a Billing and Payment Management module that automatically generates bills upon appointment completion events, records payments against generated bills, and ensures financial data immutability by capturing consultation fees at the time of billing.
•	To structure the system as a modular monolith architecture with clear package separation, consistent DTO usage across APIs, and centralized exception handling, ensuring maintainability and alignment with enterprise Java development practices.


![image-alt](https://github.com/VrudhiRedekar05/Hospital-Management-System/blob/f26405c78c399374090b0231b81ffb8476a22b43/System%20Design.png)
