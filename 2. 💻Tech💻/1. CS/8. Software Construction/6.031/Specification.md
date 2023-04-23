Specifications are good for the client of a module because they help make the module easier to understand. Having a specification lets you understand what the module does without having to read the module’s code. If you’re not convinced that reading a spec is easier than reading code, compare our spec for `find` on the left, with its tricky implementation on the right:
```java
/**
 * Find a value in an array.
 * @param arr array to search, requires that val occurs exactly once
 *            in arr
 * @param val value to search for
 * @return index i such that arr[i] = val
 */
static int find(int[] arr, int val)
```
```java
static int find(int[] arr, int val) {
    for (int i = 0, j = arr.length-1; i <= j; i++, j--) {
        if (arr[i] == val) return i;
        if (arr[j] == val) return j;
    }
    return -1;
}
```

Abstractly speaking, a _specification_ of a method has several parts:

-   a method signature, giving the name, parameter types, return type, and exceptions thrown
-   a _requires_ clause, describing additional restrictions on the parameters
-   an _effects_ clause, describing the return value, exceptions, and other effects of the method

  
Taken together, these parts form the _precondition_ and the _postcondition_ of the method.

The precondition is an obligation on the client (the caller of the method). It is a condition over the state in which the method is invoked. One aspect of the precondition is the number and types of the parameters in the method signature. Additional conditions are written down in the _requires_ clause, for example:

-   narrowing a parameter type (e.g. `x >= 0` to say that an `int` parameter x must actually be a nonnegative `int`)
-   interactions between parameters (e.g., `val` occurs exactly once in `arr`)

The postcondition is an obligation on the implementer of the method. It includes the parts that Java can statically check: the return type and declared checked exceptions. Additional conditions are written down in the _effects_ clause, including:

-   how the return value relates to the inputs
-   which exceptions are thrown, and when
-   whether and how objects are mutated


We talked then about _unit testing_, the idea that we should write tests of each module of our program in isolation. A good unit test is focused on just a single specification. Our tests will nearly always rely on the specs of Java library methods, but a unit test for one method we’ve written shouldn’t fail if a _different_ method fails to satisfy its spec. As we saw in the example, a test for `extract()` shouldn’t fail if `load()` doesn’t satisfy its postcondition.