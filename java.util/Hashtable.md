# Hashtable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Hashtable

```
open class Hashtable<K : Any!, V : Any!> : Dictionary<K, V>, Cloneable, MutableMap<K, V>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Dictionary](https://developer.android.com/reference/kotlin/java/util/Dictionary)\<K, V\> ||
| | ↳ | [java.util.Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable#) |

| Known Direct Subclasses [Properties](https://developer.android.com/reference/kotlin/java/util/Properties) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------| | [Properties](https://developer.android.com/reference/kotlin/java/util/Properties) | The`Properties`class represents a persistent set of properties. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider.html#), [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) |-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AuthProvider](https://developer.android.com/reference/kotlin/java/security/AuthProvider.html#) | Legacy security code; do not use. | | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) | This class represents a "provider" for the Java Security API, where a provider implements some or all parts of Java Security. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class implements a hash table, which maps keys to values. Any non-`null`object can be used as a key or as a value.

To successfully store and retrieve objects from a hashtable, the objects used as keys must implement the`hashCode`method and the`equals`method.

An instance of`Hashtable`has two parameters that affect its performance:*initial capacity* and*load factor* . The*capacity* is the number of*buckets* in the hash table, and the*initial capacity* is simply the capacity at the time the hash table is created. Note that the hash table is*open* : in the case of a "hash collision", a single bucket stores multiple entries, which must be searched sequentially. The*load factor*is a measure of how full the hash table is allowed to get before its capacity is automatically increased. The initial capacity and load factor parameters are merely hints to the implementation. The exact details as to when and whether the rehash method is invoked are implementation-dependent.

Generally, the default load factor (.75) offers a good tradeoff between time and space costs. Higher values decrease the space overhead but increase the time cost to look up an entry (which is reflected in most`Hashtable`operations, including`get`and`put`).

The initial capacity controls a tradeoff between wasted space and the need for`rehash`operations, which are time-consuming. No`rehash`operations will*ever* occur if the initial capacity is greater than the maximum number of entries the`Hashtable`will contain divided by its load factor. However, setting the initial capacity too high can waste space.

If many entries are to be made into a`Hashtable`, creating it with a sufficiently large capacity may allow the entries to be inserted more efficiently than letting it perform automatic rehashing as needed to grow the table.

This example creates a hashtable of numbers. It uses the names of the numbers as keys: 

```kotlin
<code>Hashtable&lt;String, Integer&gt; numbers
      = new Hashtable&lt;String, Integer&gt;();
    numbers.put("one", 1);
    numbers.put("two", 2);
    numbers.put("three", 3);</code>
```

To retrieve a number, use the following code: 

```kotlin
<code>Integer n = numbers.get("two");
    if (n != null) {
      System.out.println("two = " + n);
    }</code>
```

The iterators returned by the`iterator`method of the collections returned by all of this class's "collection view methods" are*fail-fast* : if the Hashtable is structurally modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the iterator will throw a [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future. The Enumerations returned by Hashtable's [keys](https://developer.android.com/reference/kotlin/java/util/Hashtable#keys())and [elements](https://developer.android.com/reference/kotlin/java/util/Hashtable#elements())methods are*not*fail-fast; if the Hashtable is structurally modified at any time after the enumeration is created then the results of enumerating are undefined.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

As of the Java 2 platform v1.2, this class was retrofitted to implement the [Map](https://developer.android.com/reference/kotlin/java/util/Map) interface, making it a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework). Unlike the new collection implementations,`Hashtable`is synchronized. If a thread-safe implementation is not needed, it is recommended to use [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap) in place of`Hashtable`. If a thread-safe highly-concurrent implementation is desired, then it is recommended to use [java.util.concurrent.ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap) in place of`Hashtable`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable#Hashtable())`()` Constructs a new, empty hashtable with a default initial capacity (11) and load factor (0.75). |
| [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable#Hashtable(kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new, empty hashtable with the specified initial capacity and default load factor (0.75). |
| [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable#Hashtable(kotlin.Int,%20kotlin.Float))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loadFactor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a new, empty hashtable with the specified initial capacity and the specified load factor. |
| [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable#Hashtable(kotlin.collections.MutableMap))`(`t:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` `K,` `out` `V>!`)` Constructs a new hashtable with the same mappings as the given Map. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/Hashtable#clear())`()` Clears this hashtable so that it contains no keys. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/Hashtable#clone())`()` Creates a shallow copy of this hashtable. |
| openV? | [compute](https://developer.android.com/reference/kotlin/java/util/Hashtable#compute(java.util.Hashtable.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)<in` `K,` `in` `V?,` `out` `V?>`)` Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). |
| --- | --- |
| openV | [computeIfAbsent](https://developer.android.com/reference/kotlin/java/util/Hashtable#computeIfAbsent(java.util.Hashtable.K,%20java.util.function.Function))`(`key:` `K`, `mappingFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)<in` `K,` `out` `V>`)` If the specified key is not already associated with a value (or is mapped to`null`), attempts to compute its value using the given mapping function and enters it into this map unless`null`. |
| openV? | [computeIfPresent](https://developer.android.com/reference/kotlin/java/util/Hashtable#computeIfPresent(java.util.Hashtable.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)<in` `K,` `in` `V,` `out` `V?>`)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/Hashtable#contains(kotlin.Any))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Tests if some key maps into the specified value in this hashtable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/java/util/Hashtable#containsKey(java.util.Hashtable.K))`(`key:` `K`)` Tests if the specified object is a key in this hashtable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](https://developer.android.com/reference/kotlin/java/util/Hashtable#containsValue(java.util.Hashtable.V))`(`value:` `V`)` Returns true if this hashtable maps one or more keys to this value. |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<V\>! | [elements](https://developer.android.com/reference/kotlin/java/util/Hashtable#elements())`()` Returns an enumeration of the values in this hashtable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/Hashtable#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified Object with this Map for equality, as per the definition in the Map interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/Hashtable#forEach(java.util.function.BiConsumer))`(`action:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer)<in` `K,` `in` `V>`)` <br /> |
| openV? | [get](https://developer.android.com/reference/kotlin/java/util/Hashtable#get(java.util.Hashtable.K))`(`key:` `K`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| --- | --- |
| openV | [getOrDefault](https://developer.android.com/reference/kotlin/java/util/Hashtable#getOrDefault(java.util.Hashtable.K,%20java.util.Hashtable.V))`(`key:` `K`, `defaultValue:` `V`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/Hashtable#hashCode())`()` Returns the hash code value for this Map as per the definition in the Map interface. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/Hashtable#isEmpty())`()` Tests if this hashtable maps no keys to values. |
| --- | --- |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<K\>! | [keys](https://developer.android.com/reference/kotlin/java/util/Hashtable#keys())`()` Returns an enumeration of the keys in this hashtable. |
| openV? | [merge](https://developer.android.com/reference/kotlin/java/util/Hashtable#merge(java.util.Hashtable.K,%20java.util.Hashtable.V,%20java.util.function.BiFunction))`(`key:` `K`, `value:` `V`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)<in` `V,` `in` `V,` `out` `V?>`)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. |
| openV? | [put](https://developer.android.com/reference/kotlin/java/util/Hashtable#put(java.util.Hashtable.K,%20java.util.Hashtable.V))`(`key:` `K`, `value:` `V`)` Maps the specified`key`to the specified`value`in this hashtable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](https://developer.android.com/reference/kotlin/java/util/Hashtable#putAll(kotlin.collections.Map))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<out` `K,` `V>`)` Copies all of the mappings from the specified map to this hashtable. |
| openV? | [putIfAbsent](https://developer.android.com/reference/kotlin/java/util/Hashtable#putIfAbsent(java.util.Hashtable.K,%20java.util.Hashtable.V))`(`key:` `K`, `value:` `V`)` <br /> |
| openV? | [remove](https://developer.android.com/reference/kotlin/java/util/Hashtable#remove(java.util.Hashtable.K))`(`key:` `K`)` Removes the key (and its corresponding value) from this hashtable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/Hashtable#remove(java.util.Hashtable.K,%20java.util.Hashtable.V))`(`key:` `K`, `value:` `V`)` <br /> |
| openV? | [replace](https://developer.android.com/reference/kotlin/java/util/Hashtable#replace(java.util.Hashtable.K,%20java.util.Hashtable.V))`(`key:` `K`, `value:` `V`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](https://developer.android.com/reference/kotlin/java/util/Hashtable#replace(java.util.Hashtable.K,%20java.util.Hashtable.V,%20java.util.Hashtable.V))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/Hashtable#replaceAll(java.util.function.BiFunction))`(`function:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)<in` `K,` `in` `V,` `out` `V>`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/Hashtable#toString())`()` Returns a string representation of this`Hashtable`object in the form of a set of entries, enclosed in braces and separated by the ASCII characters "` , `" (comma and space). |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rehash](https://developer.android.com/reference/kotlin/java/util/Hashtable#rehash())`()` Increases the capacity of and internally reorganizes this hashtable, in order to accommodate and access its entries more efficiently. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](https://developer.android.com/reference/kotlin/java/util/Hashtable#entries:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](https://developer.android.com/reference/kotlin/java/util/Hashtable#keys:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/Hashtable#size:kotlin.Int) Returns the number of keys in this hashtable. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](https://developer.android.com/reference/kotlin/java/util/Hashtable#values:kotlin.collections.MutableCollection) Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) view of the values contained in this map. |

## Public constructors

### Hashtable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Hashtable()
```

Constructs a new, empty hashtable with a default initial capacity (11) and load factor (0.75). 

### Hashtable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Hashtable(initialCapacity: Int)
```

Constructs a new, empty hashtable with the specified initial capacity and default load factor (0.75).

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the hashtable. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero. |

### Hashtable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Hashtable(
    initialCapacity: Int, 
    loadFactor: Float)
```

Constructs a new, empty hashtable with the specified initial capacity and the specified load factor.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the hashtable. |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the load factor of the hashtable. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero, or if the load factor is nonpositive. |

### Hashtable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Hashtable(t: MutableMap<out K, out V>!)
```

Constructs a new hashtable with the same mappings as the given Map. The hashtable is created with an initial capacity sufficient to hold the mappings in the given Map and a default load factor (0.75).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `t` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<outK,outV\>!:the map whose mappings are to be placed in this map. |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if the specified map is null. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Clears this hashtable so that it contains no keys.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates a shallow copy of this hashtable. All the structure of the hashtable itself is copied, but the keys and values are not cloned. This is a relatively expensive operation.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of the hashtable |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). For example, to either create or append a`String`msg to a value mapping: 

```kotlin
<code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code>
```
(Method [merge()](https://developer.android.com/reference/kotlin/java/util/Map#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction))is often simpler to use for such purposes.)

<br />

If the remapping function returns`null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if the remapping function modified this map during computation.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<inK,inV?,outV?\>:the remapping function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value (or is mapped to`null`), attempts to compute its value using the given mapping function and enters it into this map unless`null`.

If the mapping function returns`null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in: 

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new Value(f(k)));
  </code>
```

Or to implement a multi-value map,`Map<K,Collection<V>>`, supporting multiple values per key: 

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v);
  </code>
```

The mapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if the mapping function modified this map during computation.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `mappingFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)\<inK,outV\>:the mapping function to compute a value |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------------|
| V | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the mappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the mapping function modified this map |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value.

If the remapping function returns`null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if the remapping function modified this map during computation.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<inK,inV,outV?\>:the remapping function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(value: Any!): Boolean
```

Tests if some key maps into the specified value in this hashtable. This operation is more expensive than the [containsKey](https://developer.android.com/reference/kotlin/java/util/Hashtable#containsKey(java.util.Hashtable.K))method.

Note that this method is identical in functionality to [containsValue](https://developer.android.com/reference/kotlin/java/util/Hashtable#containsValue(java.util.Hashtable.V)), (which is part of the [Map](https://developer.android.com/reference/kotlin/java/util/Map) interface in the collections framework).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a value to search for |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if some key maps to the`value`argument in this hashtable as determined by the`equals`method;`false`otherwise. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if the value is`null` |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K): Boolean
```

Tests if the specified object is a key in this hashtable.

| Parameters ||
|-------|----------------|
| `key` | K:possible key |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified object is a key in this hashtable, as determined by the`equals`method;`false`otherwise. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the key is`null` |

**See Also**

- [#contains(Object)](https://developer.android.com/reference/kotlin/java/util/Hashtable#contains(kotlin.Any)) 

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: V): Boolean
```

Returns true if this hashtable maps one or more keys to this value.

Note that this method is identical in functionality to [contains](https://developer.android.com/reference/kotlin/java/util/Hashtable#contains(kotlin.Any))(which predates the [Map](https://developer.android.com/reference/kotlin/java/util/Map) interface).

| Parameters ||
|---------|----------------------------------------------------------|
| `value` | V:value whose presence in this hashtable is to be tested |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to the specified value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the value is`null` |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elements(): Enumeration<V>!
```

Returns an enumeration of the values in this hashtable. Use the Enumeration methods on the returned object to fetch the elements sequentially. If the hashtable is structurally modified while enumerating over the values then the results of enumerating are undefined.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<V>! | an enumeration of the values in this hashtable. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)
- <https://developer.android.com/reference/kotlin/java/util/Hashtable#keys()>
- [#values()](https://developer.android.com/reference/kotlin/java/util/Hashtable#values:kotlin.collections.MutableCollection)
- [java.util.Map](https://developer.android.com/reference/kotlin/java/util/Map) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified Object with this Map for equality, as per the definition in the Map interface.

| Parameters ||
|-------|--------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this hashtable |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified Object is equal to this Map |

**See Also**

- [java.util.Map#equals(Object)](https://developer.android.com/reference/kotlin/java/util/Hashtable#) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer)\<inK,inV\>:The action to be performed for each entry |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`(key.equals(k))`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

| Parameters ||
|-------|----------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |

| Return ||
|----|-----------------------------------------------------------------------------------------------------|
| V? | the value to which the specified key is mapped, or`null`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |

**See Also**

- [#put(Object, Object)](https://developer.android.com/reference/kotlin/java/util/Hashtable#put(java.util.Hashtable.K,%20java.util.Hashtable.V)) 

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrDefault(
    key: K, 
    defaultValue: V
): V
```

| Parameters ||
|----------------|----------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |
| `defaultValue` | V:the default mapping of the key |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------|
| V | the value to which the specified key is mapped, or`defaultValue`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this Map as per the definition in the Map interface.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this map |

**See Also**

- [java.util.Map#hashCode()](https://developer.android.com/reference/kotlin/java/util/Hashtable#) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Tests if this hashtable maps no keys to values.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this hashtable maps no keys to values;`false`otherwise. |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keys(): Enumeration<K>!
```

Returns an enumeration of the keys in this hashtable. Use the Enumeration methods on the returned object to fetch the keys sequentially. If the hashtable is structurally modified while enumerating over the keys then the results of enumerating are undefined.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<K>! | an enumeration of the keys in this hashtable. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)
- <https://developer.android.com/reference/kotlin/java/util/Hashtable#elements()>
- [#keySet()](https://developer.android.com/reference/kotlin/java/util/Hashtable#keys:kotlin.collections.MutableSet)
- [java.util.Map](https://developer.android.com/reference/kotlin/java/util/Map) 

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is`null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a`String msg`to a value mapping: 

```kotlin
<code>map.merge(key, msg, String::concat)
  </code>
```

<br />

If the remapping function returns`null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if the remapping function modified this map during computation.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the resulting value is to be associated |
| `value` | V:the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<inV,inV,outV?\>:the remapping function to recompute a value if present |
| --- | --- |

| Return ||
|----|-------------------------------------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if no value is associated with the key |

| Exceptions ||
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys or the value or remappingFunction is null |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: K, 
    value: V
): V?
```

Maps the specified`key`to the specified`value`in this hashtable. Neither the key nor the value can be`null`.

The value can be retrieved by calling the`get`method with a key that is equal to the original key.

| Parameters ||
|---------|---------------------|
| `key` | K:the hashtable key |
| `value` | V:the value |

| Return ||
|----|-------------------------------------------------------------------------------------------|
| V? | the previous value of the specified key in this hashtable, or`null`if it did not have one |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the key or value is`null` |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

**See Also**

- [java.lang.Object#equals(Object)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))
- [#get(Object)](https://developer.android.com/reference/kotlin/java/util/Hashtable#get(java.util.Hashtable.K)) 

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this hashtable. These mappings will replace any mappings that this hashtable had for any of the keys currently in the specified map.

| Parameters ||
|-----|-----------------------------------|
| `m` | mappings to be stored in this map |
| `t` | mappings to be stored in this map |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### putIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putIfAbsent(
    key: K, 
    value: V
): V?
```

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key. (A`null`return can also indicate that the map previously associated`null`with the key, if the implementation supports null values.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K): V?
```

Removes the key (and its corresponding value) from this hashtable. This method does nothing if the key is not in the hashtable.

| Parameters ||
|-------|------------------------------------|
| `key` | K:the key that needs to be removed |

| Return ||
|----|---------------------------------------------------------------------------------------------------------|
| V? | the value to which the key had been mapped in this hashtable, or`null`if the key did not have a mapping |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the key is`null` |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| --- | --- |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(
    key: K, 
    value: V
): Boolean
```

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value expected to be associated with the specified key |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| --- | --- |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    key: K, 
    value: V
): V?
```

| Parameters ||
|---------|----------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key. (A`null`return can also indicate that the map previously associated`null`with the key, if the implementation supports null values.) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

| Parameters ||
|------------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `oldValue` | V:value expected to be associated with the specified key |
| `newValue` | V:value to be associated with the specified key |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was replaced |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if oldValue is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `function` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<inK,inV,outV\>:the function to apply to each entry |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this map's entry set iterator. |
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this`Hashtable`object in the form of a set of entries, enclosed in braces and separated by the ASCII characters "` , `" (comma and space). Each entry is rendered as the key, an equals sign`=`, and the associated element, where the`toString`method is used to convert the key and element to strings.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this hashtable |

## Protected methods

### rehash

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun rehash(): Unit
```

Increases the capacity of and internally reorganizes this hashtable, in order to accommodate and access its entries more efficiently. This method is called automatically when the number of keys in the hashtable exceeds this hashtable's capacity and load factor.

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the mappings contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation, or through the`setValue`operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<K>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | a set view of the keys contained in this map |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of keys in this hashtable.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of keys in this hashtable. |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val values: MutableCollection<V>
```

Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map |
