Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayMap

```
class ArrayMap<K : Any!, V : Any!> : MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.ArrayMap](https://developer.android.com/reference/kotlin/android/util/ArrayMap#) |

ArrayMap is a generic key-\>value mapping data structure that is designed to be more memory efficient than a traditional `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`. It keeps its mappings in an array data structure -- an integer array of hash codes for each item, and an Object array of the key/value pairs. This allows it to avoid having to create an extra object for every entry put in to the map, and it also tries to control the growth of the size of these arrays more aggressively (since growing them only requires copying the entries in the array, not rebuilding a hash map).

Note that this implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a traditional HashMap, since lookups require a binary search and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is not significant, less than 50%.

Because this container is intended to better balance memory use, unlike most other standard Java containers it will shrink its array as items are removed from it. Currently you have no control over this shrinking -- if you set a capacity and then remove an item, it may reduce the capacity to better match the current size. In the future an explicit call to set the capacity should turn off this aggressive shrinking behavior.

This structure is **NOT** thread-safe.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/ArrayMap#ArrayMap()()` Create a new empty ArrayMap. |
| `https://developer.android.com/reference/kotlin/android/util/ArrayMap#ArrayMap(android.util.ArrayMap)(map: https://developer.android.com/reference/kotlin/android/util/ArrayMap#<K, V>!)` Create a new ArrayMap with the mappings from the given ArrayMap. |
| `https://developer.android.com/reference/kotlin/android/util/ArrayMap#ArrayMap(kotlin.Int)(capacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a new ArrayMap with a given initial capacity. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#clear()()` Make the array map empty. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#containsAll(kotlin.collections.MutableCollection)(collection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<*>!)` Determine if the array map contains all of the keys in the given collection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#containsKey(android.util.ArrayMap.K)(key: K)` Check whether a key exists in the array. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#containsValue(android.util.ArrayMap.V)(value: V)` Check whether a value exists in the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#ensureCapacity(kotlin.Int)(minimumCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ensure the array map can hold at least minimumCapacity items. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#forEach(java.util.function.BiConsumer)(action: https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#<in K, in V>)` Performs the given action for all elements in the stored order. |
| V? | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#get(android.util.ArrayMap.K)(key: K)` Retrieve a value from the array. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#indexOfKey(kotlin.Any)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns the index of a key in the set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#indexOfValue(kotlin.Any)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns an index for which `https://developer.android.com/reference/kotlin/android/util/ArrayMap#valueAt(kotlin.Int)` would return the specified value, or a negative number if no keys map to the specified value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#isEmpty()()` Return true if the array map contains no items. |
| --- | --- |
| K | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#keyAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the key at the given index in the array. |
| V? | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#put(android.util.ArrayMap.K,%20android.util.ArrayMap.V)(key: K, value: V)` Add a new value to the array map. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#putAll(android.util.ArrayMap)(array: https://developer.android.com/reference/kotlin/android/util/ArrayMap#<out K, out V>!)` Perform a `https://developer.android.com/reference/kotlin/android/util/ArrayMap#put(android.util.ArrayMap.K,%20android.util.ArrayMap.V)` of all key/value pairs in array |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#putAll(kotlin.collections.Map)(from: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html<out K, V>)` Perform a `https://developer.android.com/reference/kotlin/android/util/ArrayMap#put(android.util.ArrayMap.K,%20android.util.ArrayMap.V)` of all key/value pairs in map |
| V? | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#remove(android.util.ArrayMap.K)(key: K)` Remove an existing key from the array map. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#removeAll(kotlin.collections.MutableCollection)(collection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<*>!)` Remove all keys in the array map that exist in the given collection. |
| --- | --- |
| V | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#removeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove the key/value mapping at the given index. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#replaceAll(java.util.function.BiFunction)(function: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in K, in V, out V>)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#retainAll(kotlin.collections.MutableCollection)(collection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<*>!)` Remove all keys in the array map that do **not** exist in the given collection. |
| --- | --- |
| V | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#setValueAt(kotlin.Int,%20android.util.ArrayMap.V)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: V)` Set the value at a given index in the array. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#toString()()` Returns a string representation of the object. |
| V | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#valueAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the value at the given index in the array. |
| --- | --- |

| Properties ||
|---|---|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K, V\>\> | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#entries:kotlin.collections.MutableSet` Return a `https://developer.android.com/reference/kotlin/java/util/Set.html#` for iterating over and interacting with all mappings in the array map. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#keys:kotlin.collections.MutableSet` Return a `https://developer.android.com/reference/kotlin/java/util/Set.html#` for iterating over and interacting with all keys in the array map. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#size:kotlin.Int` Return the number of items in this array map. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | `https://developer.android.com/reference/kotlin/android/util/ArrayMap#values:kotlin.collections.MutableCollection` Return a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` for iterating over and interacting with all values in the array map. |

## Public constructors

### ArrayMap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayMap()
```

Create a new empty ArrayMap. The default capacity of an array map is 0, and will grow once items are added to it.

### ArrayMap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayMap(map: ArrayMap<K, V>!)
```

Create a new ArrayMap with the mappings from the given ArrayMap.

### ArrayMap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayMap(capacity: Int)
```

Create a new ArrayMap with a given initial capacity.

## Public methods

### clear

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(): Unit
```

Make the array map empty. All storage is released.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this map |

### containsAll

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsAll(collection: MutableCollection<*>!): Boolean
```

Determine if the array map contains all of the keys in the given collection.

| Parameters ||
|---|---|
| `collection` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!: The collection whose contents are to be checked against. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if this array map contains a key for every entry in collection, else returns false. |

### containsKey

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsKey(key: K): Boolean
```

Check whether a key exists in the array.

| Parameters ||
|---|---|
| `key` | K: The key to search for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the key exists, else false. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsValue(value: V): Boolean
```

Check whether a value exists in the array. This requires a linear search through the entire array.

| Parameters ||
|---|---|
| `value` | V: The value to search for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the value exists, else false. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### ensureCapacity

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ensureCapacity(minimumCapacity: Int): Unit
```

Ensure the array map can hold at least minimumCapacity items.

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

This implementation returns false if the object is not a map, or if the maps have different sizes. Otherwise, for each key in this map, values of both maps are compared. If the values for any key are not equal, the method returns false, otherwise it returns true.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this map |
| `object` | This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified object is equal to this map |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun forEach(action: BiConsumer<in K, in V>): Unit
```

Performs the given action for all elements in the stored order. This implementation overrides the default implementation to avoid iterating using the `https://developer.android.com/reference/kotlin/android/util/ArrayMap#entries:kotlin.collections.MutableSet` and iterates in the key-value order consistent with `https://developer.android.com/reference/kotlin/android/util/ArrayMap#keyAt(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#valueAt(kotlin.Int)`.

| Parameters ||
|---|---|
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<in K, in V\>: The action to be performed for each element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(key: K): V?
```

Retrieve a value from the array.

| Parameters ||
|---|---|
| `key` | K: The key of the value to retrieve. |

| Return ||
|---|---|
| `V?` | Returns the value associated with the given key, or null if there is no such key. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this map |

### indexOfKey

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOfKey(key: Any!): Int
```

Returns the index of a key in the set.

| Parameters ||
|---|---|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The key to search for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the index of the key if it exists, else a negative integer. |

### indexOfValue

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOfValue(value: Any!): Int
```

Returns an index for which `https://developer.android.com/reference/kotlin/android/util/ArrayMap#valueAt(kotlin.Int)` would return the specified value, or a negative number if no keys map to the specified value. Beware that this is a linear search, unlike lookups by key, and that multiple keys can map to the same value and this will find only one of them.

### isEmpty

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEmpty(): Boolean
```

Return true if the array map contains no items.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this map contains no key-value mappings |

### keyAt

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun keyAt(index: Int): K
```

Return the key at the given index in the array.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired index, must be between 0 and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#size:kotlin.Int`-1. |

| Return ||
|---|---|
| `K` | Returns the key stored at the given index. |

### put

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun put(
    key: K, 
    value: V
): V?
```

Add a new value to the array map.

| Parameters ||
|---|---|
| `key` | K: The key under which to store the value. If this key already exists in the array, its value will be replaced. |
| `value` | V: The value to store for the given key. |

| Return ||
|---|---|
| `V?` | Returns the old value that was stored for the given key, or null if there was no such key. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null and this map does not permit null keys or values |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `put` operation is not supported by this map |

### putAll

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putAll(array: ArrayMap<out K, out V>!): Unit
```

Perform a `https://developer.android.com/reference/kotlin/android/util/ArrayMap#put(android.util.ArrayMap.K,%20android.util.ArrayMap.V)` of all key/value pairs in array

| Parameters ||
|---|---|
| `array` | [ArrayMap](https://developer.android.com/reference/kotlin/android/util/ArrayMap#)\<out K, out V\>!: The array whose contents are to be retrieved. |

### putAll

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putAll(from: Map<out K, V>): Unit
```

Perform a `https://developer.android.com/reference/kotlin/android/util/ArrayMap#put(android.util.ArrayMap.K,%20android.util.ArrayMap.V)` of all key/value pairs in map

| Parameters ||
|---|---|
| `m` | mappings to be stored in this map |
| `map` | The map whose contents are to be retrieved. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null, or if this map does not permit null keys or values, and the specified map contains null keys or values |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `putAll` operation is not supported by this map |

### remove

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(key: K): V?
```

Remove an existing key from the array map.

| Parameters ||
|---|---|
| `key` | K: The key of the mapping to remove. |

| Return ||
|---|---|
| `V?` | Returns the value that was stored under the key, or null if there was no such key. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this map |
| --- | --- |

### removeAll

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAll(collection: MutableCollection<*>!): Boolean
```

Remove all keys in the array map that exist in the given collection.

| Parameters ||
|---|---|
| `collection` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!: The collection whose contents are to be used to remove keys. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if any keys were removed from the array map, else false. |

### removeAt

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAt(index: Int): V
```

Remove the key/value mapping at the given index.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired index, must be between 0 and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#size:kotlin.Int`-1. |

| Return ||
|---|---|
| `V` | Returns the value that was stored at this index. |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. Exceptions thrown by the function are relayed to the caller. This implementation overrides the default implementation to avoid iterating using the `https://developer.android.com/reference/kotlin/android/util/ArrayMap#entries:kotlin.collections.MutableSet` and iterates in the key-value order consistent with `https://developer.android.com/reference/kotlin/android/util/ArrayMap#keyAt(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#valueAt(kotlin.Int)`.

| Parameters ||
|---|---|
| `function` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in K, in V, out V\>: The function to apply to each entry |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### retainAll

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun retainAll(collection: MutableCollection<*>!): Boolean
```

Remove all keys in the array map that do **not** exist in the given collection.

| Parameters ||
|---|---|
| `collection` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!: The collection whose contents are to be used to determine which keys to keep. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if any keys were removed from the array map, else false. |

### setValueAt

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setValueAt(
    index: Int, 
    value: V
): V
```

Set the value at a given index in the array.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired index, must be between 0 and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#size:kotlin.Int`-1. |
| `value` | V: The new value to store at this index. |

| Return ||
|---|---|
| `V` | Returns the previous value at the given index. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

This implementation composes a string by iterating over its mappings. If this map contains itself as a key or a value, the string "(this Map)" will appear in its place.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### valueAt

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun valueAt(index: Int): V
```

Return the value at the given index in the array.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired index, must be between 0 and `https://developer.android.com/reference/kotlin/android/util/ArrayMap#size:kotlin.Int`-1. |

| Return ||
|---|---|
| `V` | Returns the value stored at the given index. |

## Properties

### entries

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val entries: MutableSet<MutableEntry<K, V>>
```

Return a `https://developer.android.com/reference/kotlin/java/util/Set.html#` for iterating over and interacting with all mappings in the array map.

**Note:** this is a very inefficient way to access the array contents, it requires generating a number of temporary objects and allocates additional state information associated with the container that will remain for the life of the container.

**Note:**
the semantics of this Set are subtly different than that of a `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`: most important, the `https://developer.android.com/reference/kotlin/java/util/Map.Entry.html#` object returned by its iterator is a single object that exists for the entire iterator, so you can **not** hold on to it after calling `https://developer.android.com/reference/kotlin/java/util/Iterator.html#next()`.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html<K, V>>` | a set view of the mappings contained in this map |

### keys

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val keys: MutableSet<K>
```

Return a `https://developer.android.com/reference/kotlin/java/util/Set.html#` for iterating over and interacting with all keys in the array map.

**Note:** this is a fairly inefficient way to access the array contents, it requires generating a number of temporary objects and allocates additional state information associated with the container that will remain for the life of the container.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<K>` | a set view of the keys contained in this map |

### size

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val size: Int
```

Return the number of items in this array map.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of key-value mappings in this map |

### values

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val values: MutableCollection<V>
```

Return a `https://developer.android.com/reference/kotlin/java/util/Collection.html#` for iterating over and interacting with all values in the array map.

**Note:** this is a fairly inefficient way to access the array contents, it requires generating a number of temporary objects and allocates additional state information associated with the container that will remain for the life of the container.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<V>` | a collection view of the values contained in this map |
