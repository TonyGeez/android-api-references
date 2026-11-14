# Spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Spliterator

```
interface Spliterator<T : Any!>
```

| [java.util.Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator#) |

| Known Direct Subclasses [Spliterator.OfPrimitive](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfPrimitive), [Spliterators.AbstractSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractSpliterator) |-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [Spliterator.OfPrimitive](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfPrimitive) | A Spliterator specialized for primitive values. | | [Spliterators.AbstractSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractSpliterator) | An abstract`Spliterator`that implements`trySplit`to permit limited parallelism. | |

| Known Indirect Subclasses [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble), [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt), [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong), [Spliterators.AbstractDoubleSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractDoubleSpliterator), [Spliterators.AbstractIntSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractIntSpliterator), [Spliterators.AbstractLongSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractLongSpliterator) |-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------| | [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble) | A Spliterator specialized for`double`values. | | [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt) | A Spliterator specialized for`int`values. | | [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong) | A Spliterator specialized for`long`values. | | [Spliterators.AbstractDoubleSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractDoubleSpliterator) | An abstract`Spliterator.OfDouble`that implements`trySplit`to permit limited parallelism. | | [Spliterators.AbstractIntSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractIntSpliterator) | An abstract`Spliterator.OfInt`that implements`trySplit`to permit limited parallelism. | | [Spliterators.AbstractLongSpliterator](https://developer.android.com/reference/kotlin/java/util/Spliterators.AbstractLongSpliterator) | An abstract`Spliterator.OfLong`that implements`trySplit`to permit limited parallelism. | |

An object for traversing and partitioning elements of a source. The source of elements covered by a Spliterator could be, for example, an array, a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection), an IO channel, or a generator function.

A Spliterator may traverse elements individually ([tryAdvance()](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer))) or sequentially in bulk ([forEachRemaining()](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))).

A Spliterator may also partition off some of its elements (using [trySplit](https://developer.android.com/reference/kotlin/java/util/Spliterator#trySplit())) as another Spliterator, to be used in possibly-parallel operations. Operations using a Spliterator that cannot split, or does so in a highly imbalanced or inefficient manner, are unlikely to benefit from parallelism. Traversal and splitting exhaust elements; each Spliterator is useful for only a single bulk computation.

A Spliterator also reports a set of [characteristics()](https://developer.android.com/reference/kotlin/java/util/Spliterator#characteristics())of its structure, source, and elements from among [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int), [DISTINCT](https://developer.android.com/reference/kotlin/java/util/Spliterator#DISTINCT:kotlin.Int), [SORTED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int), [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), [NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator#NONNULL:kotlin.Int), [IMMUTABLE](https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int), [CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator#CONCURRENT:kotlin.Int), and [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int). These may be employed by Spliterator clients to control, specialize or simplify computation. For example, a Spliterator for a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) would report`SIZED`, a Spliterator for a [Set](https://developer.android.com/reference/kotlin/java/util/Set) would report`DISTINCT`, and a Spliterator for a [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) would also report`SORTED`. Characteristics are reported as a simple unioned bit set. Some characteristics additionally constrain method behavior; for example if`ORDERED`, traversal methods must conform to their documented ordering. New characteristics may be defined in the future, so implementors should not assign meanings to unlisted values.

A Spliterator that does not report`IMMUTABLE`or`CONCURRENT`is expected to have a documented policy concerning: when the spliterator*binds* to the element source; and detection of structural interference of the element source detected after binding. A*late-binding* Spliterator binds to the source of elements at the point of first traversal, first split, or first query for estimated size, rather than at the time the Spliterator is created. A Spliterator that is not*late-binding* binds to the source of elements at the point of construction or first invocation of any method. Modifications made to the source prior to binding are reflected when the Spliterator is traversed. After binding a Spliterator should, on a best-effort basis, throw [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) if structural interference is detected. Spliterators that do this are called*fail-fast* . The bulk traversal method ([forEachRemaining()](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))) of a Spliterator may optimize traversal and check for structural interference after all elements have been traversed, rather than checking per-element and failing immediately.

Spliterators can provide an estimate of the number of remaining elements via the [estimateSize](https://developer.android.com/reference/kotlin/java/util/Spliterator#estimateSize())method. Ideally, as reflected in characteristic [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), this value corresponds exactly to the number of elements that would be encountered in a successful traversal. However, even when not exactly known, an estimated value may still be useful to operations being performed on the source, such as helping to determine whether it is preferable to split further or traverse the remaining elements sequentially.

Despite their obvious utility in parallel algorithms, spliterators are not expected to be thread-safe; instead, implementations of parallel algorithms using spliterators should ensure that the spliterator is only used by one thread at a time. This is generally easy to attain via*serial thread-confinement* , which often is a natural consequence of typical parallel algorithms that work by recursive decomposition. A thread calling [trySplit()](https://developer.android.com/reference/kotlin/java/util/Spliterator#trySplit())may hand over the returned Spliterator to another thread, which in turn may traverse or further split that Spliterator. The behaviour of splitting and traversal is undefined if two or more threads operate concurrently on the same spliterator. If the original thread hands a spliterator off to another thread for processing, it is best if that handoff occurs before any elements are consumed with [tryAdvance()](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer)), as certain guarantees (such as the accuracy of [estimateSize()](https://developer.android.com/reference/kotlin/java/util/Spliterator#estimateSize())for`SIZED`spliterators) are only valid before traversal has begun.

Primitive subtype specializations of`Spliterator`are provided for [int](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt), [long](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong), and [double](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble) values. The subtype default implementations of [Spliterator.tryAdvance(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer))and [Spliterator.forEachRemaining(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))box primitive values to instances of their corresponding wrapper class. Such boxing may undermine any performance advantages gained by using the primitive specializations. To avoid boxing, the corresponding primitive-based methods should be used. For example, [Spliterator.OfInt.tryAdvance(java.util.function.IntConsumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt#tryAdvance(java.util.function.IntConsumer))and [Spliterator.OfInt.forEachRemaining(java.util.function.IntConsumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt#forEachRemaining(java.util.function.IntConsumer))should be used in preference to [Spliterator.OfInt.tryAdvance(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt#tryAdvance(java.util.function.Consumer))and [Spliterator.OfInt.forEachRemaining(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt#forEachRemaining(java.util.function.Consumer)). Traversal of primitive values using boxing-based methods [tryAdvance()](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer))and [forEachRemaining()](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))does not affect the order in which the values, transformed to boxed values, are encountered.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble) A Spliterator specialized for`double`values. |
| abstract | [OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt) A Spliterator specialized for`int`values. |
| abstract | [OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong) A Spliterator specialized for`long`values. |
| abstract | [OfPrimitive](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfPrimitive) A Spliterator specialized for primitive values. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator#CONCURRENT:kotlin.Int) Characteristic value signifying that the element source may be safely concurrently modified (allowing additions, replacements, and/or removals) by multiple threads without external synchronization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISTINCT](https://developer.android.com/reference/kotlin/java/util/Spliterator#DISTINCT:kotlin.Int) Characteristic value signifying that, for each pair of encountered elements`x, y`,`!x.equals(y)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IMMUTABLE](https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int) Characteristic value signifying that the element source cannot be structurally modified; that is, elements cannot be added, replaced, or removed, so such changes cannot occur during traversal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator#NONNULL:kotlin.Int) Characteristic value signifying that the source guarantees that encountered elements will not be`null`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int) Characteristic value signifying that an encounter order is defined for elements. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int) Characteristic value signifying that the value returned from`estimateSize()`prior to traversal or splitting represents a finite size that, in the absence of structural source modification, represents an exact count of the number of elements that would be encountered by a complete traversal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SORTED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int) Characteristic value signifying that encounter order follows a defined sort order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int) Characteristic value signifying that all Spliterators resulting from`trySplit()`will be both [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int) and [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int). |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [characteristics](https://developer.android.com/reference/kotlin/java/util/Spliterator#characteristics())`()` Returns a set of characteristics of this Spliterator and its elements. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [estimateSize](https://developer.android.com/reference/kotlin/java/util/Spliterator#estimateSize())`()` Returns an estimate of the number of elements that would be encountered by a [forEachRemaining](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))traversal, or returns [java.lang.Long#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long) if infinite, unknown, or too expensive to compute. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachRemaining](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `T>!`)` Performs the given action for each remaining element, sequentially in the current thread, until all elements have been processed or the action throws an exception. |
| open [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inT\>! | [getComparator](https://developer.android.com/reference/kotlin/java/util/Spliterator#getComparator())`()` If this Spliterator's source is [SORTED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int) by a [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator), returns that`Comparator`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getExactSizeIfKnown](https://developer.android.com/reference/kotlin/java/util/Spliterator#getExactSizeIfKnown())`()` Convenience method that returns [estimateSize()](https://developer.android.com/reference/kotlin/java/util/Spliterator#estimateSize())if this Spliterator is [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), else`-1`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCharacteristics](https://developer.android.com/reference/kotlin/java/util/Spliterator#hasCharacteristics(kotlin.Int))`(`characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if this Spliterator's [characteristics](https://developer.android.com/reference/kotlin/java/util/Spliterator#characteristics())contain all of the given characteristics. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryAdvance](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `T>!`)` If a remaining element exists: performs the given action on it, returning`true`; else returns`false`. |
| abstract [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator#)\<T\>! | [trySplit](https://developer.android.com/reference/kotlin/java/util/Spliterator#trySplit())`()` If this spliterator can be partitioned, returns a Spliterator covering elements, that will, upon return from this method, not be covered by this Spliterator. |

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

Characteristic value signifying that, for each pair of encountered elements`x, y`,`!x.equals(y)`. This applies for example, to a Spliterator based on a [Set](https://developer.android.com/reference/kotlin/java/util/Set). 

 Value: 1

### IMMUTABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IMMUTABLE: Int
```

Characteristic value signifying that the element source cannot be structurally modified; that is, elements cannot be added, replaced, or removed, so such changes cannot occur during traversal. A Spliterator that does not report`IMMUTABLE`or`CONCURRENT`is expected to have a documented policy (for example throwing [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException)) concerning structural interference detected during traversal. 

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

Characteristic value signifying that an encounter order is defined for elements. If so, this Spliterator guarantees that method [trySplit](https://developer.android.com/reference/kotlin/java/util/Spliterator#trySplit())splits a strict prefix of elements, that method [tryAdvance](https://developer.android.com/reference/kotlin/java/util/Spliterator#tryAdvance(java.util.function.Consumer))steps by one element in prefix order, and that [forEachRemaining](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))performs actions in encounter order.

A [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) has an encounter order if the corresponding [Collection.iterator](https://developer.android.com/reference/kotlin/java/util/Collection#iterator())documents an order. If so, the encounter order is the same as the documented order. Otherwise, a collection does not have an encounter order. 

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

Characteristic value signifying that encounter order follows a defined sort order. If so, method [getComparator()](https://developer.android.com/reference/kotlin/java/util/Spliterator#getComparator())returns the associated Comparator, or`null`if all elements are [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) and are sorted by their natural ordering.

A Spliterator that reports`SORTED`must also report`ORDERED`. 

 Value: 4

### SUBSIZED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUBSIZED: Int
```

Characteristic value signifying that all Spliterators resulting from`trySplit()`will be both [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int) and [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int). (This means that all child Spliterators, whether direct or indirect, will be`SIZED`.)

A Spliterator that does not report`SIZED`as required by`SUBSIZED`is inconsistent and no guarantees can be made about any computation using that Spliterator. 

 Value: 16384

## Public methods

### characteristics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun characteristics(): Int
```

Returns a set of characteristics of this Spliterator and its elements. The result is represented as ORed values from [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int), [DISTINCT](https://developer.android.com/reference/kotlin/java/util/Spliterator#DISTINCT:kotlin.Int), [SORTED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int), [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), [NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator#NONNULL:kotlin.Int), [IMMUTABLE](https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int), [CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator#CONCURRENT:kotlin.Int), [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int). Repeated calls to`characteristics()`on a given spliterator, prior to or in-between calls to`trySplit`, should always return the same result.

If a Spliterator reports an inconsistent set of characteristics (either those returned from a single invocation or across multiple invocations), no guarantees can be made about any computation using this Spliterator.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a representation of characteristics |

### estimateSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun estimateSize(): Long
```

Returns an estimate of the number of elements that would be encountered by a [forEachRemaining](https://developer.android.com/reference/kotlin/java/util/Spliterator#forEachRemaining(java.util.function.Consumer))traversal, or returns [java.lang.Long#MAX_VALUE](https://developer.android.com/reference/kotlin/java/lang/Long.html#MAX_VALUE:kotlin.Long) if infinite, unknown, or too expensive to compute.

If this Spliterator is [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int) and has not yet been partially traversed or split, or this Spliterator is [SUBSIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int) and has not yet been partially traversed, this estimate must be an accurate count of elements that would be encountered by a complete traversal. Otherwise, this estimate may be arbitrarily inaccurate, but must decrease as specified across invocations of [trySplit](https://developer.android.com/reference/kotlin/java/util/Spliterator#trySplit()).

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the estimated size, or`Long.MAX_VALUE`if infinite, unknown, or too expensive to compute. |

### forEachRemaining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachRemaining(action: Consumer<in T>!): Unit
```

Performs the given action for each remaining element, sequentially in the current thread, until all elements have been processed or the action throws an exception. If this Spliterator is [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int), actions are performed in encounter order. Exceptions thrown by the action are relayed to the caller.

Subsequent behavior of a spliterator is unspecified if the action throws an exception.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)\<inT\>!:The action |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### getComparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComparator(): Comparator<in T>!
```

If this Spliterator's source is [SORTED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SORTED:kotlin.Int) by a [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator), returns that`Comparator`. If the source is`SORTED`in [natural order](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#), returns`null`. Otherwise, if the source is not`SORTED`, throws [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `T>! | a Comparator, or`null`if the elements are sorted in the natural order. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the spliterator does not report a characteristic of`SORTED`. |

### getExactSizeIfKnown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExactSizeIfKnown(): Long
```

Convenience method that returns [estimateSize()](https://developer.android.com/reference/kotlin/java/util/Spliterator#estimateSize())if this Spliterator is [SIZED](https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int), else`-1`.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the exact size, if known, else`-1`. |

### hasCharacteristics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasCharacteristics(characteristics: Int): Boolean
```

Returns`true`if this Spliterator's [characteristics](https://developer.android.com/reference/kotlin/java/util/Spliterator#characteristics())contain all of the given characteristics.

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

If a remaining element exists: performs the given action on it, returning`true`; else returns`false`. If this Spliterator is [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int) the action is performed on the next element in encounter order. Exceptions thrown by the action are relayed to the caller.

Subsequent behavior of a spliterator is unspecified if the action throws an exception.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)\<inT\>!:The action whose operation is performed at-most once |

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

If this Spliterator is [ORDERED](https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int), the returned Spliterator must cover a strict prefix of the elements.

Unless this Spliterator covers an infinite number of elements, repeated calls to`trySplit()`must eventually return`null`. Upon non-null return:

- the value reported for`estimateSize()`before splitting, must, after splitting, be greater than or equal to`estimateSize()`for this and the returned Spliterator; and
- if this Spliterator is`SUBSIZED`, then`estimateSize()`for this spliterator before splitting must be equal to the sum of`estimateSize()`for this and the returned Spliterator after splitting.

This method may return`null`for any reason, including emptiness, inability to split after traversal has commenced, data structure constraints, and efficiency considerations.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator#)<T>! | a`Spliterator`covering some portion of the elements, or`null`if this spliterator cannot be split |
