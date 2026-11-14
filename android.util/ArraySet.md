# ArraySet

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArraySet

Kotlin| [Java](../android/util/ArraySet.md) 
| --- | --- |

```
class ArraySet<E : Any!> : MutableCollection<E>, MutableSet<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.ArraySet](../android/util/ArraySet.md) |

ArraySet is a generic set data structure that is designed to be more memory efficient than a traditional [java.util.HashSet](../java/util/HashSet.md). The design is very similar to [ArrayMap](../android/util/ArrayMap.md), with all of the caveats described there. This implementation is separate from ArrayMap, however, so the Object array contains only one item for each entry in the set (instead of a pair for a mapping).

Note that this implementation is not intended to be appropriate for data structures that may contain large numbers of items. It is generally slower than a traditional HashSet, since lookups require a binary search and adds and removes require inserting and deleting entries in the array. For containers holding up to hundreds of items, the performance difference is not significant, less than 50%.

Because this container is intended to better balance memory use, unlike most other standard Java containers it will shrink its array as items are removed from it. Currently you have no control over this shrinking -- if you set a capacity and then remove an item, it may reduce the capacity to better match the current size. In the future an explicit call to set the capacity should turn off this aggressive shrinking behavior.

This structure is**NOT**thread-safe.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArraySet](../android/util/ArraySet.md))`()` Create a new empty ArraySet. |
| [ArraySet](../android/util/ArraySet.md))`(`set:` ` [ArraySet](../android/util/ArraySet.md)<E>!`)` Create a new ArraySet with the mappings from the given ArraySet. |
| [ArraySet](../android/util/ArraySet.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<E>?`)` Create a new ArraySet with items from the given array |
| [ArraySet](../android/util/ArraySet.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new ArraySet with a given initial capacity. |
| [ArraySet](../android/util/ArraySet.md))`(`set:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Create a new ArraySet with items from the given collection. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../android/util/ArraySet.md))`(`element:` `E`)` Adds the specified object to this set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAll](../android/util/ArraySet.md))`(`array:` ` [ArraySet](../android/util/ArraySet.md)<out` `E>!`)` Perform a [add(java.lang.Object)](../android/util/ArraySet.md))of all values in array |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../android/util/ArraySet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Perform an [add(java.lang.Object)](../android/util/ArraySet.md))of all values in collection |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/util/ArraySet.md))`()` Make the array map empty. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/util/ArraySet.md))`(`element:` `E`)` Check whether a value exists in the set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../android/util/ArraySet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Determine if the array set contains all of the values in the given collection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ensureCapacity](../android/util/ArraySet.md))`(`minimumCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Ensure the array map can hold at least minimumCapacity items. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/util/ArraySet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../android/util/ArraySet.md))`(`action:` ` [Consumer](../java/util/function/Consumer.md)<in` `E>`)` Performs the given action for all elements in the stored order. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/util/ArraySet.md))`()` Returns a hash code value for the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../android/util/ArraySet.md))`(`key:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the index of a value in the set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/util/ArraySet.md))`()` Return true if the array map contains no items. |
| --- | --- |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](../android/util/ArraySet.md))`()` Return an [java.util.Iterator](../java/util/Iterator.md) over all values in the set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../android/util/ArraySet.md))`(`element:` `E`)` Removes the specified object from this set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../android/util/ArraySet.md))`(`array:` ` [ArraySet](../android/util/ArraySet.md)<out` `E>!`)` Perform a [remove(java.lang.Object)](../android/util/ArraySet.md))of all values in array |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../android/util/ArraySet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Remove all values in the array set that exist in the given collection. |
| E | [removeAt](../android/util/ArraySet.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove the key/value mapping at the given index. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](../android/util/ArraySet.md))`(`filter:` ` [Predicate](../java/util/function/Predicate.md)<in` `E>`)` Removes all values that satisfy the predicate. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../android/util/ArraySet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Remove all values in the array set that do**not**exist in the given collection. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [toArray](../android/util/ArraySet.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [toArray](../android/util/ArraySet.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>!`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/util/ArraySet.md))`()` Returns a string representation of the object. |
| E | [valueAt](../android/util/ArraySet.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the value at the given index in the array. |

| Properties ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../android/util/ArraySet.md) Return the number of items in this array map. |

## Public constructors

### ArraySet

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArraySet()
```

Create a new empty ArraySet. The default capacity of an array map is 0, and will grow once items are added to it. 

### ArraySet

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArraySet(set: ArraySet<E>!)
```

Create a new ArraySet with the mappings from the given ArraySet. 

### ArraySet

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArraySet(array: Array<E>?)
```

Create a new ArraySet with items from the given array

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<E\>?:This value may be`null`. |

### ArraySet

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArraySet(capacity: Int)
```

Create a new ArraySet with a given initial capacity. 

### ArraySet

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArraySet(set: MutableCollection<out E>!)
```

Create a new ArraySet with items from the given collection.

## Public methods

### add

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(element: E): Boolean
```

Adds the specified object to this set. The set is not modified if it already contains the object.

| Parameters ||
|---------|---------------------------------|
| `e` | element to be added to this set |
| `value` | the object to add. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set is modified,`false`otherwise. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this set |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### addAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAll(array: ArraySet<out E>!): Unit
```

Perform a [add(java.lang.Object)](../android/util/ArraySet.md))of all values in array

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [ArraySet](../android/util/ArraySet.md)\<outE\>!:The array whose contents are to be retrieved. |

### addAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAll(elements: Collection<E>): Boolean
```

Perform an [add(java.lang.Object)](../android/util/ArraySet.md))of all values in collection

| Parameters ||
|--------------|--------------------------------------------------------|
| `c` | collection containing elements to be added to this set |
| `collection` | The collection whose contents are to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this set |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this set does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this set |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

### clear

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Make the array map empty. All storage is released.

| Exceptions ||
|-------------------------------------------|--------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`method is not supported by this set |

### contains

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(element: E): Boolean
```

Check whether a value exists in the set.

| Parameters ||
|-------|----------------------------------------------------|
| `o` | element whose presence in this set is to be tested |
| `key` | The value to search for. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if the value exists, else false. |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](../android/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](../android/util/Collection.md)) |

### containsAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun containsAll(elements: Collection<E>): Boolean
```

Determine if the array set contains all of the values in the given collection.

| Parameters ||
|--------------|----------------------------------------------------------|
| `c` | collection to be checked for containment in this set |
| `collection` | The collection whose contents are to be checked against. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if this array set contains a value for every entry in collection, else returns false. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this set ([optional](../android/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this set does not permit null elements ([optional](../android/util/Collection.md)), or if the specified collection is null |

### ensureCapacity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ensureCapacity(minimumCapacity: Int): Unit
```

Ensure the array map can hold at least minimumCapacity items. 

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

This implementation returns false if the object is not a set, or if the sets have different sizes. Otherwise, for each value in this set, it checks to make sure the value also exists in the other set. If any value doesn't exist, the method returns false; otherwise, it returns true.

| Parameters ||
|----------|--------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this set |
| `object` | This value may be`null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this set |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun forEach(action: Consumer<in E>): Unit
```

Performs the given action for all elements in the stored order. This implementation overrides the default implementation to avoid using the #iterator().

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java/util/function/Consumer.md)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this set |

### indexOf

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun indexOf(key: Any!): Int
```

Returns the index of a value in the set.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value to search for. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the index of the value if it exists, else a negative integer. |

### isEmpty

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmpty(): Boolean
```

Return true if the array map contains no items.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains no elements |

### iterator

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun iterator(): MutableIterator<E>
```

Return an [java.util.Iterator](../java/util/Iterator.md) over all values in the set.

**Note:**this is a fairly inefficient way to access the array contents, it requires generating a number of temporary objects and allocates additional state information associated with the container that will remain for the life of the container.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this set |

### remove

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun remove(element: E): Boolean
```

Removes the specified object from this set.

| Parameters ||
|----------|------------------------------------------------|
| `o` | object to be removed from this set, if present |
| `object` | the object to remove. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set was modified,`false`otherwise. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](../android/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](../android/util/Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this set |
| --- | --- |

### removeAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAll(array: ArraySet<out E>!): Boolean
```

Perform a [remove(java.lang.Object)](../android/util/ArraySet.md))of all values in array

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [ArraySet](../android/util/ArraySet.md)\<outE\>!:The array whose contents are to be removed. |

### removeAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAll(elements: Collection<E>): Boolean
```

Remove all values in the array set that exist in the given collection.

| Parameters ||
|--------------|----------------------------------------------------------------|
| `c` | collection containing elements to be removed from this set |
| `collection` | The collection whose contents are to be used to remove values. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if any values were removed from the array set, else false. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](../android/util/Collection.md)) |
| `java.lang.NullPointerException` | if this set contains a null element and the specified collection does not permit null elements ([optional](../android/util/Collection.md)), or if the specified collection is null |
| --- | --- |

### removeAt

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAt(index: Int): E
```

Remove the key/value mapping at the given index.

For indices outside of the range`0...size()-1`, the behavior is undefined for apps targeting [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and earlier, and an [ArrayIndexOutOfBoundsException](../java/lang/ArrayIndexOutOfBoundsException.md) is thrown for apps targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) and later.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired index, must be between 0 and [size()](../android/util/ArraySet.md)-1. |

| Return ||
|---|--------------------------------------------------|
| E | Returns the value that was stored at this index. |

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeIf(filter: Predicate<in E>): Boolean
```

Removes all values that satisfy the predicate. This implementation avoids using the #iterator().

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java/util/function/Predicate.md)\<inE\>:A predicate which returns true for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

### retainAll

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun retainAll(elements: Collection<E>): Boolean
```

Remove all values in the array set that do**not**exist in the given collection.

| Parameters ||
|--------------|---------------------------------------------------------------------------------|
| `c` | collection containing elements to be retained in this set |
| `collection` | The collection whose contents are to be used to determine which values to keep. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if any values were removed from the array set, else false. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](../android/util/Collection.md)) |
| `java.lang.NullPointerException` | if this set contains a null element and the specified collection does not permit null elements ([optional](../android/util/Collection.md)), or if the specified collection is null |
| --- | --- |

### toArray

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toArray(): Array<Any!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array containing all the elements in this set |

### toArray

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Any!> toArray(array: Array<T>!): Array<T>!
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | the array into which the elements of this set are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | an array containing all the elements in this set |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this set |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

This implementation composes a string by iterating over its values. If this set contains itself as a value, the string "(this Set)" will appear in its place.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### valueAt

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun valueAt(index: Int): E
```

Return the value at the given index in the array.

For indices outside of the range`0...size()-1`, the behavior is undefined for apps targeting [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and earlier, and an [ArrayIndexOutOfBoundsException](../java/lang/ArrayIndexOutOfBoundsException.md) is thrown for apps targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) and later.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired index, must be between 0 and [size()](../android/util/ArraySet.md)-1. |

| Return ||
|---|----------------------------------------------|
| E | Returns the value stored at the given index. |

## Properties

### size

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val size: Int
```

Return the number of items in this array map.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this set (its cardinality) |
