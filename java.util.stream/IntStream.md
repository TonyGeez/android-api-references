# IntStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntStream

```
interface IntStream : BaseStream<Int!, IntStream!>
```

| [java.util.stream.IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#) |

A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. This is the`int`primitive specialization of .

The following example illustrates an aggregate operation using [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#), computing the sum of the weights of the red widgets: 

```kotlin
<code>int sum = widgets.stream()
                       .filter(w -&gt; w.getColor() == RED)
                       .mapToInt(w -&gt; w.getWeight())
                       .sum();
  </code>
```
See the class documentation for [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and the package documentation for [java.util.stream](https://developer.android.com/reference/kotlin/java/util/stream/package-summary) for additional specification of streams, stream operations, stream pipelines, and parallelism.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.Builder) A mutable builder for an`IntStream`. |
| abstract | [IntMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.IntMapMultiConsumer) Represents an operation that accepts an`int`-valued argument and an IntConsumer, and returns no result. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#allMatch(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#anyMatch(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns whether any elements of this stream match the provided predicate. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [asDoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#asDoubleStream())`()` Returns a`DoubleStream`consisting of the elements of this stream, converted to`double`. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [asLongStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#asLongStream())`()` Returns a`LongStream`consisting of the elements of this stream, converted to`long`. |
| abstract [OptionalDouble](https://developer.android.com/reference/kotlin/java/util/OptionalDouble.html#)! | [average](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#average())`()` Returns an`OptionalDouble`describing the arithmetic mean of elements of this stream, or an empty optional if this stream is empty. |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | [boxed](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#boxed())`()` Returns a`Stream`consisting of the elements of this stream, each boxed to an`Integer`. |
| --- | --- |
| openstatic [IntStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.Builder)! | [builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#builder())`()` Returns a builder for an`IntStream`. |
| abstractR | [collect](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#collect(java.util.function.Supplier,%20java.util.function.ObjIntConsumer,%20java.util.function.BiConsumer))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<R>!`, `accumulator:` ` [ObjIntConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjIntConsumer.html#)<R>!`, `combiner:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<R,` `R>!`)` Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [concat](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#concat(java.util.stream.IntStream,%20java.util.stream.IntStream))`(`a:` ` [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!`, `b:` ` [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#count())`()` Returns the count of elements in this stream. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [distinct](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#distinct())`()` Returns a stream consisting of the distinct elements of this stream. |
| open [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [dropWhile](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#dropWhile(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| --- | --- |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [empty](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#empty())`()` Returns an empty sequential`IntStream`. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [filter](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#filter(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| abstract [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | [findAny](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#findAny())`()` Returns an [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#) describing some element of the stream, or an empty`OptionalInt`if the stream is empty. |
| --- | --- |
| abstract [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | [findFirst](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#findFirst())`()` Returns an [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#) describing the first element of this stream, or an empty`OptionalInt`if the stream is empty. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [flatMap](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#flatMap(java.util.function.IntFunction))`(`mapper:` ` [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)<out` ` [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#forEach(java.util.function.IntConsumer))`(`action:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!`)` Performs an action for each element of this stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#forEachOrdered(java.util.function.IntConsumer))`(`action:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!`)` Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order. |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [generate](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#generate(java.util.function.IntSupplier))`(`s:` ` [IntSupplier](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier.html#)!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`IntSupplier`. |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#iterate(kotlin.Int,%20java.util.function.IntPredicate,%20java.util.function.IntUnaryOperator))`(`seed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hasNext:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`, `next:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Returns a sequential ordered`IntStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| --- | --- |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [iterate](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#iterate(kotlin.Int,%20java.util.function.IntUnaryOperator))`(`seed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `f:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Returns an infinite sequential ordered`IntStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| abstract [PrimitiveIterator.OfInt](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt.html#)! | [iterator](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#iterator())`()` <br /> |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [limit](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#limit(kotlin.Long))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| --- | --- |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [map](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#map(java.util.function.IntUnaryOperator))`(`mapper:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| open [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#mapMulti(java.util.stream.IntStream.IntMapMultiConsumer))`(`mapper:` ` [IntStream.IntMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.IntMapMultiConsumer)!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| abstract [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [mapToDouble](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#mapToDouble(java.util.function.IntToDoubleFunction))`(`mapper:` ` [IntToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/IntToDoubleFunction.html#)!`)` Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| abstract [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [mapToLong](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#mapToLong(java.util.function.IntToLongFunction))`(`mapper:` ` [IntToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/IntToLongFunction.html#)!`)` Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<U\>! | [mapToObj](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#mapToObj(java.util.function.IntFunction))`(`mapper:` ` [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)<out` `U>!`)` Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | [max](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#max())`()` Returns an`OptionalInt`describing the maximum element of this stream, or an empty optional if this stream is empty. |
| --- | --- |
| abstract [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | [min](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#min())`()` Returns an`OptionalInt`describing the minimum element of this stream, or an empty optional if this stream is empty. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#noneMatch(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns whether no elements of this stream match the provided predicate. |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#of(kotlin.Int))`(`t:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a sequential`IntStream`containing a single element. |
| --- | --- |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [of](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#of(kotlin.Int))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a sequential ordered stream whose elements are the specified values. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [parallel](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#parallel())`()` <br /> |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [peek](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#peek(java.util.function.IntConsumer))`(`action:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| --- | --- |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [range](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#range(kotlin.Int,%20kotlin.Int))`(`startInclusive:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endExclusive:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a sequential ordered`IntStream`from`startInclusive`(inclusive) to`endExclusive`(exclusive) by an incremental step of`1`. |
| openstatic [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [rangeClosed](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#rangeClosed(kotlin.Int,%20kotlin.Int))`(`startInclusive:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endInclusive:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a sequential ordered`IntStream`from`startInclusive`(inclusive) to`endInclusive`(inclusive) by an incremental step of`1`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#reduce(kotlin.Int,%20java.util.function.IntBinaryOperator))`(`identity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. |
| --- | --- |
| abstract [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | [reduce](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#reduce(java.util.function.IntBinaryOperator))`(`op:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalInt`describing the reduced value, if any. |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [sequential](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#sequential())`()` <br /> |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [skip](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#skip(kotlin.Long))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| --- | --- |
| abstract [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [sorted](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#sorted())`()` Returns a stream consisting of the elements of this stream in sorted order. |
| abstract [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)! | [spliterator](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#spliterator())`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sum](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#sum())`()` Returns the sum of elements in this stream. |
| --- | --- |
| abstract [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#)! | [summaryStatistics](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#summaryStatistics())`()` Returns an`IntSummaryStatistics`describing various summary data about the elements of this stream. |
| open [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | [takeWhile](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#takeWhile(java.util.function.IntPredicate))`(`predicate:` ` [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [toArray](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#toArray())`()` Returns an array containing the elements of this stream. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseStream](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#isParallel())`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | S | [onClose](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#onClose(java.lang.Runnable))`(`closeHandler:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | | S | [unordered](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#unordered())`()` <br /> Returns an equivalent stream that is [unordered](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Ordering). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: IntPredicate!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: IntPredicate!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

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

### asLongStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asLongStream(): LongStream!
```

Returns a`LongStream`consisting of the elements of this stream, converted to`long`.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | a`LongStream`consisting of the elements of this stream, converted to`long` |

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
abstract fun boxed(): Stream<Int!>!
```

Returns a`Stream`consisting of the elements of this stream, each boxed to an`Integer`.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>! | a`Stream`consistent of the elements of this stream, each boxed to an`Integer` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun builder(): IntStream.Builder!
```

Returns a builder for an`IntStream`.

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------|
| [IntStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.Builder)! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: ObjIntConsumer<R>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#MutableReduction) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (int element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(int,java.util.function.IntBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#reduce(kotlin.Int,%20java.util.function.IntBinaryOperator)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [ObjIntConsumer](https://developer.android.com/reference/kotlin/java/util/function/ObjIntConsumer.html#)\<R\>!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that must fold an element into a result container. |
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
    a: IntStream!, 
    b: IntStream!
): IntStream!
```

Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. The resulting stream is ordered if both of the input streams are ordered, and parallel if either of the input streams is parallel. When the resulting stream is closed, the close handlers for both input streams are invoked.

This method operates on the two input streams and binds each stream to its source. As a result subsequent modifications to an input stream source may not be reflected in the concatenated stream result.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `a` | [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!:the first stream |
| `b` | [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!:the second stream |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the concatenation of the two input streams |

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
abstract fun distinct(): IntStream!
```

Returns a stream consisting of the distinct elements of this stream.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### dropWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: IntPredicate!): IntStream!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(): IntStream!
```

Returns an empty sequential`IntStream`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: IntPredicate!): IntStream!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to each element to determine if it should be included |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): OptionalInt!
```

Returns an [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#) describing some element of the stream, or an empty`OptionalInt`if the stream is empty.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#findFirst())instead.)

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | an`OptionalInt`describing some element of this stream, or an empty`OptionalInt`if the stream is empty |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/IntStream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): OptionalInt!
```

Returns an [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#) describing the first element of this stream, or an empty`OptionalInt`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | an`OptionalInt`describing the first element of this stream, or an empty`OptionalInt`if the stream is empty |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMap(mapper: IntFunction<out IntStream!>!): IntStream!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)\<out [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)!\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element which produces an`IntStream`of new values |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#flatMap(Function)](https://developer.android.com/reference/kotlin/java/util/stream/Stream#flatMap(java.util.function.Function)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: IntConsumer!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: IntConsumer!): Unit
```

Performs an action for each element of this stream, guaranteeing that each element is processed in encounter order for streams that have a defined encounter order.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements |

**See Also**

- [#forEach(IntConsumer)](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#forEach(java.util.function.IntConsumer)) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun generate(s: IntSupplier!): IntStream!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`IntSupplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [IntSupplier](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier.html#)!:the`IntSupplier`for generated elements |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a new infinite sequential unordered`IntStream` |

### iterate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Int, 
    hasNext: IntPredicate!, 
    next: IntUnaryOperator!
): IntStream!
```

Returns a sequential ordered`IntStream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. The stream terminates as soon as the`hasNext`predicate returns false.

`IntStream.iterate`should produce the same sequence of elements as produced by the corresponding for-loop: 

```kotlin
<code>for (int index=seed; hasNext.test(index); index = next.applyAsInt(index)) {
          ...
      }
  </code>
```

The resulting sequence may be empty if the`hasNext`predicate does not hold on the seed value. Otherwise the first element will be the supplied`seed`value, the next element (if present) will be the result of applying the`next`function to the`seed`value, and so on iteratively until the`hasNext`predicate indicates that the stream should terminate.

The action of applying the`hasNext`predicate to an element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial element |
| `hasNext` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a predicate to apply to elements to determine when the stream must terminate. |
| `next` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a new sequential`IntStream` |

### iterate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iterate(
    seed: Int, 
    f: IntUnaryOperator!
): IntStream!
```

Returns an infinite sequential ordered`IntStream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc.

The first element (position`0`) in the`IntStream`will be the provided`seed`. For`n > 0`, the element at position`n`, will be the result of applying the function`f`to the element at position`n - 1`.

The action of applying`f`for one element [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary.html#MemoryVisibility) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial element |
| `f` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a function to be applied to the previous element to produce a new element |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a new sequential`IntStream` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): PrimitiveIterator.OfInt!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [PrimitiveIterator.OfInt](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt.html#)! | the element iterator for this stream |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): IntStream!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun map(mapper: IntUnaryOperator!): IntStream!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### mapMulti

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMulti(mapper: IntStream.IntMapMultiConsumer!): IntStream!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

If the [consumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [IntStream.IntMapMultiConsumer](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.IntMapMultiConsumer)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function that generates replacement elements |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

**See Also**

- [java.util.stream.Stream#mapMulti](https://developer.android.com/reference/kotlin/java/util/stream/Stream#mapMulti(java.util.function.BiConsumer)) 

### mapToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToDouble(mapper: IntToDoubleFunction!): DoubleStream!
```

Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [IntToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/IntToDoubleFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | the new stream |

### mapToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToLong(mapper: IntToLongFunction!): LongStream!
```

Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [IntToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/IntToLongFunction.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | the new stream |

### mapToObj

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> mapToObj(mapper: IntFunction<out U>!): Stream<U>!
```

Returns an object-valued`Stream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | the element type of the new stream |
| `mapper` | [IntFunction](https://developer.android.com/reference/kotlin/java/util/function/IntFunction.html#)\<outU\>!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function to apply to each element |

| Return ||
|--------------------------------------------------------------------------------------|----------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<U>! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(): OptionalInt!
```

Returns an`OptionalInt`describing the maximum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Integer::max);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | an`OptionalInt`containing the maximum element of this stream, or an empty`OptionalInt`if the stream is empty |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(): OptionalInt!
```

Returns an`OptionalInt`describing the minimum element of this stream, or an empty optional if this stream is empty. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(Integer::min);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | an`OptionalInt`containing the minimum element of this stream, or an empty`OptionalInt`if the stream is empty |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: IntPredicate!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either no elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(t: Int): IntStream!
```

Returns a sequential`IntStream`containing a single element.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `t` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the single element |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a singleton sequential stream |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(vararg values: Int): IntStream!
```

Returns a sequential ordered stream whose elements are the specified values.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the elements of the new stream |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): IntStream!
```

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a parallel stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: IntConsumer!): IntStream!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) action to perform on the elements as they are consumed from the stream |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### range

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun range(
    startInclusive: Int, 
    endExclusive: Int
): IntStream!
```

Returns a sequential ordered`IntStream`from`startInclusive`(inclusive) to`endExclusive`(exclusive) by an incremental step of`1`.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------|
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the (inclusive) initial value |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the exclusive upper bound |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a sequential`IntStream`for the range of`int`elements |

### rangeClosed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rangeClosed(
    startInclusive: Int, 
    endInclusive: Int
): IntStream!
```

Returns a sequential ordered`IntStream`from`startInclusive`(inclusive) to`endInclusive`(inclusive) by an incremental step of`1`.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------|
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the (inclusive) initial value |
| `endInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the inclusive upper bound |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a sequential`IntStream`for the range of`int`elements |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: Int, 
    op: IntBinaryOperator!
): Int
```

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using the provided identity value and an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>int result = identity;
      for (int element : this stream)
          result = accumulator.applyAsInt(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`x`,`accumulator.apply(identity, x)`is equal to`x`. The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identity value for the accumulating function |
| `op` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the result of the reduction |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/IntStream#sum()>
- <https://developer.android.com/reference/kotlin/java/util/stream/IntStream#min()>
- <https://developer.android.com/reference/kotlin/java/util/stream/IntStream#max()>
- <https://developer.android.com/reference/kotlin/java/util/stream/IntStream#average()> 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(op: IntBinaryOperator!): OptionalInt!
```

Performs a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) on the elements of this stream, using an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) accumulation function, and returns an`OptionalInt`describing the reduced value, if any. This is equivalent to: 

```kotlin
<code>boolean foundAny = false;
      int result = null;
      for (int element : this stream) {
          if (!foundAny) {
              foundAny = true;
              result = element;
          }
          else
              result = accumulator.applyAsInt(result, element);
      }
      return foundAny ? OptionalInt.of(result) : OptionalInt.empty();
  </code>
```
but is not constrained to execute sequentially.

<br />

The`accumulator`function must be an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity) function.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `op` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:an [associative](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Associativity), [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) function for combining two values |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt.html#)! | the result of the reduction |

**See Also**

- [#reduce(int, IntBinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#reduce(kotlin.Int,%20java.util.function.IntBinaryOperator)) 

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): IntStream!
```

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | a sequential stream |

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): IntStream!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): IntStream!
```

Returns a stream consisting of the elements of this stream in sorted order.

This is a [stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator.OfInt!
```

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)! | the element spliterator for this stream |

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sum(): Int
```

Returns the sum of elements in this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) and is equivalent to: 

```kotlin
<code>return reduce(0, Integer::sum);
  </code>
```

<br />

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sum of elements in this stream |

### summaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun summaryStatistics(): IntSummaryStatistics!
```

Returns an`IntSummaryStatistics`describing various summary data about the elements of this stream. This is a special case of a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction).

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#)! | an`IntSummaryStatistics`describing various summary data about the elements of this stream |

### takeWhile

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: IntPredicate!): IntStream!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [IntPredicate](https://developer.android.com/reference/kotlin/java/util/function/IntPredicate.html#)!:a [non-interfering](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference), [stateless](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Statelessness) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream#)! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): IntArray!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array containing the elements of this stream |
