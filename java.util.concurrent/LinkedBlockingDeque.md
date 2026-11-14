# LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkedBlockingDeque

```
open class LinkedBlockingDeque<E : Any!> : AbstractQueue<E>, BlockingDeque<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](../java.util/AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.concurrent.LinkedBlockingDeque](LinkedBlockingDeque.md) |
| --- | --- | --- | --- |

An optionally-bounded [blocking deque](BlockingDeque.md) based on linked nodes.

The optional capacity bound constructor argument serves as a way to prevent excessive expansion. The capacity, if unspecified, is equal to [Integer.MAX_VALUE](../java.lang/Integer.md). Linked nodes are dynamically created upon each insertion unless this would bring the deque above capacity.

Most operations run in constant time (ignoring time spent blocking). Exceptions include #remove(java.lang.Object), #removeFirstOccurrence, #removeLastOccurrence, #contains, #iterator, and the bulk operations, all of which run in linear time.

This class and its iterator implement all of the*optional* methods of the [Collection](../java.util/Collection.md) and [Iterator](../java.util/Iterator.md) interfaces.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkedBlockingDeque](LinkedBlockingDeque.md))`()` Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](../java.lang/Integer.md). |
| [LinkedBlockingDeque](LinkedBlockingDeque.md))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`LinkedBlockingDeque`with the given (fixed) capacity. |
| [LinkedBlockingDeque](LinkedBlockingDeque.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](../java.lang/Integer.md), initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](LinkedBlockingDeque.md))`(`element:` `E`)` Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](LinkedBlockingDeque.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Appends all of the elements in the specified collection to the end of this deque, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](LinkedBlockingDeque.md))`()` Atomically removes all of the elements from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](LinkedBlockingDeque.md))`(`element:` `E?`)` Returns`true`if this deque contains the specified element. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [descendingIterator](LinkedBlockingDeque.md))`()` Returns an iterator over the elements in this deque in reverse sequential order. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](LinkedBlockingDeque.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](LinkedBlockingDeque.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openE | [element](LinkedBlockingDeque.md))`()` Retrieves, but does not remove, the head of the queue represented by this deque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](LinkedBlockingDeque.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `E>`)` <br /> |
| openE | [getFirst](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| openE | [getLast](LinkedBlockingDeque.md))`()` <br /> |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](LinkedBlockingDeque.md))`()` Returns an iterator over the elements in this deque in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](LinkedBlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](LinkedBlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](LinkedBlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| openE? | [peek](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| openE? | [peekFirst](LinkedBlockingDeque.md))`()` <br /> |
| openE? | [peekLast](LinkedBlockingDeque.md))`()` <br /> |
| openE? | [poll](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| openE | [poll](LinkedBlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| openE? | [pollFirst](LinkedBlockingDeque.md))`()` <br /> |
| openE | [pollFirst](LinkedBlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| --- | --- |
| openE? | [pollLast](LinkedBlockingDeque.md))`()` <br /> |
| openE | [pollLast](LinkedBlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| openE | [pop](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putFirst](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLast](LinkedBlockingDeque.md))`(`e:` `E`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](LinkedBlockingDeque.md))`()` Returns the number of additional elements that this deque can ideally (in the absence of memory or resource constraints) accept without blocking. |
| openE | [remove](LinkedBlockingDeque.md))`()` Retrieves and removes the head of the queue represented by this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](LinkedBlockingDeque.md))`(`element:` `E?`)` Removes the first occurrence of the specified element from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](LinkedBlockingDeque.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| openE | [removeFirst](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFirstOccurrence](LinkedBlockingDeque.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](LinkedBlockingDeque.md))`(`filter:` ` [Predicate](../java.util.function/Predicate.md)<in` `E>`)` <br /> |
| openE | [removeLast](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeLastOccurrence](LinkedBlockingDeque.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](LinkedBlockingDeque.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | [spliterator](LinkedBlockingDeque.md))`()` Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this deque. |
| --- | --- |
| openE | [take](LinkedBlockingDeque.md))`()` <br /> |
| openE | [takeFirst](LinkedBlockingDeque.md))`()` <br /> |
| openE | [takeLast](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](LinkedBlockingDeque.md))`()` Returns an array containing all of the elements in this deque, in proper sequence (from first to last element). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](LinkedBlockingDeque.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this deque, in proper sequence; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LinkedBlockingDeque.md))`()` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](LinkedBlockingDeque.md) Returns the number of elements in this deque. |

## Public constructors

### LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedBlockingDeque()
```

Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](../java.lang/Integer.md). 

### LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedBlockingDeque(capacity: Int)
```

Creates a`LinkedBlockingDeque`with the given (fixed) capacity.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the capacity of this deque |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if`capacity`is less than 1 |

### LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedBlockingDeque(c: MutableCollection<out E>!)
```

Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](../java.lang/Integer.md), initially containing the elements of the given collection, added in traversal order of the collection's iterator.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:the collection of elements to initially contain |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element at the end of this deque unless it would violate capacity restrictions. When using a capacity-restricted deque, it is generally preferable to use method #offer(java.lang.Object).

This method is equivalent to #addLast.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](../java.util/Collection.md))) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if this deque is full |

### addAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this deque, in the order that they are returned by the specified collection's iterator. Attempts to`addAll`of a deque to itself result in`IllegalArgumentException`.

| Parameters ||
|-----|---------------------------------------------|
| `c` | the elements to be inserted into this deque |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the collection is this deque |
| `java.lang.IllegalStateException` | if this deque is full |

**See Also**

### addFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(e: E): Unit
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if this deque is full |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### addLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(e: E): Unit
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if this deque is full |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### clear

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Atomically removes all of the elements from this deque. The deque will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

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
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### descendingIterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun descendingIterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in reverse sequential order. The elements will be returned in order from last (tail) to first (head).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this deque in reverse order |

### drainTo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drainTo(c: MutableCollection<in E>!): Int
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<inE\>!:the collection to transfer elements into |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements transferred |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### drainTo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drainTo(
    c: MutableCollection<in E>!, 
    maxElements: Int
): Int
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<inE\>!:the collection to transfer elements into |
| `maxElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of elements to transfer |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements transferred |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### element

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun element(): E
```

Retrieves, but does not remove, the head of the queue represented by this deque. This method differs from #peek() only in that it throws an exception if this deque is empty.

This method is equivalent to #getFirst().

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
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inE\>:The action to be performed for each element |

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

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in proper sequence. The elements will be returned in order from first (head) to last (tail).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this deque in proper sequence |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this queue, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this deque, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerFirst(e: E): Boolean
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this deque, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerFirst(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, or`false`if the specified waiting time elapses before space is available |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerLast(e: E): Boolean
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this deque, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offerLast(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, or`false`if the specified waiting time elapses before space is available |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### peek

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this deque, or`null`if this deque is empty |

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

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this deque, or`null`if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| E | the head of this deque, or`null`if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollFirst(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this deque, or`null`if this deque is empty |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollFirst(
    timeout: Long, 
    unit: TimeUnit!
): E
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| E | the head of this deque, or`null`if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollLast(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the tail of this deque, or`null`if this deque is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollLast(
    timeout: Long, 
    unit: TimeUnit!
): E
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| E | the tail of this deque, or`null`if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### pop

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pop(): E
```

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

| Parameters ||
|-----|-----------------------|
| `e` | E:the element to push |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this deque is full |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### put

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(e: E): Unit
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### putFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putFirst(e: E): Unit
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### putLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLast(e: E): Unit
```

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### remainingCapacity

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainingCapacity(): Int
```

Returns the number of additional elements that this deque can ideally (in the absence of memory or resource constraints) accept without blocking. This is always equal to the initial capacity of this deque less the current`size`of this deque.

Note that you*cannot* always tell if an attempt to insert an element will succeed by inspecting`remainingCapacity`because it may be the case that another thread is about to insert or remove an element.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the remaining capacity |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): E
```

Retrieves and removes the head of the queue represented by this deque. This method differs from #poll() only in that it throws an exception if this deque is empty.

This method is equivalent to #removeFirst().

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

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element`e`such that`o.equals(e)`(if such an element exists). Returns`true`if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

This method is equivalent to #removeFirstOccurrence(java.lang.Object).

| Parameters ||
|-----|---------------------------------------------------|
| `o` | element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this deque changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
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

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if an element was removed as a result of this call |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java.util.function/Predicate.md)\<inE\>:a predicate which returns`true`for elements to be removed |

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

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if an element was removed as a result of this call |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

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

Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this deque.

The returned spliterator is [*weakly consistent*](_package.md).

The`Spliterator`reports [Spliterator.CONCURRENT](../java.util/Spliterator.md), [Spliterator.ORDERED](../java.util/Spliterator.md), and [Spliterator.NONNULL](../java.util/Spliterator.md).

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Spliterator](../java.util/Spliterator.md)<E> | a`Spliterator`over the elements in this deque |

### take

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun take(): E
```

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### takeFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeFirst(): E
```

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### takeLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeLast(): E
```

| Return ||
|---|------------------------|
| E | the tail of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### toArray

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this deque, in proper sequence (from first to last element).

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

Returns an array containing all of the elements in this deque, in proper sequence; the runtime type of the returned array is that of the specified array. If the deque fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this deque.

If this deque fits in the specified array with room to spare (i.e., the array has more elements than this deque), the element in the array immediately following the end of the deque is set to`null`.

Like the [toArray()](LinkedBlockingDeque.md))method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

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

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
