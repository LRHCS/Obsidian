-   The `==` operator compares references. More precisely, it tests _reference_ equality. Two references are == if they point to the same storage in memory. In terms of the snapshot diagrams we’ve been drawing, two references are `==` if their arrows point to the same object bubble.
-   The `equals()` operation compares object contents – in other words, _object_ equality, in the sense that we’ve been talking about in this reading. The equals operation has to be defined appropriately for every abstract data type.

![[Pasted image 20230129102332.png]]