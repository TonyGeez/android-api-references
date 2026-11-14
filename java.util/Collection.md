# Collection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collection

```
interface Collection<E : Any!> : MutableIterable<E>
```

| [java.util.Collection](Collection.md) |

The root interface in the*collection hierarchy* . A collection represents a group of objects, known as its*elements* . Some collections allow duplicate elements and others do not. Some are ordered, and others are unordered. Collections that have a defined [encounter order](SequencedCollection.md) are generally subtypes of the [SequencedCollection](SequencedCollection.md) interface. The JDK does not provide any*direct* implementations of this interface: it provides implementations of more specific subinterfaces like`Set`and`List`. This interface is typically used to pass collections around and manipulate them where maximum generality is desired.

*Bags* or*multisets*(unordered collections that may contain duplicate elements) should implement this interface directly.

All general-purpose`Collection`implementation classes (which typically implement`Collection`indirectly through one of its subinterfaces) should provide two "standard" constructors: a void (no arguments) constructor, which creates an empty collection, and a constructor with a single argument of type`Collection`, which creates a new collection with the same elements as its argument. In effect, the latter constructor allows the user to copy any collection, producing an equivalent collection of the desired implementation type. There is no way to enforce this convention (as interfaces cannot contain constructors) but all of the general-purpose`Collection`implementations in the Java platform libraries comply.

Certain methods are specified to be*optional* . If a collection implementation doesn't implement a particular operation, it should define the corresponding method to throw`UnsupportedOperationException`. Such methods are marked "optional operation" in method specifications of the collections interfaces.

Some collection implementations have restrictions on the elements that they may contain. For example, some implementations prohibit null elements, and some have restrictions on the types of their elements. Attempting to add an ineligible element throws an unchecked exception, typically`NullPointerException`or`ClassCastException`. Attempting to query the presence of an ineligible element may throw an exception, or it may simply return false; some implementations will exhibit the former behavior and some will exhibit the latter. More generally, attempting an operation on an ineligible element whose completion would not result in the insertion of an ineligible element into the collection may throw an exception or it may succeed, at the option of the implementation. Such exceptions are marked as "optional" in the specification for this interface.

It is up to each collection to determine its own synchronization policy. In the absence of a stronger guarantee by the implementation, undefined behavior may result from the invocation of any method on a collection that is being mutated by another thread; this includes direct invocations, passing the collection to a method that might perform invocations, and using an existing iterator to examine the collection.

Many methods in Collections Framework interfaces are defined in terms of the [equals](../java.lang/Object.md))method. For example, the specification for the [contains(Object o)](Collection.md))method says: "returns`true`if and only if this collection contains at least one element`e`such that`(o==null ? e==null : o.equals(e))`." This specification should*not* be construed to imply that invoking`Collection.contains`with a non-null argument`o`will cause`o.equals(e)`to be invoked for any element`e`. Implementations are free to implement optimizations whereby the`equals`invocation is avoided, for example, by first comparing the hash codes of the two elements. (The [Object.hashCode()](../java.lang/Object.md))specification guarantees that two objects with unequal hash codes cannot be equal.) More generally, implementations of the various Collections Framework interfaces are free to take advantage of the specified behavior of underlying [Object](../java.lang/Object.md) methods wherever the implementor deems it appropriate.

Some collection operations which perform recursive traversal of the collection may fail with an exception for self-referential instances where the collection directly or indirectly contains itself. This includes the`clone()`,`equals()`,`hashCode()`and`toString()`methods. Implementations may optionally handle the self-referential scenario, however most current implementations do not do so.

## View Collections

Most collections manage storage for elements they contain. By contrast,*view collections* themselves do not store elements, but instead they rely on a backing collection to store the actual elements. Operations that are not handled by the view collection itself are delegated to the backing collection. Examples of view collections include the wrapper collections returned by methods such as [Collections.checkedCollection](Collections.md)), [Collections.synchronizedCollection](Collections.md)), and [Collections.unmodifiableCollection](Collections.md)). Other examples of view collections include collections that provide a different representation of the same elements, for example, as provided by [List.subList](List.md)), java.util.NavigableSet#subSet, [Map.entrySet](Map.md)), or [SequencedCollection.reversed](SequencedCollection.md)). Any changes made to the backing collection are visible in the view collection. Correspondingly, any changes made to the view collection --- if changes are permitted --- are written through to the backing collection. Although they technically aren't collections, instances of [Iterator](Iterator.md) and [ListIterator](ListIterator.md) can also allow modifications to be written through to the backing collection, and in some cases, modifications to the backing collection will be visible to the Iterator during iteration.

## Unmodifiable Collections

Certain methods of this interface are considered "destructive" and are called "mutator" methods in that they modify the group of objects contained within the collection on which they operate. They can be specified to throw`UnsupportedOperationException`if this collection implementation does not support the operation. Such methods should (but are not required to) throw an`UnsupportedOperationException`if the invocation would have no effect on the collection. For example, consider a collection that does not support the [add](Collection.md))operation. What will happen if the [addAll](Collection.md))method is invoked on this collection, with an empty collection as the argument? The addition of zero elements has no effect, so it is permissible for this collection simply to do nothing and not to throw an exception. However, it is recommended that such cases throw an exception unconditionally, as throwing only in certain cases can lead to programming errors.

An*unmodifiable collection* is a collection, all of whose mutator methods (as defined above) are specified to throw`UnsupportedOperationException`. Such a collection thus cannot be modified by calling any methods on it. For a collection to be properly unmodifiable, any view collections derived from it must also be unmodifiable. For example, if a List is unmodifiable, the List returned by [List.subList](List.md))is also unmodifiable.

An unmodifiable collection is not necessarily immutable. If the contained elements are mutable, the entire collection is clearly mutable, even though it might be unmodifiable. For example, consider two unmodifiable lists containing mutable elements. The result of calling`list1.equals(list2)`might differ from one call to the next if the elements had been mutated, even though both lists are unmodifiable. However, if an unmodifiable collection contains all immutable elements, it can be considered effectively immutable.

## Unmodifiable View Collections

An*unmodifiable view collection* is a collection that is unmodifiable and that is also a view onto a backing collection. Its mutator methods throw`UnsupportedOperationException`, as described above, while reading and querying methods are delegated to the backing collection. The effect is to provide read-only access to the backing collection. This is useful for a component to provide users with read access to an internal collection, while preventing them from modifying such collections unexpectedly. Examples of unmodifiable view collections are those returned by the [Collections.unmodifiableCollection](Collections.md)), [Collections.unmodifiableList](Collections.md)), and related methods.

Note that changes to the backing collection might still be possible, and if they occur, they are visible through the unmodifiable view. Thus, an unmodifiable view collection is not necessarily immutable. However, if the backing collection of an unmodifiable view is effectively immutable, or if the only reference to the backing collection is through an unmodifiable view, the view can be considered effectively immutable.

## Serializability of Collections

Serializability of collections is optional. As such, none of the collections interfaces are declared to implement the [java.io.Serializable](../java.io/Serializable.md) interface. However, serializability is regarded as being generally useful, so most collection implementations are serializable.

The collection implementations that are public classes (such as`ArrayList`or`HashMap`) are declared to implement the`Serializable`interface if they are in fact serializable. Some collections implementations are not public classes, such as the [unmodifiable collections.](Collection.md) In such cases, the serializability of such collections is described in the specification of the method that creates them, or in some other suitable place. In cases where the serializability of a collection is not specified, there is no guarantee about the serializability of such collections. In particular, many [view collections](Collection.md) are not serializable, even if the original collection is serializable.

A collection implementation that implements the`Serializable`interface cannot be guaranteed to be serializable. The reason is that in general, collections contain elements of other types, and it is not possible to determine statically whether instances of some element type are actually serializable. For example, consider a serializable`Collection<E>`, where`E`does not implement the`Serializable`interface. The collection may be serializable, if it contains only elements of some serializable subtype of`E`, or if it is empty. Collections are thus said to be*conditionally serializable,*as the serializability of the collection as a whole depends on whether the collection itself is serializable and on whether all contained elements are also serializable.

An additional case occurs with instances of [SortedSet](SortedSet.md) and [SortedMap](SortedMap.md). These collections can be created with a [Comparator](Comparator.md) that imposes an ordering on the set elements or map keys. Such a collection is serializable only if the provided`Comparator`is also serializable.

This interface is a member of the [Java Collections Framework](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/index.html).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](Collection.md))`(`e:` `E`)` Ensures that this collection contains the specified element (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](Collection.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Adds all of the elements in the specified collection to this collection (optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](Collection.md))`()` Removes all of the elements from this collection (optional operation). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](Collection.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns`true`if this collection contains the specified element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](Collection.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`)` Returns`true`if this collection contains all of the elements in the specified collection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Collection.md))`()` Returns`true`if this collection contains no elements. |
| --- | --- |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](Collection.md))`()` Returns an iterator over the elements in this collection. |
| open [Stream](../java.util.stream/Stream.md)\<E\> | [parallelStream](Collection.md))`()` Returns a possibly parallel`Stream`with this collection as its source. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](Collection.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes a single instance of the specified element from this collection, if it is present (optional operation). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](Collection.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`)` Removes all of this collection's elements that are also contained in the specified collection (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](Collection.md))`(`filter:` ` [Predicate](../java.util.function/Predicate.md)<in` `E>`)` Removes all of the elements of this collection that satisfy the given predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](Collection.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`)` Retains only the elements in this collection that are contained in the specified collection (optional operation). |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](Collection.md))`()` Returns the number of elements in this collection. |
| open [Spliterator](Spliterator.md)\<E\> | [spliterator](Collection.md))`()` Creates a [Spliterator](Spliterator.md) over the elements in this collection. |
| open [Stream](../java.util.stream/Stream.md)\<E\> | [stream](Collection.md))`()` Returns a sequential`Stream`with this collection as its source. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](Collection.md))`()` Returns an array containing all of the elements in this collection. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](Collection.md))`(`generator:` ` [IntFunction](../java.util.function/IntFunction.md)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>!>`)` Returns an array containing all of the elements in this collection, using the provided`generator`function to allocate the returned array. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](Collection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. |
| --- | --- |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(e: E): Boolean
```

Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.)

Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added.

If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns.

| Parameters ||
|-----|--------------------------------------------------------------|
| `e` | E:element whose presence in this collection is to be ensured |

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
abstract fun addAll(c: MutableCollection<out E>): Boolean
```

Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](SequencedCollection.md), processing of its elements generally occurs in that order.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:collection containing elements to be added to this collection |

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

- [#add(Object)](Collection.md)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clear(): Unit
```

Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(o: Any?): Boolean
```

Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element whose presence in this collection is to be tested |

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
abstract fun containsAll(c: MutableCollection<*>): Boolean
```

Returns`true`if this collection contains all of the elements in the specified collection.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:collection to be checked for containment in this collection |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection contains all of the elements in the specified collection |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this collection does not permit null elements (java.util.Collection#) or if the specified collection is null. |

**See Also**

- [#contains(Object)](Collection.md)) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
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

Returns an iterator over the elements in this collection. There are no guarantees concerning the order in which the elements are returned (unless this collection is an instance of some class that provides a guarantee).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an`Iterator`over the elements in this collection |

### parallelStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parallelStream(): Stream<E>
```

Returns a possibly parallel`Stream`with this collection as its source. It is allowable for this method to return a sequential stream.

This method should be overridden when the [spliterator()](Collection.md))method cannot return a spliterator that is`IMMUTABLE`,`CONCURRENT`, or*late-binding* . (See [spliterator()](Collection.md))for details.)

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Stream](../java.util.stream/Stream.md)<E> | a possibly parallel`Stream`over the elements in this collection |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(o: Any?): Boolean
```

Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to be removed from this collection, if present |

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
abstract fun removeAll(c: MutableCollection<*>): Boolean
```

Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:collection containing elements to be removed from this collection |

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

- [#remove(Object)](Collection.md))
- [#contains(Object)](Collection.md)) 

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

Removes all of the elements of this collection that satisfy the given predicate. Errors or runtime exceptions thrown during iteration or by the predicate are relayed to the caller.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java.util.function/Predicate.md)\<inE\>:a predicate which returns`true`for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun retainAll(c: MutableCollection<*>): Boolean
```

Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:collection containing elements to be retained in this collection |

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

- [#remove(Object)](Collection.md))
- [#contains(Object)](Collection.md)) 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Int
```

Returns the number of elements in this collection. If this collection contains more than`Integer.MAX_VALUE`elements, returns`Integer.MAX_VALUE`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this collection |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a [Spliterator](Spliterator.md) over the elements in this collection. Implementations should document characteristic values reported by the spliterator. Such characteristic values are not required to be reported if the spliterator reports [Spliterator.SIZED](Spliterator.md) and this collection contains no elements.

The default implementation should be overridden by subclasses that can return a more efficient spliterator. In order to preserve expected laziness behavior for the [stream()](Collection.md))and [parallelStream()](Collection.md))methods, spliterators should either have the characteristic of`IMMUTABLE`or`CONCURRENT`, or be* [late-binding](Spliterator.md)* . If none of these is practical, the overriding class should describe the spliterator's documented policy of binding and structural interference, and should override the [stream()](Collection.md))and [parallelStream()](Collection.md))methods to create streams using a`Supplier`of the spliterator, as in: 

```kotlin
<code>Stream&lt;E&gt; s = StreamSupport.stream(() -&gt; spliterator(), spliteratorCharacteristics)
  </code>
```

These requirements ensure that streams produced by the [stream()](Collection.md))and [parallelStream()](Collection.md))methods will reflect the contents of the collection as of initiation of the terminal stream operation.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Spliterator](Spliterator.md)<E> | a`Spliterator`over the elements in this collection |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stream(): Stream<E>
```

Returns a sequential`Stream`with this collection as its source.

This method should be overridden when the [spliterator()](Collection.md))method cannot return a spliterator that is`IMMUTABLE`,`CONCURRENT`, or*late-binding* . (See [spliterator()](Collection.md))for details.)

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Stream](../java.util.stream/Stream.md)<E> | a sequential`Stream`over the elements in this collection |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`.

The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array, whose [type](../java.lang/Class.md))is`Object`, containing all of the elements in this collection |

### toArray

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(generator: IntFunction<Array<T>!>): Array<T>
```

Returns an array containing all of the elements in this collection, using the provided`generator`function to allocate the returned array.

If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `generator` | [IntFunction](../java.util.function/IntFunction.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>!\>:a function which produces a new array of the desired type and the provided length |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing all of the elements in this collection |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of any element in this collection is not assignable to the [runtime component type](../java.lang/Class.md))of the generated array |
| `java.lang.NullPointerException` | if the generator function is null |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> toArray(a: Array<T>): Array<T>
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
| `java.lang.ArrayStoreException` | if the runtime type of any element in this collection is not assignable to the [runtime component type](../java.lang/Class.md))of the specified array |
| `java.lang.NullPointerException` | if the specified array is null |
