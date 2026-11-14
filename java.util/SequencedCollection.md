# SequencedCollection

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedCollection

```
interface SequencedCollection<E : Any!> : MutableCollection<E>
```

| [java.util.SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#) |

| Known Direct Subclasses [Deque](https://developer.android.com/reference/kotlin/java/util/Deque), [List](https://developer.android.com/reference/kotlin/java/util/List), [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet) |---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) | A linear collection that supports element insertion and removal at both ends. | | [List](https://developer.android.com/reference/kotlin/java/util/List) | An ordered collection, where the user has precise control over where in the list each element is inserted. | | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet) | A collection that is both a [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#) and a [Set](https://developer.android.com/reference/kotlin/java/util/Set). | |

| Known Indirect Subclasses [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque), [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque), [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque), [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet), [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList), [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet), [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet), [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque) | Resizable-array implementation of the [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) interface. | | [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) | A [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque) | An unbounded concurrent [deque](https://developer.android.com/reference/kotlin/java/util/Deque) based on linked nodes. | | [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet) | A scalable concurrent [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap). | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | | [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) | A [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) extended with navigation methods reporting closest matches for given search targets. | | [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) | A [Set](https://developer.android.com/reference/kotlin/java/util/Set) that further provides a*total ordering*on its elements. | | [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) | A [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap). | |

A collection that has a well-defined encounter order, that supports operations at both ends, and that is reversible. The elements of a sequenced collection have an*encounter order*, where conceptually the elements have a linear arrangement from the first element to the last element. Given any two elements, one element is either before (closer to the first element) or after (closer to the last element) the other element.

(Note that this definition does not imply anything about physical positioning of elements, such as their locations in a computer's memory.)

Several methods inherited from the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) interface are required to operate on elements according to this collection's encounter order. For instance, the [iterator](https://developer.android.com/reference/kotlin/java/util/Collection#iterator())method provides elements starting from the first element, proceeding through successive elements, until the last element. Other methods that are required to operate on elements in encounter order include the following: [forEach](https://developer.android.com/reference/kotlin/java/lang/Iterable.html#forEach(java.util.function.Consumer)), [parallelStream](https://developer.android.com/reference/kotlin/java/util/Collection#parallelStream()), [spliterator](https://developer.android.com/reference/kotlin/java/util/Collection#spliterator()), [stream](https://developer.android.com/reference/kotlin/java/util/Collection#stream()), and all overloads of the java.util.Collection#toArray method.

This interface provides methods to add, retrieve, and remove elements at either end of the collection.

This interface also defines the [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#reversed())method, which provides a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. In the reverse-ordered view, the concepts of first and last are inverted, as are the concepts of successor and predecessor. The first element of this collection is the last element of the reverse-ordered view, and vice-versa. The successor of some element in this collection is its predecessor in the reversed view, and vice-versa. All methods that respect the encounter order of the collection operate as if the encounter order is inverted. For instance, the [iterator](https://developer.android.com/reference/kotlin/java/util/Collection#iterator())method of the reversed view reports the elements in order from the last element of this collection to the first. The availability of the`reversed`method, and its impact on the ordering semantics of all applicable methods, allow convenient iteration, searching, copying, and streaming of the elements of this collection in either forward order or reverse order.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#addFirst(java.util.SequencedCollection.E))`(`e:` `E`)` Adds an element as the first element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#addLast(java.util.SequencedCollection.E))`(`e:` `E`)` Adds an element as the last element of this collection (optional operation). |
| openE | [getFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#getFirst())`()` Gets the first element of this collection. |
| openE | [getLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#getLast())`()` Gets the last element of this collection. |
| openE | [removeFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#removeFirst())`()` Removes and returns the first element of this collection (optional operation). |
| openE | [removeLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#removeLast())`()` Removes and returns the last element of this collection (optional operation). |
| abstract [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#)\<E\>! | [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. |

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

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#)<E>! | a reverse-ordered view of this collection |
