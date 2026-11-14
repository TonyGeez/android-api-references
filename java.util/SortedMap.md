# SortedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SortedMap

```
interface SortedMap<K : Any!, V : Any!> : MutableMap<K, V>, SequencedMap<K, V>
```

| [java.util.SortedMap](../java/util/SortedMap.md) |

| Known Direct Subclasses [NavigableMap](../java/util/NavigableMap.md) |---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NavigableMap](../java/util/NavigableMap.md) | A [SortedMap](../java/util/SortedMap.md) extended with navigation methods returning the closest matches for given search targets. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md), [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md), [TreeMap](../java/util/TreeMap.md) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) | A [ConcurrentMap](../java/util/concurrent/ConcurrentMap.md) supporting [NavigableMap](../java/util/NavigableMap.md) operations, and recursively so for its navigable sub-maps. | | [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) implementation. | | [TreeMap](../java/util/TreeMap.md) | A Red-Black tree based [NavigableMap](../java/util/NavigableMap.md) implementation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A [Map](../java/util/Map.md) that further provides a*total ordering* on its keys. The map is ordered according to the [ordering](../java/lang/Comparable.md) of its keys, or by a [Comparator](../java/util/Comparator.md) typically provided at sorted map creation time. This order is reflected when iterating over the sorted map's collection views (returned by the`entrySet`,`keySet``values`methods). Several additional operations are provided to take advantage of the ordering. (This interface is the map analogue of [SortedSet](../java/util/SortedSet.md).)

All keys inserted into a sorted map must implement the`Comparable`interface (or be accepted by the specified comparator). Furthermore, all such keys must be*mutually comparable* :`k1.compareTo(k2)`(or`comparator.compare(k1, k2)`) must not throw a`ClassCastException`for any keys`k1`and`k2`in the sorted map. Attempts to violate this restriction will cause the offending method or constructor invocation to throw a`ClassCastException`.

Note that the ordering maintained by a sorted map (whether or not an explicit comparator is provided) must be*consistent with equals* if the sorted map is to correctly implement the`Map`interface. (See the`Comparable`interface or`Comparator`interface for a precise definition of*consistent with equals* .) This is so because the`Map`interface is defined in terms of the`equals`operation, but a sorted map performs all key comparisons using its`compareTo`(or`compare`) method, so two keys that are deemed equal by this method are, from the standpoint of the sorted map, equal. The behavior of a tree map*is* well-defined even if its ordering is inconsistent with equals; it just fails to obey the general contract of the`Map`interface.

All general-purpose sorted map implementation classes should provide four "standard" constructors. It is not possible to enforce this recommendation though as required constructors cannot be specified by interfaces. The expected "standard" constructors for all sorted map implementations are:

1. A void (no arguments) constructor, which creates an empty sorted map sorted according to the natural ordering of its keys.
2. A constructor with a single argument of type`Comparator`, which creates an empty sorted map sorted according to the specified comparator.
3. A constructor with a single argument of type`Map`, which creates a new map with the same key-value mappings as its argument, sorted according to the keys' natural ordering.
4. A constructor with a single argument of type`SortedMap`, which creates a new sorted map with the same key-value mappings and the same ordering as the input sorted map.

**Note** : several methods return submaps with restricted key ranges. Such ranges are*half-open* , that is, they include their low endpoint but not their high endpoint (where applicable). If you need a*closed range* (which includes both endpoints), and the key type allows for calculation of the successor of a given key, merely request the subrange from`lowEndpoint`to`successor(highEndpoint)`. For example, suppose that`m`is a map whose keys are strings. The following idiom obtains a view containing all of the key-value mappings in`m`whose keys are between`low`and`high`, inclusive: 

```kotlin
SortedMap<String, V> sub = m.subMap(low, high+"\0");
```
A similar technique can be used to generate an*open range* (which contains neither endpoint). The following idiom obtains a view containing all of the key-value mappings in`m`whose keys are between`low`and`high`, exclusive: 

```kotlin
SortedMap<String, V> sub = m.subMap(low+"\0", high);
```

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Comparator](../java/util/Comparator.md)\<inK\>? | [comparator](../java/util/SortedMap.md))`()` Returns the comparator used to order the keys in this map, or`null`if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys. |
| abstractK | [firstKey](../java/util/SortedMap.md))`()` Returns the first (lowest) key currently in this map. |
| abstract [SortedMap](../java/util/SortedMap.md)\<K,V\> | [headMap](../java/util/SortedMap.md))`(`toKey:` `K`)` Returns a view of the portion of this map whose keys are strictly less than`toKey`. |
| --- | --- |
| abstractK | [lastKey](../java/util/SortedMap.md))`()` Returns the last (highest) key currently in this map. |
| openV? | [putFirst](../java/util/SortedMap.md))`(`k:` `K`, `v:` `V`)` Throws`UnsupportedOperationException`. |
| openV? | [putLast](../java/util/SortedMap.md))`(`k:` `K`, `v:` `V`)` Throws`UnsupportedOperationException`. |
| --- | --- |
| open [SortedMap](../java/util/SortedMap.md)\<K,V\> | [reversed](../java/util/SortedMap.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this map. |
| abstract [SortedMap](../java/util/SortedMap.md)\<K,V\> | [subMap](../java/util/SortedMap.md))`(`fromKey:` `K`, `toKey:` `K`)` Returns a view of the portion of this map whose keys range from`fromKey`, inclusive, to`toKey`, exclusive. |
| abstract [SortedMap](../java/util/SortedMap.md)\<K,V\> | [tailMap](../java/util/SortedMap.md))`(`fromKey:` `K`)` Returns a view of the portion of this map whose keys are greater than or equal to`fromKey`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [SequencedMap](../java/util/SequencedMap.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [firstEntry](../java/util/SequencedMap.md))`()` <br /> Returns the first key-value mapping in this map, or`null`if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [lastEntry](../java/util/SequencedMap.md))`()` <br /> Returns the last key-value mapping in this map, or`null`if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollFirstEntry](../java/util/SequencedMap.md))`()` <br /> Removes and returns the first key-value mapping in this map, or`null`if the map is empty (optional operation). <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollLastEntry](../java/util/SequencedMap.md))`()` <br /> Removes and returns the last key-value mapping in this map, or`null`if the map is empty (optional operation). <br /> | | [SequencedSet](../java/util/SequencedSet.md)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | [sequencedEntrySet](../java/util/SequencedMap.md))`()` <br /> Returns a`SequencedSet`view of this map's [entrySet](../java/util/Map.md)). <br /> | | [SequencedSet](../java/util/SequencedSet.md)<K>! | [sequencedKeySet](../java/util/SequencedMap.md))`()` <br /> Returns a`SequencedSet`view of this map's [keySet](../java/util/Map.md)). <br /> | | [SequencedCollection](../java/util/SequencedCollection.md)<V>! | [sequencedValues](../java/util/SequencedMap.md))`()` <br /> Returns a`SequencedCollection`view of this map's [values](../java/util/Map.md))collection. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](../java/util/SortedMap.md) Returns a [Set](../java/util/Set.md) view of the mappings contained in this map. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](../java/util/SortedMap.md) Returns a [Set](../java/util/Set.md) view of the keys contained in this map. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](../java/util/SortedMap.md) Returns a [Collection](../java/util/Collection.md) view of the values contained in this map. |
| --- | --- |

## Public methods

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun comparator(): Comparator<in K>?
```

Returns the comparator used to order the keys in this map, or`null`if this map uses the [natural ordering](../java/lang/Comparable.md) of its keys.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Comparator](../java/util/Comparator.md)<in` `K>? | the comparator used to order the keys in this map, or`null`if this map uses the natural ordering of its keys |

### firstKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun firstKey(): K
```

Returns the first (lowest) key currently in this map.

| Return ||
|---|----------------------------------------------|
| K | the first (lowest) key currently in this map |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this map is empty |

### headMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headMap(toKey: K): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys are strictly less than`toKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an`IllegalArgumentException`on an attempt to insert a key outside its range.

| Parameters ||
|---------|-------------------------------------------------------------|
| `toKey` | K:high endpoint (exclusive) of the keys in the returned map |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [SortedMap](../java/util/SortedMap.md)<K,` `V> | a view of the portion of this map whose keys are strictly less than`toKey` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toKey`is not compatible with this map's comparator (or, if the map has no comparator, if`toKey`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`toKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and`toKey`lies outside the bounds of the range |
| --- | --- |

### lastKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lastKey(): K
```

Returns the last (highest) key currently in this map.

| Return ||
|---|----------------------------------------------|
| K | the last (highest) key currently in this map |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this map is empty |

### putFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putFirst(
    k: K, 
    v: V
): V?
```

Throws`UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported.

| Parameters ||
|-----|-------------|
| `k` | K:the key |
| `v` | V:the value |

| Return ||
|----|---------------------------------------------------------|
| V? | the value previously associated with k, or null if none |

| Exceptions ||
|-------------------------------------------|--------|
| `java.lang.UnsupportedOperationException` | always |

### putLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLast(
    k: K, 
    v: V
): V?
```

Throws`UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported.

| Parameters ||
|-----|-------------|
| `k` | K:the key |
| `v` | V:the value |

| Return ||
|----|---------------------------------------------------------|
| V? | the value previously associated with k, or null if none |

| Exceptions ||
|-------------------------------------------|--------|
| `java.lang.UnsupportedOperationException` | always |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reversed(): SortedMap<K, V>
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [SortedMap](../java/util/SortedMap.md)<K,` `V> | a reverse-ordered view of this map, as a`SortedMap` |

### subMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subMap(
    fromKey: K, 
    toKey: K
): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys range from`fromKey`, inclusive, to`toKey`, exclusive. (If`fromKey`and`toKey`are equal, the returned map is empty.) The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an`IllegalArgumentException`on an attempt to insert a key outside its range.

| Parameters ||
|-----------|-------------------------------------------------------------|
| `fromKey` | K:low endpoint (inclusive) of the keys in the returned map |
| `toKey` | K:high endpoint (exclusive) of the keys in the returned map |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [SortedMap](../java/util/SortedMap.md)<K,` `V> | a view of the portion of this map whose keys range from`fromKey`, inclusive, to`toKey`, exclusive |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromKey`and`toKey`cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromKey`or`toKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`fromKey`or`toKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if`fromKey`is greater than`toKey`; or if this map itself has a restricted range, and`fromKey`or`toKey`lies outside the bounds of the range |
| --- | --- |

### tailMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailMap(fromKey: K): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys are greater than or equal to`fromKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an`IllegalArgumentException`on an attempt to insert a key outside its range.

| Parameters ||
|-----------|------------------------------------------------------------|
| `fromKey` | K:low endpoint (inclusive) of the keys in the returned map |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [SortedMap](../java/util/SortedMap.md)<K,` `V> | a view of the portion of this map whose keys are greater than or equal to`fromKey` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromKey`is not compatible with this map's comparator (or, if the map has no comparator, if`fromKey`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`fromKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and`fromKey`lies outside the bounds of the range |
| --- | --- |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](../java/util/Set.md) view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation, or through the`setValue`operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the mappings contained in this map, sorted in ascending key order |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val keys: MutableSet<K>
```

Returns a [Set](../java/util/Set.md) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | a set view of the keys contained in this map, sorted in ascending order |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val values: MutableCollection<V>
```

Returns a [Collection](../java/util/Collection.md) view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map, sorted in ascending key order |
