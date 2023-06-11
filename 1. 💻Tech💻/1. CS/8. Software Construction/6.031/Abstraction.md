  
Abstract data types are an instance of a general principle in software engineering, which goes by many names with slightly different shades of meaning. Here are some of the names that are used for this idea:

-   **Abstraction.** Omitting or hiding low-level details with a simpler, higher-level idea.
-   **Modularity.** Dividing a system into components or modules, each of which can be designed, implemented, tested, reasoned about, and reused separately from the rest of the system.
-   **Encapsulation.** Building a wall around a module so that the module is responsible for its own internal behavior, and bugs in other parts of the system can’t damage its integrity.
-   **Information hiding.** Hiding details of a module’s implementation from the rest of the system, so that those details can be changed later without changing the rest of the system.
-   **Separation of concerns.** Making a feature (or “concern”) the responsibility of a single module, rather than spreading it across multiple modules.

The operations of an abstract type are classified as follows:

-   **Creators** create new objects of the type. A creator may take values of other types as arguments, but not an object of the type being constructed.
-   **Producers** also create new objects of the type, but require one or more existing objects of the type as input. The `concat` method of `String`, for example, is a producer: it takes two strings and produces a new string representing their concatenation.
-   **Observers** take objects of the abstract type and return objects of a different type. The `size` method of `List`, for example, returns an `int`.
-   **Mutators** change objects. The `add` method of `List`, for example, mutates a list by adding an element to the end.

We can summarize these distinctions schematically like this (explanation to follow):

-   creator : t* → T
-   producer : T+, t* → T
-   observer : T+, t* → t
-   mutator : T+, t* → void | t | T


It’s better to have **a few, simple operations** that can be combined in powerful ways, rather than lots of complex operations.


In Java, we can use `private final` to make a data immutable(can't be changed)

- rep
- rep invariant
	- describe the factors that will cause an error in this class

## Why interfaces?

Interfaces are used pervasively in real Java code. Not every class is associated with an interface, but there are a few good reasons to bring an interface into the picture.

-   **Documentation for both the compiler and for humans**. Not only does an interface help the compiler catch ADT implementation bugs, but it is also much more useful for a human to read than the code for a concrete implementation. Such an implementation intersperses ADT-level types and specs with implementation details.
-   **Allowing performance trade-offs**. Different implementations of the ADT can provide methods with very different performance characteristics. Different applications may work better with different choices, but we would like to code these applications in a way that is representation-independent. From a correctness standpoint, it should be possible to drop in any new implementation of a key ADT with simple, localized code changes.
-   **Methods with intentionally underdetermined specifications**. An ADT for finite sets could leave unspecified the element order one gets when converting to a list. Some implementations might use slower method implementations that manage to keep the set representation in some sorted order, allowing quick conversion to a sorted list. Other implementations might make many methods faster by not bothering to support conversion to sorted lists.
-   **Multiple views of one class**. A Java class may implement multiple interfaces. For instance, a user interface widget displaying a drop-down list is natural to view as both a widget and a list. The class for this widget could implement both interfaces. In other words, we don’t always implement an ADT multiple times just because we are choosing different data structures. Those implementations may be various different sorts of objects that can be seen as special cases of the ADT.
-   **More and less trustworthy implementations**. Another reason to implement an interface more than once might be that it is easy to build a simple implementation that you believe is correct, while you can work harder to build a fancier version that is more likely to contain bugs. You can choose implementations for applications based on how bad it would be to get bitten by a bug.