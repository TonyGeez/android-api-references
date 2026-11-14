# AbstractQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractQueue

```
abstract class AbstractQueue<E : Any!> : AbstractCollection<E>, Queue<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> ||
| | ↳ | [java.util.AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#) |

| Known Direct Subclasses [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue), [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue), [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue), [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue), [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue), [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue), [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue) | A bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) backed by an array. | | [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue) | An unbounded thread-safe [queue](https://developer.android.com/reference/kotlin/java/util/Queue) based on linked nodes. | | [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) | An optionally-bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) based on linked nodes. | | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) based on linked nodes. | | [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) that uses the same ordering rules as class [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) and supplies blocking retrieval operations. | | [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) | An unbounded priority [queue](https://developer.android.com/reference/kotlin/java/util/Queue) based on a priority heap. | | [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) | A [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class provides skeletal implementations of some [Queue](https://developer.android.com/reference/kotlin/java/util/Queue) operations. The implementations in this class are appropriate when the base implementation does*not* allow`null`elements. Methods #add, #remove, and [element](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#element())are based on [offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E)), [poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll()), and [peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek()), respectively, but throw exceptions instead of indicating failure via`false`or`null`returns.

A`Queue`implementation that extends this class must minimally define a method [Queue.offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E))which does not permit insertion of`null`elements, along with methods [java.util.Queue#peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek()), [Queue.poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll()), [Collection.size](https://developer.android.com/reference/kotlin/java/util/Collection#size()), and [Collection.iterator](https://developer.android.com/reference/kotlin/java/util/Collection#iterator()). Typically, additional methods will be overridden as well. If these requirements cannot be met, consider instead subclassing [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection).

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#AbstractQueue())`()` Constructor for use by subclasses. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#add(java.util.AbstractQueue.E))`(`element:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Adds all of the elements in the specified collection to this queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#clear())`()` Removes all of the elements from this queue. |
| --- | --- |
| openE | [element](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#element())`()` Retrieves, but does not remove, the head of this queue. |
| openE | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractQueue#remove())`()` Retrieves and removes the head of this queue. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty())`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#iterator())`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray())`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||
| From class [Queue](https://developer.android.com/reference/kotlin/java/util/Queue) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](https://developer.android.com/reference/kotlin/java/util/Queue#add(java.util.Queue.E)), which can fail to insert an element only by throwing an exception. <br /> | | E? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek())`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll())`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int) <br /> | ||

## Protected constructors

### AbstractQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractQueue()
```

Constructor for use by subclasses.

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available.

This implementation returns`true`if`offer`succeeds, else throws an`IllegalStateException`.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null and this queue does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress.

This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a`null`element) may result in only some of the elements having been successfully added when the associated exception is thrown.

| Parameters ||
|-----|----------------------------------------------------------|
| `c` | collection containing elements to be added to this queue |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this queue changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified collection contains a null element and this queue does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this queue, or if the specified collection is this queue |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

**See Also**

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this queue. The queue will be empty after this call returns.

This implementation repeatedly invokes [poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll())until it returns`null`.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun element(): E
```

Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek())only in that it throws an exception if this queue is empty.

This implementation returns the result of`peek`unless the queue is empty.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this queue is empty |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): E
```

Retrieves and removes the head of this queue. This method differs from [poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll())only in that it throws an exception if this queue is empty.

This implementation returns the result of`poll`unless the queue is empty.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this queue is empty |
