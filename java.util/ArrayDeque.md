# ArrayDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayDeque

```
open class ArrayDeque<E : Any!> : AbstractCollection<E>, Cloneable, Deque<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> ||
| | ↳ | [java.util.ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#) |

Resizable-array implementation of the [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) interface. Array deques have no capacity restrictions; they grow as necessary to support usage. They are not thread-safe; in the absence of external synchronization, they do not support concurrent access by multiple threads. Null elements are prohibited. This class is likely to be faster than [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) when used as a stack, and faster than [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList) when used as a queue.

Most`ArrayDeque`operations run in amortized constant time. Exceptions include #remove(java.lang.Object), [removeFirstOccurrence](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeFirstOccurrence(kotlin.Any)), [removeLastOccurrence](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeLastOccurrence(kotlin.Any)), #contains, #iterator, and the bulk operations, all of which run in linear time.

The iterators returned by this class's #iterator() method are*fail-fast* : If the deque is modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the iterator will generally throw a [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

This class and its iterator implement all of the*optional* methods of the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection), [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection), and [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator) interfaces.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#ArrayDeque())`()` Constructs an empty array deque with an initial capacity sufficient to hold 16 elements. |
| [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#ArrayDeque(kotlin.Int))`(`numElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an empty array deque with an initial capacity sufficient to hold the specified number of elements. |
| [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#ArrayDeque(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Constructs a deque containing the elements of the specified collection, in the order they are returned by the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#add(java.util.ArrayDeque.E))`(`element:` `E`)` Inserts the specified element at the end of this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Adds all of the elements in the specified collection at the end of this deque, as if by calling #addLast on each one, in the order that they are returned by the collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#addFirst(java.util.ArrayDeque.E))`(`e:` `E`)` Inserts the specified element at the front of this deque. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#addLast(java.util.ArrayDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#clear())`()` Removes all of the elements from this deque. |
| open [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#)\<E\> | [clone](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#clone())`()` Returns a copy of this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#contains(java.util.ArrayDeque.E))`(`element:` `E?`)` Returns`true`if this deque contains the specified element. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [descendingIterator](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#descendingIterator())`()` <br /> |
| openE | [element](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#element())`()` Retrieves, but does not remove, the head of the queue represented by this deque. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#forEach(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `E>`)` <br /> |
| openE | [getFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#getFirst())`()` <br /> |
| openE | [getLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#getLast())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#isEmpty())`()` Returns`true`if this deque contains no elements. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#iterator())`()` Returns an iterator over the elements in this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#offer(java.util.ArrayDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#offerFirst(java.util.ArrayDeque.E))`(`e:` `E`)` Inserts the specified element at the front of this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#offerLast(java.util.ArrayDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque. |
| openE? | [peek](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#peek())`()` Retrieves, but does not remove, the head of the queue represented by this deque, or returns`null`if this deque is empty. |
| --- | --- |
| openE? | [peekFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#peekFirst())`()` <br /> |
| openE? | [peekLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#peekLast())`()` <br /> |
| openE? | [poll](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#poll())`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns`null`if this deque is empty. |
| --- | --- |
| openE? | [pollFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#pollFirst())`()` <br /> |
| openE? | [pollLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#pollLast())`()` <br /> |
| openE | [pop](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#pop())`()` Pops an element from the stack represented by this deque. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#push(java.util.ArrayDeque.E))`(`e:` `E`)` Pushes an element onto the stack represented by this deque. |
| openE | [remove](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#remove())`()` Retrieves and removes the head of the queue represented by this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#remove(java.util.ArrayDeque.E))`(`element:` `E?`)` Removes a single instance of the specified element from this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| openE | [removeFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeFirst())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFirstOccurrence](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeFirstOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the first occurrence of the specified element in this deque (when traversing the deque from head to tail). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeIf(java.util.function.Predicate))`(`filter:` ` [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate)<in` `E>`)` <br /> |
| openE | [removeLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeLast())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeLastOccurrence](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeLastOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the last occurrence of the specified element in this deque (when traversing the deque from head to tail). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)\<E\> | [spliterator](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#spliterator())`()` Creates a* [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and*fail-fast* [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) over the elements in this deque. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#toArray())`()` Returns an array containing all of the elements in this deque in proper sequence (from first to last element). |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this deque in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||
| From class [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Deque](https://developer.android.com/reference/kotlin/java/util/Deque)<E> | [reversed](https://developer.android.com/reference/kotlin/java/util/Deque#reversed())`()` <br /> Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#size:kotlin.Int) Returns the number of elements in this deque. |

## Public constructors

### ArrayDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayDeque()
```

Constructs an empty array deque with an initial capacity sufficient to hold 16 elements. 

### ArrayDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayDeque(numElements: Int)
```

Constructs an empty array deque with an initial capacity sufficient to hold the specified number of elements.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| `numElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):lower bound on initial capacity of the deque |

### ArrayDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayDeque(c: MutableCollection<out E>)
```

Constructs a deque containing the elements of the specified collection, in the order they are returned by the collection's iterator. (The first element returned by the collection's iterator becomes the first element, or*front*of the deque.)

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:the collection whose elements are to be placed into the deque |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element at the end of this deque.

This method is equivalent to #addLast.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### addAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection at the end of this deque, as if by calling #addLast on each one, in the order that they are returned by the collection's iterator.

| Parameters ||
|-----|---------------------------------------------|
| `c` | the elements to be inserted into this deque |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

### addFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(e: E): Unit
```

Inserts the specified element at the front of this deque.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### addLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(e: E): Unit
```

Inserts the specified element at the end of this deque.

This method is equivalent to #add.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### clear

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this deque. The deque will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### clone

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): ArrayDeque<E>
```

Returns a copy of this deque.

| Return ||
|---------------------------------------------------------------------------------------|----------------------|
| [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#)<E> | a copy of this deque |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Returns`true`if this deque contains the specified element. More formally, returns`true`if and only if this deque contains at least one element`e`such that`o.equals(e)`.

| Parameters ||
|-----|----------------------------------------------------|
| `o` | object to be checked for containment in this deque |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque contains the specified element |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### descendingIterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun descendingIterator(): MutableIterator<E>
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this deque in reverse sequence |

### element

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun element(): E
```

Retrieves, but does not remove, the head of the queue represented by this deque. This method differs from #peek only in that it throws an exception if this deque is empty.

This method is equivalent to #getFirst.

| Return ||
|---|-------------------------------------------------|
| E | the head of the queue represented by this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### getFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFirst(): E
```

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### getLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLast(): E
```

| Return ||
|---|------------------------|
| E | the tail of this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### isEmpty

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this deque contains no elements.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque contains no elements |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque. The elements will be ordered from first (head) to last (tail). This is the same order that elements would be dequeued (via successive calls to #remove or popped (via successive calls to [pop](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#pop())).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this deque |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

Inserts the specified element at the end of this deque.

This method is equivalent to [offerLast](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#offerLast(java.util.ArrayDeque.E)).

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Queue.offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E))) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerFirst(e: E): Boolean
```

Inserts the specified element at the front of this deque.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Deque.offerFirst](https://developer.android.com/reference/kotlin/java/util/Deque#offerFirst(java.util.Deque.E))) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerLast(e: E): Boolean
```

Inserts the specified element at the end of this deque.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Deque.offerLast](https://developer.android.com/reference/kotlin/java/util/Deque#offerLast(java.util.Deque.E))) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### peek

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): E?
```

Retrieves, but does not remove, the head of the queue represented by this deque, or returns`null`if this deque is empty.

This method is equivalent to [peekFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#peekFirst()).

| Return ||
|----|---------------------------------------------------------------------------------|
| E? | the head of the queue represented by this deque, or`null`if this deque is empty |

### peekFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekFirst(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this deque, or`null`if this deque is empty |

### peekLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekLast(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the tail of this deque, or`null`if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): E?
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns`null`if this deque is empty.

This method is equivalent to [pollFirst](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#pollFirst()).

| Return ||
|----|---------------------------------------------------------------------------------|
| E? | the head of the queue represented by this deque, or`null`if this deque is empty |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollFirst(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this deque, or`null`if this deque is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollLast(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the tail of this deque, or`null`if this deque is empty |

### pop

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pop(): E
```

Pops an element from the stack represented by this deque. In other words, removes and returns the first element of this deque.

This method is equivalent to #removeFirst().

| Return ||
|---|--------------------------------------------------------------------------------------------------|
| E | the element at the front of this deque (which is the top of the stack represented by this deque) |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### push

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun push(e: E): Unit
```

Pushes an element onto the stack represented by this deque. In other words, inserts the element at the front of this deque.

This method is equivalent to #addFirst.

| Parameters ||
|-----|-----------------------|
| `e` | E:the element to push |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): E
```

Retrieves and removes the head of the queue represented by this deque. This method differs from #poll() only in that it throws an exception if this deque is empty.

This method is equivalent to #removeFirst.

| Return ||
|---|-------------------------------------------------|
| E | the head of the queue represented by this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element`e`such that`o.equals(e)`(if such an element exists). Returns`true`if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

This method is equivalent to [removeFirstOccurrence(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#removeFirstOccurrence(kotlin.Any)).

| Parameters ||
|-----|---------------------------------------------------|
| `o` | element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque contained the specified element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

| Parameters ||
|-----|-------------------------------------------------------------------|
| `c` | collection containing elements to be removed from this collection |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`method is not supported by this collection |
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not support null elements (java.util.Collection#) or if the specified collection is null |
| --- | --- |

### removeFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeFirst(): E
```

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### removeFirstOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeFirstOccurrence(o: Any?): Boolean
```

Removes the first occurrence of the specified element in this deque (when traversing the deque from head to tail). If the deque does not contain the element, it is unchanged. More formally, removes the first element`e`such that`o.equals(e)`(if such an element exists). Returns`true`if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the deque contained the specified element |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate)\<inE\>:a predicate which returns`true`for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

### removeLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeLast(): E
```

| Return ||
|---|------------------------|
| E | the tail of this deque |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### removeLastOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeLastOccurrence(o: Any?): Boolean
```

Removes the last occurrence of the specified element in this deque (when traversing the deque from head to tail). If the deque does not contain the element, it is unchanged. More formally, removes the last element`e`such that`o.equals(e)`(if such an element exists). Returns`true`if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the deque contained the specified element |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### retainAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

| Parameters ||
|-----|------------------------------------------------------------------|
| `c` | collection containing elements to be retained in this collection |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not permit null elements (java.util.Collection#) or if the specified collection is null |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and*fail-fast* [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) over the elements in this deque.

The`Spliterator`reports [Spliterator.SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), [Spliterator.SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int), [Spliterator.ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int), and [Spliterator.NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator#NONNULL:kotlin.Int). Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)<E> | a`Spliterator`over the elements in this deque |

### toArray

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this deque in proper sequence (from first to last element).

The returned array will be "safe" in that no references to it are maintained by this deque. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all of the elements in this deque |

### toArray

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this deque in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the deque fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this deque.

If this deque fits in the specified array with room to spare (i.e., the array has more elements than this deque), the element in the array immediately following the end of the deque is set to`null`.

Like the [toArray()](https://developer.android.com/reference/kotlin/java/util/ArrayDeque#toArray())method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose`x`is a deque known to contain only strings. The following code can be used to dump the deque into a newly allocated array of`String`: 

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that`toArray(new Object[0])`is identical in function to`toArray()`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of the deque are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing all of the elements in this deque |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this deque |
| `java.lang.NullPointerException` | if the specified array is null |

## Properties

### size

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of elements in this deque.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this deque |
