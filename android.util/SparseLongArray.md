Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SparseLongArray

```
open class SparseLongArray : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.SparseLongArray](SparseLongArray.md) |

SparseLongArrays map integers to longs. Unlike a normal array of longs, there can be gaps in the indices. It is intended to be more memory efficient than using a HashMap to map Integers to Longs, both because it avoids auto-boxing keys and values and its data structure doesn't rely on an extra entry object for each mapping.

Note that this container keeps its mappings in an array data structure, using a binary search to find keys. The implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a traditional HashMap, since lookups require a binary search and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is not significant, less than 50%.

It is possible to iterate over the items in this container using keyAt and valueAt. Iterating over the keys using `keyAt(int)` with ascending values of the index will return the keys in ascending order, or the values corresponding to the keys in ascending order in the case of `valueAt(int)`.

## Summary

| Public constructors ||
|---|---|
| SparseLongArray Creates a new SparseLongArray containing no mappings. |
| SparseLongArray Creates a new SparseLongArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | append Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Removes all key-value mappings from this SparseLongArray. |
| open [SparseLongArray](SparseLongArray.md) | clone Creates and returns a copy of this object. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | compute Attempts to compute a new mapped value for the specified key based on its current mapped value (or 0 if there is no current mapping). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | delete Removes the mapping from the specified key, if there was any. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | get Gets the long mapped from the specified key, or `0` if no such mapping has been made. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | get Gets the long mapped from the specified key, or the specified value if no such mapping has been made. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | indexOfKey Returns the index for which keyAt would return the specified key, or a negative number if the specified key is not mapped. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | indexOfValue Returns an index for which valueAt would return the specified key, or a negative number if no keys map to the specified value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | keyAt Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseLongArray stores. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | put Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeAt Removes the mapping at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size Returns the number of key-value mappings that this SparseLongArray currently stores. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | valueAt Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseLongArray stores. |
| --- | --- |

## Public constructors

### SparseLongArray

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseLongArray()
```

Creates a new SparseLongArray containing no mappings.

### SparseLongArray

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseLongArray(initialCapacity: Int)
```

Creates a new SparseLongArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. If you supply an initial capacity of 0, the sparse array will be initialized with a light-weight representation not requiring any additional array allocations.

## Public methods

### append

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(
    key: Int, 
    value: Long
): Unit
```

Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array.

### clear

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all key-value mappings from this SparseLongArray.

### clone

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): SparseLongArray
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
| SparseLongArray | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Int, 
    function: LongBinaryOperator
): Long
```

Attempts to compute a new mapped value for the specified key based on its current mapped value (or 0 if there is no current mapping).

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key to compute the value for. |
| `function` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md): The function to compute the new value. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The new mapped value. |

### delete

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(key: Int): Unit
```

Removes the mapping from the specified key, if there was any.

### get

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: Int): Long
```

Gets the long mapped from the specified key, or `0` if no such mapping has been made.

### get

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    key: Int, 
    valueIfKeyNotFound: Long
): Long
```

Gets the long mapped from the specified key, or the specified value if no such mapping has been made.

### indexOfKey

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfKey(key: Int): Int
```

Returns the index for which keyAt would return the specified key, or a negative number if the specified key is not mapped.

### indexOfValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfValue(value: Long): Int
```

Returns an index for which valueAt would return the specified key, or a negative number if no keys map to the specified value. Beware that this is a linear search, unlike lookups by key, and that multiple keys can map to the same value and this will find only one of them.

### keyAt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keyAt(index: Int): Int
```

Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseLongArray stores.

The keys corresponding to indices in ascending order are guaranteed to be in ascending order, e.g., `keyAt(0)` will return the smallest key and `keyAt(size()-1)` will return the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### put

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Int, 
    value: Long
): Unit
```

Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one.

### removeAt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAt(index: Int): Unit
```

Removes the mapping at the given index.

### size

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Returns the number of key-value mappings that this SparseLongArray currently stores.

### toString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

This implementation composes a string by iterating over its mappings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### valueAt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun valueAt(index: Int): Long
```

Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseLongArray stores.

The values corresponding to indices in ascending order are guaranteed to be associated with keys in ascending order, e.g., `valueAt(0)` will return the value associated with the smallest key and `valueAt(size()-1)` will return the value associated with the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.
