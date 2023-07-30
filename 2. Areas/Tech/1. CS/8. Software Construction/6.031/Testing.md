#java #testing

-   **Correct**. A correct test suite is a legal client of the specification, and it accepts all legal implementations of the spec without complaint. This gives us the freedom to change how the module is implemented internally without necessarily having to change the test suite.
    
-   **Thorough**. A thorough test suite finds actual bugs in the implementation, caused by mistakes that programmers are likely to make.
    
-   **Small**. A small test suite, with few test cases, is faster to write in the first place, and easier to update if the specification evolves. Small test suites are also faster to run. You will be able to run your tests more frequently if your test suites are small and fast.


we divide the input space into _subdomains_, each consisting of a set of inputs. (The name _subdomain_ comes from the fact that it is a subset of the _domain_, the input space of a mathematical function.) Taken together, the subdomains form a _partition_: a collection of disjoint sets that completely covers the input space, so that every input lies in exactly one subdomain. Then we choose one test case from each subdomain, and that’s our test suite.

The idea behind subdomains is to divide the input space into sets of similar inputs on which the program has similar behavior. Then we use one representative of each set. This approach makes the best use of limited testing resources by choosing dissimilar test cases, and forcing the testing to explore areas of the input space that random testing might not reach.


```java
public class MaxTest {
  /*
   * Testing strategy
   *
   * partition:
   *    a < b
   *    a > b
   *    a = b
   */


  @Test
  public void testALessThanB() {
      assertEquals(2, Math.max(1, 2));
  }

  @Test
  public void testBothEqual() {
      assertEquals(9, Math.max(9, 9));
  }

  @Test
  public void testAGreaterThanB() {
      assertEquals(10, Math.max(10, -9));
  }
}
```


```java
public class Multiply {
  /*
   * Testing strategy
   *
   * cover the cartesian product of these partitions:
   *   partition on a: positive, negative, 0
   *   partition on b: positive, negative, 0
   *   partition on a: 1, !=1
   *   partition on b: 1, !=1
   *   partition on a: small (fits in a long value), or large (doesn't fit)
   *   partition on b: small, large
   * 
   * cover the subdomains of these partitions:
   *   partition on signs of a and b:
   *      both positive
   *      both negative
   *      different signs
   *      one or both are 0
   */
```

  
**Black box testing** means choosing test cases only from the specification, not the implementation of the function. That’s what we’ve been doing in our examples so far. We partitioned and looked for boundaries in `abs`, `max`, and `multiply` without looking at the actual code for these functions. In fact, following the test-first programming approach, we hadn’t even _written_ the code for these functions yet.
**Glass box testing** means choosing test cases with knowledge of how the function is actually implemented. For example, if the implementation selects different algorithms depending on the input, then you should partition around the points where different algorithms are chosen. If the implementation keeps an internal cache that remembers the answers to previous inputs, then you should test repeated inputs.