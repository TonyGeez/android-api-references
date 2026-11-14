# LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkedBlockingDeque

```
open class LinkedBlockingDeque<E : Any!> : AbstractQueue<E>, BlockingDeque<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#)\<E\> |||
| | ↳ | [java.util.AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#)\<E\> ||
| | | ↳ | [java.util.concurrent.LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#) |
| --- | --- | --- | --- |

An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes.

The optional capacity bound constructor argument serves as a way to prevent excessive expansion. The capacity, if unspecified, is equal to [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int). Linked nodes are dynamically created upon each insertion unless this would bring the deque above capacity.

Most operations run in constant time (ignoring time spent blocking). Exceptions include #remove(java.lang.Object), #removeFirstOccurrence, #removeLastOccurrence, #contains, #iterator, and the bulk operations, all of which run in linear time.

This class and its iterator implement all of the*optional* methods of the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) and [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator.html#) interfaces.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#LinkedBlockingDeque())`()` Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int). |
| [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#LinkedBlockingDeque(kotlin.Int))`(`capacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`LinkedBlockingDeque`with the given (fixed) capacity. |
| [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#LinkedBlockingDeque(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int), initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#add(java.util.concurrent.LinkedBlockingDeque.E))`(`element:` `E`)` Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Appends all of the elements in the specified collection to the end of this deque, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#addFirst(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#addLast(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#clear())`()` Atomically removes all of the elements from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#contains(java.util.concurrent.LinkedBlockingDeque.E))`(`element:` `E?`)` Returns`true`if this deque contains the specified element. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [descendingIterator](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#descendingIterator())`()` Returns an iterator over the elements in this deque in reverse sequential order. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#drainTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#drainTo(kotlin.collections.MutableCollection,%20kotlin.Int))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openE | [element](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#element())`()` Retrieves, but does not remove, the head of the queue represented by this deque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#forEach(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `E>`)` <br /> |
| openE | [getFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#getFirst())`()` <br /> |
| --- | --- |
| openE | [getLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#getLast())`()` <br /> |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#iterator())`()` Returns an iterator over the elements in this deque in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offer(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offer(java.util.concurrent.LinkedBlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offerFirst(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offerFirst(java.util.concurrent.LinkedBlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offerLast(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#offerLast(java.util.concurrent.LinkedBlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| openE? | [peek](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#peek())`()` <br /> |
| --- | --- |
| openE? | [peekFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#peekFirst())`()` <br /> |
| openE? | [peekLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#peekLast())`()` <br /> |
| openE? | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#poll())`()` <br /> |
| --- | --- |
| openE | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| openE? | [pollFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#pollFirst())`()` <br /> |
| openE | [pollFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#pollFirst(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| --- | --- |
| openE? | [pollLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#pollLast())`()` <br /> |
| openE | [pollLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#pollLast(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> |
| openE | [pop](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#pop())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#push(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#put(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#putFirst(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#putLast(java.util.concurrent.LinkedBlockingDeque.E))`(`e:` `E`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#remainingCapacity())`()` Returns the number of additional elements that this deque can ideally (in the absence of memory or resource constraints) accept without blocking. |
| openE | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#remove())`()` Retrieves and removes the head of the queue represented by this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#remove(java.util.concurrent.LinkedBlockingDeque.E))`(`element:` `E?`)` Removes the first occurrence of the specified element from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| openE | [removeFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeFirst())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFirstOccurrence](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeFirstOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeIf(java.util.function.Predicate))`(`filter:` ` [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)<in` `E>`)` <br /> |
| openE | [removeLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeLast())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeLastOccurrence](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#removeLastOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)\<E\> | [spliterator](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#spliterator())`()` Returns a [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#) over the elements in this deque. |
| --- | --- |
| openE | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#take())`()` <br /> |
| openE | [takeFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#takeFirst())`()` <br /> |
| openE | [takeLast](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#takeLast())`()` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#toArray())`()` Returns an array containing all of the elements in this deque, in proper sequence (from first to last element). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this deque, in proper sequence; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#toString())`()` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#size:kotlin.Int) Returns the number of elements in this deque. |

## Public constructors

### LinkedBlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedBlockingDeque()
```

Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int). 

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

Creates a`LinkedBlockingDeque`with a capacity of [Integer.MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Integer.html#MAX_VALUE:kotlin.Int), initially containing the elements of the given collection, added in traversal order of the collection's iterator.

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E))) |

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

The returned iterator is [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

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
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inE\>:The action to be performed for each element |

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

The returned iterator is [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

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
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

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
| `filter` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)\<inE\>:a predicate which returns`true`for elements to be removed |

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

Returns a [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#) over the elements in this deque.

The returned spliterator is [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

The`Spliterator`reports [Spliterator.CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int), [Spliterator.ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int), and [Spliterator.NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)<E> | a`Spliterator`over the elements in this deque |

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

Like the [toArray()](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque#toArray())method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

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
