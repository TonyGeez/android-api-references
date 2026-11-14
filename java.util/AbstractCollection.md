# AbstractCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractCollection

```
abstract class AbstractCollection<E : Any!> : MutableCollection<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#) |

| Known Direct Subclasses [AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList), [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue), [AbstractSet](https://developer.android.com/reference/kotlin/java/util/AbstractSet), [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque), [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList) | This class provides a skeletal implementation of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface to minimize the effort required to implement this interface backed by a "random access" data store (such as an array). | | [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue) | This class provides skeletal implementations of some [Queue](https://developer.android.com/reference/kotlin/java/util/Queue) operations. | | [AbstractSet](https://developer.android.com/reference/kotlin/java/util/AbstractSet) | This class provides a skeletal implementation of the`Set`interface to minimize the effort required to implement this interface. | | [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque) | Resizable-array implementation of the [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) interface. | | [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque) | An unbounded concurrent [deque](https://developer.android.com/reference/kotlin/java/util/Deque) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList), [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue), [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList), [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue), [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet), [CopyOnWriteArraySet](https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArraySet), [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue), [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet), [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue), [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet), and 8 others. |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList) | This class provides a skeletal implementation of the`List`interface to minimize the effort required to implement this interface backed by a "sequential access" data store (such as a linked list). | | [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue) | A bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) backed by an array. | | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList) | Resizable-array implementation of the`List`interface. | | [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue) | An unbounded thread-safe [queue](https://developer.android.com/reference/kotlin/java/util/Queue) based on linked nodes. | | [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet) | A scalable concurrent [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap). | | [CopyOnWriteArraySet](https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArraySet) | A [Set](https://developer.android.com/reference/kotlin/java/util/Set) that uses an internal [CopyOnWriteArrayList](https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList) for all of its operations. | | [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet) | A specialized [Set](https://developer.android.com/reference/kotlin/java/util/Set) implementation for use with enum types. | | [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet) | This class implements the`Set`interface, backed by a hash table (actually a`HashMap`instance). | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) | An optionally-bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) based on linked nodes. | | [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | | [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) based on linked nodes. | | [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) that uses the same ordering rules as class [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) and supplies blocking retrieval operations. | | [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) | An unbounded priority [queue](https://developer.android.com/reference/kotlin/java/util/Queue) based on a priority heap. | | [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) | The`Stack`class represents a last-in-first-out (LIFO) stack of objects. | | [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) | A [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) | A [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap). | | [Vector](https://developer.android.com/reference/kotlin/java/util/Vector) | The`Vector`class implements a growable array of objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class provides a skeletal implementation of the`Collection`interface, to minimize the effort required to implement this interface.

To implement an unmodifiable collection, the programmer needs only to extend this class and provide implementations for the`iterator`and`size`methods. (The iterator returned by the`iterator`method must implement`hasNext`and`next`.)

To implement a modifiable collection, the programmer must additionally override this class's`add`method (which otherwise throws an`UnsupportedOperationException`), and the iterator returned by the`iterator`method must additionally implement its`remove`method.

The programmer should generally provide a void (no argument) and`Collection`constructor, as per the recommendation in the`Collection`interface specification.

The documentation for each non-abstract method in this class describes its implementation in detail. Each of these methods may be overridden if the collection being implemented admits a more efficient implementation.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#AbstractCollection())`()` Sole constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#add(java.util.AbstractCollection.E))`(`element:` `E`)` Ensures that this collection contains the specified element (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Adds all of the elements in the specified collection to this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#clear())`()` Removes all of the elements from this collection (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` Returns`true`if this collection contains the specified element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Returns`true`if this collection contains all of the elements in the specified collection. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty())`()` Returns`true`if this collection contains no elements. |
| --- | --- |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#iterator())`()` Returns an iterator over the elements contained in this collection. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` Removes a single instance of the specified element from this collection, if it is present (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Removes all of this collection's elements that are also contained in the specified collection (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Retains only the elements in this collection that are contained in the specified collection (optional operation). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray())`()` Returns an array containing all of the elements in this collection. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` Returns a string representation of this collection. |

| Properties ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int) <br /> |

## Protected constructors

### AbstractCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractCollection()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.)

Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added.

If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns.

| Parameters ||
|-----|------------------------------------------------------------|
| `e` | element whose presence in this collection is to be ensured |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this collection |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the element prevents it from being added to this collection |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order.

| Parameters ||
|-----|---------------------------------------------------------------|
| `c` | collection containing elements to be added to this collection |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this collection |
| `java.lang.NullPointerException` | if the specified collection contains a null element and this collection does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this collection |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

**See Also**

- [#add(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#add(java.util.AbstractCollection.E)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|-----------------------------------------------------------|
| `o` | element whose presence in this collection is to be tested |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection contains the specified element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (java.util.Collection#) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsAll(elements: Collection<E>): Boolean
```

Returns`true`if this collection contains all of the elements in the specified collection.

| Parameters ||
|-----|-------------------------------------------------------------|
| `c` | collection to be checked for containment in this collection |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection contains all of the elements in the specified collection |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this collection does not permit null elements (java.util.Collection#) or if the specified collection is null. |

**See Also**

- [#contains(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E)) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this collection contains no elements.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements contained in this collection.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements contained in this collection |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call).

| Parameters ||
|-----|--------------------------------------------------------|
| `o` | element to be removed from this collection, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if an element was removed as a result of this call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection.

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

**See Also**

- [#remove(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))
- [#contains(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E)) 

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection.

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

**See Also**

- [#remove(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))
- [#contains(Object)](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E)) 

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`.

The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array, whose [type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`, containing all of the elements in this collection |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection.

If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.)

If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of this collection are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing all of the elements in this collection |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of any element in this collection is not assignable to the [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())of the specified array |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this collection |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val size: Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this collection |
