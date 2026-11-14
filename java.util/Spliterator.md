# Spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Spliterator

```
interface Spliterator<T : Any!>
```

| [java.util.Spliterator](../java/util/Spliterator.md) |

| Known Direct Subclasses [Spliterator.OfPrimitive](../java/util/Spliterator.OfPrimitive.md), [Spliterators.AbstractSpliterator](../java/util/Spliterators.AbstractSpliterator.md) |-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [Spliterator.OfPrimitive](../java/util/Spliterator.OfPrimitive.md) | A Spliterator specialized for primitive values. | | [Spliterators.AbstractSpliterator](../java/util/Spliterators.AbstractSpliterator.md) | An abstract`Spliterator`that implements`trySplit`to permit limited parallelism. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md), [Spliterator.OfInt](../java/util/Spliterator.OfInt.md), [Spliterator.OfLong](../java/util/Spliterator.OfLong.md), [Spliterators.AbstractDoubleSpliterator](../java/util/Spliterators.AbstractDoubleSpliterator.md), [Spliterators.AbstractIntSpliterator](../java/util/Spliterators.AbstractIntSpliterator.md), [Spliterators.AbstractLongSpliterator](../java/util/Spliterators.AbstractLongSpliterator.md) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------| | [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md) | A Spliterator specialized for`double`values. | | [Spliterator.OfInt](../java/util/Spliterator.OfInt.md) | A Spliterator specialized for`int`values. | | [Spliterator.OfLong](../java/util/Spliterator.OfLong.md) | A Spliterator specialized for`long`values. | | [Spliterators.AbstractDoubleSpliterator](../java/util/Spliterators.AbstractDoubleSpliterator.md) | An abstract`Spliterator.OfDouble`that implements`trySplit`to permit limited parallelism. | | [Spliterators.AbstractIntSpliterator](../java/util/Spliterators.AbstractIntSpliterator.md) | An abstract`Spliterator.OfInt`that implements`trySplit`to permit limited parallelism. | | [Spliterators.AbstractLongSpliterator](../java/util/Spliterators.AbstractLongSpliterator.md) | An abstract`Spliterator.OfLong`that implements`trySplit`to permit limited parallelism. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object for traversing and partitioning elements of a source. The source of elements covered by a Spliterator could be, for example, an array, a [Collection](../java/util/Collection.md), an IO channel, or a generator function.

A Spliterator may traverse elements individually ([tryAdvance()](../java/util/Spliterator.md))) or sequentially in bulk ([forEachRemaining()](../java/util/Spliterator.md))).

A Spliterator may also partition off some of its elements (using [trySplit](../java/util/Spliterator.md))) as another Spliterator, to be used in possibly-parallel operations. Operations using a Spliterator that cannot split, or does so in a highly imbalanced or inefficient manner, are unlikely to benefit from parallelism. Traversal and splitting exhaust elements; each Spliterator is useful for only a single bulk computation.

A Spliterator also reports a set of [characteristics()](../java/util/Spliterator.md))of its structure, source, and elements from among [ORDERED](../java/util/Spliterator.md), [DISTINCT](../java/util/Spliterator.md), [SORTED](../java/util/Spliterator.md), [SIZED](../java/util/Spliterator.md), [NONNULL](../java/util/Spliterator.md), [IMMUTABLE](../java/util/Spliterator.md), [CONCURRENT](../java/util/Spliterator.md), and [SUBSIZED](../java/util/Spliterator.md). These may be employed by Spliterator clients to control, specialize or simplify computation. For example, a Spliterator for a [Collection](../java/util/Collection.md) would report`SIZED`, a Spliterator for a [Set](../java/util/Set.md) would report`DISTINCT`, and a Spliterator for a [SortedSet](../java/util/SortedSet.md) would also report`SORTED`. Characteristics are reported as a simple unioned bit set. Some characteristics additionally constrain method behavior; for example if`ORDERED`, traversal methods must conform to their documented ordering. New characteristics may be defined in the future, so implementors should not assign meanings to unlisted values.

A Spliterator that does not report`IMMUTABLE`or`CONCURRENT`is expected to have a documented policy concerning: when the spliterator*binds* to the element source; and detection of structural interference of the element source detected after binding. A*late-binding* Spliterator binds to the source of elements at the point of first traversal, first split, or first query for estimated size, rather than at the time the Spliterator is created. A Spliterator that is not*late-binding* binds to the source of elements at the point of construction or first invocation of any method. Modifications made to the source prior to binding are reflected when the Spliterator is traversed. After binding a Spliterator should, on a best-effort basis, throw [ConcurrentModificationException](../java/util/ConcurrentModificationException.md) if structural interference is detected. Spliterators that do this are called*fail-fast* . The bulk traversal method ([forEachRemaining()](../java/util/Spliterator.md))) of a Spliterator may optimize traversal and check for structural interference after all elements have been traversed, rather than checking per-element and failing immediately.

Spliterators can provide an estimate of the number of remaining elements via the [estimateSize](../java/util/Spliterator.md))method. Ideally, as reflected in characteristic [SIZED](../java/util/Spliterator.md), this value corresponds exactly to the number of elements that would be encountered in a successful traversal. However, even when not exactly known, an estimated value may still be useful to operations being performed on the source, such as helping to determine whether it is preferable to split further or traverse the remaining elements sequentially.

Despite their obvious utility in parallel algorithms, spliterators are not expected to be thread-safe; instead, implementations of parallel algorithms using spliterators should ensure that the spliterator is only used by one thread at a time. This is generally easy to attain via*serial thread-confinement* , which often is a natural consequence of typical parallel algorithms that work by recursive decomposition. A thread calling [trySplit()](../java/util/Spliterator.md))may hand over the returned Spliterator to another thread, which in turn may traverse or further split that Spliterator. The behaviour of splitting and traversal is undefined if two or more threads operate concurrently on the same spliterator. If the original thread hands a spliterator off to another thread for processing, it is best if that handoff occurs before any elements are consumed with [tryAdvance()](../java/util/Spliterator.md)), as certain guarantees (such as the accuracy of [estimateSize()](../java/util/Spliterator.md))for`SIZED`spliterators) are only valid before traversal has begun.

Primitive subtype specializations of`Spliterator`are provided for [int](../java/util/Spliterator.OfInt.md), [long](../java/util/Spliterator.OfLong.md), and [double](../java/util/Spliterator.OfDouble.md) values. The subtype default implementations of [Spliterator.tryAdvance(java.util.function.Consumer)](../java/util/Spliterator.md))and [Spliterator.forEachRemaining(java.util.function.Consumer)](../java/util/Spliterator.md))box primitive values to instances of their corresponding wrapper class. Such boxing may undermine any performance advantages gained by using the primitive specializations. To avoid boxing, the corresponding primitive-based methods should be used. For example, [Spliterator.OfInt.tryAdvance(java.util.function.IntConsumer)](../java/util/Spliterator.OfInt.md))and [Spliterator.OfInt.forEachRemaining(java.util.function.IntConsumer)](../java/util/Spliterator.OfInt.md))should be used in preference to [Spliterator.OfInt.tryAdvance(java.util.function.Consumer)](../java/util/Spliterator.OfInt.md))and [Spliterator.OfInt.forEachRemaining(java.util.function.Consumer)](../java/util/Spliterator.OfInt.md)). Traversal of primitive values using boxing-based methods [tryAdvance()](../java/util/Spliterator.md))and [forEachRemaining()](../java/util/Spliterator.md))does not affect the order in which the values, transformed to boxed values, are encountered.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OfDouble](../java/util/Spliterator.OfDouble.md) A Spliterator specialized for`double`values. |
| abstract | [OfInt](../java/util/Spliterator.OfInt.md) A Spliterator specialized for`int`values. |
| abstract | [OfLong](../java/util/Spliterator.OfLong.md) A Spliterator specialized for`long`values. |
| --- | --- |
| abstract | [OfPrimitive](../java/util/Spliterator.OfPrimitive.md) A Spliterator specialized for primitive values. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCURRENT](../java/util/Spliterator.md) Characteristic value signifying that the element source may be safely concurrently modified (allowing additions, replacements, and/or removals) by multiple threads without external synchronization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISTINCT](../java/util/Spliterator.md) Characteristic value signifying that, for each pair of encountered elements`x, y`,`!x.equals(y)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMMUTABLE](../java/util/Spliterator.md) Characteristic value signifying that the element source cannot be structurally modified; that is, elements cannot be added, replaced, or removed, so such changes cannot occur during traversal. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONNULL](../java/util/Spliterator.md) Characteristic value signifying that the source guarantees that encountered elements will not be`null`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDERED](../java/util/Spliterator.md) Characteristic value signifying that an encounter order is defined for elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZED](../java/util/Spliterator.md) Characteristic value signifying that the value returned from`estimateSize()`prior to traversal or splitting represents a finite size that, in the absence of structural source modification, represents an exact count of the number of elements that would be encountered by a complete traversal. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SORTED](../java/util/Spliterator.md) Characteristic value signifying that encounter order follows a defined sort order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSIZED](../java/util/Spliterator.md) Characteristic value signifying that all Spliterators resulting from`trySplit()`will be both [SIZED](../java/util/Spliterator.md) and [SUBSIZED](../java/util/Spliterator.md). |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [characteristics](../java/util/Spliterator.md))`()` Returns a set of characteristics of this Spliterator and its elements. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [estimateSize](../java/util/Spliterator.md))`()` Returns an estimate of the number of elements that would be encountered by a [forEachRemaining](../java/util/Spliterator.md))traversal, or returns [java.lang.Long#MAX_VALUE](../java/lang/Long.md) if infinite, unknown, or too expensive to compute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachRemaining](../java/util/Spliterator.md))`(`action:` ` [Consumer](../java/util/function/Consumer.md)<in` `T>!`)` Performs the given action for each remaining element, sequentially in the current thread, until all elements have been processed or the action throws an exception. |
| --- | --- |
| open [Comparator](../java/util/Comparator.md)\<inT\>! | [getComparator](../java/util/Spliterator.md))`()` If this Spliterator's source is [SORTED](../java/util/Spliterator.md) by a [Comparator](../java/util/Comparator.md), returns that`Comparator`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getExactSizeIfKnown](../java/util/Spliterator.md))`()` Convenience method that returns [estimateSize()](../java/util/Spliterator.md))if this Spliterator is [SIZED](../java/util/Spliterator.md), else`-1`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCharacteristics](../java/util/Spliterator.md))`(`characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if this Spliterator's [characteristics](../java/util/Spliterator.md))contain all of the given characteristics. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryAdvance](../java/util/Spliterator.md))`(`action:` ` [Consumer](../java/util/function/Consumer.md)<in` `T>!`)` If a remaining element exists: performs the given action on it, returning`true`; else returns`false`. |
| abstract [Spliterator](../java/util/Spliterator.md)\<T\>! | [trySplit](../java/util/Spliterator.md))`()` If this spliterator can be partitioned, returns a Spliterator covering elements, that will, upon return from this method, not be covered by this Spliterator. |

## Constants

### CONCURRENT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONCURRENT: Int
```

Characteristic value signifying that the element source may be safely concurrently modified (allowing additions, replacements, and/or removals) by multiple threads without external synchronization. If so, the Spliterator is expected to have a documented policy concerning the impact of modifications during traversal.

A top-level Spliterator should not report both`CONCURRENT`and`SIZED`, since the finite size, if known, may change if the source is concurrently modified during traversal. Such a Spliterator is inconsistent and no guarantees can be made about any computation using that Spliterator. Sub-spliterators may report`SIZED`if the sub-split size is known and additions or removals to the source are not reflected when traversing.

A top-level Spliterator should not report both`CONCURRENT`and`IMMUTABLE`, since they are mutually exclusive. Such a Spliterator is inconsistent and no guarantees can be made about any computation using that Spliterator. Sub-spliterators may report`IMMUTABLE`if additions or removals to the source are not reflected when traversing. 

 Value: 4096

### DISTINCT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISTINCT: Int
```

Characteristic value signifying that, for each pair of encountered elements`x, y`,`!x.equals(y)`. This applies for example, to a Spliterator based on a [Set](../java/util/Set.md). 

 Value: 1

### IMMUTABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IMMUTABLE: Int
```

Characteristic value signifying that the element source cannot be structurally modified; that is, elements cannot be added, replaced, or removed, so such changes cannot occur during traversal. A Spliterator that does not report`IMMUTABLE`or`CONCURRENT`is expected to have a documented policy (for example throwing [ConcurrentModificationException](../java/util/ConcurrentModificationException.md)) concerning structural interference detected during traversal. 

 Value: 1024

### NONNULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONNULL: Int
```

Characteristic value signifying that the source guarantees that encountered elements will not be`null`. (This applies, for example, to most concurrent collections, queues, and maps.) 

 Value: 256

### ORDERED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORDERED: Int
```

Characteristic value signifying that an encounter order is defined for elements. If so, this Spliterator guarantees that method [trySplit](../java/util/Spliterator.md))splits a strict prefix of elements, that method [tryAdvance](../java/util/Spliterator.md))steps by one element in prefix order, and that [forEachRemaining](../java/util/Spliterator.md))performs actions in encounter order.

A [Collection](../java/util/Collection.md) has an encounter order if the corresponding [Collection.iterator](../java/util/Collection.md))documents an order. If so, the encounter order is the same as the documented order. Otherwise, a collection does not have an encounter order. 

 Value: 16

### SIZED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZED: Int
```

Characteristic value signifying that the value returned from`estimateSize()`prior to traversal or splitting represents a finite size that, in the absence of structural source modification, represents an exact count of the number of elements that would be encountered by a complete traversal. 

 Value: 64

### SORTED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SORTED: Int
```

Characteristic value signifying that encounter order follows a defined sort order. If so, method [getComparator()](../java/util/Spliterator.md))returns the associated Comparator, or`null`if all elements are [Comparable](../java/lang/Comparable.md) and are sorted by their natural ordering.

A Spliterator that reports`SORTED`must also report`ORDERED`. 

 Value: 4

### SUBSIZED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSIZED: Int
```

Characteristic value signifying that all Spliterators resulting from`trySplit()`will be both [SIZED](../java/util/Spliterator.md) and [SUBSIZED](../java/util/Spliterator.md). (This means that all child Spliterators, whether direct or indirect, will be`SIZED`.)

A Spliterator that does not report`SIZED`as required by`SUBSIZED`is inconsistent and no guarantees can be made about any computation using that Spliterator. 

 Value: 16384

## Public methods

### characteristics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun characteristics(): Int
```

Returns a set of characteristics of this Spliterator and its elements. The result is represented as ORed values from [ORDERED](../java/util/Spliterator.md), [DISTINCT](../java/util/Spliterator.md), [SORTED](../java/util/Spliterator.md), [SIZED](../java/util/Spliterator.md), [NONNULL](../java/util/Spliterator.md), [IMMUTABLE](../java/util/Spliterator.md), [CONCURRENT](../java/util/Spliterator.md), [SUBSIZED](../java/util/Spliterator.md). Repeated calls to`characteristics()`on a given spliterator, prior to or in-between calls to`trySplit`, should always return the same result.

If a Spliterator reports an inconsistent set of characteristics (either those returned from a single invocation or across multiple invocations), no guarantees can be made about any computation using this Spliterator.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a representation of characteristics |

### estimateSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun estimateSize(): Long
```

Returns an estimate of the number of elements that would be encountered by a [forEachRemaining](../java/util/Spliterator.md))traversal, or returns [java.lang.Long#MAX_VALUE](../java/lang/Long.md) if infinite, unknown, or too expensive to compute.

If this Spliterator is [SIZED](../java/util/Spliterator.md) and has not yet been partially traversed or split, or this Spliterator is [SUBSIZED](../java/util/Spliterator.md) and has not yet been partially traversed, this estimate must be an accurate count of elements that would be encountered by a complete traversal. Otherwise, this estimate may be arbitrarily inaccurate, but must decrease as specified across invocations of [trySplit](../java/util/Spliterator.md)).

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the estimated size, or`Long.MAX_VALUE`if infinite, unknown, or too expensive to compute. |

### forEachRemaining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachRemaining(action: Consumer<in T>!): Unit
```

Performs the given action for each remaining element, sequentially in the current thread, until all elements have been processed or the action throws an exception. If this Spliterator is [ORDERED](../java/util/Spliterator.md), actions are performed in encounter order. Exceptions thrown by the action are relayed to the caller.

Subsequent behavior of a spliterator is unspecified if the action throws an exception.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java/util/function/Consumer.md)\<inT\>!:The action |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### getComparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComparator(): Comparator<in T>!
```

If this Spliterator's source is [SORTED](../java/util/Spliterator.md) by a [Comparator](../java/util/Comparator.md), returns that`Comparator`. If the source is`SORTED`in [natural order](../java/lang/Comparable.md), returns`null`. Otherwise, if the source is not`SORTED`, throws [IllegalStateException](../java/lang/IllegalStateException.md).

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Comparator](../java/util/Comparator.md)<in` `T>! | a Comparator, or`null`if the elements are sorted in the natural order. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the spliterator does not report a characteristic of`SORTED`. |

### getExactSizeIfKnown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExactSizeIfKnown(): Long
```

Convenience method that returns [estimateSize()](../java/util/Spliterator.md))if this Spliterator is [SIZED](../java/util/Spliterator.md), else`-1`.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the exact size, if known, else`-1`. |

### hasCharacteristics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasCharacteristics(characteristics: Int): Boolean
```

Returns`true`if this Spliterator's [characteristics](../java/util/Spliterator.md))contain all of the given characteristics.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------|
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the characteristics to check for |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if all the specified characteristics are present, else`false` |

### tryAdvance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tryAdvance(action: Consumer<in T>!): Boolean
```

If a remaining element exists: performs the given action on it, returning`true`; else returns`false`. If this Spliterator is [ORDERED](../java/util/Spliterator.md) the action is performed on the next element in encounter order. Exceptions thrown by the action are relayed to the caller.

Subsequent behavior of a spliterator is unspecified if the action throws an exception.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java/util/function/Consumer.md)\<inT\>!:The action whose operation is performed at-most once |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if no remaining elements existed upon entry to this method, else`true`. |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### trySplit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun trySplit(): Spliterator<T>!
```

If this spliterator can be partitioned, returns a Spliterator covering elements, that will, upon return from this method, not be covered by this Spliterator.

If this Spliterator is [ORDERED](../java/util/Spliterator.md), the returned Spliterator must cover a strict prefix of the elements.

Unless this Spliterator covers an infinite number of elements, repeated calls to`trySplit()`must eventually return`null`. Upon non-null return:

- the value reported for`estimateSize()`before splitting, must, after splitting, be greater than or equal to`estimateSize()`for this and the returned Spliterator; and
- if this Spliterator is`SUBSIZED`, then`estimateSize()`for this spliterator before splitting must be equal to the sum of`estimateSize()`for this and the returned Spliterator after splitting.

This method may return`null`for any reason, including emptiness, inability to split after traversal has commenced, data structure constraints, and efficiency considerations.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<T>! | a`Spliterator`covering some portion of the elements, or`null`if this spliterator cannot be split |
