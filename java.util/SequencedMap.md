# SequencedMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedMap

```
interface SequencedMap<K : Any!, V : Any!> : MutableMap<K, V>
```

| [java.util.SequencedMap](../java/util/SequencedMap.md) |

| Known Direct Subclasses [LinkedHashMap](../java/util/LinkedHashMap.md), [SortedMap](../java/util/SortedMap.md) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------| | [LinkedHashMap](../java/util/LinkedHashMap.md) | Hash table and linked list implementation of the`Map`interface, with well-defined encounter order. | | [SortedMap](../java/util/SortedMap.md) | A [Map](../java/util/Map.md) that further provides a*total ordering*on its keys. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md), [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md), [NavigableMap](../java/util/NavigableMap.md), [TreeMap](../java/util/TreeMap.md) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) | A [ConcurrentMap](../java/util/concurrent/ConcurrentMap.md) supporting [NavigableMap](../java/util/NavigableMap.md) operations, and recursively so for its navigable sub-maps. | | [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](../java/util/concurrent/ConcurrentNavigableMap.md) implementation. | | [NavigableMap](../java/util/NavigableMap.md) | A [SortedMap](../java/util/SortedMap.md) extended with navigation methods returning the closest matches for given search targets. | | [TreeMap](../java/util/TreeMap.md) | A Red-Black tree based [NavigableMap](../java/util/NavigableMap.md) implementation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Map that has a well-defined encounter order, that supports operations at both ends, and that is reversible. The [encounter order](../java/util/SequencedCollection.md) of a`SequencedMap`is similar to that of the elements of a [SequencedCollection](../java/util/SequencedCollection.md), but the ordering applies to mappings instead of individual elements.

The bulk operations on this map, including the [forEach](../java/util/Map.md))and the [replaceAll](../java/util/Map.md))methods, operate on this map's mappings in encounter order.

The view collections provided by the [keySet](../java/util/Map.md)), [values](../java/util/Map.md)), [entrySet](../java/util/Map.md)), [sequencedKeySet](../java/util/SequencedMap.md)), [sequencedValues](../java/util/SequencedMap.md)), and [sequencedEntrySet](../java/util/SequencedMap.md))methods all reflect the encounter order of this map. Even though the return values of the`keySet`,`values`, and`entrySet`methods are not sequenced*types* , the elements in those view collections do reflect the encounter order of this map. Thus, the iterators returned by the statements {@snippet : \* var it1 = sequencedMap.entrySet().iterator(); \* var it2 = sequencedMap.sequencedEntrySet().iterator(); \* } both provide the mappings of`sequencedMap`in that map's encounter order.

This interface provides methods to add mappings, to retrieve mappings, and to remove mappings at either end of the map's encounter order.

This interface also defines the [reversed](../java/util/SequencedMap.md))method, which provides a reverse-ordered [view](../java/util/Collection.md) of this map. In the reverse-ordered view, the concepts of first and last are inverted, as are the concepts of successor and predecessor. The first mapping of this map is the last mapping of the reverse-ordered view, and vice-versa. The successor of some mapping in this map is its predecessor in the reversed view, and vice-versa. All methods that respect the encounter order of the map operate as if the encounter order is inverted. For instance, the [forEach](../java/util/Map.md))method of the reversed view reports the mappings in order from the last mapping of this map to the first. In addition, all of the view collections of the reversed view also reflect the inverse of this map's encounter order. For example, {@snippet : \* var itr = sequencedMap.reversed().entrySet().iterator(); \* } provides the mappings of this map in the inverse of the encounter order, that is, from the last mapping to the first mapping. The availability of the`reversed`method, and its impact on the ordering semantics of all applicable methods and views, allow convenient iteration, searching, copying, and streaming of this map's mappings in either forward order or reverse order.

A map's reverse-ordered view is generally not serializable, even if the original map is serializable.

The [Map.Entry](../java/util/Map.Entry.md) instances obtained by iterating the [entrySet](../java/util/Map.md))view, the [sequencedEntrySet](../java/util/SequencedMap.md))view, and its reverse-ordered view, maintain a connection to the underlying map. This connection is guaranteed only during the iteration. It is unspecified whether the connection is maintained outside of the iteration. If the underlying map permits it, calling an Entry's [setValue](../java/util/Map.Entry.md))method will modify the value of the underlying mapping. It is, however, unspecified whether modifications to the value in the underlying mapping are visible in the`Entry`instance.

The methods [firstEntry](../java/util/SequencedMap.md)), [lastEntry](../java/util/SequencedMap.md)), [pollFirstEntry](../java/util/SequencedMap.md)), and [pollLastEntry](../java/util/SequencedMap.md))return [Map.Entry](../java/util/Map.Entry.md) instances that represent snapshots of mappings as of the time of the call. They do*not* support mutation of the underlying map via the optional [setValue](../java/util/Map.Entry.md))method.

Depending upon the implementation, the`Entry`instances returned by other means might or might not be connected to the underlying map. For example, consider an`Entry`obtained in the following manner: {@snippet : \* var entry = sequencedMap.sequencedEntrySet().getFirst(); \* } It is not specified by this interface whether the`setValue`method of the`Entry`thus obtained will update a mapping in the underlying map, or whether it will throw an exception, or whether changes to the underlying map are visible in that`Entry`.

This interface has the same requirements on the`equals`and`hashCode`methods as defined by [Map.equals](../java/util/SequencedMap.md) and [Map.hashCode](../java/util/SequencedMap.md). Thus, a`Map`and a`SequencedMap`will compare equals if and only if they have equal mappings, irrespective of ordering.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [firstEntry](../java/util/SequencedMap.md))`()` Returns the first key-value mapping in this map, or`null`if the map is empty. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [lastEntry](../java/util/SequencedMap.md))`()` Returns the last key-value mapping in this map, or`null`if the map is empty. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [pollFirstEntry](../java/util/SequencedMap.md))`()` Removes and returns the first key-value mapping in this map, or`null`if the map is empty (optional operation). |
| --- | --- |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [pollLastEntry](../java/util/SequencedMap.md))`()` Removes and returns the last key-value mapping in this map, or`null`if the map is empty (optional operation). |
| openV | [putFirst](../java/util/SequencedMap.md))`(`k:` `K`, `v:` `V`)` Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). |
| openV | [putLast](../java/util/SequencedMap.md))`(`k:` `K`, `v:` `V`)` Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). |
| --- | --- |
| abstract [SequencedMap](../java/util/SequencedMap.md)\<K,V\>! | [reversed](../java/util/SequencedMap.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this map. |
| open [SequencedSet](../java/util/SequencedSet.md)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>! | [sequencedEntrySet](../java/util/SequencedMap.md))`()` Returns a`SequencedSet`view of this map's [entrySet](../java/util/Map.md)). |
| open [SequencedSet](../java/util/SequencedSet.md)\<K\>! | [sequencedKeySet](../java/util/SequencedMap.md))`()` Returns a`SequencedSet`view of this map's [keySet](../java/util/Map.md)). |
| --- | --- |
| open [SequencedCollection](../java/util/SequencedCollection.md)\<V\>! | [sequencedValues](../java/util/SequencedMap.md))`()` Returns a`SequencedCollection`view of this map's [values](../java/util/Map.md))collection. |

## Public methods

### firstEntry

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firstEntry(): MutableEntry<K, V>!
```

Returns the first key-value mapping in this map, or`null`if the map is empty.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | the first key-value mapping, or`null`if this map is empty |

### lastEntry

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastEntry(): MutableEntry<K, V>!
```

Returns the last key-value mapping in this map, or`null`if the map is empty.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | the last key-value mapping, or`null`if this map is empty |

### pollFirstEntry

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollFirstEntry(): MutableEntry<K, V>!
```

Removes and returns the first key-value mapping in this map, or`null`if the map is empty (optional operation).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | the removed first entry of this map, or`null`if this map is empty |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### pollLastEntry

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollLastEntry(): MutableEntry<K, V>!
```

Removes and returns the last key-value mapping in this map, or`null`if the map is empty (optional operation).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | the removed last entry of this map, or`null`if this map is empty |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### putFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putFirst(
    k: K, 
    v: V
): V
```

Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). After this operation completes normally, the given mapping will be present in this map, and it will be the first mapping in this map's encounter order.

| Parameters ||
|-----|-------------|
| `k` | K:the key |
| `v` | V:the value |

| Return ||
|---|---------------------------------------------------------|
| V | the value previously associated with k, or null if none |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### putLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLast(
    k: K, 
    v: V
): V
```

Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). After this operation completes normally, the given mapping will be present in this map, and it will be the last mapping in this map's encounter order.

| Parameters ||
|-----|-------------|
| `k` | K:the key |
| `v` | V:the value |

| Return ||
|---|---------------------------------------------------------|
| V | the value previously associated with k, or null if none |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reversed(): SequencedMap<K, V>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------|
| [SequencedMap](../java/util/SequencedMap.md)<K,` `V>! | a reverse-ordered view of this map |

### sequencedEntrySet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedEntrySet(): SequencedSet<MutableEntry<K, V>!>!
```

Returns a`SequencedSet`view of this map's [entrySet](../java/util/Map.md)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [SequencedSet](../java/util/SequencedSet.md)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | a`SequencedSet`view of this map's`entrySet` |

### sequencedKeySet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedKeySet(): SequencedSet<K>!
```

Returns a`SequencedSet`view of this map's [keySet](../java/util/Map.md)).

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------|
| [SequencedSet](../java/util/SequencedSet.md)<K>! | a`SequencedSet`view of this map's`keySet` |

### sequencedValues

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedValues(): SequencedCollection<V>!
```

Returns a`SequencedCollection`view of this map's [values](../java/util/Map.md))collection.

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [SequencedCollection](../java/util/SequencedCollection.md)<V>! | a`SequencedCollection`view of this map's`values`collection |
