<h1 align="center">
Design Patterns Interview Questions & Answers
</h1>

![Image Design Patterns](https://1.bp.blogspot.com/-FliyHYR2fYY/Xk3o0f4XOsI/AAAAAAAAdA4/SqBdGXG9rKY5XYtBUAxrZoKe6nBaXi2hACLcBGAsYHQ/s640/Design%2BPatterns%2Band%2Btheir%2Brelationship%2Bfor%2Bprogrammers%2Beducative.jpg)

_Note: Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would._

### 1. Explain what is a pattern?

<details>
    <summary>
        Answer
    </summary>

Design Pattern is a typical solution to commonly occurring problem in software design. You could compare DP to a blueprint that can be taken and customized to solve a particular design problem in your code.

</details>

### 2. Why we should use design patterns?

<details>
    <summary>
        Answer
    </summary>

The most important reason is that patterns simplify the design and support of programs.

- Tried and tested solutions.
- Code unification - you create fewer bugs, since you use typical unified solutions where all hidden bugs have already been discovered.
- Universal programmers’ vocabulary - instead of explaining some problem you can use pattern name that will be enough for another developer to understand the problem.

</details>

### 3. What are the main categories of design patterns?

<details>
    <summary>
        Answer
    </summary>

- Creational: all about creating new objects.
- Structural: structuring your classes effectively, making the relationships minimal etc.
- Behavioral: These design patterns are specifically concerned with communication between objects.

</details>

### 4. What is _Singleton_ pattern?

<details>
    <summary>
        Answer
    </summary>

Ensure that your class have only one instance and provide a global pointer to access it.
Singleton pattern in Java is a pattern that allows only one instance of Singleton class available in the whole application. java.lang.Runtime is a good example of a Singleton pattern in Java. There are multiple ways to write thread-safe Singleton in Java, like by writing singleton using double-checked locking, by using static Singleton instance initialized during class loading. By the way, using Java enum to create thread-safe singleton is the most simple way.   
</details>

### 5. What is _Builder_ pattern?

<details>
    <summary>
        Answer
    </summary>

Creational design pattern - Separate construction of a complex object from its representation, so you can modify it and create different representations depending on your builder.

</details>

### 6. What is _Abstract Factory_ pattern?

<details>
    <summary>
        Answer
    </summary>

Interface for creating families of object related / dependent on each other without using a concrete classes. Abstract Factory creates a factory

</details>

### 7. What is _Factory method_ pattern?

<details>
    <summary>
        Answer
    </summary>

Interface method for creating an object but letting subclasses decide on what class will be instantiated.

</details>

### 8. What is _Object pool_ pattern?

<details>
    <summary>
        Answer
    </summary>
    
Special kind of factory, which main purpose is reusing/sharing objects, that creations is hard (e.g time consuming).
Client of object poll requests object, do some operation on it. After it finish it returns object to pool instead of destroy it.
Good example of implementation Object Pool pattern is [Thread pool from .NET Framework.](https://docs.microsoft.com/en-us/dotnet/api/system.threading.threadpool?view=netframework-4.7.2)

</details>

### 9. What is _Prototype_ pattern?

<details>
    <summary>
        Answer
    </summary>

Creating new objects by coping existing ones without compromising their internals. Prototype design pattern is used which refers to creating duplicate objects. In the prototype design pattern, if a similar object is already present then cloning is done keeping performance in mind.

</details>

### 10. What is _Adapter_ pattern?

<details>
    <summary>
        Answer
    </summary>

Adapter is a special object that converts calls sent by one object to the format that another object can understand. Adapter wraps one of the objects to hide the complexity of conversion happening behind the scenes.

</details>

### 11. What is _Bridge_ pattern?

<details>
    <summary>
        Answer
    </summary>

Structural design pattern that lets you split a giant class or a set of closely related classes into two separate hierarchies, abstraction and implementation, which can be developed independently of each other. Bridge pattern is designed to isolate a class's interface from its implementation so we can vary or substitute the implementation without changing the client code

</details>

### 12. What is _Composite_ pattern?

<details>
    <summary>
        Answer
    </summary>

Composing objects into tree structures and allowing clients to work with them as if they were individual objects.

</details>

### 13. What is _Decorator_ pattern?

<details>
    <summary>
        Answer
    </summary>

Attaching new behaviors to the objects by placing them inside of a wrapper that contains those behaviors
Decorator pattern is used to implement functionality on an already created object,
</details>

### 14. What is _Facade_ pattern?

<details>
    <summary>
        Answer
    </summary>

The facade is a class that provides a simple interface to a complex subsystem containing dozens of classes. The facade may have limited functionality in comparison to working with subsystem directly. It includes only those features that clients care about.

</details>

### 15. What is _Flyweight_ pattern?

<details>
    <summary>
        Answer
    </summary>

Flyweight is a structural design pattern that lets you fit more objects into the available amount of RAM by sharing common parts of object state among multiple objects, instead of keeping it in each object.

</details>

### 16. What is _Private Class Data_ pattern?

<details>
    <summary>
        Answer
    </summary>
structural pattern -The private class data design pattern seeks to reduce exposure of attributes by limiting their visibility. It reduces the number of class attributes by encapsulating them in single Data object. 
</details>

### 17. What is _Proxy_ pattern?

<details>
    <summary>
        Answer
    </summary>

Proxy is about creating a substitute class that has the same interface as an original service object. Upon receiving the request from a client, the proxy object creates an instance of a service object and delegate it all real work. Proxy pattern is used for controlling access to an object.

</details>

### 18. What is _Chain of responsibility_ pattern?

<details>
    <summary>
        Answer
    </summary>
It minimizes the coupling. Provides flexibility while assigning the responsibilities to objects.
It permits a set of classes to act as one. The events produced in one class can be sent to other handler classes with the help of composition.
Usage of Chain of Responsibility Pattern:
When more than one objects are ready to handle a request, and the handler is unknown.
In case the collection or a group of objects that can handle the request must be specified dynamically.
</details>

### 19. What is _Command_ pattern?

<details>
    <summary>
        Answer
    </summary>
The command pattern is a behavioral design pattern that intends to encapsulate in an object all the data required for performing a given action (command), including what method to call, the method’s arguments, and the object to which the method belongs.

This model allows us to decouple objects that produce the commands from their consumers, so that’s why the pattern is commonly known as the producer-consumer pattern.
</details>

### 20. What is _Interpreter_ pattern?

<details>
    <summary>
        Answer
    </summary>

The interpreter pattern is a design pattern that specifies how to evaluate sentences in a language. The basic idea is to have a class for each symbol (terminal or nonterminal) in a specialized computer language. The syntax tree of a sentence in the language is an instance of the composite pattern and is used to evaluate (interpret) the sentence for a client.

</details>

### 21. What is _Iterator_ pattern?

<details>
    <summary>
        Answer
    </summary>
    
The Iterator pattern provides a mechanism to access the elements of an aggregate object or container sequentially without knowledge of the underlying structure of the object being iterated over. See the [C2 wiki Iterator pattern article](http://wiki.c2.com/?IteratorPattern) for further reading.

</details>

### 22. What is _Mediator_ pattern?

<details>
    <summary>
        Answer
    </summary>
The mediator pattern defines an object that encapsulates how a set of objects interact. This pattern is considered to be a behavioral pattern due to the way it can alter the program's running behavior.
With the mediator pattern, communication between objects is encapsulated within a mediator object. Objects no longer communicate directly with each other, but instead communicate through the mediator. This reduces the dependencies between communicating objects, thereby reducing coupling.
</details>

### 23. What is _Memento_ pattern?

<details>
    <summary>
        Answer
    </summary>
The memento pattern is a software design pattern that provides the ability to restore an object to its previous state (undo via rollback). 
The memento pattern is implemented with three objects: the originator, a caretaker and a memento. The originator is some object that has an internal state. The caretaker is going to do something to the originator, but wants to be able to undo the change. The caretaker first asks the originator for a memento object. Then it does whatever operation (or sequence of operations) it was going to do. To roll back to the state before the operations, it returns the memento object to the originator.
</details>

### 24. What is _Null object_ pattern?

<details>
    <summary>
        Answer
    </summary>

Null object is an object that has certain neutral ("do nothing") behavior. This design pattern describes the usage of such objects and their behavior.

In many OO languages objects can have null value and checking objects for absence of value (NULL value) can become very tedious and make the code more complex. Null object pattern allows developer incapsulate this checks by replacing NULL value with an object that "does nothing", removing special cases handling.

Futher reading: [Null object Pattern](https://en.wikipedia.org/wiki/Null_object_pattern)

</details>

### 25. What is _Observer_ pattern?

<details>
    <summary>
        Answer
    </summary>

Observer is design pattern in which one single object (Subject) notifies an open ended number of listener-objects (Observers) about any updates by calling their methods. Observer pattern widely adopted in event driven systems and lies in the base of MVC architectural pattern.

</details>

### 26. What is _State_ pattern?

<details>
    <summary>
        Answer
    </summary>
State is a behavorial pattern that allows it's behavior to be changed depending on what "state" it is in.
</details>

### 27. What is _Strategy_ pattern?

<details>
    <summary>
        Answer
    </summary>
Strategy is a behavioral software design pattern that enables selecting an algorithm at runtime. Instead of implementing a single algorithm directly, code receives run-time instructions as to which in a family of algorithms to use.
</details>

### 28. What is _Template method_ pattern?

<details>
    <summary>
        Answer
    </summary>
The template method pattern is a behavioral design pattern that defines the program skeleton of an algorithm in an operation, deferring some steps to subclasses.  Template method should be final so that the subclass can not override and change the steps of the algorithm. Still, the same time individual steps should be abstract, so that child classes can implement them.
</details>

### 29. What is _Visitor_ pattern?

<details>
    <summary>
        Answer
    </summary>
The visitor design pattern is a way of separating an algorithm from an object structure on which it operates. A practical result of this separation is the ability to add new operations to existent object structures without modifying the structures. It is one way to follow the open/closed principle.
In essence, the visitor allows adding new virtual functions to a family of classes, without modifying the classes.
</details>

### 30. What is _Factory_ pattern?

<details>
    <summary>
        Answer
    </summary>
    The Factory pattern in Java is a creation Java design pattern . Factory pattern used to create an object by providing static factory methods. There are many advantages of providing factory methods like caching immutable objects, easy to introduce new objects, etc.
</details>

### 31. What is _MVC_ pattern?

<details>
    <summary>
        Answer
    </summary>
Model-View-Controller. The abbreviation MVC is taken from the Model-view-controller concept.
Models are objects, used as blueprints for all of the objects that will be used in the application.
Views contain the presentational aspect of the data and information located in the models.
Controllers control both model and view as they serve as a connection between the two objects. The controller plays the role of an interface between View and Model and also intercepts all the incoming requests.
</details>


### 32. What is _DAO_ pattern?
<details>
    <summary>
        Answer
    </summary>
Data Access Object Pattern is used to isolate low-level data accessing API or actions from high-level business services. 
    Data Access Object Interface -  describes the standard actions to be performed on a model objec
    Data Access Object concrete class - This class implements a DAO interface. This class is accountable to get data from a data source.
    Model Object or Value Object -object is a plain old java object containing get/set methods to store data retrieved using DAO
    </details>
