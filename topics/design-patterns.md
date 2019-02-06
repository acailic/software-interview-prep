<h1 align="center">
Design Patterns Interview Questions & Answers
</h1>
<p align="center">
    <img src="https://github.com/monkey3310/full-stack-interview/blob/master/assets/design-patterns.svg" alt="Design Patterns Interview Questions & Answers" width="200" height="200"/>
</p>

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

</details>

### 4. What is _Singleton_ pattern?

<details>
    <summary>
        Answer
    </summary>

Ensure that your class have only one instance and provide a global pointer to access it.

</details>

### 5. What is _Builder_ pattern?

<details>
    <summary>
        Answer
    </summary>

Separate construction of a complex object from its representation, so you can modify it and create different representations depending on your builder.

</details>

### 6. What is _Abstract Factory_ pattern?

<details>
    <summary>
        Answer
    </summary>

Interface for creating families of object related / dependent on each other without using a concrete classes.

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

Creating new objects by coping existing ones without compromising their internals.

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

Structural design pattern that lets you split a giant class or a set of closely related classes into two separate hierarchies, abstraction and implementation, which can be developed independently of each other.

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

</details>

### 17. What is _Proxy_ pattern?

<details>
    <summary>
        Answer
    </summary>

Proxy is about creating a substitute class that has the same interface as an original service object. Upon receiving the request from a client, the proxy object creates an instance of a service object and delegate it all real work.

</details>

### 18. What is _Chain of responsibility_ pattern?

<details>
    <summary>
        Answer
    </summary>

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

</details>

### 23. What is _Memento_ pattern?

<details>
    <summary>
        Answer
    </summary>

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

Simplest example of this pattern in python:
```python
class Observable:
    def __init__(self):
        self.__observers = []
    
    def register_observer(self, observer):
        self.__observers.append(observer)
    
    def notify_observers(self, *args, **kwargs):
        for observer in self.__observers:
            observer.notify(self, *args, **kwargs)

class Observer:
    def __init__(self, observable):
        observable.register_observer(self)
    
    def notify(self, observable, *args, **kwargs):
        print('Got', args, kwargs, 'From', observable)


subject = Observable()
observer = Observer(subject)
subject.notify_observers('test')
```

Further reading: [Observer pattern](https://en.wikipedia.org/wiki/Observer_pattern)

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

</details>

### 29. What is _Visitor_ pattern?

<details>
    <summary>
        Answer
    </summary>

</details>
