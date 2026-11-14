# DoubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleStream

```
interface DoubleStream : BaseStream<Double!, DoubleStream!>
```

| [java.util.stream.DoubleStream](../java/util/stream/DoubleStream.md) |

A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. This is the`double`primitive specialization of .

The following example illustrates an aggregate operation using [Stream](../java/util/stream/Stream.md) and [DoubleStream](../java/util/stream/DoubleStream.md), computing the sum of the weights of the red widgets: 

```kotlin
<code>double sum = widgets.stream()
                          .filter(w -&gt; w.getColor() == RED)
                          .mapToDouble(w -&gt; w.getWeight())
                          .sum();
  </code>
```
See the class documentation for [Stream](../java/util/stream/Stream.md) and the package documentation for [java.util.stream](../java/util/stream/_package.md) for additional specification of streams, stream operations, stream pipelines, and parallelism.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](../java/util/stream/DoubleStream.Builder.md) A mutable builder for a`DoubleStream`. |
| abstract | [DoubleMapMultiConsumer](../java/util/stream/DoubleStream.DoubleMapMultiConsumer.md) Represents an operation that accepts a`double`-valued argument and a DoubleConsumer, and returns no result. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns whether any elements of this stream match the provided predicate. |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [average](../java/util/stream/DoubleStream.md))`()` Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. |
| --- | --- |
| abstract [Stream](../java/util/stream/Stream.md)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | [boxed](../java/util/stream/DoubleStream.md))`()` Returns a`Stream`consisting of the elements of this stream, boxed to`Double`. |
| openstatic [DoubleStream.Builder](../java/util/stream/DoubleStream.Builder.md)! | [builder](../java/util/stream/DoubleStream.md))`()` Returns a builder for a`DoubleStream`. |
| abstractR | [collect](../java/util/stream/DoubleStream.md))`(`supplier:` ` [Supplier](../java/util/function/Supplier.md)<R>!`, `accumulator:` ` [ObjDoubleConsumer](../java/util/function/ObjDoubleConsumer.md)<R>!`, `combiner:` ` [BiConsumer](../java/util/function/BiConsumer.md)<R,` `R>!`)` Performs a [mutable reduction](../java/util/stream/_package.md) operation on the elements of this stream. |
| --- | --- |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [concat](../java/util/stream/DoubleStream.md))`(`a:` ` [DoubleStream](../java/util/stream/DoubleStream.md)!`, `b:` ` [DoubleStream](../java/util/stream/DoubleStream.md)!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](../java/util/stream/DoubleStream.md))`()` Returns the count of elements in this stream. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [distinct](../java/util/stream/DoubleStream.md))`()` Returns a stream consisting of the distinct elements of this stream. |
| --- | --- |
| open [DoubleStream](../java/util/stream/DoubleStream.md)! | [dropWhile](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [empty](../java/util/stream/DoubleStream.md))`()` Returns an empty sequential`DoubleStream`. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [filter](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| --- | --- |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [findAny](../java/util/stream/DoubleStream.md))`()` Returns an [OptionalDouble](../java/util/OptionalDouble.md) describing some element of the stream, or an empty`OptionalDouble`if the stream is empty. |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [findFirst](../java/util/stream/DoubleStream.md))`()` Returns an [OptionalDouble](../java/util/OptionalDouble.md) describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [flatMap](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleFunction](../java/util/function/DoubleFunction.md)<out` ` [DoubleStream](../java/util/stream/DoubleStream.md)!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../java/util/stream/DoubleStream.md))`(`action:` ` [DoubleConsumer](../java/util/function/DoubleConsumer.md)!`)` Performs an action for each element of this stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](../java/util/stream/DoubleStream.md))`(`action:` ` [DoubleConsumer](../java/util/function/DoubleConsumer.md)!`)` Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order. |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [generate](../java/util/stream/DoubleStream.md))`(`s:` ` [DoubleSupplier](../java/util/function/DoubleSupplier.md)!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`DoubleSupplier`. |
| --- | --- |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [iterate](../java/util/stream/DoubleStream.md))`(`seed:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `hasNext:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`, `next:` ` [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!`)` Returns a sequential ordered`DoubleStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [iterate](../java/util/stream/DoubleStream.md))`(`seed:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `f:` ` [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!`)` Returns an infinite sequential ordered`DoubleStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| abstract [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)! | [iterator](../java/util/stream/DoubleStream.md))`()` <br /> |
| --- | --- |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [limit](../java/util/stream/DoubleStream.md))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [map](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| open [DoubleStream](../java/util/stream/DoubleStream.md)! | [mapMulti](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleStream.DoubleMapMultiConsumer](../java/util/stream/DoubleStream.DoubleMapMultiConsumer.md)!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| --- | --- |
| abstract [IntStream](../java/util/stream/IntStream.md)! | [mapToInt](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleToIntFunction](../java/util/function/DoubleToIntFunction.md)!`)` Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [LongStream](../java/util/stream/LongStream.md)! | [mapToLong](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleToLongFunction](../java/util/function/DoubleToLongFunction.md)!`)` Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [Stream](../java/util/stream/Stream.md)\<U\>! | [mapToObj](../java/util/stream/DoubleStream.md))`(`mapper:` ` [DoubleFunction](../java/util/function/DoubleFunction.md)<out` `U>!`)` Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [max](../java/util/stream/DoubleStream.md))`()` Returns an`OptionalDouble`describing the maximum element of this stream, or an empty OptionalDouble if this stream is empty. |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [min](../java/util/stream/DoubleStream.md))`()` Returns an`OptionalDouble`describing the minimum element of this stream, or an empty OptionalDouble if this stream is empty. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns whether no elements of this stream match the provided predicate. |
| --- | --- |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [of](../java/util/stream/DoubleStream.md))`(`t:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a sequential`DoubleStream`containing a single element. |
| openstatic [DoubleStream](../java/util/stream/DoubleStream.md)! | [of](../java/util/stream/DoubleStream.md))`(`vararg` `values:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a sequential ordered stream whose elements are the specified values. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [parallel](../java/util/stream/DoubleStream.md))`()` <br /> |
| --- | --- |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [peek](../java/util/stream/DoubleStream.md))`(`action:` ` [DoubleConsumer](../java/util/function/DoubleConsumer.md)!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduce](../java/util/stream/DoubleStream.md))`(`identity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `op:` ` [DoubleBinaryOperator](../java/util/function/DoubleBinaryOperator.md)!`)` Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using the provided identity value and an [associative](../java/util/stream/_package.md) accumulation function, and returns the reduced value. |
| abstract [OptionalDouble](../java/util/OptionalDouble.md)! | [reduce](../java/util/stream/DoubleStream.md))`(`op:` ` [DoubleBinaryOperator](../java/util/function/DoubleBinaryOperator.md)!`)` Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using an [associative](../java/util/stream/_package.md) accumulation function, and returns an`OptionalDouble`describing the reduced value, if any. |
| --- | --- |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [sequential](../java/util/stream/DoubleStream.md))`()` <br /> |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [skip](../java/util/stream/DoubleStream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| abstract [DoubleStream](../java/util/stream/DoubleStream.md)! | [sorted](../java/util/stream/DoubleStream.md))`()` Returns a stream consisting of the elements of this stream in sorted order. |
| --- | --- |
| abstract [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [spliterator](../java/util/stream/DoubleStream.md))`()` <br /> |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sum](../java/util/stream/DoubleStream.md))`()` Returns the sum of elements in this stream. |
| abstract [DoubleSummaryStatistics](../java/util/DoubleSummaryStatistics.md)! | [summaryStatistics](../java/util/stream/DoubleStream.md))`()` Returns a`DoubleSummaryStatistics`describing various summary data about the elements of this stream. |
| --- | --- |
| open [DoubleStream](../java/util/stream/DoubleStream.md)! | [takeWhile](../java/util/stream/DoubleStream.md))`(`predicate:` ` [DoublePredicate](../java/util/function/DoublePredicate.md)!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | [toArray](../java/util/stream/DoubleStream.md))`()` Returns an array containing the elements of this stream. |

| Inherited functions ||
|---|---|
| From class [BaseStream](../java/util/stream/BaseStream.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/stream/BaseStream.md))`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](../java/util/stream/BaseStream.md))`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | S | [onClose](../java/util/stream/BaseStream.md))`(`closeHandler:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](../java/util/stream/BaseStream.md))method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](../java/util/stream/_package.md). <br /> | | S | [unordered](../java/util/stream/BaseStream.md))`()` <br /> Returns an equivalent stream that is [unordered](../java/util/stream/_package.md). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](../java/util/stream/_package.md). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: DoublePredicate!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: DoublePredicate!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements of the stream match the provided predicate, otherwise`false` |

### average

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun average(): OptionalDouble!
```

Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty.

The computed average can vary numerically and have the special case behavior as computing the sum; see [sum](../java/util/stream/DoubleStream.md))for details.

The average is a special case of a [reduction](../java/util/stream/_package.md).

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`containing the average element of this stream, or an empty optional if the stream is empty |

### boxed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun boxed(): Stream<Double!>!
```

Returns a`Stream`consisting of the elements of this stream, boxed to`Double`.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!>! | a`Stream`consistent of the elements of this stream, each boxed to a`Double` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun builder(): DoubleStream.Builder!
```

Returns a builder for a`DoubleStream`.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------|
| [DoubleStream.Builder](../java/util/stream/DoubleStream.Builder.md)! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: ObjDoubleConsumer<R>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](../java/util/stream/_package.md) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (double element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(double,java.util.function.DoubleBinaryOperator)](../java/util/stream/DoubleStream.md)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](../java/util/function/Supplier.md)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [ObjDoubleConsumer](../java/util/function/ObjDoubleConsumer.md)\<R\>!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function that must fold an element into a result container. |
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
    a: DoubleStream!, 
    b: DoubleStream!
): DoubleStream!
```

Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. The resulting stream is ordered if both of the input streams are ordered, and parallel if either of the input streams is parallel. When the resulting stream is closed, the close handlers for both input streams are invoked.

This method operates on the two input streams and binds each stream to its source. As a result subsequent modifications to an input stream source may not be reflected in the concatenated stream result.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `a` | [DoubleStream](../java/util/stream/DoubleStream.md)!:the first stream |
| `b` | [DoubleStream](../java/util/stream/DoubleStream.md)!:the second stream |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the concatenation of the two input streams |

### count

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Long
```

Returns the count of elements in this stream. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return mapToLong(e -&gt; 1L).sum();
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
abstract fun distinct(): DoubleStream!
```

Returns a stream consisting of the distinct elements of this stream. The elements are compared for equality according to [java.lang.Double#compare(double, double)](../java/lang/Double.md)).

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the result stream |

### dropWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: DoublePredicate!): DoubleStream!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(): DoubleStream!
```

Returns an empty sequential`DoubleStream`.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: DoublePredicate!): DoubleStream!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to each element to determine if it should be included |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): OptionalDouble!
```

Returns an [OptionalDouble](../java/util/OptionalDouble.md) describing some element of the stream, or an empty`OptionalDouble`if the stream is empty.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](../java/util/stream/DoubleStream.md))instead.)

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`describing some element of this stream, or an empty`OptionalDouble`if the stream is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): OptionalDouble!
```

Returns an [OptionalDouble](../java/util/OptionalDouble.md) describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMap(mapper: DoubleFunction<out DoubleStream!>!): DoubleStream!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](../java/util/stream/BaseStream.md))after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleFunction](../java/util/function/DoubleFunction.md)\<out [DoubleStream](../java/util/stream/DoubleStream.md)!\>!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element which produces a`DoubleStream`of new values |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

**See Also**

- [java.util.stream.Stream#flatMap(Function)](../java/util/stream/Stream.md)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: DoubleConsumer!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](../java/util/function/DoubleConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: DoubleConsumer!): Unit
```

Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](../java/util/function/DoubleConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements |

**See Also**

- [#forEach(DoubleConsumer)](../java/util/stream/DoubleStream.md)) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun generate(s: DoubleSupplier!): DoubleStream!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`DoubleSupplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [DoubleSupplier](../java/util/function/DoubleSupplier.md)!:the`DoubleSupplier`for generated elements |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a new infinite sequential unordered`DoubleStream` |

### iterate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Double, 
    hasNext: DoublePredicate!, 
    next: DoubleUnaryOperator!
): DoubleStream!
```

Returns a sequential ordered`DoubleStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. The stream terminates as soon as the`hasNext`predicate returns false.

`DoubleStream.iterate`should produce the same sequence of elements as produced by the corresponding for-loop: 

```kotlin
<code>for (double index=seed; hasNext.test(index); index = next.applyAsDouble(index)) {
          ...
      }
  </code>
```

The resulting sequence may be empty if the`hasNext`predicate does not hold on the seed value. Otherwise the first element will be the supplied`seed`value, the next element (if present) will be the result of applying the`next`function to the`seed`value, and so on iteratively until the`hasNext`predicate indicates that the stream should terminate.

The action of applying the`hasNext`predicate to an element [*happens-before*](../java/util/concurrent/_package.md) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the initial element |
| `hasNext` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a predicate to apply to elements to determine when the stream must terminate. |
| `next` | [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!:a function to be applied to the previous element to produce a new element |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a new sequential`DoubleStream` |

### iterate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Double, 
    f: DoubleUnaryOperator!
): DoubleStream!
```

Returns an infinite sequential ordered`DoubleStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc.

The first element (position`0`) in the`DoubleStream`will be the provided`seed`. For`n > 0`, the element at position`n`, will be the result of applying the function`f`to the element at position`n - 1`.

The action of applying`f`for one element [*happens-before*](../java/util/concurrent/_package.md) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the initial element |
| `f` | [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!:a function to be applied to the previous element to produce a new element |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a new sequential`DoubleStream` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): PrimitiveIterator.OfDouble!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)! | the element iterator for this stream |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): DoubleStream!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(mapper: DoubleUnaryOperator!): DoubleStream!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleUnaryOperator](../java/util/function/DoubleUnaryOperator.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### mapMulti

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMulti(mapper: DoubleStream.DoubleMapMultiConsumer!): DoubleStream!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java/util/function/DoubleConsumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](../java/util/stream/_package.md).

If the [consumer](../java/util/function/DoubleConsumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleStream.DoubleMapMultiConsumer](../java/util/stream/DoubleStream.DoubleMapMultiConsumer.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function that generates replacement elements |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

**See Also**

- [java.util.stream.Stream#mapMulti](../java/util/stream/Stream.md)) 

### mapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToInt(mapper: DoubleToIntFunction!): IntStream!
```

Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleToIntFunction](../java/util/function/DoubleToIntFunction.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](../java/util/stream/IntStream.md)! | the new stream |

### mapToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToLong(mapper: DoubleToLongFunction!): LongStream!
```

Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleToLongFunction](../java/util/function/DoubleToLongFunction.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](../java/util/stream/LongStream.md)! | the new stream |

### mapToObj

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> mapToObj(mapper: DoubleFunction<out U>!): Stream<U>!
```

Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | the element type of the new stream |
| `mapper` | [DoubleFunction](../java/util/function/DoubleFunction.md)\<outU\>!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [Stream](../java/util/stream/Stream.md)<U>! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(): OptionalDouble!
```

Returns an`OptionalDouble`describing the maximum element of this stream, or an empty OptionalDouble if this stream is empty. The maximum element will be`Double.NaN`if any stream element was NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return reduce(Double::max);
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`containing the maximum element of this stream, or an empty optional if the stream is empty |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(): OptionalDouble!
```

Returns an`OptionalDouble`describing the minimum element of this stream, or an empty OptionalDouble if this stream is empty. The minimum element will be`Double.NaN`if any stream element was NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. This is a special case of a [reduction](../java/util/stream/_package.md) and is equivalent to: 

```kotlin
<code>return reduce(Double::min);
  </code>
```

<br />

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | an`OptionalDouble`containing the minimum element of this stream, or an empty optional if the stream is empty |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: DoublePredicate!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either no elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(t: Double): DoubleStream!
```

Returns a sequential`DoubleStream`containing a single element.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------|
| `t` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the single element |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a singleton sequential stream |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(vararg values: Double): DoubleStream!
```

Returns a sequential ordered stream whose elements are the specified values.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------|
| `values` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the elements of the new stream |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): DoubleStream!
```

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a parallel stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: DoubleConsumer!): DoubleStream!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](../java/util/stream/_package.md).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](../java/util/function/DoubleConsumer.md)!:a [non-interfering](../java/util/stream/_package.md) action to perform on the elements as they are consumed from the stream |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: Double, 
    op: DoubleBinaryOperator!
): Double
```

Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using the provided identity value and an [associative](../java/util/stream/_package.md) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>double result = identity;
      for (double element : this stream)
          result = accumulator.applyAsDouble(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`x`,`accumulator.apply(identity, x)`is equal to`x`. The`accumulator`function must be an [associative](../java/util/stream/_package.md) function.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity value for the accumulating function |
| `op` | [DoubleBinaryOperator](../java/util/function/DoubleBinaryOperator.md)!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function for combining two values |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the result of the reduction |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#sum()>
- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#min()>
- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#max()>
- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#average()> 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(op: DoubleBinaryOperator!): OptionalDouble!
```

Performs a [reduction](../java/util/stream/_package.md) on the elements of this stream, using an [associative](../java/util/stream/_package.md) accumulation function, and returns an`OptionalDouble`describing the reduced value, if any. This is equivalent to: 

```kotlin
<code>boolean foundAny = false;
      double result = null;
      for (double element : this stream) {
          if (!foundAny) {
              foundAny = true;
              result = element;
          }
          else
              result = accumulator.applyAsDouble(result, element);
      }
      return foundAny ? OptionalDouble.of(result) : OptionalDouble.empty();
  </code>
```
but is not constrained to execute sequentially.

<br />

The`accumulator`function must be an [associative](../java/util/stream/_package.md) function.

This is a [terminal operation](../java/util/stream/_package.md).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [DoubleBinaryOperator](../java/util/function/DoubleBinaryOperator.md)!:an [associative](../java/util/stream/_package.md), [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) function for combining two values |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [OptionalDouble](../java/util/OptionalDouble.md)! | the result of the reduction |

**See Also**

- [#reduce(double, DoubleBinaryOperator)](../java/util/stream/DoubleStream.md)) 

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): DoubleStream!
```

| Return ||
|------------------------------------------------------------------------------------------------|---------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a sequential stream |

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): DoubleStream!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): DoubleStream!
```

Returns a stream consisting of the elements of this stream in sorted order. The elements are compared for equality according to [java.lang.Double#compare(double, double)](../java/lang/Double.md)).

This is a [stateful intermediate operation](../java/util/stream/_package.md).

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the result stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator.OfDouble!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | the element spliterator for this stream |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sum(): Double
```

Returns the sum of elements in this stream. Summation is a special case of a [reduction](../java/util/stream/_package.md). If floating-point summation were exact, this method would be equivalent to: 

```kotlin
<code>return reduce(0, Double::sum);
  </code>
```
However, since floating-point summation is not exact, the above code is not necessarily equivalent to the summation computation done by this method.

<br />

The value of a floating-point sum is a function both of the input values as well as the order of addition operations. The order of addition operations of this method is intentionally not defined to allow for implementation flexibility to improve the speed and accuracy of the computed result. In particular, this method may be implemented using compensated summation or other technique to reduce the error bound in the numerical sum compared to a simple summation of`double`values. Because of the unspecified order of operations and the possibility of using differing summation schemes, the output of this method may vary on the same input elements.

Various conditions can result in a non-finite sum being computed. This can occur even if the all the elements being summed are finite. If any element is non-finite, the sum will be non-finite:

- If any element is a NaN, then the final sum will be NaN.
- If the elements contain one or more infinities, the sum will be infinite or NaN.
 - If the elements contain infinities of opposite sign, the sum will be NaN.
 - If the elements contain infinities of one sign and an intermediate sum overflows to an infinity of the opposite sign, the sum may be NaN.

It is possible for intermediate sums of finite values to overflow into opposite-signed infinities; if that occurs, the final sum will be NaN even if the elements are all finite. If all the elements are zero, the sign of zero is*not* guaranteed to be preserved in the final sum.

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------|------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum of elements in this stream |

### summaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun summaryStatistics(): DoubleSummaryStatistics!
```

Returns a`DoubleSummaryStatistics`describing various summary data about the elements of this stream. This is a special case of a [reduction](../java/util/stream/_package.md).

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [DoubleSummaryStatistics](../java/util/DoubleSummaryStatistics.md)! | a`DoubleSummaryStatistics`describing various summary data about the elements of this stream |

### takeWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: DoublePredicate!): DoubleStream!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](../java/util/function/DoublePredicate.md)!:a [non-interfering](../java/util/stream/_package.md), [stateless](../java/util/stream/_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): DoubleArray!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | an array containing the elements of this stream |
