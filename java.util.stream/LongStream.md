# LongStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongStream

```
interface LongStream : BaseStream<Long!, LongStream!>
```

| [java.util.stream.LongStream](../java/util/stream/LongStream.md) |

A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. This is the`long`primitive specialization of .

The following example illustrates an aggregate operation using [Stream](../java/util/stream/Stream.md) and [LongStream](../java/util/stream/LongStream.md), computing the sum of the weights of the red widgets: 

```kotlin
<code>long sum = widgets.stream()
                        .filter(w -&gt; w.getColor() == RED)
                        .mapToLong(w -&gt; w.getWeight())
                        .sum();
  </code>
```
See the class documentation for [Stream](../java/util/stream/Stream.md) and the package documentation for [java.util.stream](../java/util/stream/_package.md) for additional specification of streams, stream operations, stream pipelines, and parallelism.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](../java/util/stream/LongStream.Builder.md) A mutable builder for a`LongStream`. |
| abstract | [LongMapMultiConsumer](../java/util/stream/LongStream.LongMapMultiConsumer.md) Represents an operation that accepts a`long`-valued argument and a LongConsumer, and returns no result. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns whether any elements of this stream match the provided predicate. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [asDoubleStream](../java/util/stream/LongStream.md))`()` Returns a`DoubleStream`consisting of the elements of this stream, converted to`double`. |
| --- | --- |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [average](../java/util/stream/LongStream.md))`()` Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. |
| abstract [Stream](../java/util/stream/Stream.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [boxed](../java/util/stream/LongStream.md))`()` Returns a`Stream`consisting of the elements of this stream, each boxed to a`Long`. |
| openstatic [LongStream.Builder](../java/util/stream/LongStream.Builder.md)! | [builder](../java/util/stream/LongStream.md))`()` Returns a builder for a`LongStream`. |
| --- | --- |
| abstractR | [collect](../java/util/stream/LongStream.md))`(`supplier:` ` [Supplier](../java/util/function/Supplier.md)<R>!`, `accumulator:` ` [ObjLongConsumer](../java/util/function/ObjLongConsumer.md)<R>!`, `combiner:` ` [BiConsumer](../java/util/function/BiConsumer.md)<R,` `R>!`)` Performs a [mutable reduction](../java/util/stream/_package.md) operation on the elements of this stream. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [concat](../java/util/stream/LongStream.md))`(`a:` ` [LongStream](../java/util/stream/LongStream.md)!`, `b:` ` [LongStream](../java/util/stream/LongStream.md)!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](../java/util/stream/LongStream.md))`()` Returns the count of elements in this stream. |
| --- | --- |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [distinct](../java/util/stream/LongStream.md))`()` Returns a stream consisting of the distinct elements of this stream. |
| open [LongStream](../java/util/stream/LongStream.md)! | [dropWhile](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [empty](../java/util/stream/LongStream.md))`()` Returns an empty sequential`LongStream`. |
| --- | --- |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [filter](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| abstract [OptionalLong](../java/util/OptionalLong.md)! | [findAny](../java/util/stream/LongStream.md))`()` Returns an [OptionalLong](../java/util/OptionalLong.md) describing some element of the stream, or an empty`OptionalLong`if the stream is empty. |
| abstract [OptionalLong](../java/util/OptionalLong.md)! | [findFirst](../java/util/stream/LongStream.md))`()` Returns an [OptionalLong](../java/util/OptionalLong.md) describing the first element of this stream, or an empty`OptionalLong`if the stream is empty. |
| --- | --- |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [flatMap](../java/util/stream/LongStream.md))`(`mapper:` ` [LongFunction](../java/util/function/LongFunction.md)<out` ` [LongStream](../java/util/stream/LongStream.md)!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../java/util/stream/LongStream.md))`(`action:` ` [LongConsumer](../java/util/function/LongConsumer.md)!`)` Performs an action for each element of this stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](../java/util/stream/LongStream.md))`(`action:` ` [LongConsumer](../java/util/function/LongConsumer.md)!`)` Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order. |
| --- | --- |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [generate](../java/util/stream/LongStream.md))`(`s:` ` [LongSupplier](../java/util/function/LongSupplier.md)!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`LongSupplier`. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [iterate](../java/util/stream/LongStream.md))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `hasNext:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`, `next:` ` [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!`)` Returns a sequential ordered`LongStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [iterate](../java/util/stream/LongStream.md))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `f:` ` [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!`)` Returns an infinite sequential ordered`LongStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| --- | --- |
| abstract [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)! | [iterator](../java/util/stream/LongStream.md))`()` <br /> |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [limit](../java/util/stream/LongStream.md))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [map](../java/util/stream/LongStream.md))`(`mapper:` ` [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| open [LongStream](../java/util/stream/LongStream.md)! | [mapMulti](../java/util/stream/LongStream.md))`(`mapper:` ` [LongStream.LongMapMultiConsumer](../java/util/stream/LongStream.LongMapMultiConsumer.md)!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [mapToDouble](../java/util/stream/LongStream.md))`(`mapper:` ` [LongToDoubleFunction](../java/util/function/LongToDoubleFunction.md)!`)` Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [IntStream](../java/util/stream/IntStream.md)! | [mapToInt](../java/util/stream/LongStream.md))`(`mapper:` ` [LongToIntFunction](../java/util/function/LongToIntFunction.md)!`)` Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| abstract [Stream](../java/util/stream/Stream.md)\<U\>! | [mapToObj](../java/util/stream/LongStream.md))`(`mapper:` ` [LongFunction](../java/util/function/LongFunction.md)<out` `U>!`)` Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [OptionalLong](../java/util/OptionalLong.md)! | [max](../java/util/stream/LongStream.md))`()` Returns an`OptionalLong`describing the maximum element of this stream, or an empty optional if this stream is empty. |
| abstract [OptionalLong](../java/util/OptionalLong.md)! | [min](../java/util/stream/LongStream.md))`()` Returns an`OptionalLong`describing the minimum element of this stream, or an empty optional if this stream is empty. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns whether no elements of this stream match the provided predicate. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [of](../java/util/stream/LongStream.md))`(`t:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential`LongStream`containing a single element. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [of](../java/util/stream/LongStream.md))`(`vararg` `values:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered stream whose elements are the specified values. |
| --- | --- |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [parallel](../java/util/stream/LongStream.md))`()` <br /> |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [peek](../java/util/stream/LongStream.md))`(`action:` ` [LongConsumer](../java/util/function/LongConsumer.md)!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [range](../java/util/stream/LongStream.md))`(`startInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endExclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endExclusive`(exclusive) by an incremental step of`1`. |
| --- | --- |
| openstatic [LongStream](../java/util/stream/LongStream.md)! | [rangeClosed](../java/util/stream/LongStream.md))`(`startInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endInclusive`(inclusive) by an incremental step of`1`. |
| abstract [OptionalLong](../java/util/OptionalLong.md)! | [reduce](../java/util/stream/LongStream.md))`(`op:` ` [LongBinaryOperator](../java/util/function/LongBinaryOperator.md)!`)` Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using an [associative](../java/util/stream/_package.md) accumulation function, and returns an`OptionalLong`describing the reduced value, if any. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduce](../java/util/stream/LongStream.md))`(`identity:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `op:` ` [LongBinaryOperator](../java/util/function/LongBinaryOperator.md)!`)` Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using the provided identity value and an [associative](../java/util/stream/_package.md) accumulation function, and returns the reduced value. |
| --- | --- |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [sequential](../java/util/stream/LongStream.md))`()` <br /> |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [skip](../java/util/stream/LongStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [sorted](../java/util/stream/LongStream.md))`()` Returns a stream consisting of the elements of this stream in sorted order. |
| --- | --- |
| abstract [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [spliterator](../java/util/stream/LongStream.md))`()` <br /> |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sum](../java/util/stream/LongStream.md))`()` Returns the sum of elements in this stream. |
| abstract [LongSummaryStatistics](../java/util/LongSummaryStatistics.md)! | [summaryStatistics](../java/util/stream/LongStream.md))`()` Returns a`LongSummaryStatistics`describing various summary data about the elements of this stream. |
| --- | --- |
| open [LongStream](../java/util/stream/LongStream.md)! | [takeWhile](../java/util/stream/LongStream.md))`(`predicate:` ` [LongPredicate](../java/util/function/LongPredicate.md)!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [toArray](../java/util/stream/LongStream.md))`()` Returns an array containing the elements of this stream. |

| Inherited functions ||
|---|---|
| From class [BaseStream](../java/util/stream/BaseStream.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/stream/BaseStream.md))`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](../java/util/stream/BaseStream.md))`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | S | [onClose](../java/util/stream/BaseStream.md))`(`closeHandler:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](../java/util/stream/BaseStream.md))method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](../java/util/stream/_package.md). <br /> | | S | [unordered](../java/util/stream/BaseStream.md))`()` <br /> Returns an equivalent stream that is [unordered](../java/util/stream/_package.md). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](../java/util/stream/_package.md). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: LongPredicate!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: LongPredicate!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements of the stream match the provided predicate, otherwise`false` |

### asDoubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asDoubleStream(): DoubleStream!
```

Returns a`DoubleStream`consisting of the elements of this stream, converted to`double`.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a`DoubleStream`consisting of the elements of this stream, converted to`double` |

### average

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun average(): OptionalDouble!
```

Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](../java/util/stream/_package.md).

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`containing the average element of this stream, or an empty optional if the stream is empty |

### boxed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun boxed(): Stream<Long!>!
```

Returns a`Stream`consisting of the elements of this stream, each boxed to a`Long`.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!>! | a`Stream`consistent of the elements of this stream, each boxed to`Long` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun builder(): LongStream.Builder!
```

Returns a builder for a`LongStream`.

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------|
| [LongStream.Builder](../java/util/stream/LongStream.Builder.md)! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: ObjLongConsumer<R>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](../java/util/stream/_package.md) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (long element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(long,java.util.function.LongBinaryOperator)](../java/util/stream/LongStream.md)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](../java/util/function/Supplier.md)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [ObjLongConsumer](../java/util/function/ObjLongConsumer.md)\<R\>!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function that must fold an element into a result container. |
| --- | --- |
| `combiner` | [BiConsumer](../java/util/function/BiConsumer.md)\<R,R\>!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function that accepts two partial result containers and merges them, which must be compatible with the accumulator function. The combiner function must fold the elements from the second result container into the first result container. |

| Return ||
|---|-----------------------------|
| R | the result of the reduction |

**See Also**

- [java.util.stream.Stream#collect(Supplier, BiConsumer, BiConsumer)](../java/util/stream/Stream.md)) 

### concat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun concat(
    a: LongStream!, 
    b: LongStream!
): LongStream!
```

Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. The resulting stream is ordered if both of the input streams are ordered, and parallel if either of the input streams is parallel. When the resulting stream is closed, the close handlers for both input streams are invoked.

This method operates on the two input streams and binds each stream to its source. As a result subsequent modifications to an input stream source may not be reflected in the concatenated stream result.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `a` | [LongStream](../java/util/stream/LongStream.md)!:the first stream |
| `b` | [LongStream](../java/util/stream/LongStream.md)!:the second stream |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | the concatenation of the two input streams |

### count

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Long
```

Returns the count of elements in this stream. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return map(e -&gt; 1L).sum();
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the count of elements in this stream |

### distinct

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun distinct(): LongStream!
```

Returns a stream consisting of the distinct elements of this stream.

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### dropWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: LongPredicate!): LongStream!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(): LongStream!
```

Returns an empty sequential`LongStream`.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: LongPredicate!): LongStream!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to each element to determine if it should be included |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): OptionalLong!
```

Returns an [OptionalLong](../java/util/OptionalLong.md) describing some element of the stream, or an empty`OptionalLong`if the stream is empty.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](../java/util/stream/LongStream.md))instead.)

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [OptionalLong](../java/util/OptionalLong.md)! | an`OptionalLong`describing some element of this stream, or an empty`OptionalLong`if the stream is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): OptionalLong!
```

Returns an [OptionalLong](../java/util/OptionalLong.md) describing the first element of this stream, or an empty`OptionalLong`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalLong](../java/util/OptionalLong.md)! | an`OptionalLong`describing the first element of this stream, or an empty`OptionalLong`if the stream is empty |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMap(mapper: LongFunction<out LongStream!>!): LongStream!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](../java/util/stream/BaseStream.md))after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongFunction](../java/util/function/LongFunction.md)\<out [LongStream](../java/util/stream/LongStream.md)!\>!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element which produces a`LongStream`of new values |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

**See Also**

- [java.util.stream.Stream#flatMap(Function)](../java/util/stream/Stream.md)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: LongConsumer!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](../java/util/function/LongConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: LongConsumer!): Unit
```

Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](../java/util/function/LongConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements |

**See Also**

- [#forEach(LongConsumer)](../java/util/stream/LongStream.md)) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun generate(s: LongSupplier!): LongStream!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`LongSupplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [LongSupplier](../java/util/function/LongSupplier.md)!:the`LongSupplier`for generated elements |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a new infinite sequential unordered`LongStream` |

### iterate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Long, 
    hasNext: LongPredicate!, 
    next: LongUnaryOperator!
): LongStream!
```

Returns a sequential ordered`LongStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. The stream terminates as soon as the`hasNext`predicate returns false.

`LongStream.iterate`should produce the same sequence of elements as produced by the corresponding for-loop: 

```kotlin
<code>for (long index=seed; hasNext.test(index); index = next.applyAsLong(index)) {
          ...
      }
  </code>
```

The resulting sequence may be empty if the`hasNext`predicate does not hold on the seed value. Otherwise the first element will be the supplied`seed`value, the next element (if present) will be the result of applying the`next`function to the`seed`value, and so on iteratively until the`hasNext`predicate indicates that the stream should terminate.

The action of applying the`hasNext`predicate to an element [*happens-before*](../java/util/concurrent/_package.md) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the initial element |
| `hasNext` | [LongPredicate](../java/util/function/LongPredicate.md)!:a predicate to apply to elements to determine when the stream must terminate. |
| `next` | [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!:a function to be applied to the previous element to produce a new element |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a new sequential`LongStream` |

### iterate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Long, 
    f: LongUnaryOperator!
): LongStream!
```

Returns an infinite sequential ordered`LongStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc.

The first element (position`0`) in the`LongStream`will be the provided`seed`. For`n > 0`, the element at position`n`, will be the result of applying the function`f`to the element at position`n - 1`.

The action of applying`f`for one element [*happens-before*](../java/util/concurrent/_package.md) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the initial element |
| `f` | [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!:a function to be applied to the previous element to produce a new element |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a new sequential`LongStream` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): PrimitiveIterator.OfLong!
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)! | the element iterator for this stream |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): LongStream!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(mapper: LongUnaryOperator!): LongStream!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongUnaryOperator](../java/util/function/LongUnaryOperator.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### mapMulti

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMulti(mapper: LongStream.LongMapMultiConsumer!): LongStream!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java/util/function/LongConsumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](../java/util/stream/_package.md).

If the [consumer](../java/util/function/LongConsumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongStream.LongMapMultiConsumer](../java/util/stream/LongStream.LongMapMultiConsumer.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function that generates replacement elements |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

**See Also**

- [java.util.stream.Stream#mapMulti](../java/util/stream/Stream.md)) 

### mapToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToDouble(mapper: LongToDoubleFunction!): DoubleStream!
```

Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongToDoubleFunction](../java/util/function/LongToDoubleFunction.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### mapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToInt(mapper: LongToIntFunction!): IntStream!
```

Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongToIntFunction](../java/util/function/LongToIntFunction.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](../java/util/stream/IntStream.md)! | the new stream |

### mapToObj

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> mapToObj(mapper: LongFunction<out U>!): Stream<U>!
```

Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | the element type of the new stream |
| `mapper` | [LongFunction](../java/util/function/LongFunction.md)\<outU\>!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [Stream](../java/util/stream/Stream.md)<U>! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(): OptionalLong!
```

Returns an`OptionalLong`describing the maximum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return reduce(Long::max);
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [OptionalLong](../java/util/OptionalLong.md)! | an`OptionalLong`containing the maximum element of this stream, or an empty`OptionalLong`if the stream is empty |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(): OptionalLong!
```

Returns an`OptionalLong`describing the minimum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return reduce(Long::min);
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [OptionalLong](../java/util/OptionalLong.md)! | an`OptionalLong`containing the minimum element of this stream, or an empty`OptionalLong`if the stream is empty |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: LongPredicate!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either no elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(t: Long): LongStream!
```

Returns a sequential`LongStream`containing a single element.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------|
| `t` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the single element |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a singleton sequential stream |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(vararg values: Long): LongStream!
```

Returns a sequential ordered stream whose elements are the specified values.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `values` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the elements of the new stream |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): LongStream!
```

| Return ||
|--------------------------------------------------------------------------------------------|-------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a parallel stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: LongConsumer!): LongStream!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](../java/util/stream/_package.md).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](../java/util/function/LongConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements as they are consumed from the stream |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### range

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun range(
    startInclusive: Long, 
    endExclusive: Long
): LongStream!
```

Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endExclusive`(exclusive) by an incremental step of`1`.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------|
| `startInclusive` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (inclusive) initial value |
| `endExclusive` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the exclusive upper bound |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a sequential`LongStream`for the range of`long`elements |

### rangeClosed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rangeClosed(
    startInclusive: Long, 
    endInclusive: Long
): LongStream!
```

Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endInclusive`(inclusive) by an incremental step of`1`.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------|
| `startInclusive` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (inclusive) initial value |
| `endInclusive` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the inclusive upper bound |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a sequential`LongStream`for the range of`long`elements |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(op: LongBinaryOperator!): OptionalLong!
```

Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using an [associative](../java/util/stream/_package.md) accumulation function, and returns an`OptionalLong`describing the reduced value, if any. This is equivalent to: 

```kotlin
<code>boolean foundAny = false;
      long result = null;
      for (long element : this stream) {
          if (!foundAny) {
              foundAny = true;
              result = element;
          }
          else
              result = accumulator.applyAsLong(result, element);
      }
      return foundAny ? OptionalLong.of(result) : OptionalLong.empty();
  </code>
```
but is not constrained to execute sequentially.

<br />

The`accumulator`function must be an [associative](../java/util/stream/_package.md) function.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [LongBinaryOperator](../java/util/function/LongBinaryOperator.md)!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function for combining two values |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------|
| [OptionalLong](../java/util/OptionalLong.md)! | the result of the reduction |

**See Also**

- [#reduce(long, LongBinaryOperator)](../java/util/stream/LongStream.md)) 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: Long, 
    op: LongBinaryOperator!
): Long
```

Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using the provided identity value and an [associative](../java/util/stream/_package.md) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>long result = identity;
      for (long element : this stream)
          result = accumulator.applyAsLong(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`x`,`accumulator.apply(identity, x)`is equal to`x`. The`accumulator`function must be an [associative](../java/util/stream/_package.md) function.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity value for the accumulating function |
| `op` | [LongBinaryOperator](../java/util/function/LongBinaryOperator.md)!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function for combining two values |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the result of the reduction |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#sum()>
- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#min()>
- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#max()>
- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#average()> 

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): LongStream!
```

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a sequential stream |

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): LongStream!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): LongStream!
```

Returns a stream consisting of the elements of this stream in sorted order.

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator.OfLong!
```

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | the element spliterator for this stream |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sum(): Long
```

Returns the sum of elements in this stream. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return reduce(0, Long::sum);
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum of elements in this stream |

### summaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun summaryStatistics(): LongSummaryStatistics!
```

Returns a`LongSummaryStatistics`describing various summary data about the elements of this stream. This is a special case of a [reduction](../java/util/stream/_package.md).

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [LongSummaryStatistics](../java/util/LongSummaryStatistics.md)! | a`LongSummaryStatistics`describing various summary data about the elements of this stream |

### takeWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: LongPredicate!): LongStream!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](../java/util/function/LongPredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): LongArray!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | an array containing the elements of this stream |
