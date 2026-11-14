Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SparseIntArray

```
open class SparseIntArray : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.SparseIntArray](https://developer.android.com/reference/kotlin/android/util/SparseIntArray#) |

SparseIntArrays map integers to integers. Unlike a normal array of integers, there can be gaps in the indices. It is intended to be more memory efficient than using a HashMap to map Integers to Integers, both because it avoids auto-boxing keys and values and its data structure doesn't rely on an extra entry object for each mapping.

Note that this container keeps its mappings in an array data structure, using a binary search to find keys. The implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a traditional HashMap, since lookups require a binary search and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is not significant, less than 50%.

It is possible to iterate over the items in this container using `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#keyAt(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#valueAt(kotlin.Int)`. Iterating over the keys using `keyAt(int)` with ascending values of the index will return the keys in ascending order, or the values corresponding to the keys in ascending order in the case of `valueAt(int)`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#SparseIntArray()()` Creates a new SparseIntArray containing no mappings. |
| `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#SparseIntArray(kotlin.Int)(initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new SparseIntArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#append(kotlin.Int,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#clear()()` Removes all key-value mappings from this SparseIntArray. |
| open [SparseIntArray](https://developer.android.com/reference/kotlin/android/util/SparseIntArray#) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#clone()()` Creates and returns a copy of this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#compute(kotlin.Int,%20java.util.function.IntBinaryOperator)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, function: https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)` Attempts to compute a new mapped value for the specified key based on its current mapped value (or 0 if there is no current mapping). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#delete(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the mapping from the specified key, if there was any. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#get(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the int mapped from the specified key, or `0` if no such mapping has been made. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#get(kotlin.Int,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, valueIfKeyNotFound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the int mapped from the specified key, or the specified value if no such mapping has been made. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#indexOfKey(kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index for which `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#keyAt(kotlin.Int)` would return the specified key, or a negative number if the specified key is not mapped. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#indexOfValue(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an index for which `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#valueAt(kotlin.Int)` would return the specified key, or a negative number if no keys map to the specified value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#keyAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseIntArray stores. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#put(kotlin.Int,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#removeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the mapping at the given index. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#setValueAt(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Directly set the value at a particular index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#size()()` Returns the number of key-value mappings that this SparseIntArray currently stores. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#valueAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseIntArray stores. |

## Public constructors

### SparseIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseIntArray()
```

Creates a new SparseIntArray containing no mappings.

### SparseIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseIntArray(initialCapacity: Int)
```

Creates a new SparseIntArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. If you supply an initial capacity of 0, the sparse array will be initialized with a light-weight representation not requiring any additional array allocations.

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(
    key: Int, 
    value: Int
): Unit
```

Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array.

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all key-value mappings from this SparseIntArray.

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): SparseIntArray
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
| `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Int, 
    function: IntBinaryOperator
): Int
```

Attempts to compute a new mapped value for the specified key based on its current mapped value (or 0 if there is no current mapping).

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key to compute the value for. |
| `function` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#): The function to compute the new value. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The new mapped value. |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(key: Int): Unit
```

Removes the mapping from the specified key, if there was any.

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: Int): Int
```

Gets the int mapped from the specified key, or `0` if no such mapping has been made.

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    key: Int, 
    valueIfKeyNotFound: Int
): Int
```

Gets the int mapped from the specified key, or the specified value if no such mapping has been made.

### indexOfKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfKey(key: Int): Int
```

Returns the index for which `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#keyAt(kotlin.Int)` would return the specified key, or a negative number if the specified key is not mapped.

### indexOfValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfValue(value: Int): Int
```

Returns an index for which `https://developer.android.com/reference/kotlin/android/util/SparseIntArray#valueAt(kotlin.Int)` would return the specified key, or a negative number if no keys map to the specified value. Beware that this is a linear search, unlike lookups by key, and that multiple keys can map to the same value and this will find only one of them.

### keyAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keyAt(index: Int): Int
```

Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseIntArray stores.

The keys corresponding to indices in ascending order are guaranteed to be in ascending order, e.g., `keyAt(0)` will return the smallest key and `keyAt(size()-1)` will return the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Int, 
    value: Int
): Unit
```

Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one.

### removeAt

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAt(index: Int): Unit
```

Removes the mapping at the given index.

### setValueAt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setValueAt(
    index: Int, 
    value: Int
): Unit
```

Directly set the value at a particular index.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Returns the number of key-value mappings that this SparseIntArray currently stores.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

This implementation composes a string by iterating over its mappings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### valueAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun valueAt(index: Int): Int
```

Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseIntArray stores.

The values corresponding to indices in ascending order are guaranteed to be associated with keys in ascending order, e.g., `valueAt(0)` will return the value associated with the smallest key and `valueAt(size()-1)` will return the value associated with the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.
