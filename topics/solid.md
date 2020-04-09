# SOLID
This is an acronym, which refers to:

S: The Single Responsibility Principle 

O: The Open/Closed Principle 

L: The Liskov Substitution Principle 

I: The Interface Segregation Principle 

D: The Dependency Inversion Principle


These are key principles in Object-Oriented Programming. Design principles such as these should be able to aid developers build more maintainable systems.

## The Single Responsibility Principle 

Every module or class should have a single responsibility only.

The first of the 'SOLID' principles. This principle suggests that modules or classes should do one thing and one thing only. In more practical terms, this means that a single, small change to a feature of a program should require a change in one component only. For example, changing how a password is validated for complexity should require a change in only one part of the program.

Theoretically, this should make the code more robust, and easier to change. Knowing that a component which is being changed has a single responsibility only means that testing that change should be easier. Using the earlier example, changing the password complexity component should only be able to affect the features which relate to password complexity. It can be much more difficult to reason about the impact of a change to a component which has many responsibilities.

## The Open/Closed Principle

Entities should be open for extension and closed for modification.

The second of the 'SOLID' principles. This principle states that entities (which could be classes, modules, functions and so on) should be able to have their behaviour extended, but that their existing behaviour should not be able to be modified.

As a hypothetical example, imagine a module which is able to turn a Markdown document into HTML. If the module could be extended to handle a newly proposed markdown feature, without modifying the module internals, then it would be open for extension. If the module could not be modified by a consumer so that how existing Markdown features are handled, then it would be closed for modification.

This principle has particular relevance for object-oriented programming, where we may design objects to be easily extended, but would avoid designing objects which can have their existing behaviour changed in unexpected ways.

 
## The Liskov Substitution Principle 

It should be possible to replace a type with a subtype, without breaking the system.

The third of the 'SOLID' principles. This principle states that if a component relies on a type, then it should be able to use subtypes of that type, without the system failing or having to know the details of what that subtype is.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. If the method uses a base type 'file', then anything which derives from 'file' should be able to be used in the function. If 'file' supports seeking in reverse, and the XML parser uses that function, but the derived type 'network file' fails when reverse seeking is attempted, then the 'network file' would be violating the principle.

This principle has particular relevance for object-oriented programming, where type hierarchies must be modeled carefully to avoid confusing users of a system.
 

No client should be forced to depend on methods it does not use.

## The Interface Segregation Principle

The fourth of the 'SOLID' principles. This principle states that consumers of a component should not depend on functions of that component which it doesn't actually use. ISP splits interfaces that are very large into smaller and more specific ones so that clients will only have to know about the methods that are of interest to them.

As an example, imagine we have a method which reads an XML document from a structure which represents a file. It only needs to read bytes, move forwards or move backwards in the file. If this method needs to be updated because an unrelated feature of the file structure changes (such as an update to the permissions model used to represent file security), then the principle has been invalidated. It would be better for the file to implement a 'seekable-stream' interface, and for the XML reader to use that.

This principle has particular relevance for object-oriented programming, where interfaces, hierarchies and abstract types are used to minimise the coupling between different components. Duck typing is a methodology which enforces this principle by eliminating explicit interfaces.

 
## The Dependency Inversion Principle

High-level modules should not be dependent on low-level implementations.

The fifth of the 'SOLID' principles. This principle states that higher level orchestrating components should not have to know the details of their dependencies.

As an example, imagine we have a program which read metadata from a website. We would assume that the main component would have to know about a component to download the webpage content, then a component which can read the metadata. If we were to take dependency inversion into account, the main component would depend only on an abstract component which can fetch byte data, and then an abstract component which would be able to read metadata from a byte stream. The main component would not know about TCP/IP, HTTP, HTML, etc.

This principle is complex, as it can seem to 'invert' the expected dependencies of a system (hence the name). In practice, it also means that a separate orchestrating component must ensure the correct implementations of abstract types are used (e.g. in the previous example, something must still provide the metadata reader component a HTTP file downloader and HTML meta tag reader). This then touches on patterns such as Inversion of Control and Dependency Injection.

 
Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

## The DRY Principle

DRY is an acronym for Don't Repeat Yourself. This principle aims to help developers reducing the repetition of code and keep the information in a single place and was cited in 1999 by Andrew Hunt and Dave Thomas in the book The Pragmatic Developer

The opposite of DRY would be WET (Write Everything Twice or We Enjoy Typing).

In practice, if you have the same piece of information in two (or more) different places, you can use DRY to merge them into a single one and reuse it wherever you want/need.

 
## The KISS principle
Keep it simple, stupid

The KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore, simplicity should be a key goal in design, and unnecessary complexity should be avoided. Originating in the U.S. Navy in 1960, the phrase has been associated with aircraft engineer Kelly Johnson.

The principle is best exemplified by the story of Johnson handing a team of design engineers a handful of tools, with the challenge that the jet aircraft they were designing must be repairable by an average mechanic in the field under combat conditions with only these tools. Hence, the "stupid" refers to the relationship between the way things break and the sophistication of the tools available to repair them, not the capabilities of the engineers themselves.

 
## YAGNI
This is an acronym for You Aren't Gonna Need It.

Always implement things when you actually need them, never when you just foresee that you need them.

(Ron Jeffries) (XP co-founder and author of the book "Extreme Programming Installed")

This Extreme Programming (XP) principle suggests developers should only implement functionality that is needed for the immediate requirements, and avoid attempts to predict the future by implementing functionality that might be needed later.

Adhering to this principle should reduce the amount of unused code in the codebase, and avoid time and effort being wasted on functionality that brings no value.
