Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NavigableMap

```
interface NavigableMap<K : Any!, V : Any!> : SortedMap<K, V>
```

| [java.util.NavigableMap](NavigableMap.md) |

| Known Direct Subclasses [ConcurrentNavigableMap](../java.util.concurrent/ConcurrentNavigableMap.md), [TreeMap](TreeMap.md) |---|---| | [ConcurrentNavigableMap](../java.util.concurrent/ConcurrentNavigableMap.md) | A ConcurrentMap supporting NavigableMap operations, and recursively so for its navigable sub-maps. | | [TreeMap](TreeMap.md) | A Red-Black tree based NavigableMap implementation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentSkipListMap](../java.util.concurrent/ConcurrentSkipListMap.md) |---|---| | [ConcurrentSkipListMap](../java.util.concurrent/ConcurrentSkipListMap.md) | A scalable concurrent ConcurrentNavigableMap implementation. | |
| --- | --- | --- | --- | --- | --- | --- |

A SortedMap extended with navigation methods returning the closest matches for given search targets. Methods lowerEntry, floorEntry, ceilingEntry, and higherEntry return `Map.Entry` objects associated with keys respectively less than, less than or equal, greater than or equal, and greater than a given key, returning `null` if there is no such key. Similarly, methods lowerKey, floorKey, ceilingKey, and higherKey return only the associated keys. All of these methods are designed for locating, not traversing entries.

A `NavigableMap` may be accessed and traversed in either ascending or descending key order. The descendingMap method returns a view of the map with the senses of all relational and directional methods inverted. The performance of ascending operations and views is likely to be faster than that of descending ones. Methods subMap, headMap, and tailMap differ from the like-named `SortedMap` methods in accepting additional arguments describing whether lower and upper bounds are inclusive versus exclusive. Submaps of any `NavigableMap` must implement the `NavigableMap` interface.

This interface additionally defines methods firstEntry, pollFirstEntry, lastEntry, and pollLastEntry that return and/or remove the least and greatest mappings, if any exist, else returning `null`.

The methods ceilingEntry, firstEntry, floorEntry, higherEntry, lastEntry, lowerEntry, pollFirstEntry, and pollLastEntry return `https://developer.android.com/reference/kotlin/java/util/Map.Entry` instances that represent snapshots of mappings as of the time of the call. They do *not* support mutation of the underlying map via the optional setValue method.

Methods subMap, headMap, and tailMap are specified to return `SortedMap` to allow existing implementations of `SortedMap` to be compatibly retrofitted to implement `NavigableMap`, but extensions and implementations of this interface are encouraged to override these methods to return `NavigableMap`. Similarly, `https://developer.android.com/reference/kotlin/java/util/SortedMap#keys:kotlin.collections.MutableSet` can be overridden to return NavigableSet.

## Summary

| Public methods ||
|---|---|
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | ceilingEntry Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such key. |
| abstract K? | ceilingKey Returns the least key greater than or equal to the given key, or `null` if there is no such key. |
| abstract [NavigableSet](NavigableSet.md)\<K\> | descendingKeySet Returns a reverse order NavigableSet view of the keys contained in this map. |
| --- | --- |
| abstract [NavigableMap](NavigableMap.md)\<K, V\> | descendingMap Returns a reverse order view of the mappings contained in this map. |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | firstEntry Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty. |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | floorEntry Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key. |
| --- | --- |
| abstract K? | floorKey Returns the greatest key less than or equal to the given key, or `null` if there is no such key. |
| abstract [SortedMap](SortedMap.md)\<K, V\> | headMap Returns a view of the portion of this map whose keys are strictly less than `toKey`. |
| abstract [NavigableMap](NavigableMap.md)\<K, V\> | headMap Returns a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey`. |
| --- | --- |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | higherEntry Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key. |
| abstract K? | higherKey Returns the least key strictly greater than the given key, or `null` if there is no such key. |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | lastEntry Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty. |
| --- | --- |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | lowerEntry Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key. |
| abstract K? | lowerKey Returns the greatest key strictly less than the given key, or `null` if there is no such key. |
| abstract [NavigableSet](NavigableSet.md)\<K\> | navigableKeySet Returns a NavigableSet view of the keys contained in this map. |
| --- | --- |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | pollFirstEntry Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty (optional operation). |
| abstract [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>? | pollLastEntry Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty (optional operation). |
| open [NavigableMap](NavigableMap.md)\<K, V\> | reversed Returns a reverse-ordered [view](Collection.md) of this map. |
| --- | --- |
| abstract [NavigableMap](NavigableMap.md)\<K, V\> | subMap Returns a view of the portion of this map whose keys range from `fromKey` to `toKey`. |
| abstract [SortedMap](SortedMap.md)\<K, V\> | subMap Returns a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive. |
| abstract [SortedMap](SortedMap.md)\<K, V\> | tailMap Returns a view of the portion of this map whose keys are greater than or equal to `fromKey`. |
| --- | --- |
| abstract [NavigableMap](NavigableMap.md)\<K, V\> | tailMap Returns a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey`. |

| Inherited functions ||
|---|---|
| From class SortedMap |---|---| | `https://developer.android.com/reference/kotlin/java/util/Comparator<in K>?` | comparator Returns the comparator used to order the keys in this map, or `null` if this map uses the [natural ordering](../java.lang/Comparable.md) of its keys. <br /> | | `K` | firstKey Returns the first (lowest) key currently in this map. <br /> | | `K` | lastKey Returns the last (highest) key currently in this map. <br /> | | `V?` | putFirst Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | | `V?` | putLast Throws `UnsupportedOperationException`. The encounter order induced by this map's comparison method determines the position of mappings, so explicit positioning is not supported. <br /> | ||
| From class SequencedMap |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | firstEntry Returns the first key-value mapping in this map, or `null` if the map is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | lastEntry Returns the last key-value mapping in this map, or `null` if the map is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | pollFirstEntry Removes and returns the first key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!` | pollLastEntry Removes and returns the last key-value mapping in this map, or `null` if the map is empty (optional operation). <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedSet<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>!>!` | sequencedEntrySet Returns a `SequencedSet` view of this map's entrySet. <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedSet<K>!` | sequencedKeySet Returns a `SequencedSet` view of this map's keySet. <br /> | | `https://developer.android.com/reference/kotlin/java/util/SequencedCollection<V>!` | sequencedValues Returns a `SequencedCollection` view of this map's values collection. <br /> | ||

| Inherited properties ||
|---|---|
| From class SortedMap |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#entries:kotlin.collections.MutableSet` Returns a Set view of the mappings contained in this map. The set's iterator returns the entries in ascending key order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation, or through the `setValue` operation on a map entry returned by the iterator) the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#keys:kotlin.collections.MutableSet` Returns a Set view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | `https://developer.android.com/reference/kotlin/java/util/SortedMap#values:kotlin.collections.MutableCollection` Returns a Collection view of the values contained in this map. The collection's iterator returns the values in ascending order of the corresponding keys. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Collection.remove`, `removeAll`, `retainAll` and `clear` operations. It does not support the `add` or `addAll` operations. <br /> | ||

## Public methods

### ceilingEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun ceilingEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key greater than or equal to the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### ceilingKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun ceilingKey(key: K): K?
```

Returns the least key greater than or equal to the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the least key greater than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### descendingKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun descendingKeySet(): NavigableSet<K>
```

Returns a reverse order NavigableSet view of the keys contained in this map. The set's iterator returns the keys in descending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet<K>` | a reverse order navigable set view of the keys in this map |

### descendingMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun descendingMap(): NavigableMap<K, V>
```

Returns a reverse order view of the mappings contained in this map. The descending map is backed by this map, so changes to the map are reflected in the descending map, and vice-versa. If either map is modified while an iteration over a collection view of either map is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined.

The returned map has an ordering equivalent to reverseOrder`(comparator())`. The expression `m.descendingMap().descendingMap()` returns a view of `m` essentially equivalent to `m`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap#<K, V>` | a reverse order view of this map |

### firstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun firstEntry(): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key in this map, or `null` if the map is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key, or `null` if this map is empty |

### floorEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun floorEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key less than or equal to the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### floorKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun floorKey(key: K): K?
```

Returns the greatest key less than or equal to the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the greatest key less than or equal to `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun headMap(toKey: K): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys are strictly less than `toKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside its range.

Equivalent to `headMap(toKey, false)`.

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
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| --- | --- |

### headMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun headMap(
    toKey: K, 
    inclusive: Boolean
): NavigableMap<K, V>
```

Returns a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside its range.

| Parameters ||
|---|---|
| `toKey` | K: high endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap#<K, V>` | a view of the portion of this map whose keys are less than (or equal to, if `inclusive` is true) `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `toKey` is not compatible with this map's comparator (or, if the map has no comparator, if `toKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `toKey` is null and this map does not permit null keys |
| --- | --- |

### higherEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun higherEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the least key strictly greater than the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the least key greater than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### higherKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun higherKey(key: K): K?
```

Returns the least key strictly greater than the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the least key greater than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### lastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun lastEntry(): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key, or `null` if this map is empty |

### lowerEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun lowerEntry(key: K): MutableEntry<K, V>?
```

Returns a key-value mapping associated with the greatest key strictly less than the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | an entry with the greatest key less than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### lowerKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun lowerKey(key: K): K?
```

Returns the greatest key strictly less than the given key, or `null` if there is no such key.

| Parameters ||
|---|---|
| `key` | K: the key |

| Return ||
|---|---|
| `K?` | the greatest key less than `key`, or `null` if there is no such key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified key cannot be compared with the keys currently in the map |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys |

### navigableKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun navigableKeySet(): NavigableSet<K>
```

Returns a NavigableSet view of the keys contained in this map. The set's iterator returns the keys in ascending order. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own `remove` operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the `Iterator.remove`, `Set.remove`, `removeAll`, `retainAll`, and `clear` operations. It does not support the `add` or `addAll` operations.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableSet<K>` | a navigable set view of the keys in this map |

### pollFirstEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pollFirstEntry(): MutableEntry<K, V>?
```

Removes and returns a key-value mapping associated with the least key in this map, or `null` if the map is empty (optional operation).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed first entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `pollFirstEntry` operation is not supported by this map |

### pollLastEntry

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pollLastEntry(): MutableEntry<K, V>?
```

Removes and returns a key-value mapping associated with the greatest key in this map, or `null` if the map is empty (optional operation).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>?` | the removed last entry of this map, or `null` if this map is empty |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `pollLastEntry` operation is not supported by this map |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): NavigableMap<K, V>
```

Returns a reverse-ordered [view](Collection.md) of this map. The encounter order of mappings in the returned view is the inverse of the encounter order of mappings in this map. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the implementation permits modifications to this view, the modifications "write through" to the underlying map. Changes to the underlying map might or might not be visible in this reversed view, depending upon the implementation.

This method is equivalent to descendingMap.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap#<K, V>` | a reverse-ordered view of this map, as a `NavigableMap` |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun subMap(
    fromKey: K, 
    fromInclusive: Boolean, 
    toKey: K, 
    toInclusive: Boolean
): NavigableMap<K, V>
```

Returns a view of the portion of this map whose keys range from `fromKey` to `toKey`. If `fromKey` and `toKey` are equal, the returned map is empty unless `fromInclusive` and `toInclusive` are both true. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside of its range, or to construct a submap either of whose endpoints lie outside its range.

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `fromInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |
| `toKey` | K: high endpoint of the keys in the returned map |
| --- | --- |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the high endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap#<K, V>` | a view of the portion of this map whose keys range from `fromKey` to `toKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` and `toKey` cannot be compared to one another using this map's comparator (or, if the map has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if `fromKey` or `toKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if `fromKey` is greater than `toKey`; or if this map itself has a restricted range, and `fromKey` or `toKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| --- | --- |

### subMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun subMap(
    fromKey: K, 
    toKey: K
): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive. (If `fromKey` and `toKey` are equal, the returned map is empty.) The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside its range.

Equivalent to `subMap(fromKey, true, toKey, false)`.

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
| `java.lang.NullPointerException` | if `fromKey` or `toKey` is null and this map does not permit null keys |
| --- | --- |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun tailMap(fromKey: K): SortedMap<K, V>
```

Returns a view of the portion of this map whose keys are greater than or equal to `fromKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside its range.

Equivalent to `tailMap(fromKey, true)`.

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
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| --- | --- |

### tailMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun tailMap(
    fromKey: K, 
    inclusive: Boolean
): NavigableMap<K, V>
```

Returns a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey`. The returned map is backed by this map, so changes in the returned map are reflected in this map, and vice-versa. The returned map supports all optional map operations that this map supports.

The returned map will throw an `IllegalArgumentException` on an attempt to insert a key outside its range.

| Parameters ||
|---|---|
| `fromKey` | K: low endpoint of the keys in the returned map |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the low endpoint is to be included in the returned view |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/NavigableMap#<K, V>` | a view of the portion of this map whose keys are greater than (or equal to, if `inclusive` is true) `fromKey` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if `fromKey` is not compatible with this map's comparator (or, if the map has no comparator, if `fromKey` does not implement `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`). Implementations may, but are not required to, throw this exception if `fromKey` cannot be compared to keys currently in the map. |
| `java.lang.IllegalArgumentException` | if this map itself has a restricted range, and `fromKey` lies outside the bounds of the range |
| `java.lang.NullPointerException` | if `fromKey` is null and this map does not permit null keys |
| --- | --- |
