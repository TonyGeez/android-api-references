# SequencedMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedMap

```
interface SequencedMap<K : Any!, V : Any!> : MutableMap<K, V>
```

| [java.util.SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap#) |

| Known Direct Subclasses [LinkedHashMap](https://developer.android.com/reference/kotlin/java/util/LinkedHashMap), [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------| | [LinkedHashMap](https://developer.android.com/reference/kotlin/java/util/LinkedHashMap) | Hash table and linked list implementation of the`Map`interface, with well-defined encounter order. | | [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap) | A [Map](https://developer.android.com/reference/kotlin/java/util/Map) that further provides a*total ordering*on its keys. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap), [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap), [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap), [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap) | A [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap) supporting [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) operations, and recursively so for its navigable sub-maps. | | [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap) | A scalable concurrent [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap) implementation. | | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) | A [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap) extended with navigation methods returning the closest matches for given search targets. | | [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap) | A Red-Black tree based [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap) implementation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Map that has a well-defined encounter order, that supports operations at both ends, and that is reversible. The [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter) of a`SequencedMap`is similar to that of the elements of a [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection), but the ordering applies to mappings instead of individual elements.

The bulk operations on this map, including the [forEach](https://developer.android.com/reference/kotlin/java/util/Map#forEach(java.util.function.BiConsumer))and the [replaceAll](https://developer.android.com/reference/kotlin/java/util/Map#replaceAll(java.util.function.BiFunction))methods, operate on this map's mappings in encounter order.

The view collections provided by the [keySet](https://developer.android.com/reference/kotlin/java/util/Map#keySet()), [values](https://developer.android.com/reference/kotlin/java/util/Map#values()), [entrySet](https://developer.android.com/reference/kotlin/java/util/Map#entrySet()), [sequencedKeySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedKeySet()), [sequencedValues](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedValues()), and [sequencedEntrySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedEntrySet())methods all reflect the encounter order of this map. Even though the return values of the`keySet`,`values`, and`entrySet`methods are not sequenced*types* , the elements in those view collections do reflect the encounter order of this map. Thus, the iterators returned by the statements {@snippet : \* var it1 = sequencedMap.entrySet().iterator(); \* var it2 = sequencedMap.sequencedEntrySet().iterator(); \* } both provide the mappings of`sequencedMap`in that map's encounter order.

This interface provides methods to add mappings, to retrieve mappings, and to remove mappings at either end of the map's encounter order.

This interface also defines the [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedMap#reversed())method, which provides a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this map. In the reverse-ordered view, the concepts of first and last are inverted, as are the concepts of successor and predecessor. The first mapping of this map is the last mapping of the reverse-ordered view, and vice-versa. The successor of some mapping in this map is its predecessor in the reversed view, and vice-versa. All methods that respect the encounter order of the map operate as if the encounter order is inverted. For instance, the [forEach](https://developer.android.com/reference/kotlin/java/util/Map#forEach(java.util.function.BiConsumer))method of the reversed view reports the mappings in order from the last mapping of this map to the first. In addition, all of the view collections of the reversed view also reflect the inverse of this map's encounter order. For example, {@snippet : \* var itr = sequencedMap.reversed().entrySet().iterator(); \* } provides the mappings of this map in the inverse of the encounter order, that is, from the last mapping to the first mapping. The availability of the`reversed`method, and its impact on the ordering semantics of all applicable methods and views, allow convenient iteration, searching, copying, and streaming of this map's mappings in either forward order or reverse order.

A map's reverse-ordered view is generally not serializable, even if the original map is serializable.

The [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry) instances obtained by iterating the [entrySet](https://developer.android.com/reference/kotlin/java/util/Map#entrySet())view, the [sequencedEntrySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedEntrySet())view, and its reverse-ordered view, maintain a connection to the underlying map. This connection is guaranteed only during the iteration. It is unspecified whether the connection is maintained outside of the iteration. If the underlying map permits it, calling an Entry's [setValue](https://developer.android.com/reference/kotlin/java/util/Map.Entry#setValue(java.util.Map.Entry.V))method will modify the value of the underlying mapping. It is, however, unspecified whether modifications to the value in the underlying mapping are visible in the`Entry`instance.

The methods [firstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#firstEntry()), [lastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#lastEntry()), [pollFirstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollFirstEntry()), and [pollLastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollLastEntry())return [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry) instances that represent snapshots of mappings as of the time of the call. They do*not* support mutation of the underlying map via the optional [setValue](https://developer.android.com/reference/kotlin/java/util/Map.Entry#setValue(java.util.Map.Entry.V))method.

Depending upon the implementation, the`Entry`instances returned by other means might or might not be connected to the underlying map. For example, consider an`Entry`obtained in the following manner: {@snippet : \* var entry = sequencedMap.sequencedEntrySet().getFirst(); \* } It is not specified by this interface whether the`setValue`method of the`Entry`thus obtained will update a mapping in the underlying map, or whether it will throw an exception, or whether changes to the underlying map are visible in that`Entry`.

This interface has the same requirements on the`equals`and`hashCode`methods as defined by [Map.equals](https://developer.android.com/reference/kotlin/java/util/SequencedMap#) and [Map.hashCode](https://developer.android.com/reference/kotlin/java/util/SequencedMap#). Thus, a`Map`and a`SequencedMap`will compare equals if and only if they have equal mappings, irrespective of ordering.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [firstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#firstEntry())`()` Returns the first key-value mapping in this map, or`null`if the map is empty. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [lastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#lastEntry())`()` Returns the last key-value mapping in this map, or`null`if the map is empty. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [pollFirstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollFirstEntry())`()` Removes and returns the first key-value mapping in this map, or`null`if the map is empty (optional operation). |
| --- | --- |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>! | [pollLastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap#pollLastEntry())`()` Removes and returns the last key-value mapping in this map, or`null`if the map is empty (optional operation). |
| openV | [putFirst](https://developer.android.com/reference/kotlin/java/util/SequencedMap#putFirst(java.util.SequencedMap.K,%20java.util.SequencedMap.V))`(`k:` `K`, `v:` `V`)` Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). |
| openV | [putLast](https://developer.android.com/reference/kotlin/java/util/SequencedMap#putLast(java.util.SequencedMap.K,%20java.util.SequencedMap.V))`(`k:` `K`, `v:` `V`)` Inserts the given mapping into the map if it is not already present, or replaces the value of a mapping if it is already present (optional operation). |
| --- | --- |
| abstract [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap#)\<K,V\>! | [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedMap#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this map. |
| open [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>! | [sequencedEntrySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedEntrySet())`()` Returns a`SequencedSet`view of this map's [entrySet](https://developer.android.com/reference/kotlin/java/util/Map#entrySet()). |
| open [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)\<K\>! | [sequencedKeySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedKeySet())`()` Returns a`SequencedSet`view of this map's [keySet](https://developer.android.com/reference/kotlin/java/util/Map#keySet()). |
| --- | --- |
| open [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)\<V\>! | [sequencedValues](https://developer.android.com/reference/kotlin/java/util/SequencedMap#sequencedValues())`()` Returns a`SequencedCollection`view of this map's [values](https://developer.android.com/reference/kotlin/java/util/Map#values())collection. |

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

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------|
| [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap#)<K,` `V>! | a reverse-ordered view of this map |

### sequencedEntrySet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedEntrySet(): SequencedSet<MutableEntry<K, V>!>!
```

Returns a`SequencedSet`view of this map's [entrySet](https://developer.android.com/reference/kotlin/java/util/Map#entrySet()).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | a`SequencedSet`view of this map's`entrySet` |

### sequencedKeySet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedKeySet(): SequencedSet<K>!
```

Returns a`SequencedSet`view of this map's [keySet](https://developer.android.com/reference/kotlin/java/util/Map#keySet()).

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------|
| [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)<K>! | a`SequencedSet`view of this map's`keySet` |

### sequencedValues

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sequencedValues(): SequencedCollection<V>!
```

Returns a`SequencedCollection`view of this map's [values](https://developer.android.com/reference/kotlin/java/util/Map#values())collection.

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)<V>! | a`SequencedCollection`view of this map's`values`collection |
