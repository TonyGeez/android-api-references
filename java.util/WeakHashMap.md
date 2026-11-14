Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WeakHashMap

```
open class WeakHashMap<K : Any!, V : Any!> : AbstractMap<K, V>, MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](AbstractMap.md)\<K, V\> ||
| | ↳ | [java.util.WeakHashMap](WeakHashMap.md) |

Hash table based implementation of the `Map` interface, with *weak keys* . An entry in a `WeakHashMap` will automatically be removed when its key is no longer in ordinary use. More precisely, the presence of a mapping for a given key will not prevent the key from being discarded by the garbage collector, that is, made finalizable, finalized, and then reclaimed. When a key has been discarded its entry is effectively removed from the map, so this class behaves somewhat differently from other `Map` implementations.

Both null values and the null key are supported. This class has performance characteristics similar to those of the `HashMap` class, and has the same efficiency parameters of *initial capacity* and *load factor*.

Like most collection classes, this class is not synchronized. A synchronized `WeakHashMap` may be constructed using the `https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedMap(kotlin.collections.MutableMap)` method.

This class is intended primarily for use with key objects whose `equals` methods test for object identity using the `==` operator. Once such a key is discarded it can never be recreated, so it is impossible to do a lookup of that key in a `WeakHashMap` at some later time and be surprised that its entry has been removed. This class will work perfectly well with key objects whose `equals` methods are not based upon object identity, such as `String` instances. With such recreatable key objects, however, the automatic removal of `WeakHashMap` entries whose keys have been discarded may prove to be confusing.

The behavior of the `WeakHashMap` class depends in part upon the actions of the garbage collector, so several familiar (though not required) `Map` invariants do not hold for this class. Because the garbage collector may discard keys at any time, a `WeakHashMap` may behave as though an unknown thread is silently removing entries. In particular, even if you synchronize on a `WeakHashMap` instance and invoke none of its mutator methods, it is possible for the `size` method to return smaller values over time, for the `isEmpty` method to return `false` and then `true`, for the `containsKey` method to return `true` and later `false` for a given key, for the `get` method to return a value for a given key but later return `null`, for the `put` method to return `null` and the `remove` method to return `false` for a key that previously appeared to be in the map, and for successive examinations of the key set, the value collection, and the entry set to yield successively smaller numbers of elements.

Each key object in a `WeakHashMap` is stored indirectly as the referent of a weak reference. Therefore a key will automatically be removed only after the weak references to it, both inside and outside of the map, have been cleared by the garbage collector.

**Implementation note:** The value objects in a `WeakHashMap` are held by ordinary strong references. Thus care should be taken to ensure that value objects do not strongly refer to their own keys, either directly or indirectly, since that will prevent the keys from being discarded. Note that a value object may refer indirectly to its key via the `WeakHashMap` itself; that is, a value object may strongly refer to some other key object whose associated value object, in turn, strongly refers to the key of the first value object. If the values in the map do not rely on the map holding strong references to them, one way to deal with this is to wrap values themselves within `WeakReferences` before inserting, as in: `m.put(key, new WeakReference(value))`, and then unwrapping upon each `get`.

The iterators returned by the `iterator` method of the collections returned by all of this class's "collection view methods" are *fail-fast* : if the map is structurally modified at any time after the iterator is created, in any way except through the iterator's own `remove` method, the iterator will throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException`. Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw `ConcurrentModificationException` on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness: *the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#WeakHashMap()()` Constructs a new, empty `WeakHashMap` with the default initial capacity (16) and load factor (0.75). |
| `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#WeakHashMap(kotlin.Int)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new, empty `WeakHashMap` with the given initial capacity and the default load factor (0.75). |
| `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#WeakHashMap(kotlin.Int,%20kotlin.Float)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, loadFactor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Constructs a new, empty `WeakHashMap` with the given initial capacity and the given load factor. |
| `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#WeakHashMap(kotlin.collections.MutableMap)(m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>)` Constructs a new `WeakHashMap` with the same mappings as the specified map. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#clear()()` Removes all of the mappings from this map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#containsKey(java.util.WeakHashMap.K)(key: K?)` Returns `true` if this map contains a mapping for the specified key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#containsValue(java.util.WeakHashMap.V)(value: V?)` Returns `true` if this map maps one or more keys to the specified value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer<in K, in V>)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#get(java.util.WeakHashMap.K)(key: K?)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#isEmpty()()` Returns `true` if this map contains no key-value mappings. |
| --- | --- |
| open static [WeakHashMap](WeakHashMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#newWeakHashMap(kotlin.Int)(numMappings: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new, empty WeakHashMap suitable for the expected number of mappings. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#put(java.util.WeakHashMap.K,%20java.util.WeakHashMap.V)(key: K, value: V)` Associates the specified value with the specified key in this map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<out K, V>)` Copies all of the mappings from the specified map to this map. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#remove(java.util.WeakHashMap.K)(key: K?)` Removes the mapping for a key from this weak hash map if it is present. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractMap` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#clone()()` Returns a shallow copy of this `AbstractMap` instance: the keys and values themselves are not cloned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this map for equality. Returns `true` if the given object is also a map and the two maps represent the same mappings. More formally, two maps `m1` and `m2` represent the same mappings if `m1.entrySet().equals(m2.entrySet())`. This ensures that the `equals` method works properly across different implementations of the `Map` interface. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#hashCode()()` Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map's `entrySet()` view. This ensures that `m1.equals(m2)` implies that `m1.hashCode()==m2.hashCode()` for any two maps `m1` and `m2`, as required by the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#toString()()` Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's `entrySet` view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters `", "` (comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||

| Properties ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>\> | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#entries:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#keys:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#size:kotlin.Int` Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#values:kotlin.collections.MutableCollection` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. |

## Public constructors

### WeakHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WeakHashMap()
```

Constructs a new, empty `WeakHashMap` with the default initial capacity (16) and load factor (0.75).

### WeakHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WeakHashMap(initialCapacity: Int)
```

Constructs a new, empty `WeakHashMap` with the given initial capacity and the default load factor (0.75).

| Parameters ||
|---|---|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial capacity of the `WeakHashMap` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the initial capacity is negative |

### WeakHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WeakHashMap(
    initialCapacity: Int, 
    loadFactor: Float)
```

Constructs a new, empty `WeakHashMap` with the given initial capacity and the given load factor.

| Parameters ||
|---|---|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial capacity of the `WeakHashMap` |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The load factor of the `WeakHashMap` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the initial capacity is negative, or if the load factor is nonpositive. |

### WeakHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WeakHashMap(m: MutableMap<out K, out V>)
```

Constructs a new `WeakHashMap` with the same mappings as the specified map. The `WeakHashMap` is created with the default load factor (0.75) and an initial capacity sufficient to hold the mappings in the specified map.

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

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: K?): Boolean
```

Returns `true` if this map contains a mapping for the specified key.

| Parameters ||
|---|---|
| `key` | K?: The key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is a mapping for `key`; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V?): Boolean
```

Returns `true` if this map maps one or more keys to the specified value.

| Parameters ||
|---|---|
| `value` | V?: value whose presence in this map is to be tested |

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
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<in K, in V\>: The action to be performed for each entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K?): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `Objects.equals(key, k)`, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

A return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#containsKey(java.util.WeakHashMap.K)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | K?: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#put(java.util.WeakHashMap.K,%20java.util.WeakHashMap.V)`

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this map contains no key-value mappings. This result is a snapshot, and may not reflect unprocessed entries that will be removed before next attempted access because they are no longer referenced.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains no key-value mappings |

### newWeakHashMap

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <K : Any!, V : Any!> newWeakHashMap(numMappings: Int): WeakHashMap<K, V>
```

Creates a new, empty WeakHashMap suitable for the expected number of mappings. The returned map uses the default load factor of 0.75, and its initial capacity is generally large enough so that the expected number of mappings can be added without resizing the map.

| Parameters ||
|---|---|
| `<K>` | the type of keys maintained by the new map |
| `<V>` | the type of mapped values |
| `numMappings` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the expected number of mappings |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/WeakHashMap#<K, V>` | the newly created map |

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

Associates the specified value with the specified key in this map. If the map previously contained a mapping for this key, the old value is replaced.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated. |
| `value` | V: value to be associated with the specified key. |

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
| `m` | mappings to be stored in this map. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putAll` operation is not supported by this map |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K?): V?
```

Removes the mapping for a key from this weak hash map if it is present. More formally, if this map contains a mapping from key `k` to value `v` such that `(key==null ? k==null : key.equals(k))`, that mapping is removed. (The map can contain at most one such mapping.)

Returns the value to which this map previously associated the key, or `null` if the map contained no mapping for the key. A return value of `null` does not *necessarily* indicate that the map contained no mapping for the key; it's also possible that the map explicitly mapped the key to `null`.

The map will not contain a mapping for the specified key once the call returns.

| Parameters ||
|---|---|
| `key` | K?: key whose mapping is to be removed from the map |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

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

Returns the number of key-value mappings in this map. This result is a snapshot, and may not reflect unprocessed entries that will be removed before next attempted access because they are no longer referenced.

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
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a collection view of the values contained in this map |
