<h1 align="center">
Design Principles Interview Questions & Answers
</h1>
<p align="center">
    <img src="https://github.com/monkey3310/full-stack-interview/blob/master/assets/design-principles.svg" alt="Design Principles Interview Questions & Answers" width="200" height="200"/>
</p>

_Note: Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would._

### 1. Explain _DRY_

<details>
    <summary>
        Answer
    </summary>

**Don't repeat yourself** - reduce repetition of software patterns, replace them with abstractions and data normalization. This can also be applied not only on data and code, but your CI, deployment etc - relay on automation, code generation and scripts over manual repeatable processes.

</details>

### 2. Explain _KISS_

<details>
    <summary>
        Answer
    </summary>

**Keep it simple, stupid** - most systems works the best if they are kept simple rather than complicated. So the goal of all your designs should be aiming to achive that simplicity of your system, and unnecessary complexity should be avoided.

</details>

### 3. Explain _YAGNI_

<details>
    <summary>
        Answer
    </summary>

**You aren't gonna need it** - XP (extreme programming) principle that states that you should not add some functionality into your code until you need it. Always design with extendability in mind, not with all possible scenarios already covered.

</details>

### 4. Explain _Convention over configuration_

<details>
    <summary>
        Answer
    </summary>

Developing programs according to typical programming conventions, versus programmer defined configurations. It enables quick and simple software creation while maintaining base software requirements.

Downside of following coding by convention is the fact, that from programing point of view, everything is working fine until you are aware of all conventions in the project.

</details>

### 5. Explain _Separation of concerns_

<details>
    <summary>
        Answer
    </summary>

Separate your program into distinct sections, so each section is only responsible for one thing. In OOP this is done on language level by classes - each class should be responsible only for actions related to itself. You can also talk about SoC on higher level, like splitting the presentation layer from data processing etc.

</details>

### 6. Explain _Single source of truth_

<details>
    <summary>
        Answer
    </summary>

Practice of structuring information models and associated data schema such that every data element is stored exactly once.

</details>

### 7. Explain _Inversion of control_

<details>
    <summary>
        Answer
    </summary>

Moving the control over flow of your application and interactions between objects / functions from the objects to a program framework - for example when you have two classes that are building something together, rather than controlling that flow from within that classes, it should be done by some orchestration layer above that, keeping both object not dependent of each other.

There are several ways of implementing this pattern, for example:

- service locator pattern
- dependency injection
- template method design pattern.

</details>

### 8. Explain _SOLID_

<details>
    <summary>
        Answer
    </summary>

| *   | Rule                            | Description                                                                                                                                                                                                                                             |
| --- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| S   | Single responsibility principle | Each module should be responsible to one and only action                                                                                                                                                                                                |
| O   | Open/Closed principle           | A software artifact should be open for extension but closed for modification.                                                                                                                                                                           |
| L   | Liskov substitution principle   | It should be possible to substitute the derived class with base class.                                                                                                                                                                                  |
| I   | Interface segregation principle | Many client-specific interfaces are better than one general-purpose interface.                                                                                                                                                                          |
| D   | Dependency inversion principle  | Depend upon Abstractions but not on concretions. This means that each module should be separated from other using an abstract layer which binds them together. Source code dependency points in the opposite direction compared to the flow of control. |

</details>

### 9. What can you tell about _Microservices_

<details>
    <summary>
        Answer
    </summary>

Style of software architecture that involves delivering systems as a set of very small, granular, independent collaborating services.
Pros of microservices:The services are easy to replace, Services can be implemented using different programming languages, databases, hardware and software environment, depending on what fits best

</details>

### 10. 3-tier architecture

<details>
    <summary>
        Answer
    </summary>

Three-tier architecture is a client–server software architecture pattern in which the user interface (**presentation**), functional process logic ("**business rules**"), computer data storage and **data access** are developed and maintained as independent modules, most often on separate platforms.

</details>

### 11. Composition over inheritance?

<details>
    <summary>
        Answer
    </summary>

Principle that classes should achieve polymorphic behavior and code reuse by their composition (by containing instances of other classes that implement the desired functionality) rather than inheritance from a base or parent class

</details>

### 12. Can you explain what is _deadly diamond of death_?

<details>
    <summary>
        Answer
    </summary>

The "diamond problem" (sometimes referred to as the "deadly diamond of death"[5]) is an ambiguity that arises when two classes B and C inherit from A, and class D inherits from both B and C. If there is a method in A that B and C have overridden, and D does not override it, then which version of the method does D inherit: that of B, or that of C?

</details>
