Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SparseBooleanArray

```
open class SparseBooleanArray : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.SparseBooleanArray](SparseBooleanArray.md) |

SparseBooleanArrays map integers to booleans. Unlike a normal array of booleans there can be gaps in the indices. It is intended to be more memory efficient than using a HashMap to map Integers to Booleans, both because it avoids auto-boxing keys and values and its data structure doesn't rely on an extra entry object for each mapping.

Note that this container keeps its mappings in an array data structure, using a binary search to find keys. The implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a traditional HashMap, since lookups require a binary search and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is not significant, less than 50%.

It is possible to iterate over the items in this container using keyAt and valueAt. Iterating over the keys using `keyAt(int)` with ascending values of the index will return the keys in ascending order, or the values corresponding to the keys in ascending order in the case of `valueAt(int)`.

## Summary

| Public constructors ||
|---|---|
| SparseBooleanArray Creates a new SparseBooleanArray containing no mappings. |
| SparseBooleanArray Creates a new SparseBooleanArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | append Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Removes all key-value mappings from this SparseBooleanArray. |
| open [SparseBooleanArray](SparseBooleanArray.md) | clone Creates and returns a copy of this object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | compute Attempts to compute a new mapped value for the specified key based on its current mapped value (or false if there is no current mapping). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | delete Removes the mapping from the specified key, if there was any. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | get Gets the boolean mapped from the specified key, or `false` if no such mapping has been made. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | get Gets the boolean mapped from the specified key, or the specified value if no such mapping has been made. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | indexOfKey Returns the index for which keyAt would return the specified key, or a negative number if the specified key is not mapped. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | indexOfValue Returns an index for which valueAt would return the specified key, or a negative number if no keys map to the specified value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | keyAt Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseBooleanArray stores. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | put Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeAt Removes the mapping at the specified index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setValueAt Directly set the value at a particular index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size Returns the number of key-value mappings that this SparseBooleanArray currently stores. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | valueAt Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseBooleanArray stores. |
| --- | --- |

## Public constructors

### SparseBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseBooleanArray()
```

Creates a new SparseBooleanArray containing no mappings.

### SparseBooleanArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SparseBooleanArray(initialCapacity: Int)
```

Creates a new SparseBooleanArray containing no mappings that will not require any additional memory allocation to store the specified number of mappings. If you supply an initial capacity of 0, the sparse array will be initialized with a light-weight representation not requiring any additional array allocations.

## Public methods

### append

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun append(
    key: Int, 
    value: Boolean
): Unit
```

Puts a key/value pair into the array, optimizing for the case where the key is greater than all existing keys in the array.

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all key-value mappings from this SparseBooleanArray.

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): SparseBooleanArray
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
| SparseBooleanArray | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compute

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compute(
    key: Int, 
    function: IntBinaryOperator
): Boolean
```

Attempts to compute a new mapped value for the specified key based on its current mapped value (or false if there is no current mapping). The boolean values passed to and returned from the function are converted to integers (0 for false and true otherwise) to avoid type boxing.

| Parameters ||
|---|---|
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key to compute the value for. |
| `function` | [IntBinaryOperator](../java.util.function/IntBinaryOperator.md): The function to compute the new value. For the second argument that represents the current mapped value, 0 is used for false and 1 for true. The returned value will be converted to a boolean similarly, 0 for false and true otherwise. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The new mapped value. |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(key: Int): Unit
```

Removes the mapping from the specified key, if there was any.

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `that` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(key: Int): Boolean
```

Gets the boolean mapped from the specified key, or `false` if no such mapping has been made.

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(
    key: Int, 
    valueIfKeyNotFound: Boolean
): Boolean
```

Gets the boolean mapped from the specified key, or the specified value if no such mapping has been made.

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### indexOfKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfKey(key: Int): Int
```

Returns the index for which keyAt would return the specified key, or a negative number if the specified key is not mapped.

### indexOfValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOfValue(value: Boolean): Int
```

Returns an index for which valueAt would return the specified key, or a negative number if no keys map to the specified value. Beware that this is a linear search, unlike lookups by key, and that multiple keys can map to the same value and this will find only one of them.

### keyAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keyAt(index: Int): Int
```

Given an index in the range `0...size()-1`, returns the key from the `index`th key-value mapping that this SparseBooleanArray stores.

The keys corresponding to indices in ascending order are guaranteed to be in ascending order, e.g., `keyAt(0)` will return the smallest key and `keyAt(size()-1)` will return the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(
    key: Int, 
    value: Boolean
): Unit
```

Adds a mapping from the specified key to the specified value, replacing the previous mapping from the specified key if there was one.

### removeAt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAt(index: Int): Unit
```

Removes the mapping at the specified index.

For indices outside of the range `0...size()-1`, the behavior is undefined.

### setValueAt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setValueAt(
    index: Int, 
    value: Boolean
): Unit
```

Directly set the value at a particular index.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Returns the number of key-value mappings that this SparseBooleanArray currently stores.

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
open fun valueAt(index: Int): Boolean
```

Given an index in the range `0...size()-1`, returns the value from the `index`th key-value mapping that this SparseBooleanArray stores.

The values corresponding to indices in ascending order are guaranteed to be associated with keys in ascending order, e.g., `valueAt(0)` will return the value associated with the smallest key and `valueAt(size()-1)` will return the value associated with the largest key.

For indices outside of the range `0...size()-1`, the behavior is undefined for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int` and earlier, and an `https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException.html#` is thrown for apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` and later.
