The data it contains has a "key" and "value"

The index is calculated by the **hash value** and **the size of the table**

![[Pasted image 20221224191653.png]]

If the index already contains a data, then in this index it will have a [[Linked List]]

![[Pasted image 20221224191744.png]]

##  unordered_map
- no ordering
- Hash Table

```cpp
    unordered_map<string, double> umap;

    umap["PI"] = 3.14;

    umap["root2"] = 1.414;

    umap["root3"] = 1.732;

    umap["log10"] = 2.302;

    umap["loge"] = 1.0;

   `// itr works as a pointer to`

    `// pair<string, double> type`

    `// itr->first stores the key part and`

    `// itr->second stores the value part`

    unordered_map<string, double>::iterator itr;

    for(itr= umap.begin(); itr != umap.end(); itr++){

        cout << itr->first << "  " <<

            itr->second << endl;

    }
```

## Map
- increasing  order
- Self balancing BST(red-black tree)

```cpp
 `// Ordered map`

    `std::map<``int``,` `int``> order;`

    `// Mapping values to keys`

    `order[5] = 10;`

    `order[3] = 5;`

    `order[20] = 100;`

    `order[1] = 1;`

    `// Iterating the map and`

    `// printing ordered values`

    `for` `(``auto` `i = order.begin(); i`

         `!= order.end(); i++) {`

        `std::cout << i->first`

                  `<<` `" : "`

                  `<< i->second <<` `'\n'``;`

    `}`
```