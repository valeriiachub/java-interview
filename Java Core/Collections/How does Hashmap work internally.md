## **How Hashmap works internally?**
**Default capacity**: 16 buckets.
**Load factor**: 0.75f

There are four constructors:

-    `HashMap(int initialCapacity, float loadFactor);`
- `HashMap(int initialCapacity);`
- `HashMap();`
- `HashMap(Map<? extends K, ? extends V>);`


----------
**What will happen in the situation when we have collision + equals objects? Insertion, replacement, nothing?**
Map.put() method's javadoc states:

> Associates the specified value with the specified key in this map. If
> the map previously contained a mapping for the key, **the old value is**
> **replaced**.
----------
**Does HashMap allows null keys/values?**
HashMap allows one null key and any number of null values.


----------
**Explain bucket's index calculation process**
From JDK:

    h & (length-1)

it's super-fast variant of

    h % length
----------
How does the `get(Object key)` method works?

 1. Hashcode of the key is calculated.
 2. `hashcode % capacity` = index in the array.
 3. Search the value in the bucket.
----------
How does `put(K, V)` method works?

1. Calculate hashcode of key
2. If basket with that hashcode is present then use the equals method on the key search the keys i that basket to determine if the element is to be added or replace.
3. If not there then create new basket (rehashing) and add that element to that.


----------
**How can we lost value?**

 - Mutable key.
 - Multithreading(one thread do `remove(Object key, Object value)` and another tries to find it.