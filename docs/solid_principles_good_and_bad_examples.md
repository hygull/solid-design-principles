Here are Python examples for each of the five SOLID principles, with a "bad" version that violates the principle and a "good" version that adheres to it. 

# 1. Single Responsibility Principle (SRP)
A class should have only one reason to change. This means a class should have only one job or responsibility. 

### Bad example: Violation of SRP
The User class is responsible for two unrelated things: managing user data and communicating via email. 

### Good example: Adherence to SRP
The responsibilities are separated into different classes: User for data, UserRepository for saving, and EmailService for sending emails. 

# 2. Open/Closed Principle (OCP)
Software entities should be open for extension but closed for modification. This means you should be able to add new functionality without changing existing code. 

### Bad example: Violation of OCP
An AreaCalculator class that requires modification every time a new shape type is added is an example of violating OCP.

### Good example: Adherence to OCP
Using an abstract base class Shape with an area() method, new shapes can be added by extending Shape without altering the AreaCalculator. 

# 3. Liskov Substitution Principle (LSP)
Subtypes must be substitutable for their base types. A function using a base class should work correctly with a subclass. 

### Bad example: Violation of LSP
A subclass, such as Ostrich, that cannot perform an action expected of its base class, like a Bird's fly() method, violates LSP. 

### Good example: Adherence to LSP
Splitting the base class into categories like FlyingBird and NonFlyingBird allows subclasses such as Ostrich to accurately reflect their capabilities. 

# 4. Interface Segregation Principle (ISP)
Clients should not be forced to depend on interfaces they do not use. This principle suggests creating smaller, focused interfaces. 

### Bad example: Violation of ISP
A single, large Printer interface requiring a BasicPrinter to implement methods like fax() and scan() that it doesn't support violates ISP. 

### Good example: Adherence to ISP
Breaking down interfaces into smaller, role-specific ones like Printable and Scannable allows classes to implement only what they need. 

# 5. Dependency Inversion Principle (DIP)
High-level modules should not depend on low-level modules; both should depend on abstractions. This approach promotes loose coupling between components. 

### Bad example: Violation of DIP
A high-level module, like NotificationService, directly depending on a low-level module, such as a concrete EmailSender, demonstrates a violation of DIP. 

### Good example: Adherence to DIP
Achieving DIP involves both the high-level module and specific implementations depending on an abstraction (e.g., a MessageSender interface), with the specific implementation being injected into the high-level module. 