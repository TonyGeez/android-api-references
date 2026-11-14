# Vector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Vector

```
open class Vector<E : Any!> : AbstractList<E>, Cloneable, MutableList<E>, RandomAccess, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> |||
| | ↳ | [java.util.AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList)\<E\> ||
| | | ↳ | [java.util.Vector](https://developer.android.com/reference/kotlin/java/util/Vector#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) |-------------------------------------------------------------------------|-------------------------------------------------------------------------| | [Stack](https://developer.android.com/reference/kotlin/java/util/Stack) | The`Stack`class represents a last-in-first-out (LIFO) stack of objects. | |
| --- | --- | --- | --- | --- | --- | --- |

The`Vector`class implements a growable array of objects. Like an array, it contains components that can be accessed using an integer index. However, the size of a`Vector`can grow or shrink as needed to accommodate adding and removing items after the`Vector`has been created.

Each vector tries to optimize storage management by maintaining a`capacity`and a`capacityIncrement`. The`capacity`is always at least as large as the vector size; it is usually larger because as components are added to the vector, the vector's storage increases in chunks the size of`capacityIncrement`. An application can increase the capacity of a vector before inserting a large number of components; this reduces the amount of incremental reallocation.

The iterators returned by this class's #iterator() and [listIterator](https://developer.android.com/reference/kotlin/java/util/Vector#listIterator(kotlin.Int))methods are*fail-fast* : if the vector is structurally modified at any time after the iterator is created, in any way except through the iterator's own [remove](https://developer.android.com/reference/kotlin/java/util/ListIterator#remove())or [add](https://developer.android.com/reference/kotlin/java/util/ListIterator#add(java.util.ListIterator.E))methods, the iterator will throw a [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future. The [Enumerations](https://developer.android.com/reference/kotlin/java/util/Enumeration) returned by the [elements](https://developer.android.com/reference/kotlin/java/util/Vector#elements())method are*not*fail-fast; if the Vector is structurally modified at any time after the enumeration is created then the results of enumerating are undefined.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

As of the Java 2 platform v1.2, this class was retrofitted to implement the [List](https://developer.android.com/reference/kotlin/java/util/List) interface, making it a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework). Unlike the new collection implementations,`Vector`is synchronized. If a thread-safe implementation is not needed, it is recommended to use [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList) in place of`Vector`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Vector](https://developer.android.com/reference/kotlin/java/util/Vector#Vector())`()` Constructs an empty vector so that its internal data array has size`10`and its standard capacity increment is zero. |
| [Vector](https://developer.android.com/reference/kotlin/java/util/Vector#Vector(kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an empty vector with the specified initial capacity and with its capacity increment equal to zero. |
| [Vector](https://developer.android.com/reference/kotlin/java/util/Vector#Vector(kotlin.Int,%20kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `capacityIncrement:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an empty vector with the specified initial capacity and capacity increment. |
| [Vector](https://developer.android.com/reference/kotlin/java/util/Vector#Vector(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Constructs a vector containing the elements of the specified collection, in the order they are returned by the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/Vector#add(java.util.Vector.E))`(`element:` `E`)` Appends the specified element to the end of this Vector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/Vector#add(kotlin.Int,%20java.util.Vector.E))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Inserts the specified element at the specified position in this Vector. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/Vector#addAll(kotlin.Int,%20kotlin.collections.Collection))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Inserts all of the elements in the specified Collection into this Vector at the specified position. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/Vector#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Appends all of the elements in the specified Collection to the end of this Vector, in the order that they are returned by the specified Collection's Iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addElement](https://developer.android.com/reference/kotlin/java/util/Vector#addElement(java.util.Vector.E))`(`obj:` `E`)` Adds the specified component to the end of this vector, increasing its size by one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacity](https://developer.android.com/reference/kotlin/java/util/Vector#capacity())`()` Returns the current capacity of this vector. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/Vector#clear())`()` Removes all of the elements from this Vector. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/Vector#clone())`()` Returns a clone of this vector. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/Vector#contains(java.util.Vector.E))`(`element:` `E?`)` Returns`true`if this vector contains the specified element. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/Vector#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Returns true if this Vector contains all of the elements in the specified Collection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyInto](https://developer.android.com/reference/kotlin/java/util/Vector#copyInto(kotlin.Array))`(`anArray:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>`)` Copies the components of this vector into the specified array. |
| openE | [elementAt](https://developer.android.com/reference/kotlin/java/util/Vector#elementAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the component at the specified index. |
| --- | --- |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<E\> | [elements](https://developer.android.com/reference/kotlin/java/util/Vector#elements())`()` Returns an enumeration of the components of this vector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ensureCapacity](https://developer.android.com/reference/kotlin/java/util/Vector#ensureCapacity(kotlin.Int))`(`minCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increases the capacity of this vector, if necessary, to ensure that it can hold at least the number of components specified by the minimum capacity argument. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/Vector#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified Object with this Vector for equality. |
| --- | --- |
| openE | [firstElement](https://developer.android.com/reference/kotlin/java/util/Vector#firstElement())`()` Returns the first component (the item at index`0`) of this vector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/Vector#forEach(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `E>`)` <br /> |
| openE | [get](https://developer.android.com/reference/kotlin/java/util/Vector#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the element at the specified position in this Vector. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/Vector#hashCode())`()` Returns the hash code value for this Vector. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](https://developer.android.com/reference/kotlin/java/util/Vector#indexOf(kotlin.Any,%20kotlin.Int))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the first occurrence of the specified element in this vector, searching forwards from`index`, or returns -1 if the element is not found. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](https://developer.android.com/reference/kotlin/java/util/Vector#indexOf(java.util.Vector.E))`(`element:` `E?`)` Returns the index of the first occurrence of the specified element in this vector, or -1 if this vector does not contain the element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [insertElementAt](https://developer.android.com/reference/kotlin/java/util/Vector#insertElementAt(java.util.Vector.E,%20kotlin.Int))`(`obj:` `E`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inserts the specified object as a component in this vector at the specified`index`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/Vector#isEmpty())`()` Tests if this vector has no components. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/Vector#iterator())`()` Returns an iterator over the elements in this list in proper sequence. |
| --- | --- |
| openE | [lastElement](https://developer.android.com/reference/kotlin/java/util/Vector#lastElement())`()` Returns the last component of the vector. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](https://developer.android.com/reference/kotlin/java/util/Vector#lastIndexOf(kotlin.Any,%20kotlin.Int))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the last occurrence of the specified element in this vector, searching backwards from`index`, or returns -1 if the element is not found. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](https://developer.android.com/reference/kotlin/java/util/Vector#lastIndexOf(java.util.Vector.E))`(`element:` `E?`)` Returns the index of the last occurrence of the specified element in this vector, or -1 if this vector does not contain the element. |
| --- | --- |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](https://developer.android.com/reference/kotlin/java/util/Vector#listIterator())`()` Returns a list iterator over the elements in this list (in proper sequence). |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](https://developer.android.com/reference/kotlin/java/util/Vector#listIterator(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/Vector#remove(java.util.Vector.E))`(`element:` `E?`)` Removes the first occurrence of the specified element in this Vector If the Vector does not contain the element, it is unchanged. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/Vector#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Removes from this Vector all of its elements that are contained in the specified Collection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllElements](https://developer.android.com/reference/kotlin/java/util/Vector#removeAllElements())`()` Removes all components from this vector and sets its size to zero. |
| openE | [removeAt](https://developer.android.com/reference/kotlin/java/util/Vector#removeAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes the element at the specified position in this Vector. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeElement](https://developer.android.com/reference/kotlin/java/util/Vector#removeElement(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the first (lowest-indexed) occurrence of the argument from this vector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeElementAt](https://developer.android.com/reference/kotlin/java/util/Vector#removeElementAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Deletes the component at the specified index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](https://developer.android.com/reference/kotlin/java/util/Vector#removeIf(java.util.function.Predicate))`(`filter:` ` [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate)<in` `E>`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/Vector#replaceAll(java.util.function.UnaryOperator))`(`operator:` ` [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator)<E>`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/Vector#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Retains only the elements in this Vector that are contained in the specified Collection. |
| openE | [set](https://developer.android.com/reference/kotlin/java/util/Vector#set(kotlin.Int,%20java.util.Vector.E))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Replaces the element at the specified position in this Vector with the specified element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementAt](https://developer.android.com/reference/kotlin/java/util/Vector#setElementAt(java.util.Vector.E,%20kotlin.Int))`(`obj:` `E`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the component at the specified`index`of this vector to be the specified object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSize](https://developer.android.com/reference/kotlin/java/util/Vector#setSize(kotlin.Int))`(`newSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the size of this vector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](https://developer.android.com/reference/kotlin/java/util/Vector#sort(java.util.Comparator))`(`c:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `E>?`)` <br /> |
| --- | --- |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)\<E\> | [spliterator](https://developer.android.com/reference/kotlin/java/util/Vector#spliterator())`()` Creates a* [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and*fail-fast* [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) over the elements in this list. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | [subList](https://developer.android.com/reference/kotlin/java/util/Vector#subList(kotlin.Int,%20kotlin.Int))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a view of the portion of this List between fromIndex, inclusive, and toIndex, exclusive. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](https://developer.android.com/reference/kotlin/java/util/Vector#toArray())`()` Returns an array containing all of the elements in this Vector in the correct order. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](https://developer.android.com/reference/kotlin/java/util/Vector#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this Vector in the correct order; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/Vector#toString())`()` Returns a string representation of this Vector, containing the String representation of each element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trimToSize](https://developer.android.com/reference/kotlin/java/util/Vector#trimToSize())`()` Trims the capacity of this vector to be the vector's current size. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeRange](https://developer.android.com/reference/kotlin/java/util/Vector#removeRange(kotlin.Int,%20kotlin.Int))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty())`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray())`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [capacityIncrement](https://developer.android.com/reference/kotlin/java/util/Vector#capacityIncrement:kotlin.Int) The amount by which the capacity of the vector is automatically incremented when its size becomes greater than its capacity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [elementCount](https://developer.android.com/reference/kotlin/java/util/Vector#elementCount:kotlin.Int) The number of valid components in this`Vector`object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [elementData](https://developer.android.com/reference/kotlin/java/util/Vector#elementData:kotlin.Array) The array buffer into which the components of the vector are stored. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/Vector#size:kotlin.Int) Returns the number of components in this vector. |

| Inherited properties ||
|---|---|
| From class [AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [modCount](https://developer.android.com/reference/kotlin/java/util/AbstractList#modCount:kotlin.Int) <br /> The number of times this list has been*structurally modified*. Structural modifications are those that change the size of the list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results. This field is used by the iterator and list iterator implementation returned by the`iterator`and`listIterator`methods. If the value of this field changes unexpectedly, the iterator (or list iterator) will throw a`ConcurrentModificationException`in response to the`next`,`remove`,`previous`,`set`or`add`operations. This provides*fail-fast*behavior, rather than non-deterministic behavior in the face of concurrent modification during iteration. **Use of this field by subclasses is optional.** If a subclass wishes to provide fail-fast iterators (and list iterators), then it merely has to increment this field in its`add(int, E)`and`remove(int)`methods (and any other methods that it overrides that result in structural modifications to the list). A single call to`add(int, E)`or`remove(int)`must add no more than one to this field, or the iterators (and list iterators) will throw bogus`ConcurrentModificationExceptions`. If an implementation does not wish to provide fail-fast iterators, this field may be ignored. <br /> | ||
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int) <br /> | ||

## Public constructors

### Vector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Vector()
```

Constructs an empty vector so that its internal data array has size`10`and its standard capacity increment is zero. 

### Vector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Vector(initialCapacity: Int)
```

Constructs an empty vector with the specified initial capacity and with its capacity increment equal to zero.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the vector |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified initial capacity is negative |

### Vector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Vector(
    initialCapacity: Int, 
    capacityIncrement: Int)
```

Constructs an empty vector with the specified initial capacity and capacity increment.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the vector |
| `capacityIncrement` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the capacity is increased when the vector overflows |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified initial capacity is negative |

### Vector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Vector(c: MutableCollection<out E>)
```

Constructs a vector containing the elements of the specified collection, in the order they are returned by the collection's iterator.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:the collection whose elements are to be placed into this vector |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Appends the specified element to the end of this Vector.

| Parameters ||
|-----|---------------------------------------|
| `e` | element to be appended to this Vector |

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

Inserts the specified element at the specified position in this Vector. Shifts the element currently at that position (if any) and any subsequent elements to the right (adds one to their indices).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which the specified element is to be inserted |
| `element` | E:element to be inserted |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| --- | --- | --- | --- |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(
    index: Int, 
    elements: Collection<E>
): Boolean
```

Inserts all of the elements in the specified Collection into this Vector at the specified position. Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in the Vector in the order that they are returned by the specified Collection's iterator.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which to insert the first element from the specified collection |
| `c` | elements to be inserted into this Vector |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this Vector changed as a result of the call |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| --- | --- | --- | --- |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified Collection to the end of this Vector, in the order that they are returned by the specified Collection's Iterator. The behavior of this operation is undefined if the specified Collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified Collection is this Vector, and this Vector is nonempty.)

| Parameters ||
|-----|------------------------------------------|
| `c` | elements to be inserted into this Vector |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this Vector changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

### addElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addElement(obj: E): Unit
```

Adds the specified component to the end of this vector, increasing its size by one. The capacity of this vector is increased if its size becomes greater than its capacity.

This method is identical in functionality to the #add(java.lang.Object) method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface).

| Parameters ||
|-------|-----------------------------|
| `obj` | E:the component to be added |

### capacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun capacity(): Int
```

Returns the current capacity of this vector.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current capacity (the length of its internal data array, kept in the field`elementData`of this vector) |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this Vector. The Vector will be empty after this call returns (unless it throws an exception).

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this list |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a clone of this vector. The copy will contain a reference to a clone of the internal data array, not a reference to the original internal data array of this`Vector`object.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this vector |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Returns`true`if this vector contains the specified element. More formally, returns`true`if and only if this vector contains at least one element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|-------------------------------------------------------|
| `o` | element whose presence in this vector is to be tested |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this vector contains the specified element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsAll(elements: Collection<E>): Boolean
```

Returns true if this Vector contains all of the elements in the specified Collection.

| Parameters ||
|-----|---------------------------------------------------------------------------|
| `c` | a collection whose elements will be tested for containment in this Vector |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Vector contains all of the elements in the specified collection |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified collection is null |

### copyInto

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun copyInto(anArray: Array<Any!>): Unit
```

Copies the components of this vector into the specified array. The item at index`k`in this vector is copied into component`k`of`anArray`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `anArray` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>:the array into which the components get copied |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given array is null |
| `java.lang.IndexOutOfBoundsException` | if the specified array is not large enough to hold all the components of this vector |
| `java.lang.ArrayStoreException` | if a component of this vector is not of a runtime type that can be stored in the specified array |
| --- | --- |

**See Also**

### elementAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elementAt(index: Int): E
```

Returns the component at the specified index.

This method is identical in functionality to the [get(int)](https://developer.android.com/reference/kotlin/java/util/Vector#get(kotlin.Int))method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index into this vector |

| Return ||
|---|--------------------------------------|
| E | the component at the specified index |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elements(): Enumeration<E>
```

Returns an enumeration of the components of this vector. The returned`Enumeration`object will generate all items in this vector. The first item generated is the item at index`0`, then the item at index`1`, and so on. If the vector is structurally modified while enumerating over the elements then the results of enumerating are undefined.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<E> | an enumeration of the components of this vector |

**See Also**

- [java.util.Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator) 

### ensureCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ensureCapacity(minCapacity: Int): Unit
```

Increases the capacity of this vector, if necessary, to ensure that it can hold at least the number of components specified by the minimum capacity argument.

If the current capacity of this vector is less than`minCapacity`, then its capacity is increased by replacing its internal data array, kept in the field`elementData`, with a larger one. The size of the new data array will be the old size plus`capacityIncrement`, unless the value of`capacityIncrement`is less than or equal to zero, in which case the new capacity will be twice the old capacity; but if this new size is still smaller than`minCapacity`, then the new capacity will be`minCapacity`.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `minCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the desired minimum capacity |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified Object with this Vector for equality. Returns true if and only if the specified Object is also a List, both Lists have the same size, and all corresponding pairs of elements in the two Lists are*equal* . (Two elements`e1`and`e2`are*equal* if`Objects.equals(e1, e2)`.) In other words, two Lists are defined to be equal if they contain the same elements in the same order.

| Parameters ||
|-------|---------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the Object to be compared for equality with this Vector |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified Object is equal to this Vector |

### firstElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun firstElement(): E
```

Returns the first component (the item at index`0`) of this vector.

| Return ||
|---|------------------------------------|
| E | the first component of this vector |

| Exceptions ||
|------------------------------------|----------------------------------|
| `java.util.NoSuchElementException` | if this vector has no components |

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

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): E
```

Returns the element at the specified position in this Vector.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to return |

| Return ||
|---|-------------------------------|
| E | object at the specified index |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this Vector.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this list |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun indexOf(
    o: Any?, 
    index: Int
): Int
```

Returns the index of the first occurrence of the specified element in this vector, searching forwards from`index`, or returns -1 if the element is not found. More formally, returns the lowest index`i`such that`(i >= index && Objects.equals(o, get(i)))`, or -1 if there is no such index.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to search for |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index to start searching from |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first occurrence of the element in this vector at position`index`or later in the vector;`-1`if the element is not found. |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

**See Also**

- [java.lang.Object#equals(Object)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)) 

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun indexOf(element: E?): Int
```

Returns the index of the first occurrence of the specified element in this vector, or -1 if this vector does not contain the element. More formally, returns the lowest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first occurrence of the specified element in this vector, or -1 if this vector does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### insertElementAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun insertElementAt(
    obj: E, 
    index: Int
): Unit
```

Inserts the specified object as a component in this vector at the specified`index`. Each component in this vector with an index greater or equal to the specified`index`is shifted upward to have an index one greater than the value it had previously.

The index must be a value greater than or equal to`0`and less than or equal to the current size of the vector. (If the index is equal to the current size of the vector, the new element is appended to the Vector.)

This method is identical in functionality to the [add(int, E)](https://developer.android.com/reference/kotlin/java/util/Vector#add(kotlin.Int,%20java.util.Vector.E))method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface). Note that the`add`method reverses the order of the parameters, to more closely match array usage.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `obj` | E:the component to insert |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):where to insert the new component |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Tests if this vector has no components.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if this vector has no components, that is, its size is zero;`false`otherwise. |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list in proper sequence.

The returned iterator is [*fail-fast*](https://developer.android.com/reference/kotlin/java/util/Vector#fail-fast).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this list in proper sequence |

### lastElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastElement(): E
```

Returns the last component of the vector.

| Return ||
|---|----------------------------------------------------------------------------|
| E | the last component of the vector, i.e., the component at index`size() - 1` |

| Exceptions ||
|------------------------------------|-------------------------|
| `java.util.NoSuchElementException` | if this vector is empty |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastIndexOf(
    o: Any?, 
    index: Int
): Int
```

Returns the index of the last occurrence of the specified element in this vector, searching backwards from`index`, or returns -1 if the element is not found. More formally, returns the highest index`i`such that`(i <= index && Objects.equals(o, get(i)))`, or -1 if there is no such index.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:element to search for |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index to start searching backwards from |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the last occurrence of the element at position less than or equal to`index`in this vector; -1 if the element is not found. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is greater than or equal to the current size of this vector |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastIndexOf(element: E?): Int
```

Returns the index of the last occurrence of the specified element in this vector, or -1 if this vector does not contain the element. More formally, returns the highest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the last occurrence of the specified element in this vector, or -1 if this vector does not contain the element |

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

The returned list iterator is [*fail-fast*](https://developer.android.com/reference/kotlin/java/util/Vector#fail-fast).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence) |

**See Also**

- [#listIterator(int)](https://developer.android.com/reference/kotlin/java/util/Vector#listIterator(kotlin.Int)) 

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. The specified index indicates the first element that would be returned by an initial call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next()). An initial call to [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())would return the element with the specified index minus one.

The returned list iterator is [*fail-fast*](https://developer.android.com/reference/kotlin/java/util/Vector#fail-fast).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first element to be returned from the list iterator (by a call to [next](https://developer.android.com/reference/kotlin/java/util/ListIterator#next())) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element in this Vector If the Vector does not contain the element, it is unchanged. More formally, removes the element with the lowest index i such that`Objects.equals(o, get(i))`(if such an element exists).

| Parameters ||
|-----|----------------------------------------------------|
| `o` | element to be removed from this Vector, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the Vector contained the specified element |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes from this Vector all of its elements that are contained in the specified Collection.

| Parameters ||
|-----|--------------------------------------------------------|
| `c` | a collection of elements to be removed from the Vector |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Vector changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the types of one or more elements in this vector are incompatible with the specified collection ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if this vector contains one or more null elements and the specified collection does not support null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |
| --- | --- |

### removeAllElements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAllElements(): Unit
```

Removes all components from this vector and sets its size to zero.

This method is identical in functionality to the #clear method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface). 

### removeAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAt(index: Int): E
```

Removes the element at the specified position in this Vector. Shifts any subsequent elements to the left (subtracts one from their indices). Returns the element that was removed from the Vector.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the element to be removed |

| Return ||
|---|--------------------------|
| E | element that was removed |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| --- | --- | --- | --- |

### removeElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeElement(obj: Any?): Boolean
```

Removes the first (lowest-indexed) occurrence of the argument from this vector. If the object is found in this vector, each component in the vector with an index greater or equal to the object's index is shifted downward to have an index one smaller than the value it had previously.

This method is identical in functionality to the #remove(java.lang.Object) method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the component to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the argument was a component of this vector;`false`otherwise. |

### removeElementAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeElementAt(index: Int): Unit
```

Deletes the component at the specified index. Each component in this vector with an index greater or equal to the specified`index`is shifted downward to have an index one smaller than the value it had previously. The size of this vector is decreased by`1`.

The index must be a value greater than or equal to`0`and less than the current size of the vector.

This method is identical in functionality to the [remove(int)](https://developer.android.com/reference/kotlin/java/util/Vector#removeAt(kotlin.Int))method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface). Note that the`remove`method returns the old value that was stored at the specified position.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the object to remove |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

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

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(operator: UnaryOperator<E>): Unit
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `operator` | [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator)\<E\>:the operator to apply to each element |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this list is unmodifiable. Implementations may throw this exception if an element cannot be replaced or if, in general, modification is not supported |
| `java.lang.NullPointerException` | if the specified operator is null or if the operator result is a null value and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this Vector that are contained in the specified Collection. In other words, removes from this Vector all of its elements that are not contained in the specified Collection.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------|
| `c` | a collection of elements to be retained in this Vector (all other elements are removed) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Vector changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the types of one or more elements in this vector are incompatible with the specified collection ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if this vector contains one or more null elements and the specified collection does not support null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |
| --- | --- |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    index: Int, 
    element: E
): E
```

Replaces the element at the specified position in this Vector with the specified element.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to replace |
| `element` | E:element to be stored at the specified position |

| Return ||
|---|--------------------------------------------------|
| E | the element previously at the specified position |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| --- | --- | --- | --- |

### setElementAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setElementAt(
    obj: E, 
    index: Int
): Unit
```

Sets the component at the specified`index`of this vector to be the specified object. The previous component at that position is discarded.

The index must be a value greater than or equal to`0`and less than the current size of the vector.

This method is identical in functionality to the [set(int, E)](https://developer.android.com/reference/kotlin/java/util/Vector#set(kotlin.Int,%20java.util.Vector.E))method (which is part of the [List](https://developer.android.com/reference/kotlin/java/util/List) interface). Note that the`set`method reverses the order of the parameters, to more closely match array usage. Note also that the`set`method returns the old value that was stored at the specified position.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `obj` | E:what the component is to be set to |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the specified index |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### setSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSize(newSize: Int): Unit
```

Sets the size of this vector. If the new size is greater than the current size, new`null`items are added to the end of the vector. If the new size is less than the current size, all components at index`newSize`and greater are discarded.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------|
| `newSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new size of this vector |

| Exceptions ||
|--------------------------------------------|-----------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the new size is negative |

### sort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sort(c: Comparator<in E>?): Unit
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inE\>?:the`Comparator`used to compare list elements. A`null`value indicates that the elements' [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) should be used |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*using the specified comparator |
| `java.lang.UnsupportedOperationException` | if the list's list-iterator does not support the`set`operation |
| `java.lang.IllegalArgumentException` | ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) if the comparator is found to violate the [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator) contract |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and*fail-fast* [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) over the elements in this list.

The`Spliterator`reports [Spliterator.SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), [Spliterator.SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int), and [Spliterator.ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int). Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)<E> | a`Spliterator`over the elements in this list |

### subList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subList(
    fromIndex: Int, 
    toIndex: Int
): MutableList<E>
```

Returns a view of the portion of this List between fromIndex, inclusive, and toIndex, exclusive. (If fromIndex and toIndex are equal, the returned List is empty.) The returned List is backed by this List, so changes in the returned List are reflected in this List, and vice-versa. The returned List supports all of the optional List operations supported by this List.

This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a List can be used as a range operation by operating on a subList view instead of a whole List. For example, the following idiom removes a range of elements from a List: 

```kotlin
list.subList(from, to).clear();
  
```
Similar idioms may be constructed for indexOf and lastIndexOf, and all of the algorithms in the Collections class can be applied to a subList.

The semantics of the List returned by this method become undefined if the backing list (i.e., this List) is*structurally modified*in any way other than via the returned List. (Structural modifications are those that change the size of the List, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):low endpoint (inclusive) of the subList |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):high endpoint (exclusive) of the subList |

| Return ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E> | a view of the specified range within this List |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if an endpoint index value is out of range`(fromIndex < 0 || toIndex > size)` |
| `java.lang.IllegalArgumentException` | if the endpoint indices are out of order`(fromIndex > toIndex)` |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this Vector in the correct order.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all of the elements in this list in proper sequence |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this Vector in the correct order; the runtime type of the returned array is that of the specified array. If the Vector fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this Vector.

If the Vector fits in the specified array with room to spare (i.e., the array has more elements than the Vector), the element in the array immediately following the end of the Vector is set to null. (This is useful in determining the length of the Vector*only*if the caller knows that the Vector does not contain any null elements.)

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | type of array elements. The same type as`<E>`or a supertype of`<E>`. |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of the Vector are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing the elements of the Vector |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of a,`<T>`, is not a supertype of the runtime type,`<E>`, of every element in this Vector |
| `java.lang.NullPointerException` | if the given array is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this Vector, containing the String representation of each element.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### trimToSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trimToSize(): Unit
```

Trims the capacity of this vector to be the vector's current size. If the capacity of this vector is larger than its current size, then the capacity is changed to equal the size by replacing its internal data array, kept in the field`elementData`, with a smaller one. An application can use this operation to minimize the storage of a vector.

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

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of first element to be removed |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after last element to be removed |

## Properties

### capacityIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var capacityIncrement: Int
```

The amount by which the capacity of the vector is automatically incremented when its size becomes greater than its capacity. If the capacity increment is less than or equal to zero, the capacity of the vector is doubled each time it needs to grow. 

### elementCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var elementCount: Int
```

The number of valid components in this`Vector`object. Components`elementData[0]`through`elementData[elementCount-1]`are the actual items. 

### elementData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var elementData: Array<Any!>
```

The array buffer into which the components of the vector are stored. The capacity of the vector is the length of this array buffer, and is at least large enough to contain all the vector's elements.

Any array elements following the last element in the Vector are null. 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of components in this vector.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of components in this vector |
