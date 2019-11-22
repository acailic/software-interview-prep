# OOP

- Encapsulation – an object contains (encapsulates) both (1) data and (2) the relevant processing instructions, as we have seen. Once an object has been created, it can be reused in other programs.
- Inheritance – once you have created an object, you can use it as the foundation for similar objects that have the same behavior and characteristics.
- Polymorphism – generics, the presence of "many shapes." In object-oriented programming, polymorphism means that a message (generalized request) produces different results based on the object that it is sent to.

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

- Adapter
- Facade
- Decorator
- Proxy

### Behavioral

- Chain of responsibility
- Command
- Iterator
- Visitor
