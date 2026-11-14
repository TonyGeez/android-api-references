Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Map

```
interface Map<K : Any!, V : Any!>
```

| [java.util.Map](Map.md) |

An object that maps keys to values. A map cannot contain duplicate keys; each key can map to at most one value.

This interface takes the place of the `Dictionary` class, which was a totally abstract class rather than an interface.

The `Map` interface provides three *collection views* , which allow a map's contents to be viewed as a set of keys, collection of values, or set of key-value mappings. The *order* of a map is defined as the order in which the iterators on the map's collection views return their elements. Some map implementations, like the `TreeMap` class, make specific guarantees as to their encounter order; others, like the `HashMap` class, do not. Maps with a defined [encounter order](SequencedCollection.md) are generally subtypes of the `https://developer.android.com/reference/kotlin/java/util/SequencedMap` interface.

Note: great care must be exercised if mutable objects are used as map keys. The behavior of a map is not specified if the value of an object is changed in a manner that affects `equals` comparisons while the object is a key in the map. A special case of this prohibition is that it is not permissible for a map to contain itself as a key. While it is permissible for a map to contain itself as a value, extreme caution is advised: the `equals` and `hashCode` methods are no longer well defined on such a map.

All general-purpose map implementation classes should provide two "standard" constructors: a void (no arguments) constructor which creates an empty map, and a constructor with a single argument of type `Map`, which creates a new map with the same key-value mappings as its argument. In effect, the latter constructor allows the user to copy any map, producing an equivalent map of the desired class. There is no way to enforce this recommendation (as interfaces cannot contain constructors) but all of the general-purpose map implementations in the JDK comply.

The "destructive" methods contained in this interface, that is, the methods that modify the map on which they operate, are specified to throw `UnsupportedOperationException` if this map does not support the operation. If this is the case, these methods may, but are not required to, throw an `UnsupportedOperationException` if the invocation would have no effect on the map. For example, invoking the `https://developer.android.com/reference/kotlin/java/util/Map#putAll(kotlin.collections.MutableMap)` method on an unmodifiable map may, but is not required to, throw the exception if the map whose mappings are to be "superimposed" is empty.

Some map implementations have restrictions on the keys and values they may contain. For example, some implementations prohibit null keys and values, and some have restrictions on the types of their keys. Attempting to insert an ineligible key or value throws an unchecked exception, typically `NullPointerException` or `ClassCastException`. Attempting to query the presence of an ineligible key or value may throw an exception, or it may simply return false; some implementations will exhibit the former behavior and some will exhibit the latter. More generally, attempting an operation on an ineligible key or value whose completion would not result in the insertion of an ineligible element into the map may throw an exception or it may succeed, at the option of the implementation. Such exceptions are marked as "optional" in the specification for this interface.

Many methods in Collections Framework interfaces are defined in terms of the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method. For example, the specification for the `https://developer.android.com/reference/kotlin/java/util/Map#containsKey(kotlin.Any)` method says: "returns `true` if and only if this map contains a mapping for a key `k` such that `(key==null ? k==null : key.equals(k))`." This specification should *not* be construed to imply that invoking `Map.containsKey` with a non-null argument `key` will cause `key.equals(k)` to be invoked for any key `k`. Implementations are free to implement optimizations whereby the `equals` invocation is avoided, for example, by first comparing the hash codes of the two keys. (The `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()` specification guarantees that two objects with unequal hash codes cannot be equal.) More generally, implementations of the various Collections Framework interfaces are free to take advantage of the specified behavior of underlying `https://developer.android.com/reference/kotlin/java/lang/Object.html#` methods wherever the implementor deems it appropriate.

Some map operations which perform recursive traversal of the map may fail with an exception for self-referential instances where the map directly or indirectly contains itself. This includes the `clone()`, `equals()`, `hashCode()` and `toString()` methods. Implementations may optionally handle the self-referential scenario, however most current implementations do not do so.

## Unmodifiable Maps

The `https://developer.android.com/reference/kotlin/java/util/Map#of()`, `https://developer.android.com/reference/kotlin/java/util/Map#ofEntries(kotlin.collections.MutableMap.MutableEntry)`, and `https://developer.android.com/reference/kotlin/java/util/Map#copyOf(kotlin.collections.MutableMap)` static factory methods provide a convenient way to create unmodifiable maps. The `Map` instances created by these methods have the following characteristics:

- They are [*unmodifiable*](Collection.md). Keys and values cannot be added, removed, or updated. Calling any mutator method on the Map will always cause `UnsupportedOperationException` to be thrown. However, if the contained keys or values are themselves mutable, this may cause the Map to behave inconsistently or its contents to appear to change.
- They disallow `null` keys and values. Attempts to create them with `null` keys or values result in `NullPointerException`.
- They are serializable if all keys and values are serializable.
- They reject duplicate keys at creation time. Duplicate keys passed to a static factory method result in `IllegalArgumentException`.
- The iteration order of mappings is unspecified and is subject to change.
- They are [value-based](../java/lang/doc-files/ValueBased.md). Programmers should treat instances that are [equal](Map.md) as interchangeable and should not use them for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. Callers should make no assumptions about the identity of the returned instances. Factories are free to create new instances or reuse existing ones.
- They are serialized as specified on the [Serialized Form](https://developer.android.com//serialized-form.html#java.util.CollSer) page.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/java/util/Map.Entry` A map entry (key-value pair). |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#clear()()` Removes all of the mappings from this map (optional operation). |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#compute(java.util.Map.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V?, out V?>)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). |
| open V | `https://developer.android.com/reference/kotlin/java/util/Map#computeIfAbsent(java.util.Map.K,%20java.util.function.Function)(key: K, mappingFunction: https://developer.android.com/reference/kotlin/java/util/function/Function<in K, out V>)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#computeIfPresent(java.util.Map.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V?>)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#containsKey(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns `true` if this map contains a mapping for the specified key. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#containsValue(kotlin.Any)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns `true` if this map maps one or more keys to the specified value. |
| --- | --- |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#copyOf(kotlin.collections.MutableMap)(map: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>)` Returns an [unmodifiable Map](Map.md) containing the entries of the given Map. |
| open static [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#entry(java.util.Map.entry.K,%20java.util.Map.entry.V)(k: K, v: V)` Returns an unmodifiable `https://developer.android.com/reference/kotlin/java/util/Map.Entry` containing the given key and value. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>!\> | `https://developer.android.com/reference/kotlin/java/util/Map#entrySet()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer<in K, in V>)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| abstract V? | `https://developer.android.com/reference/kotlin/java/util/Map#get(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#getOrDefault(kotlin.Any,%20java.util.Map.V)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, defaultValue: V?)` Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#isEmpty()()` Returns `true` if this map contains no key-value mappings. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | `https://developer.android.com/reference/kotlin/java/util/Map#keySet()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)(key: K, value: V, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in V, in V, out V?>)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. |
| --- | --- |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of()()` Returns an unmodifiable map containing zero mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V)` Returns an unmodifiable map containing a single mapping. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V)` Returns an unmodifiable map containing two mappings. |
| --- | --- |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V)` Returns an unmodifiable map containing three mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V)` Returns an unmodifiable map containing four mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V)` Returns an unmodifiable map containing five mappings. |
| --- | --- |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V, k6: K, v6: V)` Returns an unmodifiable map containing six mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V, k6: K, v6: V, k7: K, v7: V)` Returns an unmodifiable map containing seven mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V, k6: K, v6: V, k7: K, v7: V, k8: K, v8: V)` Returns an unmodifiable map containing eight mappings. |
| --- | --- |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V, k6: K, v6: V, k7: K, v7: V, k8: K, v8: V, k9: K, v9: V)` Returns an unmodifiable map containing nine mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#of(java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V,%20java.util.Map.of.K,%20java.util.Map.of.V)(k1: K, v1: V, k2: K, v2: V, k3: K, v3: V, k4: K, v4: V, k5: K, v5: V, k6: K, v6: V, k7: K, v7: V, k8: K, v8: V, k9: K, v9: V, k10: K, v10: V)` Returns an unmodifiable map containing ten mappings. |
| open static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/Map#ofEntries(kotlin.collections.MutableMap.MutableEntry)(vararg entries: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<out K, out V>!)` Returns an unmodifiable map containing keys and values extracted from the given entries. |
| --- | --- |
| abstract V? | `https://developer.android.com/reference/kotlin/java/util/Map#put(java.util.Map.K,%20java.util.Map.V)(key: K, value: V)` Associates the specified value with the specified key in this map (optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#putAll(kotlin.collections.MutableMap)(m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>)` Copies all of the mappings from the specified map to this map (optional operation). |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#putIfAbsent(java.util.Map.K,%20java.util.Map.V)(key: K, value: V)` If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value. |
| --- | --- |
| abstract V? | `https://developer.android.com/reference/kotlin/java/util/Map#remove(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Removes the mapping for a key from this map if it is present (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#remove(kotlin.Any,%20kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Removes the entry for the specified key only if it is currently mapped to the specified value. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/Map#replace(java.util.Map.K,%20java.util.Map.V)(key: K, value: V)` Replaces the entry for the specified key only if it is currently mapped to some value. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#replace(java.util.Map.K,%20java.util.Map.V,%20java.util.Map.V)(key: K, oldValue: V, newValue: V)` Replaces the entry for the specified key only if currently mapped to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Map#size()()` Returns the number of key-value mappings in this map. |
| --- | --- |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/java/util/Map#values()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clear(): Unit
```

Removes all of the mappings from this map (optional operation). The map will be empty after this call returns.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). For example, to either create or append a `String` msg to a value mapping:

```kotlin
<code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code>
```
(Method `https://developer.android.com/reference/kotlin/java/util/Map#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` is often simpler to use for such purposes.)

<br />

If the remapping function returns `null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in K, in V?, out V?\>: the remapping function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`.

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

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `mappingFunction` | [Function](../java.util.function/Function.md)\<in K, out V\>: the mapping function to compute a value |

| Return ||
|---|---|
| `V` | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the mappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value.

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in K, in V, out V?\>: the remapping function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun containsKey(key: Any?): Boolean
```

Returns `true` if this map contains a mapping for the specified key. More formally, returns `true` if and only if this map contains a mapping for a key `k` such that `Objects.equals(key, k)`. (There can be at most one such mapping.)

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains a mapping for the specified key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun containsValue(value: Any?): Boolean
```

Returns `true` if this map maps one or more keys to the specified value. More formally, returns `true` if and only if this map contains at least one mapping to a value `v` such that `Objects.equals(value, v)`. This operation will probably require time linear in the map size for most implementations of the `Map` interface.

| Parameters ||
|---|---|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map maps one or more keys to the specified value |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### copyOf

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> copyOf(map: MutableMap<out K, out V>): MutableMap<K, V>
```

Returns an [unmodifiable Map](Map.md) containing the entries of the given Map. The given Map must not be null, and it must not contain any null keys or values. If the given Map is subsequently modified, the returned Map will not reflect such modifications.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out K, out V\>: a `Map` from which entries are drawn, must be non-null |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the entries of the given `Map` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if map is null, or if it contains any null keys or values |

### entry

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> entry(
    k: K, 
    v: V
): MutableEntry<K, V>
```

Returns an unmodifiable `https://developer.android.com/reference/kotlin/java/util/Map.Entry` containing the given key and value. These entries are suitable for populating `Map` instances using the `https://developer.android.com/reference/kotlin/java/util/Map#ofEntries(kotlin.collections.MutableMap.MutableEntry)` method. The `Entry` instances created by this method have the following characteristics:

- They disallow `null` keys and values. Attempts to create them using a `null` key or value result in `NullPointerException`.
- They are unmodifiable. Calls to `https://developer.android.com/reference/kotlin/java/util/Map.Entry#setValue(java.util.Map.Entry.V)` on a returned `Entry` result in `UnsupportedOperationException`.
- They are not serializable.
- They are [value-based](../java/lang/doc-files/ValueBased.md). Programmers should treat instances that are [equal](Map.md) as interchangeable and should not use them for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. Callers should make no assumptions about the identity of the returned instances. This method is free to create new instances or reuse existing ones.

<br />

| Parameters ||
|---|---|
| `<K>` | the key's type |
| `<V>` | the value's type |
| `k` | K: the key |
| --- | --- |
| `v` | V: the value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>` | an `Entry` containing the specified key and value |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the key or value is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Map#ofEntries(kotlin.collections.MutableMap.MutableEntry)`

### entrySet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun entrySet(): MutableSet<MutableEntry<K, V>!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!>` | a set view of the mappings contained in this map |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in K, in V\>: The action to be performed for each entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(key: Any?): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `Objects.equals(key, k)`, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

If this map permits null values, then a return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/Map#containsKey(kotlin.Any)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrDefault(
    key: Any?, 
    defaultValue: V?
): V?
```

Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the key whose associated value is to be returned |
| `defaultValue` | V?: the default mapping of the key |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isEmpty(): Boolean
```

Returns `true` if this map contains no key-value mappings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains no key-value mappings |

### keySet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun keySet(): MutableSet<K>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | a set view of the keys contained in this map |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is `null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a `String msg` to a value mapping:

```kotlin
<code>map.merge(key, msg, String::concat)
  </code>
```

<br />

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the resulting value is to be associated |
| `value` | V: the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<in V, in V, out V?\>: the remapping function to recompute a value if present |
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
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(): MutableMap<K, V>
```

Returns an unmodifiable map containing zero mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | an empty `Map` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing a single mapping. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the mapping's key |
| --- | --- |
| `v1` | V: the mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mapping |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the key or the value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing two mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the keys are duplicates |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing three mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing four mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing five mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V, 
    k6: K, 
    v6: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing six mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |
| `k6` | K: the sixth mapping's key |
| `v6` | V: the sixth mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V, 
    k6: K, 
    v6: V, 
    k7: K, 
    v7: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing seven mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |
| `k6` | K: the sixth mapping's key |
| `v6` | V: the sixth mapping's value |
| `k7` | K: the seventh mapping's key |
| --- | --- |
| `v7` | V: the seventh mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V, 
    k6: K, 
    v6: V, 
    k7: K, 
    v7: V, 
    k8: K, 
    v8: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing eight mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |
| `k6` | K: the sixth mapping's key |
| `v6` | V: the sixth mapping's value |
| `k7` | K: the seventh mapping's key |
| --- | --- |
| `v7` | V: the seventh mapping's value |
| `k8` | K: the eighth mapping's key |
| `v8` | V: the eighth mapping's value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V, 
    k6: K, 
    v6: V, 
    k7: K, 
    v7: V, 
    k8: K, 
    v8: V, 
    k9: K, 
    v9: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing nine mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |
| `k6` | K: the sixth mapping's key |
| `v6` | V: the sixth mapping's value |
| `k7` | K: the seventh mapping's key |
| --- | --- |
| `v7` | V: the seventh mapping's value |
| `k8` | K: the eighth mapping's key |
| `v8` | V: the eighth mapping's value |
| --- | --- |
| `k9` | K: the ninth mapping's key |
| `v9` | V: the ninth mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> of(
    k1: K, 
    v1: V, 
    k2: K, 
    v2: V, 
    k3: K, 
    v3: V, 
    k4: K, 
    v4: V, 
    k5: K, 
    v5: V, 
    k6: K, 
    v6: V, 
    k7: K, 
    v7: V, 
    k8: K, 
    v8: V, 
    k9: K, 
    v9: V, 
    k10: K, 
    v10: V
): MutableMap<K, V>
```

Returns an unmodifiable map containing ten mappings. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `k1` | K: the first mapping's key |
| --- | --- |
| `v1` | V: the first mapping's value |
| `k2` | K: the second mapping's key |
| `v2` | V: the second mapping's value |
| --- | --- |
| `k3` | K: the third mapping's key |
| `v3` | V: the third mapping's value |
| `k4` | K: the fourth mapping's key |
| --- | --- |
| `v4` | V: the fourth mapping's value |
| `k5` | K: the fifth mapping's key |
| `v5` | V: the fifth mapping's value |
| --- | --- |
| `k6` | K: the sixth mapping's key |
| `v6` | V: the sixth mapping's value |
| `k7` | K: the seventh mapping's key |
| --- | --- |
| `v7` | V: the seventh mapping's value |
| `k8` | K: the eighth mapping's key |
| `v8` | V: the eighth mapping's value |
| --- | --- |
| `k9` | K: the ninth mapping's key |
| `v9` | V: the ninth mapping's value |
| `k10` | K: the tenth mapping's key |
| --- | --- |
| `v10` | V: the tenth mapping's value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any key or value is `null` |

### ofEntries

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
@SafeVarargs open static fun <K : Any!, V : Any!> ofEntries(vararg entries: MutableEntry<out K, out V>!): MutableMap<K, V>
```

Returns an unmodifiable map containing keys and values extracted from the given entries. The entries themselves are not stored in the map. See [Unmodifiable Maps](Map.md) for details.

| Parameters ||
|---|---|
| `<K>` | the `Map`'s key type |
| `<V>` | the `Map`'s value type |
| `entries` | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<out K, out V\>!: `Map.Entry`s containing the keys and values from which the map is populated |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, V>` | a `Map` containing the specified mappings |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there are any duplicate keys |
| `java.lang.NullPointerException` | if any entry, key, or value is `null`, or if the `entries` array is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Map#entry(java.util.Map.entry.K,%20java.util.Map.entry.V)`

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun put(
    key: K, 
    value: V
): V?
```

Associates the specified value with the specified key in this map (optional operation). If the map previously contained a mapping for the key, the old value is replaced by the specified value. (A map `m` is said to contain a mapping for a key `k` if and only if `https://developer.android.com/reference/kotlin/java/util/Map#containsKey(kotlin.Any)` would return `true`.)

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `value` | V: value to be associated with the specified key |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`, if the implementation supports `null` values.) |

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
abstract fun putAll(m: MutableMap<out K, out V>): Unit
```

Copies all of the mappings from the specified map to this map (optional operation). The effect of this call is equivalent to that of calling `https://developer.android.com/reference/kotlin/java/util/Map#put(java.util.Map.K,%20java.util.Map.V)` on this map once for each mapping from key `k` to value `v` in the specified map. The behavior of this operation is undefined if the specified map is modified while the operation is in progress. If the specified map has a defined [encounter order](SequencedCollection.md), processing of its mappings generally occurs in that order.

| Parameters ||
|---|---|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out K, out V\>: mappings to be stored in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null, or if this map does not permit null keys or values, and the specified map contains null keys or values |
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

If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value.

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
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(key: Any?): V?
```

Removes the mapping for a key from this map if it is present (optional operation). More formally, if this map contains a mapping from key `k` to value `v` such that `Objects.equals(key, k)`, that mapping is removed. (The map can contain at most one such mapping.)

Returns the value to which this map previously associated the key, or `null` if the map contained no mapping for the key.

If this map permits null values, then a return value of `null` does not *necessarily* indicate that the map contained no mapping for the key; it's also possible that the map explicitly mapped the key to `null`.

The map will not contain a mapping for the specified key once the call returns.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: key whose mapping is to be removed from the map |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. |

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
    key: Any?, 
    value: Any?
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: key with which the specified value is associated |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: value expected to be associated with the specified key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the value was removed |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map (java.util.Collection#) |
| --- | --- |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: K, 
    value: V
): V?
```

Replaces the entry for the specified key only if it is currently mapped to some value.

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
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value.

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
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map (java.util.Collection#) |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. Exceptions thrown by the function are relayed to the caller.

| Parameters ||
|---|---|
| `function` | [BiFunction](../java.util.function/BiFunction.md)\<in K, in V, out V\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `set` operation is not supported by this map's entry set iterator. |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun size(): Int
```

Returns the number of key-value mappings in this map. If the map contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun values(): MutableCollection<V>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a collection view of the values contained in this map |
