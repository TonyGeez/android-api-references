# SortedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SortedMap

```
interface SortedMap<K : Any!, V : Any!> : MutableMap<K, V>, SequencedMap<K, V>
```

| [java.util.SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#) |

| Known Direct Subclasses [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) |---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) | A [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#) extended with navigation methods returning the closest matches for given search targets. | |

| Known Indirect Subclasses [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap), [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap), [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap) | A [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap) supporting [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) operations, and recursively so for its navigable sub-maps. | | [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap) | A scalable concurrent [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap) implementation. | | [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap) | A Red-Black tree based [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) implementation. | |

A [Map](https://developer.android.com/reference/kotlin/java/util/Map) that further provides a*total ordering* on its keys. The map is ordered according to the [ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its keys, or by a [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator) typically provided at sorted map creation time. This order is reflected when iterating over the sorted map's collection views (returned by the`entrySet`,`keySet``values`methods). Several additional operations are provided to take advantage of the ordering. (This interface is the map analogue of [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet).)

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
| abstract [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inK\>? | [comparator](https://developer.android.com/reference/kotlin/java/util/SortedMap#comparator())`()` Returns the comparator used to order the keys in this map, or`null`if this map uses the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its keys. |
| abstractK | [firstKey](https://developer.android.com/reference/kotlin/java/util/SortedMap#firstKey())`()` Returns the first (lowest) key currently in this map. |
| abstract [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)\<K,V\> | [headMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#headMap(java.util.SortedMap.K))`(`toKey:` `K`)` Returns a view of the portion of this map whose keys are strictly less than`toKey`. |
| abstractK | [lastKey](https://developer.android.com/reference/kotlin/java/util/SortedMap#lastKey())`()` Returns the last (highest) key currently in this map. |
| openV? | [putFirst](https://developer.android.com/reference/kotlin/java/util/SortedMap#putFirst(java.util.SortedMap.K,%20java.util.SortedMap.V))`(`k:` `K`, `v:` `V`)` Throws`UnsupportedOperationException`. |
| openV? | [putLast](https://developer.android.com/reference/kotlin/java/util/SortedMap#putLast(java.util.SortedMap.K,%20java.util.SortedMap.V))`(`k:` `K`, `v:` `V`)` Throws`UnsupportedOperationException`. |
| open [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)\<K,V\> | [reversed](https://developer.android.com/reference/kotlin/java/util/SortedMap#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this map. |
| abstract [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)\<K,V\> | [subMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#subMap(java.util.SortedMap.K,%20java.util.SortedMap.K))`(`fromKey:` `K`, `toKey:` `K`)` Returns a view of the portion of this map whose keys range from`fromKey`, inclusive, to`toKey`, exclusive. |
| abstract [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)\<K,V\> | [tailMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#tailMap(java.util.SortedMap.K))`(`fromKey:` `K`)` Returns a view of the portion of this map whose keys are greater than or equal to`fromKey`. |

| Inherited functions ||
|---|---|
| From class [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [firstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#firstEntry())`()` <br /> Returns the first key-value mapping in this map, or`null`if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [lastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#lastEntry())`()` <br /> Returns the last key-value mapping in this map, or`null`if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollFirstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollFirstEntry())`()` <br /> Removes and returns the first key-value mapping in this map, or`null`if the map is empty (optional operation). <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollLastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollLastEntry())`()` <br /> Removes and returns the last key-value mapping in this map, or`null`if the map is empty (optional operation). <br /> | | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | [sequencedEntrySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedEntrySet())`()` <br /> Returns a`SequencedSet`view of this map's [entrySet](https://developer.android.com/reference/kotlin/java/util/Map#entrySet()). <br /> | | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)<K>! | [sequencedKeySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedKeySet())`()` <br /> Returns a`SequencedSet`view of this map's [keySet](https://developer.android.com/reference/kotlin/java/util/Map#keySet()). <br /> | | [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)<V>! | [sequencedValues](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedValues())`()` <br /> Returns a`SequencedCollection`view of this map's [values](https://developer.android.com/reference/kotlin/java/util/Map#values())collection. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](https://developer.android.com/reference/kotlin/java/util/SortedMap#entries:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the mappings contained in this map. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](https://developer.android.com/reference/kotlin/java/util/SortedMap#keys:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the keys contained in this map. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](https://developer.android.com/reference/kotlin/java/util/SortedMap#values:kotlin.collections.MutableCollection) Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) view of the values contained in this map. |

## Public methods

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun comparator(): Comparator<in K>?
```

Returns the comparator used to order the keys in this map, or`null`if this map uses the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its keys.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `K>? | the comparator used to order the keys in this map, or`null`if this map uses the natural ordering of its keys |

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
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)<K,` `V> | a view of the portion of this map whose keys are strictly less than`toKey` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toKey`is not compatible with this map's comparator (or, if the map has no comparator, if`toKey`does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if`toKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`toKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and`toKey`lies outside the bounds of the range |

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

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)<K,` `V> | a reverse-ordered view of this map, as a`SortedMap` |

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
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)<K,` `V> | a view of the portion of this map whose keys range from`fromKey`, inclusive, to`toKey`, exclusive |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromKey`and`toKey`cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromKey`or`toKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`fromKey`or`toKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if`fromKey`is greater than`toKey`; or if this map itself has a restricted range, and`fromKey`or`toKey`lies outside the bounds of the range |

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
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap#)<K,` `V> | a view of the portion of this map whose keys are greater than or equal to`fromKey` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromKey`is not compatible with this map's comparator (or, if the map has no comparator, if`fromKey`does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if`fromKey`cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if`fromKey`is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and`fromKey`lies outside the bounds of the range |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation, or through the`setValue`operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the mappings contained in this map, sorted in ascending key order |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val keys: MutableSet<K>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | a set view of the keys contained in this map, sorted in ascending order |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val values: MutableCollection<V>
```

Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map, sorted in ascending key order |
