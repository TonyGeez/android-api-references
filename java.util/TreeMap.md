Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TreeMap

```
open class TreeMap<K : Any!, V : Any!> : AbstractMap<K, V>, Cloneable, NavigableMap<K, V>, Serializable, MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](../java/util/AbstractMap.md)\<K, V\> ||
| | ↳ | [java.util.TreeMap](../java/util/TreeMap.md) |

A Red-Black tree based `https://developer.android.com/reference/kotlin/java/util/NavigableMap` implementation. The map is sorted according to the [natural](../java/lang/Comparable.md) of its keys, or by a `https://developer.android.com/reference/kotlin/java/util/Comparator` provided at map creation time, depending on which constructor is used.

This implementation provides guaranteed log(n) time cost for the `containsKey`, `get`, `put` and `remove` operations. Algorithms are adaptations of those in Cormen, Leiserson, and Rivest's *Introduction to Algorithms*.

Note that the ordering maintained by a tree map, like any sorted map, and whether or not an explicit comparator is provided, must be *consistent with `equals`* if this sorted map is to correctly implement the `Map` interface. (See `Comparable` or `Comparator` for a precise definition of *consistent with equals* .) This is so because the `Map` interface is defined in terms of the `equals` operation, but a sorted map performs all key comparisons using its `compareTo` (or `compare`) method, so two keys that are deemed equal by this method are, from the standpoint of the sorted map, equal. The behavior of a sorted map *is* well-defined even if its ordering is inconsistent with `equals`; it just fails to obey the general contract of the `Map` interface.

**Note that this implementation is not synchronized.** If multiple threads access a map concurrently, and at least one of the threads modifies the map structurally, it *must* be synchronized externally. (A structural modification is any operation that adds or deletes one or more mappings; merely changing the value associated with an existing key is not a structural modification.) This is typically accomplished by synchronizing on some object that naturally encapsulates the map. If no such object exists, the map should be "wrapped" using the `https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedSortedMap(java.util.SortedMap)` method. This is best done at creation time, to prevent accidental unsynchronized access to the map:

```kotlin
SortedMap m = Collections.synchronizedSortedMap(new TreeMap(...));
```

The iterators returned by the `iterator` method of the collections returned by all of this class's "collection view methods" are *fail-fast* : if the map is structurally modified at any time after the iterator is created, in any way except through the iterator's own `remove` method, the iterator will throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException`. Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw `ConcurrentModificationException` on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness: *the fail-fast behavior of iterators should be used only to detect bugs.*

The methods `https://developer.android.com/reference/kotlin/java/util/TreeMap#ceilingEntry(java.util.TreeMap.K)`, #firstEntry, `https://developer.android.com/reference/kotlin/java/util/TreeMap#floorEntry(java.util.TreeMap.K)`, `https://developer.android.com/reference/kotlin/java/util/TreeMap#higherEntry(java.util.TreeMap.K)`, #lastEntry, `https://developer.android.com/reference/kotlin/java/util/TreeMap#lowerEntry(java.util.TreeMap.K)`, #pollFirstEntry, and #pollLastEntry return `https://developer.android.com/reference/kotlin/java/util/Map.Entry` instances that represent snapshots of mappings as of the time of the call. They do *not* support mutation of the underlying map via the optional `https://developer.android.com/reference/kotlin/java/util/Map.Entry#setValue(java.util.Map.Entry.V)` method.

The #putFirst and #putLast methods of this class throw `UnsupportedOperationException`. The encounter order of mappings is determined by the comparison method; therefore, explicit positioning is not supported.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/TreeMap#TreeMap()()` Constructs a new, empty tree map, using the natural ordering of its keys. |
| `https://developer.android.com/reference/kotlin/java/util/TreeMap#TreeMap(java.util.Comparator)(comparator: https://developer.android.com/reference/kotlin/java/util/Comparator<in K>?)` Constructs a new, empty tree map, ordered according to the given comparator. |
| `https://developer.android.com/reference/kotlin/java/util/TreeMap#TreeMap(kotlin.collections.MutableMap)(m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<out K, out V>)` Constructs a new tree map containing the same mappings as the given map, ordered according to the *natural ordering* of its keys. |
| `https://developer.android.com/reference/kotlin/java/util/TreeMap#TreeMap(java.util.SortedMap)(m: https://developer.android.com/reference/kotlin/java/util/SortedMap<K, out V>)` Constructs a new tree map containing the same mappings and using the same ordering as the specified sorted map. |

| Public methods ||
|---|---|
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#ceilingEntry(java.util.TreeMap.K)(key: K)` <br /> |
| open K? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#ceilingKey(java.util.TreeMap.K)(key: K)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#clear()()` Removes all of the mappings from this map. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#clone()()` Returns a shallow copy of this `TreeMap` instance. |
| open [Comparator](../java/util/Comparator.md)\<in K\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#comparator()()` Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#compute(java.util.TreeMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V?, out V?>)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). |
| --- | --- |
| open V | `https://developer.android.com/reference/kotlin/java/util/TreeMap#computeIfAbsent(java.util.TreeMap.K,%20java.util.function.Function)(key: K, mappingFunction: https://developer.android.com/reference/kotlin/java/util/function/Function<in K, out V>)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#computeIfPresent(java.util.TreeMap.K,%20java.util.function.BiFunction)(key: K, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V?>)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsKey(java.util.TreeMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsKey(java.util.TreeMap.K)(key: K)` Returns `true` if this map contains a mapping for the specified key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsValue(java.util.TreeMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsValue(java.util.TreeMap.V)(value: V)` Returns `true` if this map maps one or more keys to the specified value. |
| --- | --- |
| open [NavigableSet](../java/util/NavigableSet.md)\<K\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#descendingKeySet()()` <br /> |
| open [NavigableMap](../java/util/NavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#descendingMap()()` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#firstEntry()()` <br /> |
| --- | --- |
| open K | `https://developer.android.com/reference/kotlin/java/util/TreeMap#firstKey()()` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#floorEntry(java.util.TreeMap.K)(key: K)` <br /> |
| open K? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#floorKey(java.util.TreeMap.K)(key: K)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer<in K, in V>)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#get(java.util.TreeMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#get(java.util.TreeMap.K)(key: K)` Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key. |
| --- | --- |
| open [SortedMap](../java/util/SortedMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#headMap(java.util.TreeMap.K)(toKey: K)` <br /> |
| open [NavigableMap](../java/util/NavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#headMap(java.util.TreeMap.K,%20kotlin.Boolean)(toKey: K, inclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#higherEntry(java.util.TreeMap.K)(key: K)` <br /> |
| --- | --- |
| open K? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#higherKey(java.util.TreeMap.K)(key: K)` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#lastEntry()()` <br /> |
| open K | `https://developer.android.com/reference/kotlin/java/util/TreeMap#lastKey()()` <br /> |
| --- | --- |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#lowerEntry(java.util.TreeMap.K)(key: K)` <br /> |
| open K? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#lowerKey(java.util.TreeMap.K)(key: K)` <br /> |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#merge(java.util.TreeMap.K,%20java.util.TreeMap.V,%20java.util.function.BiFunction)(key: K, value: V, remappingFunction: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in V, in V, out V?>)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. |
| --- | --- |
| open [NavigableSet](../java/util/NavigableSet.md)\<K\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#navigableKeySet()()` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#pollFirstEntry()()` <br /> |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#pollLastEntry()()` <br /> |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#put(java.util.TreeMap.K,%20java.util.TreeMap.V)(key: K, value: V)` Associates the specified value with the specified key in this map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<out K, V>)` Copies all of the mappings from the specified map to this map. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#putFirst(java.util.TreeMap.K,%20java.util.TreeMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#putIfAbsent(java.util.TreeMap.K,%20java.util.TreeMap.V)(key: K, value: V)` If the specified key is not already associated with a value (or is mapped to `null`) associates it with the given value and returns `null`, else returns the current value. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#putLast(java.util.TreeMap.K,%20java.util.TreeMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#remove(java.util.TreeMap.K)(key: K)` Removes the mapping for this key from this TreeMap if present. |
| --- | --- |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#remove(java.util.TreeMap.K)(key: K)` Removes the mapping for this key from this TreeMap if present. |
| open V? | `https://developer.android.com/reference/kotlin/java/util/TreeMap#replace(java.util.TreeMap.K,%20java.util.TreeMap.V)(key: K, value: V)` Replaces the entry for the specified key only if it is currently mapped to some value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#replace(java.util.TreeMap.K,%20java.util.TreeMap.V,%20java.util.TreeMap.V)(key: K, oldValue: V, newValue: V)` Replaces the entry for the specified key only if currently mapped to the specified value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. |
| open [NavigableMap](../java/util/NavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#subMap(java.util.TreeMap.K,%20kotlin.Boolean,%20java.util.TreeMap.K,%20kotlin.Boolean)(fromKey: K, fromInclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, toKey: K, toInclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |
| open [SortedMap](../java/util/SortedMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#subMap(java.util.TreeMap.K,%20java.util.TreeMap.K)(fromKey: K, toKey: K)` <br /> |
| --- | --- |
| open [SortedMap](../java/util/SortedMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#tailMap(java.util.TreeMap.K)(fromKey: K)` <br /> |
| open [NavigableMap](../java/util/NavigableMap.md)\<K, V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#tailMap(java.util.TreeMap.K,%20kotlin.Boolean)(fromKey: K, inclusive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/SortedMap` |---|---| | `https://developer.android.com/reference/kotlin/java/util/Comparator<in K>?` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#comparator()()` Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys. <br /> | | `K` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#firstKey()()` Returns the first (lowest) key currently in this map. <br /> | | `K` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#lastKey()()` Returns the last (highest) key currently in this map. <br /> | | `V?` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#putFirst(java.util.SortedMap.K,%20java.util.SortedMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | | `V?` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#putLast(java.util.SortedMap.K,%20java.util.SortedMap.V)(k: K, v: V)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractMap` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this map for equality. Returns `true` if the given object is also a map and the two maps represent the same mappings. More formally, two maps `m1` and `m2` represent the same mappings if `m1.entrySet().equals(m2.entrySet())`. This ensures that the `equals` method works properly across different implementations of the `Map` interface. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#hashCode()()` Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map's `entrySet()` view. This ensures that `m1.equals(m2)` implies that `m1.hashCode()==m2.hashCode()` for any two maps `m1` and `m2`, as required by the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#isEmpty()()` Returns `true` if this map contains no key-value mappings. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractMap#toString()()` Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's `entrySet` view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters `", "` (comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/SequencedMap` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#firstEntry()()` Returns the first key-value mapping in this map, or `null` if the map is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#lastEntry()()` Returns the last key-value mapping in this map, or `null` if the map is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollFirstEntry()()` Removes and returns the first key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollLastEntry()()` Removes and returns the last key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedSet<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedEntrySet()()` Returns a `SequencedSet` view of this map's `https://developer.android.com/reference/kotlin/java/util/Map#entrySet()`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedSet<K>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedKeySet()()` Returns a `SequencedSet` view of this map's `https://developer.android.com/reference/kotlin/java/util/Map#keySet()`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedCollection<V>!` | `https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedValues()()` Returns a `SequencedCollection` view of this map's `https://developer.android.com/reference/kotlin/java/util/Map#values()` collection. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class `https://developer.android.com/reference/kotlin/java/util/NavigableMap` |---|---| | `https://developer.android.com/reference/kotlin/java/util/NavigableMap<K, V>` | `https://developer.android.com/reference/kotlin/java/util/NavigableMap#reversed()()` Returns a reverse-ordered [view](../java/util/Collection.md) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation. This method is equivalent to `https://developer.android.com/reference/kotlin/java/util/NavigableMap#descendingMap()`. <br /> | ||

| Properties ||
|---|---|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#entries:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#keys:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/TreeMap#size:kotlin.Int` Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/java/util/TreeMap#values:kotlin.collections.MutableCollection` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/SortedMap` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#entries:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#keys:kotlin.collections.MutableSet` Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#values:kotlin.collections.MutableCollection` Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | ||

## Public constructors

### TreeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TreeMap()
```

Constructs a new, empty tree map, using the natural ordering of its keys. All keys inserted into the map must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all such keys must be *mutually comparable* : `k1.compareTo(k2)` must not throw a `ClassCastException` for any keys `k1` and `k2` in the map. If the user attempts to put a key into the map that violates this constraint (for example, the user attempts to put a string key into a map whose keys are integers), the `put(Object key, Object value)` call will throw a `ClassCastException`.

### TreeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TreeMap(comparator: Comparator<in K>?)
```

Constructs a new, empty tree map, ordered according to the given comparator. All keys inserted into the map must be *mutually comparable* by the given comparator: `comparator.compare(k1, k2)` must not throw a `ClassCastException` for any keys `k1` and `k2` in the map. If the user attempts to put a key into the map that violates this constraint, the `put(Object key, Object value)` call will throw a `ClassCastException`.

| Parameters ||
|---|---|
| `comparator` | [Comparator](../java/util/Comparator.md)\<in K\>?: the comparator that will be used to order this map. If `null`, the [natural](../java/lang/Comparable.md) of the keys will be used. |

### TreeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TreeMap(m: MutableMap<out K, out V>)
```

Constructs a new tree map containing the same mappings as the given map, ordered according to the *natural ordering* of its keys. All keys inserted into the new map must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all such keys must be *mutually comparable* : `k1.compareTo(k2)` must not throw a `ClassCastException` for any keys `k1` and `k2` in the map. This method runs in n\*log(n) time.

| Parameters ||
|---|---|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<out K, out V\>: the map whose mappings are to be placed in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the keys in m are not `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`, or are not mutually comparable |
| `java.lang.NullPointerException` | if the specified map is null |

### TreeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TreeMap(m: SortedMap<K, out V>)
```

Constructs a new tree map containing the same mappings and using the same ordering as the specified sorted map. This method runs in linear time.

| Parameters ||
|---|---|
| `m` | [SortedMap](../java/util/SortedMap.md)\<K, out V\>: the sorted map whose mappings are to be placed in this map, and whose comparator is to be used to sort this map |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified map is null |

## Public methods

### ceilingEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ceilingEntry(key: K): MutableEntry<K, V>?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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

Returns a shallow copy of this `TreeMap` instance. (The keys and values themselves are not cloned.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a shallow copy of this map |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun comparator(): Comparator<in K>?
```

Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator<in K>?` | the comparator used to order the keys in this map, or `null` if this map uses the natural ordering of its keys |

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

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V?, out V?\>: the remapping function to compute a value |

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
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

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

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the mapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `mappingFunction` | [Function](../java/util/function/Function.md)\<in K, out V\>: the mapping function to compute a value |

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

If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V, out V?\>: the remapping function to compute a value |

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
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value. More formally, returns `true` if and only if this map contains at least one mapping to a value `v` such that `(value==null ? v==null : value.equals(v))`. This operation will probably require time linear in the map size for most implementations.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a mapping to `value` exists; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsValue(value: V): Boolean
```

Returns `true` if this map maps one or more keys to the specified value. More formally, returns `true` if and only if this map contains at least one mapping to a value `v` such that `(value==null ? v==null : value.equals(v))`. This operation will probably require time linear in the map size for most implementations.

| Parameters ||
|---|---|
| `value` | V: value whose presence in this map is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if a mapping to `value` exists; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### descendingKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingKeySet(): NavigableSet<K>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet<K>` | a reverse order navigable set view of the keys in this map |

### descendingMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingMap(): NavigableMap<K, V>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap<K, V>` | a reverse order view of this map |

### firstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun firstEntry(): MutableEntry<K, V>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key, or `null` if this map is empty |

### firstKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `key` compares equal to `k` according to the map's ordering, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

A return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsKey(java.util.TreeMap.K)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key `k` to a value `v` such that `key` compares equal to `k` according to the map's ordering, then this method returns `v`; otherwise it returns `null`. (There can be at most one such mapping.)

A return value of `null` does not *necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to `null`. The `https://developer.android.com/reference/kotlin/java/util/TreeMap#containsKey(java.util.TreeMap.K)` operation may be used to distinguish these two cases.

| Parameters ||
|---|---|
| `key` | K: the key whose associated value is to be returned |

| Return ||
|---|---|
| `V?` | the value to which the specified key is mapped, or `null` if this map contains no mapping for the key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

### headMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun headMap(toKey: K): SortedMap<K, V>
```

| Parameters ||
|---|---|
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/SortedMap<K, V>` | a view of the portion of this map whose keys are strictly less than `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `toKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun headMap(
    toKey: K, 
    inclusive: Boolean
): NavigableMap<K, V>
```

| Parameters ||
|---|---|
| `toKey` | K: high endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap<K, V>` | a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `toKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

### higherEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun higherEntry(key: K): MutableEntry<K, V>?
```

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

### lastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastEntry(): MutableEntry<K, V>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key, or `null` if this map is empty |

### lastKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |

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

This method will, on a best-effort basis, throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException` if it is detected that the remapping function modifies this map during computation.

| Parameters ||
|---|---|
| `key` | K: key with which the resulting value is to be associated |
| `value` | V: the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](../java/util/function/BiFunction.md)\<in V, in V, out V?\>: the remapping function to recompute a value if present |
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
| `java.util.ConcurrentModificationException` | if it is detected that the remapping function modified this map |

### navigableKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun navigableKeySet(): NavigableSet<K>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet<K>` | a navigable set view of the keys in this map |

### pollFirstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollFirstEntry(): MutableEntry<K, V>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed first entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### pollLastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollLastEntry(): MutableEntry<K, V>?
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed last entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

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
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this map. These mappings replace any mappings that this map had for any of the keys currently in the specified map.

| Parameters ||
|---|---|
| `m` | mappings to be stored in this map |
| `map` | mappings to be stored in this map |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null or the specified map contains a null key and this map does not permit null keys |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putAll` operation is not supported by this map |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for this key from this TreeMap if present.

| Parameters ||
|---|---|
| `key` | K: key for which mapping should be removed |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: K): V?
```

Removes the mapping for this key from this TreeMap if present.

| Parameters ||
|---|---|
| `key` | K: key for which mapping should be removed |

| Return ||
|---|---|
| `V?` | the previous value associated with `key`, or `null` if there was no mapping for `key`. (A `null` return can also indicate that the map previously associated `null` with `key`.) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map uses natural ordering, or its comparator does not permit null keys |
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
| `function` | [BiFunction](../java/util/function/BiFunction.md)\<in K, in V, out V\>: the function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `set` operation is not supported by this map's entry set iterator. |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subMap(
    fromKey: K, 
    fromInclusive: Boolean, 
    toKey: K, 
    toInclusive: Boolean
): NavigableMap<K, V>
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
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap<K, V>` | a view of the portion of this map whose keys range from `fromKey` to `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

### subMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subMap(
    fromKey: K, 
    toKey: K
): SortedMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/SortedMap<K, V>` | a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

### tailMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun tailMap(fromKey: K): SortedMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/SortedMap<K, V>` | a view of the portion of this map whose keys are greater than or equal to `fromKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun tailMap(
    fromKey: K, 
    inclusive: Boolean
): NavigableMap<K, V>
```

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap<K, V>` | a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` is null and this map uses natural ordering, or its comparator does not permit null keys |
| --- | --- |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the mappings contained in this map.

The set's iterator returns the entries in ascending key order. The set's spliterator is * [late-binding](../java/util/Spliterator.md)* , *fail-fast* , and additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int` with an encounter order that is ascending key order.

The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | a set view of the mappings contained in this map, sorted in ascending key order |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val keys: MutableSet<K>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set` view of the keys contained in this map.

The set's iterator returns the keys in ascending order. The set's spliterator is * [late-binding](../java/util/Spliterator.md)* , *fail-fast* , and additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int` with an encounter order that is ascending key order. The spliterator's comparator (see `https://developer.android.com/reference/kotlin/java/util/Spliterator#getComparator()`) is `null` if the tree map's comparator (see `https://developer.android.com/reference/kotlin/java/util/TreeMap#comparator()`) is `null`. Otherwise, the spliterator's comparator is the same as or imposes the same total ordering as the tree map's comparator.

The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | a set view of the keys contained in this map, sorted in ascending order |

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

Returns a `https://developer.android.com/reference/kotlin/java/util/Collection` view of the values contained in this map.

The collection's iterator returns the values in ascending order of the corresponding keys. The collection's spliterator is * [late-binding](../java/util/Spliterator.md)* , *fail-fast* , and additionally reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int` with an encounter order that is ascending order of the corresponding keys.

The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a collection view of the values contained in this map, sorted in ascending key order |
