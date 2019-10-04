## Lambdas and Functional Interfaces


Today in class we learned that a lambda expression is a function which can be 
created without belonging to any class. A lambda expression can be passed around 
as if it was an object and executed on demand. It is Java's attempt at Functional 
Programming and implements single method interfaces, or functional interfaces. 

How do you know when you can use a functional interface with a Lambda Expression?

* Does the interface have only one abstract (unimplemented) method?


* Does the parameters of the lambda expression match the parameters of the single method?


* Does the return type of the lambda expression match the return type of the single method? 

If so, then the interface can be paired with the lambda expression. 

### Some examples of Funtional Interfaces include :

    * Runnable
    * ActionListener
    * Comparable
    * Square
    * Predicate
    * BinaryOperator
    * Function

**@FunctionalInterface** annotation is used to ensure that the functional interface can’t have more than one abstract method. 

*The java.util.function package contains many builtin functional interfaces in Java 8.*
