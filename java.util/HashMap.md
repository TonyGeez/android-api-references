Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HashMap

```
open class HashMap<K : Any!, V : Any!> : AbstractMap<K, V>, Cloneable, Serializable, MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](https://developer.android.com/reference/kotlin/java/util/AbstractMap)\<K, V\> ||
| | ↳ | [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap#) |

| Known Direct Subclasses [LinkedHashMap](https://developer.android.com/reference/kotlin/java/util/LinkedHashMap) |---|---| | [LinkedHashMap](https://developer.android.com/reference/kotlin/java/util/LinkedHashMap) | Hash table and linked list implementation of the `Map` interface, with well-defined encounter order. | |
| --- | --- | --- | --- | --- | --- | --- |

Hash table based implementation of the `Map` interface. This implementation provides all of the optional map operations, and permits `null` values and the `null` key. (The `HashMap` class is roughly equivalent to `Hashtable`, except that it is unsynchronized and permits nulls.) This class makes no guarantees as to the order of the map; in particular, it does not guarantee that the order will remain constant over time.

This implementation provides constant-time performance for the basic operations (`get` and `put`), assuming the hash function disperses the elements properly among the buckets. Iteration over collection views requires time proportional to the "capacity" of the `HashMap` instance (the number of buckets) plus its size (the number of key-value mappings). Thus, it's very important not to set the initial capacity too high (or the load factor too low) if iteration performance is important.

An instance of `HashMap` has two parameters that affect its performance: *initial capacity* and *load factor* . The *capacity* is the number of buckets in the hash table, and the initial capacity is simply the capacity at the time the hash table is created. The *load factor* is a measure of how full the hash table is allowed to get before its capacity is automatically increased. When the number of entries in the hash table exceeds the product of the load factor and the current capacity, the hash table is *rehashed* (that is, internal data structures are rebuilt) so that the hash table has approximately twice the number of buckets.

As a general rule, the default load factor (.75) offers a good tradeoff between time and space costs. Higher values decrease the space overhead but increase the lookup cost (reflected in most of the operations of the `HashMap` class, including `get` and `put`). The expected number of entries in the map and its load factor should be taken into account when setting its initial capacity, so as to minimize the number of rehash operations. If the initial capacity is greater than the maximum number of entries divided by the load factor, no rehash operations will ever occur.

If many mappings are to be stored in a `HashMap` instance, creating it with a sufficiently large capacity will allow the mappings to be stored more efficiently than letting it perform automatic rehashing as needed to grow the table. Note that using many keys with the same `hashCode()` is a sure way to slow down performance of any hash table. To ameliorate impact, when keys are `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`, this class may use comparison order among keys to help break ties.

**Note that this implementation is not synchronized.** If multiple threads access a hash map concurrently, and at least one of the threads modifies the map structurally, it *must* be synchronized externally. (A structural modification is any operation that adds or deletes one or more mappings; merely changing the value associated with a key that an instance already contains is not a structural modification.) This is typically accomplished by synchronizing on some object that naturally encapsulates the map. If no such object exists, the map should be "wrapped" using the `https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedMap(kotlin.collections.MutableMap)` method. This is best done at creation time, to prevent accidental unsynchronized access to the map:

```kotlin
Map m = Collections.synchronizedMap(new HashMap(...));
```

The iterators returned by all of this class's "collection view methods" are *fail-fast* : if the map is structurally modified at any time after the iterator is created, in any way except through the iterator's own `remove` method, the iterator will throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException`. Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw `ConcurrentModificationException` on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness: *the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/HashMap#HashMap()()` Constructs an empty `HashMap` with the default initial capacity (16) and the default load factor (0.75). |
| `https://developer.android.com/reference/kotlin/java/util/HashMap#HashMap(kotlin.Int)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an empty `HashMap` with the specified initial capacity and the default load factor (0.75). |
| `https://developer.android.com/reference/kotlin/java/util/HashMap#HashMap(kotlin.Int,%20kotlin.Float)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, loadFactor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Constructs an empty `HashMap` with the specified initial capacity and load factor. |
| `https://developer.android.com/reference/kotlin/java/util/HashMap#HashMap(kotlin.collections.MutableMap)(m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>)` Constructs a new `HashMap` with the same mappings as the specified `Map`. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#clear()()` Removes all of the mappings from this map. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#clone()()` Returns a shallow copy of this `HashMap` instance: the keys and values themselves are not cloned. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#compute(java.util.HashMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V?, out V?>)` Attempts to compute a mapping for the specified key and its current mapped value, or `null` if there is no current mapping (optional operation). |
| --- | --- |
| open V | `https://developer.android.com/reference/kotlin/java/util/HashMap#computeIfAbsent(java.util.HashMap.K,%20java.util.function.Function)(key: K, mappingFunction: https://developer.android.com/reference/kotlin/java/util/function/Function<in K, out V>)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null` (optional operation). |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#computeIfPresent(java.util.HashMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V?>)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#containsKey(java.util.HashMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#containsKey(java.util.HashMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#containsValue(java.util.HashMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#containsValue(java.util.HashMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer<in K, in V>)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#get(java.util.HashMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#get(java.util.HashMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| --- | --- |
| open V | `https://developer.android.com/reference/kotlin/java/util/HashMap#getOrDefault(java.util.HashMap.K,%20java.util.HashMap.V)(key: K, defaultValue: V)` Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#isEmpty()()` Returns `true` if this map contains no key-value mappings. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#merge(java.util.HashMap.K,%20java.util.HashMap.V,%20java.util.function.BiFunction)(key: K, value: V, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in V, in V, out V?>)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value (optional operation). |
| --- | --- |
| open static [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap#)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/HashMap#newHashMap(kotlin.Int)(numMappings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new, empty HashMap suitable for the expected number of mappings. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#put(java.util.HashMap.K,%20java.util.HashMap.V)(key: K, value: V)` Associates the specified value with the specified key in this map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<out K, V>)` Copies all of the mappings from the specified map to this map. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#putIfAbsent(java.util.HashMap.K,%20java.util.HashMap.V)(key: K, value: V)` If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value (optional operation). |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#remove(java.util.HashMap.K)(key: K)` Removes the mapping for the specified key from this map if present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#remove(java.util.HashMap.K,%20java.util.HashMap.V)(key: K, value: V)` Removes the entry for the specified key only if it is currently mapped to the specified value (optional operation). |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#remove(java.util.HashMap.K)(key: K)` Removes the mapping for the specified key from this map if present. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/HashMap#replace(java.util.HashMap.K,%20java.util.HashMap.V)(key: K, value: V)` Replaces the entry for the specified key only if it is currently mapped to some value (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#replace(java.util.HashMap.K,%20java.util.HashMap.V,%20java.util.HashMap.V)(key: K, oldValue: V, newValue: V)` Replaces the entry for the specified key only if currently mapped to the specified value (optional operation). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractMap` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this map for equality. Returns `true` if the given object is also a map and the two maps represent the same mappings. More formally, two maps `m1` and `m2` represent the same mappings if `m1.entrySet().equals(m2.entrySet())`. This ensures that the `equals` method works properly across different implementations of the `Map` interface. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#hashCode()()` Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map's `entrySet()` view. This ensures that `m1.equals(m2)` implies that `m1.hashCode()==m2.hashCode()` for any two maps `m1` and `m2`, as required by the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#toString()()` Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's `entrySet` view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters `", "` (comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||

| Properties ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>\> | `https://developer.android.com/reference/kotlin/java/util/HashMap#entries:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | `https://developer.android.com/reference/kotlin/java/util/HashMap#keys:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/HashMap#size:kotlin.Int` Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/java/util/HashMap#values:kotlin.collections.MutableCollection` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. |

## Public constructors

### HashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HashMap()
```

Constructs an empty `HashMap` with the default initial capacity (16) and the default load factor (0.75).

### HashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HashMap(initialCapacity: Int)
```

Constructs an empty `HashMap` with the specified initial capacity and the default load factor (0.75).

| Parameters ||
|---|---|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the initial capacity is negative. |

### HashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HashMap(
    initialCapacity: Int, 
    loadFactor: Float)
```

Constructs an empty `HashMap` with the specified initial capacity and load factor.

| Parameters ||
|---|---|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial capacity |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the load factor |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the initial capacity is negative or the load factor is nonpositive |

### HashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
HashMap(m: MutableMap<out K, out V>)
```

Constructs a new `HashMap` with the same mappings as the specified `Map`. The `HashMap` is created with default load factor (0.75) and an initial capacity sufficient to hold the mappings in the specified `Map`.

| Parameters ||
|---|---|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out K, out V\>: the map whose mappings are to be placed in this map |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified map is null |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all of the mappings from this map. The map will be empty after this call returns.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Returns a shallow copy of this `HashMap` instance: the keys and values themselves are not cloned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a shallow copy of this map |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value, or `null` if there is no current mapping (optional operation). For example, to either create or append a `String` msg to a value mapping:

```kotlin
<code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code>
```
(Method `https://developer.android.com/reference/kotlin/java/util/Map#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` is often simpler to use for such purposes.)

<br />

If the remapping function returns `null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<in K, in V?, out V?\>: the remapping function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `compute` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null` (optional operation).

If the mapping function returns `null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in:

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new Value(f(k)));
  </code>
```

Or to implement a multi-value map, `Map<K,Collection<V>>`, supporting multiple values per key:

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v);
  </code>
```

The mapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the mapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `mappingFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)\<in K, out V\>: the mapping function to compute a value |

| Return ||
|---|---|
| `V` | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the mappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfAbsent` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the mapping function modified this map |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value (optional operation).

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<in K, in V, out V?\>: the remapping function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfPresent` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: K): Boolean
```

Returns `true` if this map contains a mapping for the specified key.

| Parameters ||
|---|---|
| `key` | K: The key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains a mapping for the specified key. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: K): Boolean
```

Returns `true` if this map contains a mapping for the specified key.

| Parameters ||
|---|---|
| `key` | K: The key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains a mapping for the specified key. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map maps one or more keys to the specified value |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map maps one or more keys to the specified value |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller.

| Parameters ||
|---|---|
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer)\<in K, in V\>: The action to be performed for each entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `(key==null ? k==null : key.equals(k))`, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

A return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/HashMap#containsKey(java.util.HashMap.K)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/HashMap#put(java.util.HashMap.K,%20java.util.HashMap.V)`

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `(key==null ? k==null : key.equals(k))`, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

A return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/HashMap#containsKey(java.util.HashMap.K)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/HashMap#put(java.util.HashMap.K,%20java.util.HashMap.V)`

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrDefault(
    key: K, 
    defaultValue: V
): V
```

Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key.

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |
| `defaultValue` | V: the default mapping of the key |

| Return ||
|---|---|
| `V` | the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this map contains no key-value mappings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains no key-value mappings |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value (optional operation). Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is `null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a `String msg` to a value mapping:

```kotlin
<code>map.merge(key, msg, String::concat)
  </code>
```

<br />

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the resulting value is to be associated |
| `value` | V: the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<in V, in V, out V?\>: the remapping function to recompute a value if present |
| --- | --- |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if no value is associated with the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys or the value or remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `merge` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### newHashMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> newHashMap(numMappings: Int): HashMap<K, V>
```

Creates a new, empty HashMap suitable for the expected number of mappings. The returned map uses the default load factor of 0.75, and its initial capacity is generally large enough so that the expected number of mappings can be added without resizing the map.

| Parameters ||
|---|---|
| `<K>` | the type of keys maintained by the new map |
| `<V>` | the type of mapped values |
| `numMappings` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the expected number of mappings |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/HashMap#<K, V>` | the newly created map |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if numMappings is negative |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: K, 
    value: V
): V?
```

Associates the specified value with the specified key in this map. If the map previously contained a mapping for the key, the old value is replaced.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `value` | V: value to be associated with the specified key |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null and this map does not permit null keys or values |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this map. These mappings will replace any mappings that this map had for any of the keys currently in the specified map.

| Parameters ||
|---|---|
| `m` | mappings to be stored in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putAll` operation is not supported by this map |

### putIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putIfAbsent(
    key: K, 
    value: V
): V?
```

If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value (optional operation).

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `value` | V: value to be associated with the specified key |

| Return ||
|---|---|
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key. (A `null` return can also indicate that the map previously associated `null` with the key, if the implementation supports null values.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putIfAbsent` operation is not supported by this map (java.util.Collection#) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for the specified key from this map if present.

| Parameters ||
|---|---|
| `key` | K: key whose mapping is to be removed from the map |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(
    key: K, 
    value: V
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value (optional operation).

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is associated |
| `value` | V: value expected to be associated with the specified key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value was removed |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map (java.util.Collection#) |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for the specified key from this map if present.

| Parameters ||
|---|---|
| `key` | K: key whose mapping is to be removed from the map |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: K, 
    value: V
): V?
```

Replaces the entry for the specified key only if it is currently mapped to some value (optional operation).

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is associated |
| `value` | V: value to be associated with the specified key |

| Return ||
|---|---|
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key. (A `null` return can also indicate that the map previously associated `null` with the key, if the implementation supports null values.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replace` operation is not supported by this map (java.util.Collection#) |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value (optional operation).

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is associated |
| `oldValue` | V: value expected to be associated with the specified key |
| `newValue` | V: value to be associated with the specified key |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value was replaced |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if oldValue is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replace` operation is not supported by this map (java.util.Collection#) |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). Exceptions thrown by the function are relayed to the caller.

| Parameters ||
|---|---|
| `function` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction)\<in K, in V, out V\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | a set view of the mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val keys: MutableSet<K>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | a set view of the keys contained in this map |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of key-value mappings in this map.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val values: MutableCollection<V>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a view of the values contained in this map |
