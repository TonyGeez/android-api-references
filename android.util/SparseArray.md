Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SparseArray

```
open class SparseArray<E : Any!> : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.SparseArray](../android/util/SparseArray.md) |

`SparseArray` maps integers to Objects and, unlike a normal array of Objects, its indices can contain gaps. `SparseArray` is intended to be more memory-efficient than a [`HashMap`](../reference/java/util/HashMap.md), because it avoids auto-boxing keys and its data structure doesn't rely on an extra entry object for each mapping.

Note that this container keeps its mappings in an array data structure, using a binary search to find keys. The implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a `HashMap` because lookups require a binary search, and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is less than 50%.

To help with performance, the container includes an optimization when removing keys: instead of compacting its array immediately, it leaves the removed entry marked as deleted. The entry can then be re-used for the same key or compacted later in a single garbage collection of all removed entries. This garbage collection must be performed whenever the array needs to be grown, or when the map size or entry values are retrieved.

It is possible to iterate over the items in this container using `https://developer.android.com/reference/kotlin/android/util/SparseArray#keyAt(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/util/SparseArray#valueAt(kotlin.Int)`. Iterating over the keys using `keyAt(int)` with ascending values of the index returns the keys in ascending order. In the case of `valueAt(int)`, the values corresponding to the keys are returned in ascending order.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray#SparseArray()()` Creates a new SparseArray containing no mappings. |
| `https://developer.android.com/reference/kotlin/android/util/SparseArray#SparseArray(kotlin.Int)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new SparseArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#append(kotlin.Int,%20android.util.SparseArray.E)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: E)` Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#clear()()` Removes all key-value mappings from this SparseArray. |
| open [SparseArray](../android/util/SparseArray.md)\<E\> | `https://developer.android.com/reference/kotlin/android/util/SparseArray#clone()()` Creates and returns a copy of this object. |
| --- | --- |
| open E? | `https://developer.android.com/reference/kotlin/android/util/SparseArray#compute(kotlin.Int,%20android.util.function.IntObjFunction)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, function: https://developer.android.com/reference/kotlin/android/util/function/IntObjFunction<in E, out E>)` Attempts to compute a new mapped value for the specified key based on its current mapping (or null if there is no current mapping). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#contains(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the key exists in the array. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#contentEquals(android.util.SparseArray)(other: https://developer.android.com/reference/kotlin/android/util/SparseArray#<*>?)` Compares the contents of this `https://developer.android.com/reference/kotlin/android/util/SparseArray#` to the specified `https://developer.android.com/reference/kotlin/android/util/SparseArray#`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#contentHashCode()()` Returns a hash code value for the contents of this `https://developer.android.com/reference/kotlin/android/util/SparseArray#`, combining the `https://developer.android.com/reference/kotlin/java/util/Objects.html#hashCode(kotlin.Any)` result of all its keys and values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#delete(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the mapping from the specified key, if there was any. |
| open E | `https://developer.android.com/reference/kotlin/android/util/SparseArray#get(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the Object mapped from the specified key, or `null` if no such mapping has been made. |
| --- | --- |
| open E | `https://developer.android.com/reference/kotlin/android/util/SparseArray#get(kotlin.Int,%20android.util.SparseArray.E)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, valueIfKeyNotFound: E)` Gets the Object mapped from the specified key, or the specified Object if no such mapping has been made. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#indexOfKey(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index for which `https://developer.android.com/reference/kotlin/android/util/SparseArray#keyAt(kotlin.Int)` would return the specified key, or a negative number if the specified key is not mapped. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#indexOfValue(android.util.SparseArray.E)(value: E)` Returns an index for which `https://developer.android.com/reference/kotlin/android/util/SparseArray#valueAt(kotlin.Int)` would return the specified value, or a negative number if no keys map to the specified value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#keyAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseArray stores. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#put(kotlin.Int,%20android.util.SparseArray.E)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: E)` Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#remove(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Alias for `https://developer.android.com/reference/kotlin/android/util/SparseArray#delete(kotlin.Int)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#removeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the mapping at the specified index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#removeAtRange(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove a range of mappings as a batch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#set(kotlin.Int,%20android.util.SparseArray.E)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: E)` Alias for `https://developer.android.com/reference/kotlin/android/util/SparseArray#put(kotlin.Int,%20android.util.SparseArray.E)` to support Kotlin \[index\]= operator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#setValueAt(kotlin.Int,%20android.util.SparseArray.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: E)` Given an index in the range `0...size()-1`, sets a new value for the `index`th key-value mapping that this SparseArray stores. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#size()()` Returns the number of key-value mappings that this SparseArray currently stores. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseArray#toString()()` Returns a string representation of the object. |
| --- | --- |
| open E | `https://developer.android.com/reference/kotlin/android/util/SparseArray#valueAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseArray stores. |

## Public constructors

### SparseArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseArray()
```

Creates a new SparseArray containing no mappings.

### SparseArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseArray(initialCapacity: Int)
```

Creates a new SparseArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. If you supply an initial capacity of 0, the sparse array will be initialized with a light-weight representation not requiring any additional array allocations.

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(
    key: Int, 
    value: E
): Unit
```

Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array.

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all key-value mappings from this SparseArray.

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): SparseArray<E>
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseArray#<E>` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Int, 
    function: IntObjFunction<in E, out E>
): E?
```

Attempts to compute a new mapped value for the specified key based on its current mapping (or null if there is no current mapping). If the function returns null, the mapping is removed (or remains absent if initially absent).

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key to compute the value for. |
| `function` | [IntObjFunction](../android/util/function/IntObjFunction.md)\<in E, out E\>: The function to compute the new value. This value cannot be `null`. |

| Return ||
|---|---|
| `E?` | The new mapped value, or null if none. |

### contains

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(key: Int): Boolean
```

Returns true if the key exists in the array. This is equivalent to `https://developer.android.com/reference/kotlin/android/util/SparseArray#indexOfKey(kotlin.Int)` \>= 0.

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Potential key in the mapping |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the key is defined in the mapping |

### contentEquals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contentEquals(other: SparseArray<*>?): Boolean
```

Compares the contents of this `https://developer.android.com/reference/kotlin/android/util/SparseArray#` to the specified `https://developer.android.com/reference/kotlin/android/util/SparseArray#`. For backwards compatibility reasons, `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` cannot be implemented, so this serves as a manually invoked alternative.

| Parameters ||
|---|---|
| `other` | [SparseArray](../android/util/SparseArray.md)\<\*\>?: This value may be `null`. |

### contentHashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contentHashCode(): Int
```

Returns a hash code value for the contents of this `https://developer.android.com/reference/kotlin/android/util/SparseArray#`, combining the `https://developer.android.com/reference/kotlin/java/util/Objects.html#hashCode(kotlin.Any)` result of all its keys and values. For backwards compatibility, `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()` cannot be implemented, so this serves as a manually invoked alternative.

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(key: Int): Unit
```

Removes the mapping from the specified key, if there was any.

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: Int): E
```

Gets the Object mapped from the specified key, or `null` if no such mapping has been made.

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    key: Int, 
    valueIfKeyNotFound: E
): E
```

Gets the Object mapped from the specified key, or the specified Object if no such mapping has been made.

### indexOfKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfKey(key: Int): Int
```

Returns the index for which `https://developer.android.com/reference/kotlin/android/util/SparseArray#keyAt(kotlin.Int)` would return the specified key, or a negative number if the specified key is not mapped.

### indexOfValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfValue(value: E): Int
```

Returns an index for which `https://developer.android.com/reference/kotlin/android/util/SparseArray#valueAt(kotlin.Int)` would return the specified value, or a negative number if no keys map to the specified value.

Beware that this is a linear search, unlike lookups by key, and that multiple keys can map to the same value and this will find only one of them.

Note also that unlike most collections' `indexOf` methods, this method compares values using `==` rather than `equals`.

### keyAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keyAt(index: Int): Int
```

Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseArray stores.

The keys corresponding to indices in ascending order are guaranteed to be in ascending order, e.g., `keyAt(0)` will return the smallest key and `keyAt(size()-1)` will return the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Int, 
    value: E
): Unit
```

Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one.

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(key: Int): Unit
```

Alias for `https://developer.android.com/reference/kotlin/android/util/SparseArray#delete(kotlin.Int)`.

### removeAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAt(index: Int): Unit
```

Removes the mapping at the specified index.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### removeAtRange

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAtRange(
    index: Int, 
    size: Int
): Unit
```

Remove a range of mappings as a batch.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index to begin at |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of mappings to remove For indices outside of the range `0...size()-1`, the behavior is undefined. |

### set

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    key: Int, 
    value: E
): Unit
```

Alias for `https://developer.android.com/reference/kotlin/android/util/SparseArray#put(kotlin.Int,%20android.util.SparseArray.E)` to support Kotlin \[index\]= operator.
**See Also**

- `https://developer.android.com/reference/kotlin/android/util/SparseArray#put(kotlin.Int,%20android.util.SparseArray.E)`

### setValueAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setValueAt(
    index: Int, 
    value: E
): Unit
```

Given an index in the range `0...size()-1`, sets a new value for the `index`th key-value mapping that this SparseArray stores.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Returns the number of key-value mappings that this SparseArray currently stores.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

This implementation composes a string by iterating over its mappings. If this map contains itself as a value, the string "(this Map)" will appear in its place.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### valueAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun valueAt(index: Int): E
```

Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseArray stores.

The values corresponding to indices in ascending order are guaranteed to be associated with keys in ascending order, e.g., `valueAt(0)` will return the value associated with the smallest key and `valueAt(size()-1)` will return the value associated with the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.
