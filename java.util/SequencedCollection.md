# SequencedCollection

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedCollection

```
interface SequencedCollection<E : Any!> : MutableCollection<E>
```

| [java.util.SequencedCollection](../java/util/SequencedCollection.md) |

| Known Direct Subclasses [Deque](../java/util/Deque.md), [List](../java/util/List.md), [SequencedSet](../java/util/SequencedSet.md) |---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Deque](../java/util/Deque.md) | A linear collection that supports element insertion and removal at both ends. | | [List](../java/util/List.md) | An ordered collection, where the user has precise control over where in the list each element is inserted. | | [SequencedSet](../java/util/SequencedSet.md) | A collection that is both a [SequencedCollection](../java/util/SequencedCollection.md) and a [Set](../java/util/Set.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrayDeque](../java/util/ArrayDeque.md), [BlockingDeque](../java/util/concurrent/BlockingDeque.md), [ConcurrentLinkedDeque](../java/util/concurrent/ConcurrentLinkedDeque.md), [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md), [LinkedBlockingDeque](../java/util/concurrent/LinkedBlockingDeque.md), [LinkedHashSet](../java/util/LinkedHashSet.md), [LinkedList](../java/util/LinkedList.md), [NavigableSet](../java/util/NavigableSet.md), [SortedSet](../java/util/SortedSet.md), [TreeSet](../java/util/TreeSet.md) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayDeque](../java/util/ArrayDeque.md) | Resizable-array implementation of the [Deque](../java/util/Deque.md) interface. | | [BlockingDeque](../java/util/concurrent/BlockingDeque.md) | A [Deque](../java/util/Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [ConcurrentLinkedDeque](../java/util/concurrent/ConcurrentLinkedDeque.md) | An unbounded concurrent [deque](../java/util/Deque.md) based on linked nodes. | | [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java/util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md). | | [LinkedBlockingDeque](../java/util/concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java/util/concurrent/BlockingDeque.md) based on linked nodes. | | [LinkedHashSet](../java/util/LinkedHashSet.md) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | | [LinkedList](../java/util/LinkedList.md) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [NavigableSet](../java/util/NavigableSet.md) | A [SortedSet](../java/util/SortedSet.md) extended with navigation methods reporting closest matches for given search targets. | | [SortedSet](../java/util/SortedSet.md) | A [Set](../java/util/Set.md) that further provides a*total ordering*on its elements. | | [TreeSet](../java/util/TreeSet.md) | A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A collection that has a well-defined encounter order, that supports operations at both ends, and that is reversible. The elements of a sequenced collection have an*encounter order*, where conceptually the elements have a linear arrangement from the first element to the last element. Given any two elements, one element is either before (closer to the first element) or after (closer to the last element) the other element.

(Note that this definition does not imply anything about physical positioning of elements, such as their locations in a computer's memory.)

Several methods inherited from the [Collection](../java/util/Collection.md) interface are required to operate on elements according to this collection's encounter order. For instance, the [iterator](../java/util/Collection.md))method provides elements starting from the first element, proceeding through successive elements, until the last element. Other methods that are required to operate on elements in encounter order include the following: [forEach](../java/lang/Iterable.md)), [parallelStream](../java/util/Collection.md)), [spliterator](../java/util/Collection.md)), [stream](../java/util/Collection.md)), and all overloads of the java.util.Collection#toArray method.

This interface provides methods to add, retrieve, and remove elements at either end of the collection.

This interface also defines the [reversed](../java/util/SequencedCollection.md))method, which provides a reverse-ordered [view](../java/util/Collection.md) of this collection. In the reverse-ordered view, the concepts of first and last are inverted, as are the concepts of successor and predecessor. The first element of this collection is the last element of the reverse-ordered view, and vice-versa. The successor of some element in this collection is its predecessor in the reversed view, and vice-versa. All methods that respect the encounter order of the collection operate as if the encounter order is inverted. For instance, the [iterator](../java/util/Collection.md))method of the reversed view reports the elements in order from the last element of this collection to the first. The availability of the`reversed`method, and its impact on the ordering semantics of all applicable methods, allow convenient iteration, searching, copying, and streaming of the elements of this collection in either forward order or reverse order.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/SequencedCollection.md))`(`e:` `E`)` Adds an element as the first element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/SequencedCollection.md))`(`e:` `E`)` Adds an element as the last element of this collection (optional operation). |
| openE | [getFirst](../java/util/SequencedCollection.md))`()` Gets the first element of this collection. |
| --- | --- |
| openE | [getLast](../java/util/SequencedCollection.md))`()` Gets the last element of this collection. |
| openE | [removeFirst](../java/util/SequencedCollection.md))`()` Removes and returns the first element of this collection (optional operation). |
| openE | [removeLast](../java/util/SequencedCollection.md))`()` Removes and returns the last element of this collection (optional operation). |
| --- | --- |
| abstract [SequencedCollection](../java/util/SequencedCollection.md)\<E\>! | [reversed](../java/util/SequencedCollection.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. |

## Public methods

### addFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(e: E): Unit
```

Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order.

| Parameters ||
|-----|---------------------------|
| `e` | E:the element to be added |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### addLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(e: E): Unit
```

Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order.

| Parameters ||
|-----|----------------------------|
| `e` | E:the element to be added. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### getFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFirst(): E
```

Gets the first element of this collection.

| Return ||
|---|-----------------------|
| E | the retrieved element |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |

### getLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLast(): E
```

Gets the last element of this collection.

| Return ||
|---|-----------------------|
| E | the retrieved element |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |

### removeFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeFirst(): E
```

Removes and returns the first element of this collection (optional operation).

| Return ||
|---|---------------------|
| E | the removed element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### removeLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeLast(): E
```

Removes and returns the last element of this collection (optional operation).

| Return ||
|---|---------------------|
| E | the removed element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reversed(): SequencedCollection<E>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [SequencedCollection](../java/util/SequencedCollection.md)<E>! | a reverse-ordered view of this collection |
