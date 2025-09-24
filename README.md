# solid-design-principles

The repository containing the details (examples, code, explanations) related to SOLID principles (Solid design principles).

# SOLID PRINCIPLES

SOLID is an acronym for five fundamental principles of object-oriented programming (OOP) that help developers create more maintainable, flexible, and scalable software. The concepts, compiled by Robert C. Martin ("Uncle Bob") in the early 2000s, guide engineers to build code that is less tightly coupled and more resilient to change. 

# The five principles
## S: Single Responsibility Principle (SRP)
A class should have one, and only one, reason to change. This means that a class or module should have a single responsibility or job. 
- **Adherence:** Separate business logic from other functionalities like data persistence or user notification. A User class, for example, should only manage user data, while a NotificationService handles sending emails.
- **Violation:** A single class that handles everything from user registration to sending a welcome email and saving data to a database is harder to maintain and test. 

## O: Open-Closed Principle (OCP)
Software entities should be open for extension but closed for modification. This allows adding new features without changing existing code. Adherence involves using interfaces or abstract classes, such as an AreaCalculator accepting a Shape interface, while violation occurs when using conditional logic that requires modification for each new shape. 

## L: Liskov Substitution Principle (LSP)
Subtypes must be substitutable for their base types without affecting program correctness. Derived classes should maintain the behavior expected of their parent. A classic violation is a Square class inheriting from Rectangle and breaking the expected behavior of independent side changes. 
I: Interface Segregation Principle (ISP)
Clients should not depend on interfaces they don't use. This favors small, specific interfaces over large, general ones. For example, a class needing both managing and working capabilities would implement separate ILead and IProgrammer interfaces, rather than being forced to implement unnecessary methods from a single large interface. 

## D: Dependency Inversion Principle (DIP)
High-level modules should depend on abstractions, not low-level modules or concrete implementations. This inverts the typical dependency. For instance, an ExceptionLogger depending on an ILogger interface (abstraction) allows it to use any logger implementing that interface, avoiding tight coupling with a specific concrete logger class like FileLogger.


## Benefits of using SOLID principles
SOLID principles improve maintainability, flexibility, and scalability by making code easier to understand, extend, and adapt. They also facilitate easier testing and reduce technical debt. 

## Potential drawbacks
Applying SOLID can sometimes increase complexity, especially in simpler projects, and requires experience to avoid "over-engineering". The principles demand careful consideration of the project's context, as blind adherence might lead to less efficient code. 