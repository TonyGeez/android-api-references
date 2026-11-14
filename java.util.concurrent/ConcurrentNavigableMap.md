# ConcurrentNavigableMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentNavigableMap

```
interface ConcurrentNavigableMap<K : Any!, V : Any!> : ConcurrentMap<K, V>, NavigableMap<K, V>
```

| [java.util.concurrent.ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#) |

| Known Direct Subclasses [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap) | A scalable concurrent [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#) implementation. | |

A [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap) supporting [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#) operations, and recursively so for its navigable sub-maps.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)\<K\> | [descendingKeySet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#descendingKeySet())`()` Returns a reverse order [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [descendingMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#descendingMap())`()` Returns a reverse order view of the mappings contained in this map. |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [headMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#headMap(java.util.concurrent.ConcurrentNavigableMap.K))`(`toKey:` `K`)` <br /> |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [headMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#headMap(java.util.concurrent.ConcurrentNavigableMap.K,%20kotlin.Boolean))`(`toKey:` `K`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| abstract [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)\<K\> | [navigableKeySet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#navigableKeySet())`()` Returns a [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [subMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#subMap(java.util.concurrent.ConcurrentNavigableMap.K,%20kotlin.Boolean,%20java.util.concurrent.ConcurrentNavigableMap.K,%20kotlin.Boolean))`(`fromKey:` `K`, `fromInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `toKey:` `K`, `toInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [subMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#subMap(java.util.concurrent.ConcurrentNavigableMap.K,%20java.util.concurrent.ConcurrentNavigableMap.K))`(`fromKey:` `K`, `toKey:` `K`)` <br /> |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [tailMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#tailMap(java.util.concurrent.ConcurrentNavigableMap.K))`(`fromKey:` `K`)` <br /> |
| abstract [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)\<K, V\> | [tailMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#tailMap(java.util.concurrent.ConcurrentNavigableMap.K,%20kotlin.Boolean))`(`fromKey:` `K`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#) |---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [ceilingEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#ceilingEntry(java.util.NavigableMap.K))`(`key:` `K`)` Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such key. <br /> | | K? | [ceilingKey](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#ceilingKey(java.util.NavigableMap.K))`(`key:` `K`)` Returns the least key greater than or equal to the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [firstEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#firstEntry())`()` Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [floorEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#floorEntry(java.util.NavigableMap.K))`(`key:` `K`)` Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key. <br /> | | K? | [floorKey](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#floorKey(java.util.NavigableMap.K))`(`key:` `K`)` Returns the greatest key less than or equal to the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [higherEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#higherEntry(java.util.NavigableMap.K))`(`key:` `K`)` Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key. <br /> | | K? | [higherKey](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#higherKey(java.util.NavigableMap.K))`(`key:` `K`)` Returns the least key strictly greater than the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [lastEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#lastEntry())`()` Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [lowerEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#lowerEntry(java.util.NavigableMap.K))`(`key:` `K`)` Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key. <br /> | | K? | [lowerKey](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#lowerKey(java.util.NavigableMap.K))`(`key:` `K`)` Returns the greatest key strictly less than the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [pollFirstEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#pollFirstEntry())`()` Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [pollLastEntry](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#pollLastEntry())`()` Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. <br /> | | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#)<K,` `V> | [reversed](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection.html#view) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation. This method is equivalent to [descendingMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap.html#descendingMap()). <br /> | ||
| From class [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)<in` `K>? | [comparator](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#comparator())`()` Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its keys. <br /> | | K | [firstKey](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#firstKey())`()` Returns the first (lowest) key currently in this map. <br /> | | K | [lastKey](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#lastKey())`()` Returns the last (highest) key currently in this map. <br /> | | V? | [putFirst](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#putFirst(java.util.SortedMap.K,%20java.util.SortedMap.V))`(`k:` `K`, `v:` `V`)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | | V? | [putLast](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#putLast(java.util.SortedMap.K,%20java.util.SortedMap.V))`(`k:` `K`, `v:` `V`)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | ||
| From class [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V? | [compute](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#compute(java.util.concurrent.ConcurrentMap.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V?,` `out` `V?>`)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). For example, to either create or append a `String` msg to a value mapping: ```kotlin <code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code> ``` (Method [merge()](https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)) is often simpler to use for such purposes.) <br /> If the remapping function returns `null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | V | [computeIfAbsent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#computeIfAbsent(java.util.concurrent.ConcurrentMap.K,%20java.util.function.Function))`(`key:` `K`, `mappingFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `K,` `out` `V>`)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`. If the mapping function returns `null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in: ```kotlin <code>map.computeIfAbsent(key, k -&gt; new Value(f(k))); </code> ``` Or to implement a multi-value map, `Map<K,Collection<V>>`, supporting multiple values per key: ```kotlin <code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v); </code> ``` The mapping function should not modify this map during computation. <br /> | | V? | [computeIfPresent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#computeIfPresent(java.util.concurrent.ConcurrentMap.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `V?>`)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#forEach(java.util.function.BiConsumer))`(`action:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<in` `K,` `in` `V>`)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller. <br /> | | V | [getOrDefault](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#getOrDefault(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V))`(`key:` `K`, `defaultValue:` `V`)` Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key. <br /> | | V? | [merge](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#merge(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V,%20java.util.function.BiFunction))`(`key:` `K`, `value:` `V`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `V,` `in` `V,` `out` `V?>`)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is `null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a `String msg` to a value mapping: ```kotlin <code>map.merge(key, msg, String::concat) </code> ``` <br /> If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | V? | [putIfAbsent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#putIfAbsent(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V))`(`key:` `K`, `value:` `V`)` If the specified key is not already associated with a value, associates it with the given value. This is equivalent to, for this `map`: ```kotlin <code>if (!map.containsKey(key)) return map.put(key, value); else return map.get(key);</code> ``` except that the action is performed atomically. <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#remove(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V))`(`key:` `K`, `value:` `V`)` Removes the entry for a key only if currently mapped to a given value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key) &amp;&amp; Objects.equals(map.get(key), value)) { map.remove(key); return true; } else { return false; }</code> ``` except that the action is performed atomically. <br /> <br /> | | V? | [replace](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#replace(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V))`(`key:` `K`, `value:` `V`)` Replaces the entry for a key only if currently mapped to some value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key)) return map.put(key, value); else return null;</code> ``` except that the action is performed atomically. <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#replace(java.util.concurrent.ConcurrentMap.K,%20java.util.concurrent.ConcurrentMap.V,%20java.util.concurrent.ConcurrentMap.V))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` Replaces the entry for a key only if currently mapped to a given value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key) &amp;&amp; Objects.equals(map.get(key), oldValue)) { map.put(key, newValue); return true; } else { return false; }</code> ``` except that the action is performed atomically. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap#replaceAll(java.util.function.BiFunction))`(`function:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `V>`)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. Exceptions thrown by the function are relayed to the caller. <br /> | ||
| From class [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [firstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#firstEntry())`()` Returns the first key-value mapping in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [lastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#lastEntry())`()` Returns the last key-value mapping in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollFirstEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#pollFirstEntry())`()` Removes and returns the first key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollLastEntry](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#pollLastEntry())`()` Removes and returns the last key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | [sequencedEntrySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#sequencedEntrySet())`()` Returns a `SequencedSet` view of this map's [entrySet](https://developer.android.com/reference/kotlin/java/util/Map.html#entrySet()). <br /> | | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet.html#)<K>! | [sequencedKeySet](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#sequencedKeySet())`()` Returns a `SequencedSet` view of this map's [keySet](https://developer.android.com/reference/kotlin/java/util/Map.html#keySet()). <br /> | | [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection.html#)<V>! | [sequencedValues](https://developer.android.com/reference/kotlin/java/util/SequencedMap.html#sequencedValues())`()` Returns a `SequencedCollection` view of this map's [values](https://developer.android.com/reference/kotlin/java/util/Map.html#values()) collection. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)\<K\> | [keys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#keys:java.util.NavigableSet) Returns a [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. |

| Inherited properties ||
|---|---|
| From class [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | [entries](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#entries:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | [keys](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#keys:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | [values](https://developer.android.com/reference/kotlin/java/util/SortedMap.html#values:kotlin.collections.MutableCollection) Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | ||

## Public methods

### descendingKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingKeySet(): NavigableSet<K>
```

Returns a reverse order [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. The set's iterator returns the keys in descending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)<K> | a reverse order navigable set view of the keys in this map |

### descendingMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingMap(): ConcurrentNavigableMap<K, V>
```

Returns a reverse order view of the mappings contained in this map. The descending map is backed by this map, so changes to the map are reflected in the descending map, and vice-versa.

The returned map has an ordering equivalent to java.util.Collections#reverseOrder(Comparator)`(comparator())`. The expression `m.descendingMap().descendingMap()` returns a view of `m` essentially equivalent to `m`.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a reverse order view of this map |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headMap(toKey: K): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|---------|--------------------------------------------------------------|
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys are strictly less than `toKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headMap(
    toKey: K, 
    inclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toKey` | K: high endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |

### navigableKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun navigableKeySet(): NavigableSet<K>
```

Returns a [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)<K> | a navigable set view of the keys in this map |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subMap(
    fromKey: K, 
    fromInclusive: Boolean, 
    toKey: K, 
    toInclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `fromInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |
| `toKey` | K: high endpoint of the keys in the returned map |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys range from `fromKey` to `toKey` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subMap(
    fromKey: K, 
    toKey: K
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|-----------|--------------------------------------------------------------|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |
| `toKey` | K: high endpoint (exclusive) of the keys in the returned map |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailMap(fromKey: K): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|-----------|-------------------------------------------------------------|
| `fromKey` | K: low endpoint (inclusive) of the keys in the returned map |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys are greater than or equal to `fromKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailMap(
    fromKey: K, 
    inclusive: Boolean
): ConcurrentNavigableMap<K, V>
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentNavigableMap#)<K,` `V> | a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#)). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |

## Properties

### keys

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val keys: NavigableSet<K>
```

Returns a [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

This method is equivalent to method `navigableKeySet`.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet.html#)<K> | a navigable set view of the keys in this map |
