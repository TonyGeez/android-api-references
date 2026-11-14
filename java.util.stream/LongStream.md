# LongStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongStream

```
interface LongStream : BaseStream<Long!, LongStream!>
```

| [java.util.stream.LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#) |

A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. This is the`long`primitive specialization of .

The following example illustrates an aggregate operation using [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#), computing the sum of the weights of the red widgets: 

```kotlin
<code>long sum = widgets.stream()
                        .filter(w -&gt; w.getColor() == RED)
                        .mapToLong(w -&gt; w.getWeight())
                        .sum();
  </code>
```
See the class documentation for [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and the package documentation for [java.util.stream](https://developer.android.com/reference/kotlin/java/util/stream/package-summary) for additional specification of streams, stream operations, stream pipelines, and parallelism.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.Builder) A mutable builder for a`LongStream`. |
| abstract | [LongMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.LongMapMultiConsumer) Represents an operation that accepts a`long`-valued argument and a LongConsumer, and returns no result. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#allMatch(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#anyMatch(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns whether any elements of this stream match the provided predicate. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [asDoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#asDoubleStream())`()` Returns a`DoubleStream`consisting of the elements of this stream, converted to`double`. |
| --- | --- |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [average](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#average())`()` Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | [boxed](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#boxed())`()` Returns a`Stream`consisting of the elements of this stream, each boxed to a`Long`. |
| openstatic [LongStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.Builder)! | [builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#builder())`()` Returns a builder for a`LongStream`. |
| --- | --- |
| abstractR | [collect](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#collect(java.util.function.Supplier,%20java.util.function.ObjLongConsumer,%20java.util.function.BiConsumer))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<R>!`, `accumulator:` ` [ObjLongConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjLongConsumer.html#)<R>!`, `combiner:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<R,` `R>!`)` Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [concat](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#concat(java.util.stream.LongStream,%20java.util.stream.LongStream))`(`a:` ` [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!`, `b:` ` [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#count())`()` Returns the count of elements in this stream. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [distinct](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#distinct())`()` Returns a stream consisting of the distinct elements of this stream. |
| open [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [dropWhile](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#dropWhile(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [empty](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#empty())`()` Returns an empty sequential`LongStream`. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [filter](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#filter(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| abstract [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | [findAny](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#findAny())`()` Returns an [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#) describing some element of the stream, or an empty`OptionalLong`if the stream is empty. |
| abstract [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | [findFirst](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#findFirst())`()` Returns an [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#) describing the first element of this stream, or an empty`OptionalLong`if the stream is empty. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [flatMap](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#flatMap(java.util.function.LongFunction))`(`mapper:` ` [LongFunction](https://developer.android.com/reference/kotlin/java/util/function/LongFunction.html#)<out` ` [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#forEach(java.util.function.LongConsumer))`(`action:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!`)` Performs an action for each element of this stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#forEachOrdered(java.util.function.LongConsumer))`(`action:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!`)` Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order. |
| --- | --- |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [generate](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#generate(java.util.function.LongSupplier))`(`s:` ` [LongSupplier](https://developer.android.com/reference/kotlin/java/util/function/LongSupplier.html#)!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`LongSupplier`. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#iterate(kotlin.Long,%20java.util.function.LongPredicate,%20java.util.function.LongUnaryOperator))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `hasNext:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`, `next:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!`)` Returns a sequential ordered`LongStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#iterate(kotlin.Long,%20java.util.function.LongUnaryOperator))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `f:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!`)` Returns an infinite sequential ordered`LongStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| --- | --- |
| abstract [PrimitiveIterator.OfLong](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong.html#)! | [iterator](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#iterator())`()` <br /> |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [limit](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#limit(kotlin.Long))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [map](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#map(java.util.function.LongUnaryOperator))`(`mapper:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| open [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#mapMulti(java.util.stream.LongStream.LongMapMultiConsumer))`(`mapper:` ` [LongStream.LongMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.LongMapMultiConsumer)!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [mapToDouble](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#mapToDouble(java.util.function.LongToDoubleFunction))`(`mapper:` ` [LongToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/LongToDoubleFunction.html#)!`)` Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | [mapToInt](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#mapToInt(java.util.function.LongToIntFunction))`(`mapper:` ` [LongToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/LongToIntFunction.html#)!`)` Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<U\>! | [mapToObj](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#mapToObj(java.util.function.LongFunction))`(`mapper:` ` [LongFunction](https://developer.android.com/reference/kotlin/java/util/function/LongFunction.html#)<out` `U>!`)` Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | [max](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#max())`()` Returns an`OptionalLong`describing the maximum element of this stream, or an empty optional if this stream is empty. |
| abstract [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | [min](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#min())`()` Returns an`OptionalLong`describing the minimum element of this stream, or an empty optional if this stream is empty. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#noneMatch(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns whether no elements of this stream match the provided predicate. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#of(kotlin.Long))`(`t:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential`LongStream`containing a single element. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#of(kotlin.Long))`(`vararg` `values:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered stream whose elements are the specified values. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [parallel](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#parallel())`()` <br /> |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [peek](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#peek(java.util.function.LongConsumer))`(`action:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [range](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#range(kotlin.Long,%20kotlin.Long))`(`startInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endExclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endExclusive`(exclusive) by an incremental step of`1`. |
| --- | --- |
| openstatic [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [rangeClosed](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#rangeClosed(kotlin.Long,%20kotlin.Long))`(`startInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endInclusive:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a sequential ordered`LongStream`from`startInclusive`(inclusive) to`endInclusive`(inclusive) by an incremental step of`1`. |
| abstract [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#reduce(java.util.function.LongBinaryOperator))`(`op:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalLong`describing the reduced value, if any. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#reduce(kotlin.Long,%20java.util.function.LongBinaryOperator))`(`identity:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `op:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [sequential](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#sequential())`()` <br /> |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [skip](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [sorted](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#sorted())`()` Returns a stream consisting of the elements of this stream in sorted order. |
| --- | --- |
| abstract [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)! | [spliterator](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#spliterator())`()` <br /> |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sum](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#sum())`()` Returns the sum of elements in this stream. |
| abstract [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#)! | [summaryStatistics](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#summaryStatistics())`()` Returns a`LongSummaryStatistics`describing various summary data about the elements of this stream. |
| --- | --- |
| open [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | [takeWhile](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#takeWhile(java.util.function.LongPredicate))`(`predicate:` ` [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [toArray](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#toArray())`()` Returns an array containing the elements of this stream. |

| Inherited functions ||
|---|---|
| From class [BaseStream](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#isParallel())`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | S | [onClose](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#onClose(java.lang.Runnable))`(`closeHandler:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | | S | [unordered](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#unordered())`()` <br /> Returns an equivalent stream that is [unordered](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Ordering). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: LongPredicate!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: LongPredicate!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements of the stream match the provided predicate, otherwise`false` |

### asDoubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asDoubleStream(): DoubleStream!
```

Returns a`DoubleStream`consisting of the elements of this stream, converted to`double`.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | a`DoubleStream`consisting of the elements of this stream, converted to`double` |

### average

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun average(): OptionalDouble!
```

Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction).

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | an`OptionalDouble`containing the average element of this stream, or an empty optional if the stream is empty |

### boxed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun boxed(): Stream<Long!>!
```

Returns a`Stream`consisting of the elements of this stream, each boxed to a`Long`.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!>! | a`Stream`consistent of the elements of this stream, each boxed to`Long` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun builder(): LongStream.Builder!
```

Returns a builder for a`LongStream`.

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------|
| [LongStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.Builder)! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: ObjLongConsumer<R>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (long element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(long,java.util.function.LongBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#reduce(kotlin.Long,%20java.util.function.LongBinaryOperator)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [ObjLongConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjLongConsumer.html#)\<R\>!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that must fold an element into a result container. |
| --- | --- |
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
    a: LongStream!, 
    b: LongStream!
): LongStream!
```

Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. The resulting stream is ordered if both of the input streams are ordered, and parallel if either of the input streams is parallel. When the resulting stream is closed, the close handlers for both input streams are invoked.

This method operates on the two input streams and binds each stream to its source. As a result subsequent modifications to an input stream source may not be reflected in the concatenated stream result.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `a` | [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!:the first stream |
| `b` | [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!:the second stream |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the concatenation of the two input streams |

### count

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Long
```

Returns the count of elements in this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return map(e -&gt; 1L).sum();
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
abstract fun distinct(): LongStream!
```

Returns a stream consisting of the distinct elements of this stream.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### dropWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: LongPredicate!): LongStream!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(): LongStream!
```

Returns an empty sequential`LongStream`.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: LongPredicate!): LongStream!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to each element to determine if it should be included |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): OptionalLong!
```

Returns an [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#) describing some element of the stream, or an empty`OptionalLong`if the stream is empty.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#findFirst())instead.)

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | an`OptionalLong`describing some element of this stream, or an empty`OptionalLong`if the stream is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/LongStream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): OptionalLong!
```

Returns an [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#) describing the first element of this stream, or an empty`OptionalLong`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | an`OptionalLong`describing the first element of this stream, or an empty`OptionalLong`if the stream is empty |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMap(mapper: LongFunction<out LongStream!>!): LongStream!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongFunction](https://developer.android.com/reference/kotlin/java/util/function/LongFunction.html#)\<out [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)!\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element which produces a`LongStream`of new values |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#flatMap(Function)](https://developer.android.com/reference/kotlin/java/util/stream/Stream#flatMap(java.util.function.Function)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: LongConsumer!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: LongConsumer!): Unit
```

Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

**See Also**

- [#forEach(LongConsumer)](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#forEach(java.util.function.LongConsumer)) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun generate(s: LongSupplier!): LongStream!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`LongSupplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [LongSupplier](https://developer.android.com/reference/kotlin/java/util/function/LongSupplier.html#)!:the`LongSupplier`for generated elements |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a new infinite sequential unordered`LongStream` |

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

The action of applying the`hasNext`predicate to an element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the initial element |
| `hasNext` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a predicate to apply to elements to determine when the stream must terminate. |
| `next` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a new sequential`LongStream` |

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

The action of applying`f`for one element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the initial element |
| `f` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a new sequential`LongStream` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): PrimitiveIterator.OfLong!
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [PrimitiveIterator.OfLong](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong.html#)! | the element iterator for this stream |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): LongStream!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(mapper: LongUnaryOperator!): LongStream!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### mapMulti

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMulti(mapper: LongStream.LongMapMultiConsumer!): LongStream!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

If the [consumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongStream.LongMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.LongMapMultiConsumer)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that generates replacement elements |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/Stream#mapMulti(java.util.function.BiConsumer)) 

### mapToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToDouble(mapper: LongToDoubleFunction!): DoubleStream!
```

Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/LongToDoubleFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | the new stream |

### mapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToInt(mapper: LongToIntFunction!): IntStream!
```

Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [LongToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/LongToIntFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | the new stream |

### mapToObj

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> mapToObj(mapper: LongFunction<out U>!): Stream<U>!
```

Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | the element type of the new stream |
| `mapper` | [LongFunction](https://developer.android.com/reference/kotlin/java/util/function/LongFunction.html#)\<outU\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<U>! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(): OptionalLong!
```

Returns an`OptionalLong`describing the maximum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Long::max);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | an`OptionalLong`containing the maximum element of this stream, or an empty`OptionalLong`if the stream is empty |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(): OptionalLong!
```

Returns an`OptionalLong`describing the minimum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Long::min);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | an`OptionalLong`containing the minimum element of this stream, or an empty`OptionalLong`if the stream is empty |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: LongPredicate!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

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
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a singleton sequential stream |

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
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): LongStream!
```

| Return ||
|--------------------------------------------------------------------------------------------|-------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a parallel stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: LongConsumer!): LongStream!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements as they are consumed from the stream |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

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
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a sequential`LongStream`for the range of`long`elements |

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
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a sequential`LongStream`for the range of`long`elements |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(op: LongBinaryOperator!): OptionalLong!
```

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalLong`describing the reduced value, if any. This is equivalent to: 

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

The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong.html#)! | the result of the reduction |

**See Also**

- [#reduce(long, LongBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#reduce(kotlin.Long,%20java.util.function.LongBinaryOperator)) 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: Long, 
    op: LongBinaryOperator!
): Long
```

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>long result = identity;
      for (long element : this stream)
          result = accumulator.applyAsLong(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`x`,`accumulator.apply(identity, x)`is equal to`x`. The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity value for the accumulating function |
| `op` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

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
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | a sequential stream |

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): LongStream!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): LongStream!
```

Returns a stream consisting of the elements of this stream in sorted order.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator.OfLong!
```

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)! | the element spliterator for this stream |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sum(): Long
```

Returns the sum of elements in this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(0, Long::sum);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum of elements in this stream |

### summaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun summaryStatistics(): LongSummaryStatistics!
```

Returns a`LongSummaryStatistics`describing various summary data about the elements of this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction).

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#)! | a`LongSummaryStatistics`describing various summary data about the elements of this stream |

### takeWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: LongPredicate!): LongStream!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [LongPredicate](https://developer.android.com/reference/kotlin/java/util/function/LongPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream#)! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): LongArray!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | an array containing the elements of this stream |
