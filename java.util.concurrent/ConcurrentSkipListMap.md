Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentSkipListMap

```
open class ConcurrentSkipListMap<K : Any!, V : Any!> : AbstractMap<K, V>, Cloneable, ConcurrentNavigableMap<K, V>, Serializable, MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](../java/util/AbstractMap.md)\<K, V\> ||
| | ↳ | [java.util.concurrent.ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md) |

A scalable concurrent `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap` implementation. The map is sorted according to the [natural](../java/lang/Comparable.md) of its keys, or by a `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` provided at map creation time, depending on which constructor is used.

This class implements a concurrent variant of [SkipLists](http://en.wikipedia.org/wiki/Skip_list) providing expected average *log(n)* time cost for the `containsKey`, `get`, `put` and `remove` operations and their variants. Insertion, removal, update, and access operations safely execute concurrently by multiple threads.

Iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

Ascending key ordered views and their iterators are faster than descending ones.

All `Map.Entry` pairs returned by methods in this class and its views represent snapshots of mappings at the time they were produced. They do *not* support the `Entry.setValue` method. (Note however that it is possible to change mappings in the associated map using `put`, `putIfAbsent`, or `replace`, depending on exactly which effect you need.)

Beware that bulk operations `putAll`, `equals`, `toArray`, `containsValue`, and `clear` are *not* guaranteed to be performed atomically. For example, an iterator operating concurrently with a `putAll` operation might view only some of the added elements.

This class and its views and iterators implement all of the *optional* methods of the `https://developer.android.com/reference/kotlin/java/util/Map.html#` and `https://developer.android.com/reference/kotlin/java/util/Iterator.html#` interfaces. Like most other concurrent collections, this class does *not* permit the use of `null` keys or values because some null return values cannot be reliably distinguished from the absence of elements.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ConcurrentSkipListMap()()` Constructs a new, empty map, sorted according to the [natural ordering](../java/lang/Comparable.md) of the keys. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ConcurrentSkipListMap(java.util.Comparator)(comparator: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in K>!)` Constructs a new, empty map, sorted according to the specified comparator. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ConcurrentSkipListMap(kotlin.collections.MutableMap)(m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>!)` Constructs a new map containing the same mappings as the given map, sorted according to the [natural ordering](../java/lang/Comparable.md) of the keys. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ConcurrentSkipListMap(java.util.SortedMap)(m: https://developer.android.com/reference/kotlin/java/util/SortedMap.html#<K, out V>!)` Constructs a new map containing the same mappings and using the same ordering as the specified sorted map. |

| Public methods ||
|---|---|
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ceilingEntry(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such entry. |
| open K? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#ceilingKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#clear()()` Removes all of the mappings from this map. |
| --- | --- |
| open [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#clone()()` Returns a shallow copy of this `ConcurrentSkipListMap` instance. |
| open [Comparator](../java/util/Comparator.md)\<in K\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#comparator()()` Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#compute(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in K, in V?, out V?>)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). |
| --- | --- |
| open V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#computeIfAbsent(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.function.Function)(key: K, mappingFunction: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in K, out V>)` If the specified key is not already associated with a value, attempts to compute its value using the given mapping function and enters it into this map unless `null`. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#computeIfPresent(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in K, in V, out V?>)` If the value for the specified key is present, attempts to compute a new mapping given the key and its current mapped value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#containsKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#containsKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#containsValue(java.util.concurrent.ConcurrentSkipListMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#containsValue(java.util.concurrent.ConcurrentSkipListMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| --- | --- |
| open [NavigableSet](../java/util/NavigableSet.md)\<K\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#descendingKeySet()()` Returns a reverse order `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map. |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#descendingMap()()` Returns a reverse order view of the mappings contained in this map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this map for equality. |
| --- | --- |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#firstEntry()()` Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. |
| open K | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#firstKey()()` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#floorEntry(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key. |
| --- | --- |
| open K? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#floorKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#<in K, in V>)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#get(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#get(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open V | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#getOrDefault(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, defaultValue: V)` Returns the value to which the specified key is mapped, or the given defaultValue if this map contains no mapping for the key. |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#headMap(java.util.concurrent.ConcurrentSkipListMap.K)(toKey: K)` <br /> |
| --- | --- |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#headMap(java.util.concurrent.ConcurrentSkipListMap.K,%20kotlin.Boolean)(toKey: K, inclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#higherEntry(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key. |
| open K? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#higherKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#isEmpty()()` Returns `true` if this map contains no key-value mappings. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#lastEntry()()` Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. |
| open K | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#lastKey()()` <br /> |
| --- | --- |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#lowerEntry(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key. |
| open K? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#lowerKey(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` <br /> |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#merge(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V,%20java.util.function.BiFunction)(key: K, value: V, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in V, in V, out V?>)` If the specified key is not already associated with a value, associates it with the given value. |
| --- | --- |
| open [NavigableSet](../java/util/NavigableSet.md)\<K\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#navigableKeySet()()` Returns a `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#pollFirstEntry()()` Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#pollLastEntry()()` Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#put(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, value: V)` Associates the specified value with the specified key in this map. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#putFirst(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#putIfAbsent(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, value: V)` If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value (optional operation). |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#putLast(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#remove(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Removes the mapping for the specified key from this map if present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#remove(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, value: V)` Removes the entry for the specified key only if it is currently mapped to the specified value (optional operation). |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#remove(java.util.concurrent.ConcurrentSkipListMap.K)(key: K)` Removes the mapping for the specified key from this map if present. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#replace(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, value: V)` Replaces the entry for the specified key only if it is currently mapped to some value (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#replace(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.V,%20java.util.concurrent.ConcurrentSkipListMap.V)(key: K, oldValue: V, newValue: V)` Replaces the entry for the specified key only if currently mapped to the specified value (optional operation). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#subMap(java.util.concurrent.ConcurrentSkipListMap.K,%20kotlin.Boolean,%20java.util.concurrent.ConcurrentSkipListMap.K,%20kotlin.Boolean)(fromKey: K, fromInclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, toKey: K, toInclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#subMap(java.util.concurrent.ConcurrentSkipListMap.K,%20java.util.concurrent.ConcurrentSkipListMap.K)(fromKey: K, toKey: K)` <br /> |
| --- | --- |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#tailMap(java.util.concurrent.ConcurrentSkipListMap.K)(fromKey: K)` <br /> |
| open [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#tailMap(java.util.concurrent.ConcurrentSkipListMap.K,%20kotlin.Boolean)(fromKey: K, inclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#hashCode()()` Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map's `entrySet()` view. This ensures that `m1.equals(m2)` implies that `m1.hashCode()==m2.hashCode()` for any two maps `m1` and `m2`, as required by the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<out K, V>)` Copies all of the mappings from the specified map to this map (optional operation). The effect of this call is equivalent to that of calling `https://developer.android.com/reference/kotlin/java/util/Map.html#put(java.util.Map.K,%20java.util.Map.V)` on this map once for each mapping from key `k` to value `v` in the specified map. The behavior of this operation is undefined if the specified map is modified while the operation is in progress. If the specified map has a defined [encounter order](../java/util/SequencedCollection.md), processing of its mappings generally occurs in that order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#toString()()` Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's `entrySet` view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters `", "` (comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||

| Properties ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#entries:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the mappings contained in this map. |
| open [NavigableSet](../java/util/NavigableSet.md)\<K\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#keys:java.util.NavigableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#size:kotlin.Int` Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#values:kotlin.collections.MutableCollection` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` view of the values contained in this map. |

## Public constructors

### ConcurrentSkipListMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentSkipListMap()
```

Constructs a new, empty map, sorted according to the [natural ordering](../java/lang/Comparable.md) of the keys.

### ConcurrentSkipListMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentSkipListMap(comparator: Comparator<in K>!)
```

Constructs a new, empty map, sorted according to the specified comparator.

| Parameters ||
|---|---|
| `comparator` | [Comparator](../java/util/Comparator.md)\<in K\>!: the comparator that will be used to order this map. If `null`, the [natural](../java/lang/Comparable.md) of the keys will be used. |

### ConcurrentSkipListMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentSkipListMap(m: MutableMap<out K, out V>!)
```

Constructs a new map containing the same mappings as the given map, sorted according to the [natural ordering](../java/lang/Comparable.md) of the keys.

| Parameters ||
|---|---|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out K, out V\>!: the map whose mappings are to be placed in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the keys in `m` are not `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`, or are not mutually comparable |
| `java.lang.NullPointerException` | if the specified map or any of its keys or values are null |

### ConcurrentSkipListMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentSkipListMap(m: SortedMap<K, out V>!)
```

Constructs a new map containing the same mappings and using the same ordering as the specified sorted map.

| Parameters ||
|---|---|
| `m` | [SortedMap](../java/util/SortedMap.md)\<K, out V\>!: the sorted map whose mappings are to be placed in this map, and whose comparator is to be used to sort this map |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified sorted map or any of its keys or values are null |

## Public methods

### ceilingEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ceilingEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such entry. The returned entry does *not* support the `Entry.setValue` method.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### ceilingKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ceilingKey(key: K): K?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the least key greater than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### clear

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all of the mappings from this map.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |

### clone

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): ConcurrentSkipListMap<K, V>
```

Returns a shallow copy of this `ConcurrentSkipListMap` instance. (The keys and values themselves are not cloned.)

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap#<K, V>` | a shallow copy of this map |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### comparator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun comparator(): Comparator<in K>?
```

Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in K>?` | the comparator used to order the keys in this map, or `null` if this map uses the natural ordering of its keys |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). The function is *NOT* guaranteed to be applied once atomically.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V?, out V?\>: the function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `compute` operation is not supported by this map (java.util.Collection#) |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value, attempts to compute its value using the given mapping function and enters it into this map unless `null`. The function is *NOT* guaranteed to be applied once atomically only if the value is not present.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `mappingFunction` | [Function](../java/util/function/Function.md)\<in K, out V\>: the function to compute a value |

| Return ||
|---|---|
| `V` | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null or the mappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfAbsent` operation is not supported by this map (java.util.Collection#) |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present, attempts to compute a new mapping given the key and its current mapped value. The function is *NOT* guaranteed to be applied once atomically.

| Parameters ||
|---|---|
| `key` | K: key with which a value may be associated |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V, out V?\>: the function to compute a value |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `computeIfPresent` operation is not supported by this map (java.util.Collection#) |

### containsKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: K): Boolean
```

Returns `true` if this map contains a mapping for the specified key.

| Parameters ||
|---|---|
| `key` | K: key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains a mapping for the specified key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### containsKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: K): Boolean
```

Returns `true` if this map contains a mapping for the specified key.

| Parameters ||
|---|---|
| `key` | K: key whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains a mapping for the specified key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### containsValue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value. This operation requires time linear in the map size. Additionally, it is possible for the map to change during execution of this method, in which case the returned result may be inaccurate.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a mapping to `value` exists; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null |

### containsValue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value. This operation requires time linear in the map size. Additionally, it is possible for the map to change during execution of this method, in which case the returned result may be inaccurate.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a mapping to `value` exists; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null |

### descendingKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingKeySet(): NavigableSet<K>
```

Returns a reverse order `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map. The set's iterator returns the keys in descending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#<K>` | a reverse order navigable set view of the keys in this map |

### descendingMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingMap(): ConcurrentNavigableMap<K, V>
```

Returns a reverse order view of the mappings contained in this map. The descending map is backed by this map, so changes to the map are reflected in the descending map, and vice-versa.

The returned map has an ordering equivalent to java.util.Collections#reverseOrder(Comparator)`(comparator())`. The expression `m.descendingMap().descendingMap()` returns a view of `m` essentially equivalent to `m`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a reverse order view of this map |

### equals

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this map for equality. Returns `true` if the given object is also a map and the two maps represent the same mappings. More formally, two maps `m1` and `m2` represent the same mappings if `m1.entrySet().equals(m2.entrySet())`. This operation may return misleading results if either map is concurrently modified during execution of this method.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this map |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified object is equal to this map |

### firstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun firstEntry(): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. The returned entry does *not* support the `Entry.setValue` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key, or `null` if this map is empty |

### firstKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun firstKey(): K
```

| Return ||
|---|---|
| `K` | the first (lowest) key currently in this map |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this map is empty |

### floorEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun floorEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key. The returned entry does *not* support the `Entry.setValue` method.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### floorKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun floorKey(key: K): K?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the greatest key less than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller.

| Parameters ||
|---|---|
| `action` | [BiConsumer](../java/util/function/BiConsumer.md)\<in K, in V\>: The action to be performed for each entry |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `key` compares equal to `k` according to the map's ordering, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### get

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `key` compares equal to `k` according to the map's ordering, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOrDefault(
    key: K, 
    defaultValue: V
): V
```

Returns the value to which the specified key is mapped, or the given defaultValue if this map contains no mapping for the key.

| Parameters ||
|---|---|
| `key` | K: the key |
| `defaultValue` | V: the value to return if this map contains no mapping for the given key |

| Return ||
|---|---|
| `V` | the mapping for the key, if present; else the defaultValue |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun headMap(toKey: K): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys are strictly less than `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `toKey` is null |
| --- | --- |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun headMap(
    toKey: K, 
    inclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `toKey` | K: high endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `toKey` is null |
| --- | --- |

### higherEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun higherEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key. The returned entry does *not* support the `Entry.setValue` method.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### higherKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun higherKey(key: K): K?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the least key greater than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### isEmpty

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this map contains no key-value mappings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains no key-value mappings |

### lastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastEntry(): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. The returned entry does *not* support the `Entry.setValue` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key, or `null` if this map is empty |

### lastKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastKey(): K
```

| Return ||
|---|---|
| `K` | the last (highest) key currently in this map |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this map is empty |

### lowerEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lowerEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key. The returned entry does *not* support the `Entry.setValue` method.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### lowerKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lowerKey(key: K): K?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the greatest key less than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a value, associates it with the given value. Otherwise, replaces the value with the results of the given remapping function, or removes if `null`. The function is *NOT* guaranteed to be applied once atomically.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `value` | V: the value to use if absent |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in V, in V, out V?\>: the function to recompute a value if present |
| --- | --- |

| Return ||
|---|---|
| `V?` | the new value associated with the specified key, or null if none |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null or the remappingFunction is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `merge` operation is not supported by this map (java.util.Collection#) |

### navigableKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun navigableKeySet(): NavigableSet<K>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#<K>` | a navigable set view of the keys in this map |

### pollFirstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollFirstEntry(): MutableEntry<K, V>?
```

Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. The returned entry does *not* support the `Entry.setValue` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed first entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `pollFirstEntry` operation is not supported by this map |

### pollLastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollLastEntry(): MutableEntry<K, V>?
```

Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. The returned entry does *not* support the `Entry.setValue` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed last entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `pollLastEntry` operation is not supported by this map |

### put

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putFirst(
    k: K, 
    v: V
): V?
```

Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported.

| Parameters ||
|---|---|
| `k` | K: the key |
| `v` | V: the value |

| Return ||
|---|---|
| `V?` | the value previously associated with k, or null if none |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | always |

### putIfAbsent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putLast(
    k: K, 
    v: V
): V?
```

Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported.

| Parameters ||
|---|---|
| `k` | K: the key |
| `v` | V: the value |

| Return ||
|---|---|
| `V?` | the value previously associated with k, or null if none |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | always |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for the specified key from this map if present.

| Parameters ||
|---|---|
| `key` | K: key for which mapping should be removed |

| Return ||
|---|---|
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for the specified key from this map if present.

| Parameters ||
|---|---|
| `key` | K: key for which mapping should be removed |

| Return ||
|---|---|
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### replace

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `V?` | the previous value associated with the specified key, or `null` if there was no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### replace

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if any of the arguments are null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception (optional operation). Exceptions thrown by the function are relayed to the caller.

| Parameters ||
|---|---|
| `function` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V, out V\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subMap(
    fromKey: K, 
    fromInclusive: Boolean, 
    toKey: K, 
    toInclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `fromInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |
| `toKey` | K: high endpoint of the keys in the returned map |
| --- | --- |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys range from `fromKey` to `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null |
| --- | --- |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subMap(
    fromKey: K, 
    toKey: K
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null |
| --- | --- |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun tailMap(fromKey: K): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys are greater than or equal to `fromKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` is null |
| --- | --- |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun tailMap(
    fromKey: K, 
    inclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap<K, V>` | a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` is null |
| --- | --- |

## Properties

### entries

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the mappings contained in this map.

The set's iterator returns the entries in ascending key order. The set's spliterator additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#SORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, with an encounter order that is ascending key order.

The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

The `Map.Entry` elements traversed by the `iterator` or `spliterator` do *not* support the `setValue` operation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | a set view of the mappings contained in this map, sorted in ascending key order |

### keys

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val keys: NavigableSet<K>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#` view of the keys contained in this map.

The set's iterator returns the keys in ascending order. The set's spliterator additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#SORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, with an encounter order that is ascending key order.

The [spliterator's comparator](../java/util/Spliterator.md)) is `null` if the [map's comparator](../java/util/concurrent/ConcurrentSkipListMap.md)) is `null`. Otherwise, the spliterator's comparator is the same as or imposes the same total ordering as the map's comparator.

The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

This method is equivalent to method `navigableKeySet`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#<K>` | a navigable set view of the keys in this map |

### size

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of key-value mappings in this map. If the map contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of key-value mappings in this map |

### values

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val values: MutableCollection<V>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` view of the values contained in this map.

The collection's iterator returns the values in ascending order of the corresponding keys. The collections's spliterator additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, with an encounter order that is ascending order of the corresponding keys.

The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](../java/util/concurrent/_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a collection view of the values contained in this map, sorted in ascending key order |
