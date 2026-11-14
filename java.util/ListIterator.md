# ListIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ListIterator

```
interface ListIterator<E : Any!> : MutableIterator<E>
```

| [java.util.ListIterator](https://developer.android.com/reference/kotlin/java/util/ListIterator#) |

An iterator for lists that allows the programmer to traverse the list in either direction, modify the list during iteration, and obtain the iterator's current position in the list. A`ListIterator`has no current element; its*cursor position* always lies between the element that would be returned by a call to`previous()`and the element that would be returned by a call to`next()`. An iterator for a list of length`n`has`n+1`possible cursor positions, as illustrated by the carets (`^`) below: 

```kotlin
Element(0)   Element(1)   Element(2)   ... Element(n-1)
  cursor positions:  ^            ^            ^            ^                  ^
  
```
Note that the [remove](https://developer.android.com/reference/kotlin/java/util/ListIterator#remove())and [set(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/ListIterator#set(java.util.ListIterator.E))methods are*not* defined in terms of the cursor position; they are defined to operate on the last element returned by a call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())or [previous()](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous()).

<br />

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/ListIterator#add(java.util.ListIterator.E))`(`e:` `E`)` Inserts the specified element into the list (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNext](https://developer.android.com/reference/kotlin/java/util/ListIterator#hasNext())`()` Returns`true`if this list iterator has more elements when traversing the list in the forward direction. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPrevious](https://developer.android.com/reference/kotlin/java/util/ListIterator#hasPrevious())`()` Returns`true`if this list iterator has more elements when traversing the list in the reverse direction. |
| abstractE | [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())`()` Returns the next element in the list and advances the cursor position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextIndex](https://developer.android.com/reference/kotlin/java/util/ListIterator#nextIndex())`()` Returns the index of the element that would be returned by a subsequent call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next()). |
| abstractE | [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())`()` Returns the previous element in the list and moves the cursor position backwards. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousIndex](https://developer.android.com/reference/kotlin/java/util/ListIterator#previousIndex())`()` Returns the index of the element that would be returned by a subsequent call to [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/ListIterator#remove())`()` Removes from the list the last element that was returned by [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())or [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())(optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/ListIterator#set(java.util.ListIterator.E))`(`e:` `E`)` Replaces the last element returned by [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())or [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())with the specified element (optional operation). |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(e: E): Unit
```

Inserts the specified element into the list (optional operation). The element is inserted immediately before the element that would be returned by [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next()), if any, and after the element that would be returned by [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous()), if any. (If the list contains no elements, the new element becomes the sole element on the list.) The new element is inserted before the implicit cursor: a subsequent call to`next`would be unaffected, and a subsequent call to`previous`would return the new element. (This call increases by one the value that would be returned by a call to`nextIndex`or`previousIndex`.)

| Parameters ||
|-----|-------------------------|
| `e` | E:the element to insert |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`method is not supported by this list iterator |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some aspect of this element prevents it from being added to this list |

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasNext(): Boolean
```

Returns`true`if this list iterator has more elements when traversing the list in the forward direction. (In other words, returns`true`if [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())would return an element rather than throwing an exception.)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the list iterator has more elements when traversing the list in the forward direction |

### hasPrevious

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasPrevious(): Boolean
```

Returns`true`if this list iterator has more elements when traversing the list in the reverse direction. (In other words, returns`true`if [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())would return an element rather than throwing an exception.)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the list iterator has more elements when traversing the list in the reverse direction |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): E
```

Returns the next element in the list and advances the cursor position. This method may be called repeatedly to iterate through the list, or intermixed with calls to [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())to go back and forth. (Note that alternating calls to`next`and`previous`will return the same element repeatedly.)

| Return ||
|---|------------------------------|
| E | the next element in the list |

| Exceptions ||
|------------------------------------|--------------------------------------|
| `java.util.NoSuchElementException` | if the iteration has no next element |

### nextIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextIndex(): Int
```

Returns the index of the element that would be returned by a subsequent call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next()). (Returns list size if the list iterator is at the end of the list.)

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the element that would be returned by a subsequent call to`next`, or list size if the list iterator is at the end of the list |

### previous

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previous(): E
```

Returns the previous element in the list and moves the cursor position backwards. This method may be called repeatedly to iterate through the list backwards, or intermixed with calls to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())to go back and forth. (Note that alternating calls to`next`and`previous`will return the same element repeatedly.)

| Return ||
|---|----------------------------------|
| E | the previous element in the list |

| Exceptions ||
|------------------------------------|------------------------------------------|
| `java.util.NoSuchElementException` | if the iteration has no previous element |

### previousIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previousIndex(): Int
```

Returns the index of the element that would be returned by a subsequent call to [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous()). (Returns -1 if the list iterator is at the beginning of the list.)

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the element that would be returned by a subsequent call to`previous`, or -1 if the list iterator is at the beginning of the list |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(): Unit
```

Removes from the list the last element that was returned by [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())or [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())(optional operation). This call can only be made once per call to`next`or`previous`. It can be made only if [add](https://developer.android.com/reference/kotlin/java/util/ListIterator#add(java.util.ListIterator.E))has not been called after the last call to`next`or`previous`.

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list iterator |
| `java.lang.IllegalStateException` | if neither`next`nor`previous`have been called, or`remove`or`add`have been called after the last call to`next`or`previous` |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun set(e: E): Unit
```

Replaces the last element returned by [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())or [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())with the specified element (optional operation). This call can be made only if neither [remove](https://developer.android.com/reference/kotlin/java/util/ListIterator#remove())nor [add](https://developer.android.com/reference/kotlin/java/util/ListIterator#add(java.util.ListIterator.E))have been called after the last call to`next`or`previous`.

| Parameters ||
|-----|------------------------------------------------------------------------------------|
| `e` | E:the element with which to replace the last element returned by`next`or`previous` |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this list iterator |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some aspect of the specified element prevents it from being added to this list |
| `java.lang.IllegalStateException` | if neither`next`nor`previous`have been called, or`remove`or`add`have been called after the last call to`next`or`previous` |
