# SequencedSet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SequencedSet

```
interface SequencedSet<E : Any!> : SequencedCollection<E>, MutableSet<E>
```

| [java.util.SequencedSet](../java/util/SequencedSet.md) |

| Known Direct Subclasses [LinkedHashSet](../java/util/LinkedHashSet.md), [SortedSet](../java/util/SortedSet.md) |-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------| | [LinkedHashSet](../java/util/LinkedHashSet.md) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | | [SortedSet](../java/util/SortedSet.md) | A [Set](../java/util/Set.md) that further provides a*total ordering*on its elements. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md), [NavigableSet](../java/util/NavigableSet.md), [TreeSet](../java/util/TreeSet.md) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java/util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md). | | [NavigableSet](../java/util/NavigableSet.md) | A [SortedSet](../java/util/SortedSet.md) extended with navigation methods reporting closest matches for given search targets. | | [TreeSet](../java/util/TreeSet.md) | A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A collection that is both a [SequencedCollection](../java/util/SequencedCollection.md) and a [Set](../java/util/Set.md). As such, it can be thought of either as a`Set`that also has a well-defined [encounter order](../java/util/SequencedCollection.md), or as a`SequencedCollection`that also has unique elements.

This interface has the same requirements on the`equals`and`hashCode`methods as defined by java.util.Set#equals and java.util.Set#hashCode. Thus, a`Set`and a`SequencedSet`will compare equals if and only if they have equal elements, irrespective of ordering.

`SequencedSet`defines the [reversed](../java/util/SequencedSet.md))method, which provides a reverse-ordered [view](../java/util/Collection.md) of this set. The only difference from the [SequencedCollection.reversed](../java/util/SequencedCollection.md))method is that the return type of`SequencedSet.reversed`is`SequencedSet`.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SequencedSet](../java/util/SequencedSet.md)\<E\>! | [reversed](../java/util/SequencedSet.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. |

| Inherited functions ||
|---|---|
| From class [SequencedCollection](../java/util/SequencedCollection.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/SequencedCollection.md))`(`e:` `E`)` <br /> Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/SequencedCollection.md))`(`e:` `E`)` <br /> Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order. <br /> | | E | [getFirst](../java/util/SequencedCollection.md))`()` <br /> Gets the first element of this collection. <br /> | | E | [getLast](../java/util/SequencedCollection.md))`()` <br /> Gets the last element of this collection. <br /> | | E | [removeFirst](../java/util/SequencedCollection.md))`()` <br /> Removes and returns the first element of this collection (optional operation). <br /> | | E | [removeLast](../java/util/SequencedCollection.md))`()` <br /> Removes and returns the last element of this collection (optional operation). <br /> | ||

## Public methods

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reversed(): SequencedSet<E>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [SequencedSet](../java/util/SequencedSet.md)<E>! | a reverse-ordered view of this collection, as a`SequencedSet` |
