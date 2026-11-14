Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSet

```
abstract class AbstractSet<E : Any!> : AbstractCollection<E>, MutableSet<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> ||
| | ↳ | [java.util.AbstractSet](https://developer.android.com/reference/kotlin/java/util/AbstractSet#) |

| Known Direct Subclasses [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet), [CopyOnWriteArraySet](https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArraySet), [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet), [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet), [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) |---|---| | [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet) | A scalable concurrent `https://developer.android.com/reference/kotlin/java/util/NavigableSet` implementation based on a `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap`. | | [CopyOnWriteArraySet](https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArraySet) | A `https://developer.android.com/reference/kotlin/java/util/Set` that uses an internal `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList` for all of its operations. | | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet) | A specialized `https://developer.android.com/reference/kotlin/java/util/Set` implementation for use with enum types. | | [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet) | This class implements the `Set` interface, backed by a hash table (actually a `HashMap` instance). | | [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) | A `https://developer.android.com/reference/kotlin/java/util/NavigableSet` implementation based on a `https://developer.android.com/reference/kotlin/java/util/TreeMap`. | |

| Known Indirect Subclasses [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet) |---|---| | [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet) | Hash table and linked list implementation of the `Set` interface, with well-defined encounter order. | |

This class provides a skeletal implementation of the `Set` interface to minimize the effort required to implement this interface.

The process of implementing a set by extending this class is identical to that of implementing a Collection by extending AbstractCollection, except that all of the methods and constructors in subclasses of this class must obey the additional constraints imposed by the `Set` interface (for instance, the add method must not permit addition of multiple instances of an object to a set).

Note that this class does not override any of the implementations from the `AbstractCollection` class. It merely adds implementations for `equals` and `hashCode`.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/AbstractSet#AbstractSet()()` Sole constructor. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/AbstractSet#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this set for equality. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/AbstractSet#hashCode()()` Returns the hash code value for this set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/AbstractSet#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Removes from this set all of its elements that are contained in the specified collection (optional operation). |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#add(java.util.AbstractCollection.E)(element: E)` Ensures that this collection contains the specified element (optional operation). Returns `true` if this collection changed as a result of the call. (Returns `false` if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add `null` elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it *must* throw an exception (rather than returning `false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#clear()()` Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E)(element: E?)` Returns `true` if this collection contains the specified element. More formally, returns `true` if and only if this collection contains at least one element `e` such that `Objects.equals(o, e)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Returns `true` if this collection contains all of the elements in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty()()` Returns `true` if this collection contains no elements. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#iterator()()` Returns an iterator over the elements contained in this collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E)(element: E?)` Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element `e` such that `Objects.equals(o, e)`, if this collection contains one or more such elements. Returns `true` if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray()()` Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType()) is `Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to `null`. (This is useful in determining the length of this collection *only* if the caller knows that this collection does not contain any `null` elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString()()` Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int` Returns the number of elements in this collection. If this collection contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`. <br /> | ||

## Protected constructors

### AbstractSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractSet()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this set for equality. Returns `true` if the given object is also a set, the two sets have the same size, and every member of the given set is contained in this set. This ensures that the `equals` method works properly across different implementations of the `Set` interface.

This implementation first checks if the specified object is this set; if so it returns `true`. Then, it checks if the specified object is a set whose size is identical to the size of this set; if not, it returns false. If so, it returns `containsAll((Collection) o)`.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this set |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified object is equal to this set |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a `null` element is defined to be zero. This ensures that `s1.equals(s2)` implies that `s1.hashCode()==s2.hashCode()` for any two sets `s1` and `s2`, as required by the general contract of `https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()`.

This implementation iterates over the set, calling the `hashCode` method on each element in the set, and adding up the results.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this set |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the *asymmetric set difference* of the two sets.

This implementation determines which is the smaller of this set and the specified collection, by invoking the `size` method on each. If this set has fewer elements, then the implementation iterates over this set, checking each element returned by the iterator in turn to see if it is contained in the specified collection. If it is so contained, it is removed from this set with the iterator's `remove` method. If the specified collection has fewer elements, then the implementation iterates over the specified collection, removing from this set each element returned by the iterator, using this set's `remove` method.

Note that this implementation will throw an `UnsupportedOperationException` if the iterator returned by the `iterator` method does not implement the `remove` method.

| Parameters ||
|---|---|
| `c` | collection containing elements to be removed from this set |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this set changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if this set contains a null element and the specified collection does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `removeAll` operation is not supported by this set |

**See Also**
