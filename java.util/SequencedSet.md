# SequencedSet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedSet

```
interface SequencedSet<E : Any!> : SequencedCollection<E>, MutableSet<E>
```

| [java.util.SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet#) |

| Known Direct Subclasses [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet), [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) |-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------| | [LinkedHashSet](https://developer.android.com/reference/kotlin/java/util/LinkedHashSet) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | | [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) | A [Set](https://developer.android.com/reference/kotlin/java/util/Set) that further provides a*total ordering*on its elements. | |

| Known Indirect Subclasses [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet), [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet), [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListSet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListSet) | A scalable concurrent [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [ConcurrentSkipListMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentSkipListMap). | | [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) | A [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) extended with navigation methods reporting closest matches for given search targets. | | [TreeSet](https://developer.android.com/reference/kotlin/java/util/TreeSet) | A [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet) implementation based on a [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap). | |

A collection that is both a [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection) and a [Set](https://developer.android.com/reference/kotlin/java/util/Set). As such, it can be thought of either as a`Set`that also has a well-defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), or as a`SequencedCollection`that also has unique elements.

This interface has the same requirements on the`equals`and`hashCode`methods as defined by java.util.Set#equals and java.util.Set#hashCode. Thus, a`Set`and a`SequencedSet`will compare equals if and only if they have equal elements, irrespective of ordering.

`SequencedSet`defines the [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedSet#reversed())method, which provides a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this set. The only difference from the [SequencedCollection.reversed](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#reversed())method is that the return type of`SequencedSet.reversed`is`SequencedSet`.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet#)\<E\>! | [reversed](https://developer.android.com/reference/kotlin/java/util/SequencedSet#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. |

| Inherited functions ||
|---|---|
| From class [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#addFirst(java.util.SequencedCollection.E))`(`e:` `E`)` <br /> Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#addLast(java.util.SequencedCollection.E))`(`e:` `E`)` <br /> Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order. <br /> | | E | [getFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#getFirst())`()` <br /> Gets the first element of this collection. <br /> | | E | [getLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#getLast())`()` <br /> Gets the last element of this collection. <br /> | | E | [removeFirst](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#removeFirst())`()` <br /> Removes and returns the first element of this collection (optional operation). <br /> | | E | [removeLast](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#removeLast())`()` <br /> Removes and returns the last element of this collection (optional operation). <br /> | ||

## Public methods

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reversed(): SequencedSet<E>!
```

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet#)<E>! | a reverse-ordered view of this collection, as a`SequencedSet` |
