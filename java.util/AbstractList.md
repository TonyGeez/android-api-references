# AbstractList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractList

```
abstract class AbstractList<E : Any!> : AbstractCollection<E>, MutableList<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> ||
| | ↳ | [java.util.AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList#) |

| Known Direct Subclasses [AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList), [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList), [Vector](https://developer.android.com/reference/kotlin/java/util/Vector) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList) | This class provides a skeletal implementation of the`List`interface to minimize the effort required to implement this interface backed by a "sequential access" data store (such as a linked list). | | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList) | Resizable-array implementation of the`List`interface. | | [Vector](https://developer.android.com/reference/kotlin/java/util/Vector) | The`Vector`class implements a growable array of objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList), [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) | The`Stack`class represents a last-in-first-out (LIFO) stack of objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class provides a skeletal implementation of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface to minimize the effort required to implement this interface backed by a "random access" data store (such as an array). For sequential access data (such as a linked list), [AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList) should be used in preference to this class.

To implement an unmodifiable list, the programmer needs only to extend this class and provide implementations for the [get(int)](https://developer.android.com/reference/kotlin/java/util/AbstractList#get(kotlin.Int))and [size()](https://developer.android.com/reference/kotlin/java/util/List#size:kotlin.Int) methods.

To implement a modifiable list, the programmer must additionally override the [set(int, E)](https://developer.android.com/reference/kotlin/java/util/AbstractList#set(kotlin.Int,%20java.util.AbstractList.E))method (which otherwise throws an`UnsupportedOperationException`). If the list is variable-size the programmer must additionally override the [add(int, E)](https://developer.android.com/reference/kotlin/java/util/AbstractList#add(kotlin.Int,%20java.util.AbstractList.E))and [remove(int)](https://developer.android.com/reference/kotlin/java/util/AbstractList#removeAt(kotlin.Int))methods.

The programmer should generally provide a void (no argument) and collection constructor, as per the recommendation in the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) interface specification.

Unlike the other abstract collection implementations, the programmer does*not* have to provide an iterator implementation; the iterator and list iterator are implemented by this class, on top of the "random access" methods: [get(int)](https://developer.android.com/reference/kotlin/java/util/AbstractList#get(kotlin.Int)), [set(int, E)](https://developer.android.com/reference/kotlin/java/util/AbstractList#set(kotlin.Int,%20java.util.AbstractList.E)), [add(int, E)](https://developer.android.com/reference/kotlin/java/util/AbstractList#add(kotlin.Int,%20java.util.AbstractList.E))and [remove(int)](https://developer.android.com/reference/kotlin/java/util/AbstractList#removeAt(kotlin.Int)).

The documentation for each non-abstract method in this class describes its implementation in detail. Each of these methods may be overridden if the collection being implemented admits a more efficient implementation.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList#AbstractList())`()` Sole constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/AbstractList#add(java.util.AbstractList.E))`(`element:` `E`)` Appends the specified element to the end of this list (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/AbstractList#add(kotlin.Int,%20java.util.AbstractList.E))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Inserts the specified element at the specified position in this list (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractList#addAll(kotlin.Int,%20kotlin.collections.Collection))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Inserts all of the elements in the specified collection into this list at the specified position (optional operation). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/AbstractList#clear())`()` Removes all of the elements from this list (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/AbstractList#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this list for equality. |
| abstractE | [get](https://developer.android.com/reference/kotlin/java/util/AbstractList#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the element at the specified position in this list. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/AbstractList#hashCode())`()` Returns the hash code value for this list. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](https://developer.android.com/reference/kotlin/java/util/AbstractList#indexOf(java.util.AbstractList.E))`(`element:` `E?`)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/AbstractList#iterator())`()` Returns an iterator over the elements in this list in proper sequence. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](https://developer.android.com/reference/kotlin/java/util/AbstractList#lastIndexOf(java.util.AbstractList.E))`(`element:` `E?`)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](https://developer.android.com/reference/kotlin/java/util/AbstractList#listIterator())`()` Returns a list iterator over the elements in this list (in proper sequence). |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](https://developer.android.com/reference/kotlin/java/util/AbstractList#listIterator(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. |
| --- | --- |
| openE | [removeAt](https://developer.android.com/reference/kotlin/java/util/AbstractList#removeAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes the element at the specified position in this list (optional operation). |
| openE | [set](https://developer.android.com/reference/kotlin/java/util/AbstractList#set(kotlin.Int,%20java.util.AbstractList.E))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Replaces the element at the specified position in this list with the specified element (optional operation). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | [subList](https://developer.android.com/reference/kotlin/java/util/AbstractList#subList(kotlin.Int,%20kotlin.Int))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a view of the portion of this list between the specified`fromIndex`, inclusive, and`toIndex`, exclusive. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeRange](https://developer.android.com/reference/kotlin/java/util/AbstractList#removeRange(kotlin.Int,%20kotlin.Int))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty())`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray())`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||

| Properties ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [modCount](https://developer.android.com/reference/kotlin/java/util/AbstractList#modCount:kotlin.Int) The number of times this list has been*structurally modified*. |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int) <br /> | ||

## Protected constructors

### AbstractList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractList()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Appends the specified element to the end of this list (optional operation).

Lists that support this operation may place limitations on what elements may be added to this list. In particular, some lists will refuse to add null elements, and others will impose restrictions on the type of elements that may be added. List classes should clearly specify in their documentation any restrictions on what elements may be added.

| Parameters ||
|-----|-------------------------------------|
| `e` | element to be appended to this list |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this list |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    index: Int, 
    element: E
): Unit
```

Inserts the specified element at the specified position in this list (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (adds one to their indices).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which the specified element is to be inserted |
| `element` | E:element to be inserted |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(
    index: Int, 
    elements: Collection<E>
): Boolean
```

Inserts all of the elements in the specified collection into this list at the specified position (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in this list in the order that they are returned by the specified collection's iterator. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (Note that this will occur if the specified collection is this list, and it's nonempty.)

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which to insert the first element from the specified collection |
| `c` | collection containing elements to be added to this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this list (optional operation). The list will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this list |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this list for equality. Returns`true`if and only if the specified object is also a list, both lists have the same size, and all corresponding pairs of elements in the two lists are*equal* . (Two elements`e1`and`e2`are*equal* if`(e1==null ? e2==null : e1.equals(e2))`.) In other words, two lists are defined to be equal if they contain the same elements in the same order.

| Parameters ||
|-------|-------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared for equality with this list |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this list |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(index: Int): E
```

Returns the element at the specified position in this list.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to return |

| Return ||
|---|----------------------------------------------------|
| E | the element at the specified position in this list |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this list.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this list |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun indexOf(element: E?): Int
```

Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list in proper sequence.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this list in proper sequence |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastIndexOf(element: E?): Int
```

Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun listIterator(): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence) |

**See Also**

- [#listIterator(int)](https://developer.android.com/reference/kotlin/java/util/AbstractList#listIterator(kotlin.Int)) 

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. The specified index indicates the first element that would be returned by an initial call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next()). An initial call to [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())would return the element with the specified index minus one.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first element to be returned from the list iterator (by a call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### removeAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAt(index: Int): E
```

Removes the element at the specified position in this list (optional operation). Shifts any subsequent elements to the left (subtracts one from their indices). Returns the element that was removed from the list.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the element to be removed |

| Return ||
|---|--------------------------------------------------|
| E | the element previously at the specified position |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    index: Int, 
    element: E
): E
```

Replaces the element at the specified position in this list with the specified element (optional operation).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to replace |
| `element` | E:element to be stored at the specified position |

| Return ||
|---|--------------------------------------------------|
| E | the element previously at the specified position |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### subList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subList(
    fromIndex: Int, 
    toIndex: Int
): MutableList<E>
```

Returns a view of the portion of this list between the specified`fromIndex`, inclusive, and`toIndex`, exclusive. (If`fromIndex``toIndex`are equal, the returned list is empty.) The returned list is backed by this list, so non-structural changes in the returned list are reflected in this list, and vice-versa. The returned list supports all of the optional list operations supported by this list.

This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a list can be used as a range operation by passing a subList view instead of a whole list. For example, the following idiom removes a range of elements from a list: 

```kotlin
<code>list.subList(from, to).clear();
  </code>
```
Similar idioms may be constructed for`indexOf`and`lastIndexOf`, and all of the algorithms in the`Collections`class can be applied to a subList.

The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is*structurally modified*in any way other than via the returned list. (Structural modifications are those that change the size of this list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):low endpoint (inclusive) of the subList |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):high endpoint (exclusive) of the subList |

| Return ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E> | a view of the specified range within this list |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if an endpoint index value is out of range`(fromIndex < 0 || toIndex > size)` |
| `java.lang.IllegalArgumentException` | if the endpoint indices are out of order`(fromIndex > toIndex)` |

## Protected methods

### removeRange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun removeRange(
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. Shifts any succeeding elements to the left (reduces their index). This call shortens the list by`(toIndex - fromIndex)`elements. (If`toIndex==fromIndex`, this operation has no effect.)

This method is called by the`clear`operation on this list and its subLists. Overriding this method to take advantage of the internals of the list implementation can*substantially* improve the performance of the`clear`operation on this list and its subLists.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of first element to be removed |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after last element to be removed |

## Properties

### modCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var modCount: Int
```

The number of times this list has been*structurally modified*. Structural modifications are those that change the size of the list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.

This field is used by the iterator and list iterator implementation returned by the`iterator`and`listIterator`methods. If the value of this field changes unexpectedly, the iterator (or list iterator) will throw a`ConcurrentModificationException`in response to the`next`,`remove`,`previous`,`set`or`add`operations. This provides*fail-fast*behavior, rather than non-deterministic behavior in the face of concurrent modification during iteration.

**Use of this field by subclasses is optional.** If a subclass wishes to provide fail-fast iterators (and list iterators), then it merely has to increment this field in its`add(int, E)`and`remove(int)`methods (and any other methods that it overrides that result in structural modifications to the list). A single call to`add(int, E)`or`remove(int)`must add no more than one to this field, or the iterators (and list iterators) will throw bogus`ConcurrentModificationExceptions`. If an implementation does not wish to provide fail-fast iterators, this field may be ignored.
