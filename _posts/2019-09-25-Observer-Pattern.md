# What is the Observer Pattern?

A design pattern that defines a one-to-many dependency between objects so that when one object changes state, all of its 
dependents are automatically notified and updated.    

*It is one of the most heavily used patterns in the Java development kit.*

The object that is being watched is referred to as the ``subject``. The objects that are watching the changes are called the ``observers``.


When using an observer, ``Subject`` and ``Observer`` objects must be defined. There are a few different ways to implement Observer Pattern. Most use a class design that will include Subject and Observer interfaces. 

## Properties of the Observer Pattern

- The responsibility of the subject is to maintain a list of the observers and to notify them of states changes by calling their
`update()` operation.

- The responsibility of the observer is to register themselves on a subject and to update their state changes when they are notified.

- The subject and observers have no knowledge of each other. 

- Observers can be added and removed independently
at run time.

- An observable object can have one or more observers.

- The observer pattern provides and object design where subjects and observers are *loosely coupled*, meaning the objects can interact but know little about each other.  

### How Dependency Comes Into Play

The subject is the sole owner of the data and observers are dependent on the subject to update them when the data changes.

New observers can be added at any time because the subject only depends on the list of objects that implement the Observer interface.

Because subjects and observers are loosely coupled, changes to either will not affect the other, as long as the objects still implement the subject or observer interfaces. 

Loosely coupled designs allow programmers to build flexible object oriented systems because the interpedency between objects is minimized. 

### How is the Observer Pattern Implemented in Java Language?

* Objects can register (and remove themselves) as observers in the `Subject Interface`
    * ex: registerObserver(), removeObserver(), notifyObserver()
    
* All potential observers need to implement the `Observer Interface`
    * Observer interface only has one method, `update()`, that gets called when the Subject's state changes
    
* Concrete subjects may also have methods for setting and getting its state
    * ex: getState(), setState()
