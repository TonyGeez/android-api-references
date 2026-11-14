# DoubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleStream

```
interface DoubleStream : BaseStream<Double!, DoubleStream!>
```

| [java.util.stream.DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#) |

A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. This is the`double`primitive specialization of .

The following example illustrates an aggregate operation using [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#), computing the sum of the weights of the red widgets: 

```kotlin
<code>double sum = widgets.stream()
                          .filter(w -&gt; w.getColor() == RED)
                          .mapToDouble(w -&gt; w.getWeight())
                          .sum();
  </code>
```
See the class documentation for [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and the package documentation for [java.util.stream](https://developer.android.com/reference/kotlin/java/util/stream/package-summary) for additional specification of streams, stream operations, stream pipelines, and parallelism.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.Builder) A mutable builder for a`DoubleStream`. |
| abstract | [DoubleMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.DoubleMapMultiConsumer) Represents an operation that accepts a`double`-valued argument and a DoubleConsumer, and returns no result. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#allMatch(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#anyMatch(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns whether any elements of this stream match the provided predicate. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [average](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#average())`()` Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | [boxed](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#boxed())`()` Returns a`Stream`consisting of the elements of this stream, boxed to`Double`. |
| openstatic [DoubleStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.Builder)! | [builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#builder())`()` Returns a builder for a`DoubleStream`. |
| abstractR | [collect](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#collect(java.util.function.Supplier,%20java.util.function.ObjDoubleConsumer,%20java.util.function.BiConsumer))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<R>!`, `accumulator:` ` [ObjDoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjDoubleConsumer.html#)<R>!`, `combiner:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<R,` `R>!`)` Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [concat](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#concat(java.util.stream.DoubleStream,%20java.util.stream.DoubleStream))`(`a:` ` [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!`, `b:` ` [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#count())`()` Returns the count of elements in this stream. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [distinct](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#distinct())`()` Returns a stream consisting of the distinct elements of this stream. |
| open [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [dropWhile](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#dropWhile(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [empty](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#empty())`()` Returns an empty sequential`DoubleStream`. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [filter](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#filter(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [findAny](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#findAny())`()` Returns an [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#) describing some element of the stream, or an empty`OptionalDouble`if the stream is empty. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [findFirst](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#findFirst())`()` Returns an [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#) describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [flatMap](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#flatMap(java.util.function.DoubleFunction))`(`mapper:` ` [DoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction.html#)<out` ` [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#forEach(java.util.function.DoubleConsumer))`(`action:` ` [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!`)` Performs an action for each element of this stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#forEachOrdered(java.util.function.DoubleConsumer))`(`action:` ` [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!`)` Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [generate](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#generate(java.util.function.DoubleSupplier))`(`s:` ` [DoubleSupplier](https://developer.android.com/reference/kotlin/java/util/function/DoubleSupplier.html#)!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`DoubleSupplier`. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#iterate(kotlin.Double,%20java.util.function.DoublePredicate,%20java.util.function.DoubleUnaryOperator))`(`seed:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `hasNext:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`, `next:` ` [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!`)` Returns a sequential ordered`DoubleStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#iterate(kotlin.Double,%20java.util.function.DoubleUnaryOperator))`(`seed:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `f:` ` [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!`)` Returns an infinite sequential ordered`DoubleStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| abstract [PrimitiveIterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble.html#)! | [iterator](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#iterator())`()` <br /> |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [limit](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#limit(kotlin.Long))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [map](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#map(java.util.function.DoubleUnaryOperator))`(`mapper:` ` [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| open [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#mapMulti(java.util.stream.DoubleStream.DoubleMapMultiConsumer))`(`mapper:` ` [DoubleStream.DoubleMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.DoubleMapMultiConsumer)!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | [mapToInt](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#mapToInt(java.util.function.DoubleToIntFunction))`(`mapper:` ` [DoubleToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleToIntFunction.html#)!`)` Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [mapToLong](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#mapToLong(java.util.function.DoubleToLongFunction))`(`mapper:` ` [DoubleToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleToLongFunction.html#)!`)` Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<U\>! | [mapToObj](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#mapToObj(java.util.function.DoubleFunction))`(`mapper:` ` [DoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction.html#)<out` `U>!`)` Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [max](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#max())`()` Returns an`OptionalDouble`describing the maximum element of this stream, or an empty OptionalDouble if this stream is empty. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [min](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#min())`()` Returns an`OptionalDouble`describing the minimum element of this stream, or an empty OptionalDouble if this stream is empty. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#noneMatch(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns whether no elements of this stream match the provided predicate. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#of(kotlin.Double))`(`t:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a sequential`DoubleStream`containing a single element. |
| openstatic [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#of(kotlin.Double))`(`vararg` `values:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a sequential ordered stream whose elements are the specified values. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [parallel](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#parallel())`()` <br /> |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [peek](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#peek(java.util.function.DoubleConsumer))`(`action:` ` [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#reduce(kotlin.Double,%20java.util.function.DoubleBinaryOperator))`(`identity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `op:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#reduce(java.util.function.DoubleBinaryOperator))`(`op:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalDouble`describing the reduced value, if any. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [sequential](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#sequential())`()` <br /> |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [skip](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [sorted](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#sorted())`()` Returns a stream consisting of the elements of this stream in sorted order. |
| abstract [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)! | [spliterator](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#spliterator())`()` <br /> |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sum](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#sum())`()` Returns the sum of elements in this stream. |
| abstract [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#)! | [summaryStatistics](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#summaryStatistics())`()` Returns a`DoubleSummaryStatistics`describing various summary data about the elements of this stream. |
| open [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | [takeWhile](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#takeWhile(java.util.function.DoublePredicate))`(`predicate:` ` [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | [toArray](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#toArray())`()` Returns an array containing the elements of this stream. |

| Inherited functions ||
|---|---|
| From class [BaseStream](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#isParallel())`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | S | [onClose](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#onClose(java.lang.Runnable))`(`closeHandler:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | | S | [unordered](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#unordered())`()` <br /> Returns an equivalent stream that is [unordered](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Ordering). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: DoublePredicate!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: DoublePredicate!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements of the stream match the provided predicate, otherwise`false` |

### average

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun average(): OptionalDouble!
```

Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty.

The computed average can vary numerically and have the special case behavior as computing the sum; see [sum](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#sum())for details.

The average is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction).

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`containing the average element of this stream, or an empty optional if the stream is empty |

### boxed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun boxed(): Stream<Double!>!
```

Returns a`Stream`consisting of the elements of this stream, boxed to`Double`.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!>! | a`Stream`consistent of the elements of this stream, each boxed to a`Double` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun builder(): DoubleStream.Builder!
```

Returns a builder for a`DoubleStream`.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------|
| [DoubleStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.Builder)! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: ObjDoubleConsumer<R>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (double element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(double,java.util.function.DoubleBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#reduce(kotlin.Double,%20java.util.function.DoubleBinaryOperator)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [ObjDoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjDoubleConsumer.html#)\<R\>!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that must fold an element into a result container. |
| `combiner` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<R,R\>!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that accepts two partial result containers and merges them, which must be compatible with the accumulator function. The combiner function must fold the elements from the second result container into the first result container. |

| Return ||
|---|-----------------------------|
| R | the result of the reduction |

**See Also**

- [java.util.stream.Stream#collect(Supplier, BiConsumer, BiConsumer)](https://developer.android.com/reference/kotlin/java/util/stream/Stream#collect(java.util.function.Supplier,%20java.util.function.BiConsumer,%20java.util.function.BiConsumer)) 

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
| `a` | [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!:the first stream |
| `b` | [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!:the second stream |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the concatenation of the two input streams |

### count

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Long
```

Returns the count of elements in this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return mapToLong(e -&gt; 1L).sum();
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the count of elements in this stream |

### distinct

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun distinct(): DoubleStream!
```

Returns a stream consisting of the distinct elements of this stream. The elements are compared for equality according to [java.lang.Double#compare(double, double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#compare(kotlin.Double,%20kotlin.Double)).

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the result stream |

### dropWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: DoublePredicate!): DoubleStream!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(): DoubleStream!
```

Returns an empty sequential`DoubleStream`.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: DoublePredicate!): DoubleStream!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to each element to determine if it should be included |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): OptionalDouble!
```

Returns an [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#) describing some element of the stream, or an empty`OptionalDouble`if the stream is empty.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#findFirst())instead.)

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`describing some element of this stream, or an empty`OptionalDouble`if the stream is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): OptionalDouble!
```

Returns an [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#) describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`describing the first element of this stream, or an empty`OptionalDouble`if the stream is empty |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMap(mapper: DoubleFunction<out DoubleStream!>!): DoubleStream!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction.html#)\<out [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)!\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element which produces a`DoubleStream`of new values |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#flatMap(Function)](https://developer.android.com/reference/kotlin/java/util/stream/Stream#flatMap(java.util.function.Function)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: DoubleConsumer!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: DoubleConsumer!): Unit
```

Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

**See Also**

- [#forEach(DoubleConsumer)](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#forEach(java.util.function.DoubleConsumer)) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun generate(s: DoubleSupplier!): DoubleStream!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`DoubleSupplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [DoubleSupplier](https://developer.android.com/reference/kotlin/java/util/function/DoubleSupplier.html#)!:the`DoubleSupplier`for generated elements |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a new infinite sequential unordered`DoubleStream` |

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

The action of applying the`hasNext`predicate to an element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the initial element |
| `hasNext` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a predicate to apply to elements to determine when the stream must terminate. |
| `next` | [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a new sequential`DoubleStream` |

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

The action of applying`f`for one element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the initial element |
| `f` | [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a new sequential`DoubleStream` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): PrimitiveIterator.OfDouble!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [PrimitiveIterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble.html#)! | the element iterator for this stream |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): DoubleStream!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(mapper: DoubleUnaryOperator!): DoubleStream!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleUnaryOperator.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### mapMulti

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMulti(mapper: DoubleStream.DoubleMapMultiConsumer!): DoubleStream!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

If the [consumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleStream.DoubleMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.DoubleMapMultiConsumer)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that generates replacement elements |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/Stream#mapMulti(java.util.function.BiConsumer)) 

### mapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToInt(mapper: DoubleToIntFunction!): IntStream!
```

Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleToIntFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | the new stream |

### mapToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToLong(mapper: DoubleToLongFunction!): LongStream!
```

Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [DoubleToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleToLongFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | the new stream |

### mapToObj

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> mapToObj(mapper: DoubleFunction<out U>!): Stream<U>!
```

Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | the element type of the new stream |
| `mapper` | [DoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/DoubleFunction.html#)\<outU\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<U>! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(): OptionalDouble!
```

Returns an`OptionalDouble`describing the maximum element of this stream, or an empty OptionalDouble if this stream is empty. The maximum element will be`Double.NaN`if any stream element was NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Double::max);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`containing the maximum element of this stream, or an empty optional if the stream is empty |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(): OptionalDouble!
```

Returns an`OptionalDouble`describing the minimum element of this stream, or an empty OptionalDouble if this stream is empty. The minimum element will be`Double.NaN`if any stream element was NaN. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Double::min);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`containing the minimum element of this stream, or an empty optional if the stream is empty |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: DoublePredicate!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

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
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a singleton sequential stream |

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
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): DoubleStream!
```

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a parallel stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: DoubleConsumer!): DoubleStream!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements as they are consumed from the stream |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: Double, 
    op: DoubleBinaryOperator!
): Double
```

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>double result = identity;
      for (double element : this stream)
          result = accumulator.applyAsDouble(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`x`,`accumulator.apply(identity, x)`is equal to`x`. The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity value for the accumulating function |
| `op` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

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

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalDouble`describing the reduced value, if any. This is equivalent to: 

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

The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | the result of the reduction |

**See Also**

- [#reduce(double, DoubleBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#reduce(kotlin.Double,%20java.util.function.DoubleBinaryOperator)) 

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): DoubleStream!
```

| Return ||
|------------------------------------------------------------------------------------------------|---------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | a sequential stream |

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): DoubleStream!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): DoubleStream!
```

Returns a stream consisting of the elements of this stream in sorted order. The elements are compared for equality according to [java.lang.Double#compare(double, double)](https://developer.android.com/reference/kotlin/java/lang/Double.html#compare(kotlin.Double,%20kotlin.Double)).

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the result stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator.OfDouble!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)! | the element spliterator for this stream |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sum(): Double
```

Returns the sum of elements in this stream. Summation is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction). If floating-point summation were exact, this method would be equivalent to: 

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

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------|------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum of elements in this stream |

### summaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun summaryStatistics(): DoubleSummaryStatistics!
```

Returns a`DoubleSummaryStatistics`describing various summary data about the elements of this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction).

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#)! | a`DoubleSummaryStatistics`describing various summary data about the elements of this stream |

### takeWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: DoublePredicate!): DoubleStream!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [DoublePredicate](https://developer.android.com/reference/kotlin/java/util/function/DoublePredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream#)! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): DoubleArray!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | an array containing the elements of this stream |
