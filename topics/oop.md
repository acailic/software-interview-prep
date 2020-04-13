# OOP

- Encapsulation – an object contains (encapsulates) both (1) data and (2) the relevant processing instructions, as we have seen. Once an object has been created, it can be reused in other programs.
- Inheritance – once you have created an object, you can use it as the foundation for similar objects that have the same behavior and characteristics.
- Polymorphism – generics, the presence of "many shapes." In object-oriented programming, polymorphism means that a message (generalized request) produces different results based on the object that it is sent to.
- Abstraction: Abstraction is the methodology of hiding the implementation details from the user and only providing the functionality to the users. 

## Design Patterns Examples

### Creation

- Factory : 

  define an interface or abstract class for creating an object but let the subclasses decide which class to instantiate
  plus: allows the sub-classes to choose the type of objects to create, loose-coupling
      
- Builder :

  construct a complex object from simple objects using step-by-step approach.
  plus: clear separation between the construction and representation,change the internal representation of objects.

- Singleton :

  define a class that has only one instance and provides a global point of access to it.
  plus: Saves memory because object is not created at each request. Only single instance is reused. mostly used in multi-threaded and           database applications. It is used in logging, caching, thread pools, configuration settings.

### Composition (Structural)

- Adapter : 
  converts the interface of a class into another interface that a client wants.
  
- Facade : 
  provide a unified and simplified interface to a set of interfaces in a subsystem, therefore it hides the complexities of the       subsystem from the client. Higher-level interface that makes the sub-system

- Decorator : 
  attach a flexible additional responsibilities to an object dynamically. uses composition instead of inheritance to extend the     functionality of an object at runtime.The Decorator Pattern is also known as Wrapper.

- Proxy : 
  provides the control for accessing the original object. It provides the protection to the original object. Virtual, Remote..


### Behavioral

- Chain of responsibility :
  avoid coupling the sender of a request to its receiver by giving multiple objects a chance to handle the request.
  reduces the coupling and adds flexibility while assigning the responsibilities to objects. Events produced in one class can be     sent to other handler classes with the help of composition
  
- Command :
  encapsulate a request under an object as a command and pass it to invoker object. Invoker object looks for the appropriate         object which can handle this command and pass the command to the corresponding object and that object executes the command.       separates the object that invokes the operation from the object that actually performs the operation

- Iterator :
  Cursor
- Visitor :
  Represent an operation to be performed on elements of an object structure. Visitor lets you define a new operation without changing the classes of the elements on which it operates.
