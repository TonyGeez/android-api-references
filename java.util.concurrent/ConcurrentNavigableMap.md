# ConcurrentNavigableMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentNavigableMap

```
interface ConcurrentNavigableMap<K : Any!, V : Any!> : ConcurrentMap<K, V>, NavigableMap<K, V>
```

| [java.util.concurrent.ConcurrentNavigableMap](ConcurrentNavigableMap.md) |

| Known Direct Subclasses [ConcurrentSkipListMap](ConcurrentSkipListMap.md) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListMap](ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](ConcurrentNavigableMap.md) implementation. | |
| --- | --- | --- | --- | --- | --- | --- |

A [ConcurrentMap](ConcurrentMap.md) supporting [NavigableMap](../java.util/NavigableMap.md) operations, and recursively so for its navigable sub-maps.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NavigableSet](../java.util/NavigableSet.md)\<K\> | [descendingKeySet](ConcurrentNavigableMap.md))`()` Returns a reverse order [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [descendingMap](ConcurrentNavigableMap.md))`()` Returns a reverse order view of the mappings contained in this map. |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [headMap](ConcurrentNavigableMap.md))`(`toKey:` `K`)` <br /> |
| --- | --- |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [headMap](ConcurrentNavigableMap.md))`(`toKey:` `K`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| abstract [NavigableSet](../java.util/NavigableSet.md)\<K\> | [navigableKeySet](ConcurrentNavigableMap.md))`()` Returns a [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [subMap](ConcurrentNavigableMap.md))`(`fromKey:` `K`, `fromInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `toKey:` `K`, `toInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [subMap](ConcurrentNavigableMap.md))`(`fromKey:` `K`, `toKey:` `K`)` <br /> |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [tailMap](ConcurrentNavigableMap.md))`(`fromKey:` `K`)` <br /> |
| abstract [ConcurrentNavigableMap](ConcurrentNavigableMap.md)\<K, V\> | [tailMap](ConcurrentNavigableMap.md))`(`fromKey:` `K`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [NavigableMap](../java.util/NavigableMap.md) |---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [ceilingEntry](../java.util/NavigableMap.md))`(`key:` `K`)` Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such key. <br /> | | K? | [ceilingKey](../java.util/NavigableMap.md))`(`key:` `K`)` Returns the least key greater than or equal to the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [firstEntry](../java.util/NavigableMap.md))`()` Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [floorEntry](../java.util/NavigableMap.md))`(`key:` `K`)` Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key. <br /> | | K? | [floorKey](../java.util/NavigableMap.md))`(`key:` `K`)` Returns the greatest key less than or equal to the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [higherEntry](../java.util/NavigableMap.md))`(`key:` `K`)` Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key. <br /> | | K? | [higherKey](../java.util/NavigableMap.md))`(`key:` `K`)` Returns the least key strictly greater than the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [lastEntry](../java.util/NavigableMap.md))`()` Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [lowerEntry](../java.util/NavigableMap.md))`(`key:` `K`)` Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key. <br /> | | K? | [lowerKey](../java.util/NavigableMap.md))`(`key:` `K`)` Returns the greatest key strictly less than the given key, or `null` if there is no such key. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [pollFirstEntry](../java.util/NavigableMap.md))`()` Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | [pollLastEntry](../java.util/NavigableMap.md))`()` Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. <br /> | | [NavigableMap](../java.util/NavigableMap.md)<K,` `V> | [reversed](../java.util/NavigableMap.md))`()` Returns a reverse-ordered [view](../java.util/Collection.md) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation. This method is equivalent to [descendingMap](../java.util/NavigableMap.md)). <br /> | ||
| From class [SortedMap](../java.util/SortedMap.md) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Comparator](../java.util/Comparator.md)<in` `K>? | [comparator](../java.util/SortedMap.md))`()` Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java.lang/Comparable.md) of its keys. <br /> | | K | [firstKey](../java.util/SortedMap.md))`()` Returns the first (lowest) key currently in this map. <br /> | | K | [lastKey](../java.util/SortedMap.md))`()` Returns the last (highest) key currently in this map. <br /> | | V? | [putFirst](../java.util/SortedMap.md))`(`k:` `K`, `v:` `V`)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | | V? | [putLast](../java.util/SortedMap.md))`(`k:` `K`, `v:` `V`)` Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | ||
| From class [ConcurrentMap](ConcurrentMap.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V? | [compute](ConcurrentMap.md))`(`key:` `K`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V?,` `out` `V?>`)` Attempts to compute a mapping for the specified key and its current mapped value (or `null` if there is no current mapping). For example, to either create or append a `String` msg to a value mapping: ```kotlin <code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code> ``` (Method [merge()](../java.util/Map.md)) is often simpler to use for such purposes.) <br /> If the remapping function returns `null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | V | [computeIfAbsent](ConcurrentMap.md))`(`key:` `K`, `mappingFunction:` ` [Function](../java.util.function/Function.md)<in` `K,` `out` `V>`)` If the specified key is not already associated with a value (or is mapped to `null`), attempts to compute its value using the given mapping function and enters it into this map unless `null`. If the mapping function returns `null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in: ```kotlin <code>map.computeIfAbsent(key, k -&gt; new Value(f(k))); </code> ``` Or to implement a multi-value map, `Map<K,Collection<V>>`, supporting multiple values per key: ```kotlin <code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v); </code> ``` The mapping function should not modify this map during computation. <br /> | | V? | [computeIfPresent](ConcurrentMap.md))`(`key:` `K`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V,` `out` `V?>`)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ConcurrentMap.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `K,` `in` `V>`)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller. <br /> | | V | [getOrDefault](ConcurrentMap.md))`(`key:` `K`, `defaultValue:` `V`)` Returns the value to which the specified key is mapped, or `defaultValue` if this map contains no mapping for the key. <br /> | | V? | [merge](ConcurrentMap.md))`(`key:` `K`, `value:` `V`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `V,` `in` `V,` `out` `V?>`)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is `null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a `String msg` to a value mapping: ```kotlin <code>map.merge(key, msg, String::concat) </code> ``` <br /> If the remapping function returns `null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged. The remapping function should not modify this map during computation. <br /> | | V? | [putIfAbsent](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` If the specified key is not already associated with a value, associates it with the given value. This is equivalent to, for this `map`: ```kotlin <code>if (!map.containsKey(key)) return map.put(key, value); else return map.get(key);</code> ``` except that the action is performed atomically. <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` Removes the entry for a key only if currently mapped to a given value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key) &amp;&amp; Objects.equals(map.get(key), value)) { map.remove(key); return true; } else { return false; }</code> ``` except that the action is performed atomically. <br /> <br /> | | V? | [replace](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` Replaces the entry for a key only if currently mapped to some value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key)) return map.put(key, value); else return null;</code> ``` except that the action is performed atomically. <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](ConcurrentMap.md))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` Replaces the entry for a key only if currently mapped to a given value. This is equivalent to, for this `map`: ```kotlin <code>if (map.containsKey(key) &amp;&amp; Objects.equals(map.get(key), oldValue)) { map.put(key, newValue); return true; } else { return false; }</code> ``` except that the action is performed atomically. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](ConcurrentMap.md))`(`function:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V,` `out` `V>`)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. Exceptions thrown by the function are relayed to the caller. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [SequencedMap](../java.util/SequencedMap.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [firstEntry](../java.util/SequencedMap.md))`()` Returns the first key-value mapping in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [lastEntry](../java.util/SequencedMap.md))`()` Returns the last key-value mapping in this map, or `null` if the map is empty. <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollFirstEntry](../java.util/SequencedMap.md))`()` Removes and returns the first key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>! | [pollLastEntry](../java.util/SequencedMap.md))`()` Removes and returns the last key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | [SequencedSet](../java.util/SequencedSet.md)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>! | [sequencedEntrySet](../java.util/SequencedMap.md))`()` Returns a `SequencedSet` view of this map's [entrySet](../java.util/Map.md)). <br /> | | [SequencedSet](../java.util/SequencedSet.md)<K>! | [sequencedKeySet](../java.util/SequencedMap.md))`()` Returns a `SequencedSet` view of this map's [keySet](../java.util/Map.md)). <br /> | | [SequencedCollection](../java.util/SequencedCollection.md)<V>! | [sequencedValues](../java.util/SequencedMap.md))`()` Returns a `SequencedCollection` view of this map's [values](../java.util/Map.md)) collection. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [NavigableSet](../java.util/NavigableSet.md)\<K\> | [keys](ConcurrentNavigableMap.md) Returns a [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. |

| Inherited properties ||
|---|---|
| From class [SortedMap](../java.util/SortedMap.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | [entries](../java.util/SortedMap.md) Returns a [Set](../java.util/Set.md) view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | [keys](../java.util/SortedMap.md) Returns a [Set](../java.util/Set.md) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | [values](../java.util/SortedMap.md) Returns a [Collection](../java.util/Collection.md) view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | ||

## Public methods

### descendingKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingKeySet(): NavigableSet<K>
```

Returns a reverse order [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. The set's iterator returns the keys in descending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](_package.md).

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<K> | a reverse order navigable set view of the keys in this map |

### descendingMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingMap(): ConcurrentNavigableMap<K, V>
```

Returns a reverse order view of the mappings contained in this map. The descending map is backed by this map, so changes to the map are reflected in the descending map, and vice-versa.

The returned map has an ordering equivalent to java.util.Collections#reverseOrder(Comparator)`(comparator())`. The expression `m.descendingMap().descendingMap()` returns a view of `m` essentially equivalent to `m`.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a reverse order view of this map |

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
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys are strictly less than `toKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| --- | --- |

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
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| --- | --- |

### navigableKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun navigableKeySet(): NavigableSet<K>
```

Returns a [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](_package.md).

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<K> | a navigable set view of the keys in this map |

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
| --- | --- |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys range from `fromKey` to `toKey` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| --- | --- |

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
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| --- | --- |

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
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys are greater than or equal to `fromKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| --- | --- |

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
| [ConcurrentNavigableMap](ConcurrentNavigableMap.md)<K,` `V> | a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| --- | --- |

## Properties

### keys

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val keys: NavigableSet<K>
```

Returns a [NavigableSet](../java.util/NavigableSet.md) view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

The view's iterators and spliterators are [*weakly consistent*](_package.md).

This method is equivalent to method `navigableKeySet`.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<K> | a navigable set view of the keys in this map |
