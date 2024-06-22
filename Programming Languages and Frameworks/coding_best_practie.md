# Development Best Practices

## Good Practices
- Clean Code
- Design patterns
  - **Creational Patterns**
    - **Singleton Pattern**:  
    Ensures that a class has only one instance and provides a global point of access to that instance.
    - **Factory Method Pattern**:  
    Defines an interface for creating objects, allowing subclasses to decide which class to instantiate.
    - **Abstract Factory Method Pattern**:  
    Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
    - **Builder Pattern**:  
    Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
    - **Prototype Pattern**:  
    Creates new objects by copying an existing object, avoiding the overhead of creating objects from scratch.
  - **Structural Pattern**
    - **Adapter Pattern**:  
    Converts the interface of a class into another interface that clients expect, enabling classes with incompatible interfaces to work together.
    - **Bridge Pattern**:  
    Decouples an abstraction from its implementation, allowing both to evolve independently.
    - **Composite Pattern**:  
    Composes objects into tree structures to represent part-whole hierarchies, making it easier to work with individual objects and compositions.
    - **Decorator Pattern**:  
    Dynamically adds responsibilities to objects, providing a flexible alternative to subclassing for extending functionality.
    - **Facade Pattern**:  
    Provides a simplified interface to a complex subsystem, making it easier to use and understand.
    - **Flyweight Pattern**:  
    Shares instances of objects to support large numbers of fine-grained objects efficiently.
    - **Proxy Pattern**:  
    Provide a substitute or placeholder for another object to control access to the original object
  - **Behavioral Patterns**
    - **Chain of Responsibility Pattern**:  
    Creates a chain of objects that can handle requests, avoiding coupling the sender with its receivers.
    - **Command Pattern**:  
    Turns a request into a stand-alone object, allowing parameterization of clients with different requests.
    - **Interpreter Pattern**:  
    Defines a grammar for a language and an interpreter to interpret sentences in the language.
    - **Iterator Pattern**:  
    Provides a way to access elements of a collection without exposing its underlying representation.
    - **Mediator Pattern**:  
    Defines an object that centralizes communication between multiple objects, reducing direct dependencies between them.
    - **Memento Pattern**:  
    Captures and restores an object’s internal state, allowing it to be restored to a previous state.
    - **Observer Pattern**:  
    Defines a dependency between objects, ensuring that when one object changes state, all its dependents are notified and updated automatically.
    - **State Pattern**:  
    Allows an object to change its behavior when its internal state changes, enabling cleaner, more maintainable conditional logic.
    - **Strategy Pattern**:  
    Defines a family of algorithms, encapsulates each one and makes them interchangeable. Clients can choose an algorithm from this family without modifying their code.
    - **Template Method Pattern**:  
    Defines the structure of an algorithm in a superclass but lets subclasses override specific steps of the algorithm.
    - **Visitor Pattern**:  
    Separates an algorithm from an object structure, allowing new operations to be added without modifying the objects themselves.
- SOLID Principles
- Different Software Architectures
- Algorithms
- Name things properly
- Test your code


## 12 factors processes..
- codebase
- dependency
- config
- backend service
- build release & run
- processes
- port bind
- concurrency
- disposable
- dev/prod parity
- logs
- admin procs