# Stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Stream

```
interface Stream<T : Any!> : BaseStream<T, Stream<T>!>
```

| [java.util.stream.Stream](Stream.md) |

A sequence of elements supporting sequential and parallel aggregate operations. The following example illustrates an aggregate operation using [Stream](Stream.md) and [IntStream](IntStream.md): 

```kotlin
<code>int sum = widgets.stream()
                       .filter(w -&gt; w.getColor() == RED)
                       .mapToInt(w -&gt; w.getWeight())
                       .sum();
  </code>
```
In this example,`widgets`is a`Collection<Widget>`. We create a stream of`Widget`objects via [Collection.stream()](../java.util/Collection.md)), filter it to produce a stream containing only the red widgets, and then transform it into a stream of`int`values representing the weight of each red widget. Then this stream is summed to produce a total weight.

<br />

In addition to`Stream`, which is a stream of object references, there are primitive specializations for [IntStream](IntStream.md), [LongStream](LongStream.md), and [DoubleStream](DoubleStream.md), all of which are referred to as "streams" and conform to the characteristics and restrictions described here.

To perform a computation, stream [operations](_package.md) are composed into a*stream pipeline* . A stream pipeline consists of a source (which might be an array, a collection, a generator function, an I/O channel, etc), zero or more*intermediate operations* (which transform a stream into another stream, such as [Stream.filter(Predicate)](Stream.md))), and a*terminal operation* (which produces a result or side-effect, such as [Stream.count()](Stream.md))or [Stream.forEach(Consumer)](Stream.md))). Streams are lazy; computation on the source data is only performed when the terminal operation is initiated, and source elements are consumed only as needed.

A stream implementation is permitted significant latitude in optimizing the computation of the result. For example, a stream implementation is free to elide operations (or entire stages) from a stream pipeline -- and therefore elide invocation of behavioral parameters -- if it can prove that it would not affect the result of the computation. This means that side-effects of behavioral parameters may not always be executed and should not be relied upon, unless otherwise specified (such as by the terminal operations`forEach`and`forEachOrdered`). (For a specific example of such an optimization, see the API note documented on the [count](Stream.md))operation. For more detail, see the [side-effects](_package.md) section of the stream package documentation.)

Collections and streams, while bearing some superficial similarities, have different goals. Collections are primarily concerned with the efficient management of, and access to, their elements. By contrast, streams do not provide a means to directly access or manipulate their elements, and are instead concerned with declaratively describing their source and the computational operations which will be performed in aggregate on that source. However, if the provided stream operations do not offer the desired functionality, the [iterator()](BaseStream.md))and [spliterator()](BaseStream.md))operations can be used to perform a controlled traversal.

A stream pipeline, like the "widgets" example above, can be viewed as a*query* on the stream source. Unless the source was explicitly designed for concurrent modification (such as a [ConcurrentHashMap](../java.util.concurrent/ConcurrentHashMap.md)), unpredictable or erroneous behavior may result from modifying the stream source while it is being queried.

Most stream operations accept parameters that describe user-specified behavior, such as the lambda expression`w -> w.getWeight()`passed to`mapToInt`in the example above. To preserve correct behavior, these*behavioral parameters*:

- must be [non-interfering](_package.md)(they do not modify the stream source); and
- in most cases must be [stateless](_package.md)(their result should not depend on any state that might change during execution of the stream pipeline).

Such parameters are always instances of a [functional interface](../java.util.function/_package.md) such as [java.util.function.Function](../java.util.function/Function.md), and are often lambda expressions or method references. Unless otherwise specified these parameters must be*non-null*.

A stream should be operated on (invoking an intermediate or terminal stream operation) only once. This rules out, for example, "forked" streams, where the same source feeds two or more pipelines, or multiple traversals of the same stream. A stream implementation may throw [IllegalStateException](../java.lang/IllegalStateException.md) if it detects that the stream is being reused. However, since some stream operations may return their receiver rather than a new stream object, it may not be possible to detect reuse in all cases.

Streams have a [close()](BaseStream.md))method and implement [AutoCloseable](../java.lang/AutoCloseable.md). Operating on a stream after it has been closed will throw [IllegalStateException](../java.lang/IllegalStateException.md). Most stream instances do not actually need to be closed after use, as they are backed by collections, arrays, or generating functions, which require no special resource management. Generally, only streams whose source is an IO channel, such as those returned by [Files.lines(Path)](../java.nio.file/Files.md)), will require closing. If a stream does require closing, it must be opened as a resource within a try-with-resources statement or similar control structure to ensure that it is closed promptly after its operations have completed.

Stream pipelines may execute either sequentially or in [parallel](_package.md). This execution mode is a property of the stream. Streams are created with an initial choice of sequential or parallel execution. (For example, [Collection.stream()](../java.util/Collection.md))creates a sequential stream, and [Collection.parallelStream()](../java.util/Collection.md))creates a parallel one.) This choice of execution mode may be modified by the [sequential()](BaseStream.md))or [parallel()](BaseStream.md))methods, and may be queried with the [isParallel()](BaseStream.md))method.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| abstract | [Builder](../java/util/stream/Stream.Builder.md) A mutable builder for a`Stream`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allMatch](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns whether all elements of this stream match the provided predicate. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [anyMatch](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns whether any elements of this stream match the provided predicate. |
| openstatic [Stream.Builder](../java/util/stream/Stream.Builder.md)\<T\>! | [builder](Stream.md))`()` Returns a builder for a`Stream`. |
| --- | --- |
| abstractR | [collect](Stream.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<R>!`, `accumulator:` ` [BiConsumer](../java.util.function/BiConsumer.md)<R,` `in` `T>!`, `combiner:` ` [BiConsumer](../java.util.function/BiConsumer.md)<R,` `R>!`)` Performs a [mutable reduction](_package.md) operation on the elements of this stream. |
| abstractR | [collect](Stream.md))`(`collector:` ` [Collector](Collector.md)<in` `T,` `A,` `R>!`)` Performs a [mutable reduction](_package.md) operation on the elements of this stream using a`Collector`. |
| openstatic [Stream](Stream.md)\<T\>! | [concat](Stream.md))`(`a:` ` [Stream](Stream.md)<out` `T>!`, `b:` ` [Stream](Stream.md)<out` `T>!`)` Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [count](Stream.md))`()` Returns the count of elements in this stream. |
| abstract [Stream](Stream.md)\<T\>! | [distinct](Stream.md))`()` Returns a stream consisting of the distinct elements (according to [Object.equals(Object)](../java.lang/Object.md))) of this stream. |
| open [Stream](Stream.md)\<T\>! | [dropWhile](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. |
| --- | --- |
| openstatic [Stream](Stream.md)\<T\>! | [empty](Stream.md))`()` Returns an empty sequential`Stream`. |
| abstract [Stream](Stream.md)\<T\>! | [filter](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns a stream consisting of the elements of this stream that match the given predicate. |
| abstract [Optional](../java.util/Optional.md)\<T\>! | [findAny](Stream.md))`()` Returns an [Optional](../java.util/Optional.md) describing some element of the stream, or an empty`Optional`if the stream is empty. |
| --- | --- |
| abstract [Optional](../java.util/Optional.md)\<T\>! | [findFirst](Stream.md))`()` Returns an [Optional](../java.util/Optional.md) describing the first element of this stream, or an empty`Optional`if the stream is empty. |
| abstract [Stream](Stream.md)\<R\>! | [flatMap](Stream.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [Stream](Stream.md)<out` `R>!>!`)` Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [DoubleStream](DoubleStream.md)! | [flatMapToDouble](Stream.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [DoubleStream](DoubleStream.md)!>!`)` Returns an`DoubleStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| --- | --- |
| abstract [IntStream](IntStream.md)! | [flatMapToInt](Stream.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [IntStream](IntStream.md)!>!`)` Returns an`IntStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [LongStream](LongStream.md)! | [flatMapToLong](Stream.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [LongStream](LongStream.md)!>!`)` Returns an`LongStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](Stream.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Performs an action for each element of this stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachOrdered](Stream.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Performs an action for each element of this stream, in the encounter order of the stream if the stream has a defined encounter order. |
| open [Stream](Stream.md)\<R\>! | [gather](Stream.md))`(`gatherer:` ` [Gatherer](Gatherer.md)<in` `T,` `*,` `R>!`)` Returns a stream consisting of the results of applying the given [Gatherer](Gatherer.md) to the elements of this stream. |
| openstatic [Stream](Stream.md)\<T\>! | [generate](Stream.md))`(`s:` ` [Supplier](../java.util.function/Supplier.md)<out` `T>!`)` Returns an infinite sequential unordered stream where each element is generated by the provided`Supplier`. |
| --- | --- |
| openstatic [Stream](Stream.md)\<T\>! | [iterate](Stream.md))`(`seed:` `T`, `hasNext:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`, `next:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<T>!`)` Returns a sequential ordered`Stream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. |
| openstatic [Stream](Stream.md)\<T\>! | [iterate](Stream.md))`(`seed:` `T`, `f:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<T>!`)` Returns an infinite sequential ordered`Stream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc. |
| abstract [Stream](Stream.md)\<T\>! | [limit](Stream.md))`(`maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length. |
| --- | --- |
| abstract [Stream](Stream.md)\<R\>! | [map](Stream.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` `R>!`)` Returns a stream consisting of the results of applying the given function to the elements of this stream. |
| open [Stream](Stream.md)\<R\>! | [mapMulti](Stream.md))`(`mapper:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [Consumer](../java.util.function/Consumer.md)<R>!>!`)` Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| open [DoubleStream](DoubleStream.md)! | [mapMultiToDouble](Stream.md))`(`mapper:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [DoubleConsumer](../java.util.function/DoubleConsumer.md)!>!`)` Returns a`DoubleStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| --- | --- |
| open [IntStream](IntStream.md)! | [mapMultiToInt](Stream.md))`(`mapper:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [IntConsumer](../java.util.function/IntConsumer.md)!>!`)` Returns an`IntStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| open [LongStream](LongStream.md)! | [mapMultiToLong](Stream.md))`(`mapper:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `T,` `in` ` [LongConsumer](../java.util.function/LongConsumer.md)!>!`)` Returns a`LongStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. |
| abstract [DoubleStream](DoubleStream.md)! | [mapToDouble](Stream.md))`(`mapper:` ` [ToDoubleFunction](../java.util.function/ToDoubleFunction.md)<in` `T>!`)` Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream. |
| --- | --- |
| abstract [IntStream](IntStream.md)! | [mapToInt](Stream.md))`(`mapper:` ` [ToIntFunction](../java.util.function/ToIntFunction.md)<in` `T>!`)` Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [LongStream](LongStream.md)! | [mapToLong](Stream.md))`(`mapper:` ` [ToLongFunction](../java.util.function/ToLongFunction.md)<in` `T>!`)` Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream. |
| abstract [Optional](../java.util/Optional.md)\<T\>! | [max](Stream.md))`(`comparator:` ` [Comparator](../java.util/Comparator.md)<in` `T>!`)` Returns the maximum element of this stream according to the provided`Comparator`. |
| --- | --- |
| abstract [Optional](../java.util/Optional.md)\<T\>! | [min](Stream.md))`(`comparator:` ` [Comparator](../java.util/Comparator.md)<in` `T>!`)` Returns the minimum element of this stream according to the provided`Comparator`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [noneMatch](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns whether no elements of this stream match the provided predicate. |
| openstatic [Stream](Stream.md)\<T\>! | [of](Stream.md))`(`t:` `T`)` Returns a sequential`Stream`containing a single element. |
| --- | --- |
| openstatic [Stream](Stream.md)\<T\>! | [of](Stream.md))`(`vararg` `values:` `T`)` Returns a sequential ordered stream whose elements are the specified values. |
| openstatic [Stream](Stream.md)\<T\>! | [ofNullable](Stream.md))`(`t:` `T`)` Returns a sequential`Stream`containing a single element, if non-null, otherwise returns an empty`Stream`. |
| abstract [Stream](Stream.md)\<T\>! | [peek](Stream.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`)` Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream. |
| --- | --- |
| abstract [Optional](../java.util/Optional.md)\<T\>! | [reduce](Stream.md))`(`accumulator:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<T>!`)` Performs a [reduction](_package.md) on the elements of this stream, using an [associative](_package.md) accumulation function, and returns an`Optional`describing the reduced value, if any. |
| abstractT | [reduce](Stream.md))`(`identity:` `T`, `accumulator:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<T>!`)` Performs a [reduction](_package.md) on the elements of this stream, using the provided identity value and an [associative](_package.md) accumulation function, and returns the reduced value. |
| abstractU | [reduce](Stream.md))`(`identity:` `U`, `accumulator:` ` [BiFunction](../java.util.function/BiFunction.md)<U,` `in` `T,` `U>!`, `combiner:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<U>!`)` Performs a [reduction](_package.md) on the elements of this stream, using the provided identity, accumulation and combining functions. |
| --- | --- |
| abstract [Stream](Stream.md)\<T\>! | [skip](Stream.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. |
| abstract [Stream](Stream.md)\<T\>! | [sorted](Stream.md))`()` Returns a stream consisting of the elements of this stream, sorted according to natural order. |
| abstract [Stream](Stream.md)\<T\>! | [sorted](Stream.md))`(`comparator:` ` [Comparator](../java.util/Comparator.md)<in` `T>!`)` Returns a stream consisting of the elements of this stream, sorted according to the provided`Comparator`. |
| --- | --- |
| open [Stream](Stream.md)\<T\>! | [takeWhile](Stream.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [toArray](Stream.md))`()` Returns an array containing the elements of this stream. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\>! | [toArray](Stream.md))`(`generator:` ` [IntFunction](../java.util.function/IntFunction.md)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<A>!>!`)` Returns an array containing the elements of this stream, using the provided`generator`function to allocate the returned array, as well as any additional arrays that might be required for a partitioned execution or for resizing. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>! | [toList](Stream.md))`()` Accumulates the elements of this stream into a`List`. |

| Inherited functions ||
|---|---|
| From class [BaseStream](BaseStream.md) |---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](BaseStream.md))`()` <br /> Closes this stream, causing all close handlers for this stream pipeline to be called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](BaseStream.md))`()` <br /> Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>! | [iterator](BaseStream.md))`()` <br /> Returns an iterator for the elements of this stream. This is a [terminal operation](_package.md). <br /> | | S | [onClose](BaseStream.md))`(`closeHandler:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](BaseStream.md))method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself. This is an [intermediate operation](_package.md). <br /> | | S | [parallel](BaseStream.md))`()` <br /> Returns an equivalent stream that is parallel. May return itself, either because the stream was already parallel, or because the underlying stream state was modified to be parallel. This is an [intermediate operation](_package.md). <br /> | | S | [sequential](BaseStream.md))`()` <br /> Returns an equivalent stream that is sequential. May return itself, either because the stream was already sequential, or because the underlying stream state was modified to be sequential. This is an [intermediate operation](_package.md). <br /> | | [Spliterator](../java.util/Spliterator.md)<T>! | [spliterator](BaseStream.md))`()` <br /> Returns a spliterator for the elements of this stream. This is a [terminal operation](_package.md). <br /> | | S | [unordered](BaseStream.md))`()` <br /> Returns an equivalent stream that is [unordered](_package.md). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered. This is an [intermediate operation](_package.md). <br /> | ||

## Public methods

### allMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun allMatch(predicate: Predicate<in T>!): Boolean
```

Returns whether all elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](_package.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either all elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### anyMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun anyMatch(predicate: Predicate<in T>!): Boolean
```

Returns whether any elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`false`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](_package.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements of the stream match the provided predicate, otherwise`false` |

### builder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> builder(): Stream.Builder<T>!
```

Returns a builder for a`Stream`.

| Parameters ||
|-------|------------------|
| `<T>` | type of elements |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------|
| [Stream.Builder](../java/util/stream/Stream.Builder.md)<T>! | a stream builder |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> collect(
    supplier: Supplier<R>!, 
    accumulator: BiConsumer<R, in T>!, 
    combiner: BiConsumer<R, R>!
): R
```

Performs a [mutable reduction](_package.md) operation on the elements of this stream. A mutable reduction is one in which the reduced value is a mutable result container, such as an`ArrayList`, and elements are incorporated by updating the state of the result rather than by replacing the result. This produces a result equivalent to: 

```kotlin
<code>R result = supplier.get();
      for (T element : this stream)
          accumulator.accept(result, element);
      return result;
  </code>
```

<br />

Like [reduce(java.lang.Object,java.util.function.BinaryOperator)](Stream.md)),`collect`operations can be parallelized without requiring additional synchronization.

This is a [terminal operation](_package.md).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the mutable result container |
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<R\>!:a function that creates a new mutable result container. For a parallel execution, this function may be called multiple times and must return a fresh value each time. |
| `accumulator` | [BiConsumer](../java.util.function/BiConsumer.md)\<R,inT\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function that must fold an element into a result container. |
| --- | --- |
| `combiner` | [BiConsumer](../java.util.function/BiConsumer.md)\<R,R\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function that accepts two partial result containers and merges them, which must be compatible with the accumulator function. The combiner function must fold the elements from the second result container into the first result container. |

| Return ||
|---|-----------------------------|
| R | the result of the reduction |

### collect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!, A : Any!> collect(collector: Collector<in T, A, R>!): R
```

Performs a [mutable reduction](_package.md) operation on the elements of this stream using a`Collector`. A`Collector`encapsulates the functions used as arguments to [collect(java.util.function.Supplier,java.util.function.BiConsumer,java.util.function.BiConsumer)](Stream.md)), allowing for reuse of collection strategies and composition of collect operations such as multiple-level grouping or partitioning.

If the stream is parallel, and the`Collector`is [concurrent](../java/util/stream/Collector.Characteristics.md), and either the stream is unordered or the collector is [unordered](../java/util/stream/Collector.Characteristics.md), then a concurrent reduction will be performed (see [Collector](Collector.md) for details on concurrent reduction.)

This is a [terminal operation](_package.md).

When executed in parallel, multiple intermediate results may be instantiated, populated, and merged so as to maintain isolation of mutable data structures. Therefore, even when executed in parallel with non-thread-safe data structures (such as`ArrayList`), no additional synchronization is needed for a parallel reduction.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | the type of the result |
| `<A>` | the intermediate accumulation type of the`Collector` |
| `collector` | [Collector](Collector.md)\<inT,A,R\>!:the`Collector`describing the reduction |
| --- | --- |

| Return ||
|---|-----------------------------|
| R | the result of the reduction |

**See Also**

- [#collect(Supplier, BiConsumer, BiConsumer)](Stream.md))
- [java.util.stream.Collectors](Collectors.md) 

### concat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> concat(
    a: Stream<out T>!, 
    b: Stream<out T>!
): Stream<T>!
```

Creates a lazily concatenated stream whose elements are all the elements of the first stream followed by all the elements of the second stream. The resulting stream is ordered if both of the input streams are ordered, and parallel if either of the input streams is parallel. When the resulting stream is closed, the close handlers for both input streams are invoked.

This method operates on the two input streams and binds each stream to its source. As a result subsequent modifications to an input stream source may not be reflected in the concatenated stream result.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of stream elements |
| `a` | [Stream](Stream.md)\<outT\>!:the first stream |
| `b` | [Stream](Stream.md)\<outT\>!:the second stream |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------|
| [Stream](Stream.md)<T>! | the concatenation of the two input streams |

### count

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Long
```

Returns the count of elements in this stream. This is a special case of a [reduction](_package.md) and is equivalent to: 

```kotlin
<code>return mapToLong(e -&gt; 1L).sum();
  </code>
```

<br />

This is a [terminal operation](_package.md).

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the count of elements in this stream |

### distinct

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun distinct(): Stream<T>!
```

Returns a stream consisting of the distinct elements (according to [Object.equals(Object)](../java.lang/Object.md))) of this stream.

For ordered streams, the selection of distinct elements is stable (for duplicated elements, the element appearing first in the encounter order is preserved.) For unordered streams, no stability guarantees are made.

This is a [stateful intermediate operation](_package.md).

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### dropWhile

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dropWhile(predicate: Predicate<in T>!): Stream<T>!
```

Returns, if this stream is ordered, a stream consisting of the remaining elements of this stream after dropping the longest prefix of elements that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of the remaining elements of this stream after dropping a subset of elements that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to drop any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation drops all elements (the result is an empty stream), or if no elements of the stream match the given predicate then no elements are dropped (the result is the same as the input).

This is a [stateful intermediate operation](_package.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> empty(): Stream<T>!
```

Returns an empty sequential`Stream`.

| Parameters ||
|-------|-----------------------------|
| `<T>` | the type of stream elements |

| Return ||
|---------------------------------------------------------------------------------------|----------------------------|
| [Stream](Stream.md)<T>! | an empty sequential stream |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(predicate: Predicate<in T>!): Stream<T>!
```

Returns a stream consisting of the elements of this stream that match the given predicate.

This is an [intermediate operation](_package.md).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to each element to determine if it should be included |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### findAny

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findAny(): Optional<T>!
```

Returns an [Optional](../java.util/Optional.md) describing some element of the stream, or an empty`Optional`if the stream is empty.

This is a [short-circuiting terminal operation](_package.md).

The behavior of this operation is explicitly nondeterministic; it is free to select any element in the stream. This is to allow for maximal performance in parallel operations; the cost is that multiple invocations on the same source may not return the same result. (If a stable result is desired, use [findFirst()](Stream.md))instead.)

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)<T>! | an`Optional`describing some element of this stream, or an empty`Optional`if the stream is empty |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the element selected is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/stream/Stream#findFirst()> 

### findFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findFirst(): Optional<T>!
```

Returns an [Optional](../java.util/Optional.md) describing the first element of this stream, or an empty`Optional`if the stream is empty. If the stream has no encounter order, then any element may be returned.

This is a [short-circuiting terminal operation](_package.md).

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)<T>! | an`Optional`describing the first element of this stream, or an empty`Optional`if the stream is empty |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the element selected is null |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> flatMap(mapper: Function<in T, out Stream<out R>!>!): Stream<R>!
```

Returns a stream consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](BaseStream.md))after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | The element type of the new stream |
| `mapper` | [Function](../java.util.function/Function.md)\<inT,out [Stream](Stream.md)\<outR\>!\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element which produces a stream of new values |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<R>! | the new stream |

**See Also**

- [#mapMulti](Stream.md)) 

### flatMapToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMapToDouble(mapper: Function<in T, out DoubleStream!>!): DoubleStream!
```

Returns an`DoubleStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](BaseStream.md))after its contents have placed been into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [Function](../java.util.function/Function.md)\<inT,out [DoubleStream](DoubleStream.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element which produces a stream of new values |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](DoubleStream.md)! | the new stream |

**See Also**

- [#flatMap](Stream.md)) 

### flatMapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMapToInt(mapper: Function<in T, out IntStream!>!): IntStream!
```

Returns an`IntStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](BaseStream.md))after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [Function](../java.util.function/Function.md)\<inT,out [IntStream](IntStream.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element which produces a stream of new values |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](IntStream.md)! | the new stream |

**See Also**

- [#flatMap](Stream.md)) 

### flatMapToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun flatMapToLong(mapper: Function<in T, out LongStream!>!): LongStream!
```

Returns an`LongStream`consisting of the results of replacing each element of this stream with the contents of a mapped stream produced by applying the provided mapping function to each element. Each mapped stream is [closed](BaseStream.md))after its contents have been placed into this stream. (If a mapped stream is`null`an empty stream is used, instead.)

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [Function](../java.util.function/Function.md)\<inT,out [LongStream](LongStream.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element which produces a stream of new values |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](LongStream.md)! | the new stream |

**See Also**

- [#flatMap](Stream.md)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEach(action: Consumer<in T>!): Unit
```

Performs an action for each element of this stream.

This is a [terminal operation](_package.md).

The behavior of this operation is explicitly nondeterministic. For parallel stream pipelines, this operation does*not*guarantee to respect the encounter order of the stream, as doing so would sacrifice the benefit of parallelism. For any given element, the action may be performed at whatever time and in whatever thread the library chooses. If the action accesses shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:a [non-interfering](_package.md) action to perform on the elements |

### forEachOrdered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachOrdered(action: Consumer<in T>!): Unit
```

Performs an action for each element of this stream, in the encounter order of the stream if the stream has a defined encounter order.

This is a [terminal operation](_package.md).

This operation processes the elements one at a time, in encounter order if one exists. Performing the action for one element [*happens-before*](../java.util.concurrent/_package.md) performing the action for subsequent elements, but for any given element, the action may be performed in whatever thread the library chooses.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:a [non-interfering](_package.md) action to perform on the elements |

**See Also**

- [#forEach(Consumer)](Stream.md)) 

### gather

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> gather(gatherer: Gatherer<in T, *, R>!): Stream<R>!
```

Returns a stream consisting of the results of applying the given [Gatherer](Gatherer.md) to the elements of this stream.

This is a [stateful intermediate operation](_package.md) that is an [extension point](_package.md).

Gatherers are highly flexible and can describe a vast array of possibly stateful operations, with support for short-circuiting, and parallelization.

When executed in parallel, multiple intermediate results may be instantiated, populated, and merged so as to maintain isolation of mutable data structures. Therefore, even when executed in parallel with non-thread-safe data structures (such as`ArrayList`), no additional synchronization is needed for a parallel reduction.

Implementations are allowed, but not required, to detect consecutive invocations and compose them into a single, fused, operation. This would make the first expression below behave like the second: 

```kotlin
<code>var stream1 = Stream.of(...).gather(gatherer1).gather(gatherer2);
      var stream2 = Stream.of(...).gather(gatherer1.andThen(gatherer2));
  </code>
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `<R>` | The element type of the new stream |
| `gatherer` | [Gatherer](Gatherer.md)\<inT,\*,R\>!:a gatherer |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<R>! | the new stream |

**See Also**

- [java.util.stream.Gatherers](Gatherers.md) 

### generate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> generate(s: Supplier<out T>!): Stream<T>!
```

Returns an infinite sequential unordered stream where each element is generated by the provided`Supplier`. This is suitable for generating constant streams, streams of random elements, etc.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `s` | [Supplier](../java.util.function/Supplier.md)\<outT\>!:the`Supplier`of generated elements |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------|
| [Stream](Stream.md)<T>! | a new infinite sequential unordered`Stream` |

### iterate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> iterate(
    seed: T, 
    hasNext: Predicate<in T>!, 
    next: UnaryOperator<T>!
): Stream<T>!
```

Returns a sequential ordered`Stream`produced by iterative application of the given`next`function to an initial element, conditioned on satisfying the given`hasNext`predicate. The stream terminates as soon as the`hasNext`predicate returns false.

`Stream.iterate`should produce the same sequence of elements as produced by the corresponding for-loop: 

```kotlin
<code>for (T index=seed; hasNext.test(index); index = next.apply(index)) {
          ...
      }
  </code>
```

The resulting sequence may be empty if the`hasNext`predicate does not hold on the seed value. Otherwise the first element will be the supplied`seed`value, the next element (if present) will be the result of applying the`next`function to the`seed`value, and so on iteratively until the`hasNext`predicate indicates that the stream should terminate.

The action of applying the`hasNext`predicate to an element [*happens-before*](../java.util.concurrent/_package.md) the action of applying the`next`function to that element. The action of applying the`next`function for one element*happens-before* the action of applying the`hasNext`predicate for subsequent elements. For any given element an action may be performed in whatever thread the library chooses.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `seed` | T:the initial element |
| `hasNext` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a predicate to apply to elements to determine when the stream must terminate. |
| --- | --- |
| `next` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<T\>!:a function to be applied to the previous element to produce a new element |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------|
| [Stream](Stream.md)<T>! | a new sequential`Stream` |

### iterate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> iterate(
    seed: T, 
    f: UnaryOperator<T>!
): Stream<T>!
```

Returns an infinite sequential ordered`Stream`produced by iterative application of a function`f`to an initial element`seed`, producing a`Stream`consisting of`seed`,`f(seed)`,`f(f(seed))`, etc.

The first element (position`0`) in the`Stream`will be the provided`seed`. For`n > 0`, the element at position`n`, will be the result of applying the function`f`to the element at position`n - 1`.

The action of applying`f`for one element [*happens-before*](../java.util.concurrent/_package.md) the action of applying`f`for subsequent elements. For any given element the action may be performed in whatever thread the library chooses.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `seed` | T:the initial element |
| `f` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<T\>!:a function to be applied to the previous element to produce a new element |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------|
| [Stream](Stream.md)<T>! | a new sequential`Stream` |

### limit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun limit(maxSize: Long): Stream<T>!
```

Returns a stream consisting of the elements of this stream, truncated to be no longer than`maxSize`in length.

This is a [short-circuiting stateful intermediate operation](_package.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of elements the stream should be limited to |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`maxSize`is negative |

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <R : Any!> map(mapper: Function<in T, out R>!): Stream<R>!
```

Returns a stream consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | The element type of the new stream |
| `mapper` | [Function](../java.util.function/Function.md)\<inT,outR\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<R>! | the new stream |

### mapMulti

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <R : Any!> mapMulti(mapper: BiConsumer<in T, in Consumer<R>!>!): Stream<R>!
```

Returns a stream consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java.util.function/Consumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](_package.md).

If the [consumer](../java.util.function/Consumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<R>` | The element type of the new stream |
| `mapper` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [Consumer](../java.util.function/Consumer.md)\<R\>!\>!:a [non-interfering](_package.md), [stateless](_package.md) function that generates replacement elements |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<R>! | the new stream |

**See Also**

- [#flatMap](Stream.md)) 

### mapMultiToDouble

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMultiToDouble(mapper: BiConsumer<in T, in DoubleConsumer!>!): DoubleStream!
```

Returns a`DoubleStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java.util.function/DoubleConsumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](_package.md).

If the [consumer](../java.util.function/DoubleConsumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [DoubleConsumer](../java.util.function/DoubleConsumer.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function that generates replacement elements |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](DoubleStream.md)! | the new stream |

**See Also**

- [#mapMulti](Stream.md)) 

### mapMultiToInt

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMultiToInt(mapper: BiConsumer<in T, in IntConsumer!>!): IntStream!
```

Returns an`IntStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java.util.function/IntConsumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](_package.md).

If the [consumer](../java.util.function/IntConsumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [IntConsumer](../java.util.function/IntConsumer.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function that generates replacement elements |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](IntStream.md)! | the new stream |

**See Also**

- [#mapMulti](Stream.md)) 

### mapMultiToLong

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapMultiToLong(mapper: BiConsumer<in T, in LongConsumer!>!): LongStream!
```

Returns a`LongStream`consisting of the results of replacing each element of this stream with multiple elements, specifically zero or more elements. Replacement is performed by applying the provided mapping function to each element in conjunction with a [consumer](../java.util.function/LongConsumer.md) argument that accepts replacement elements. The mapping function calls the consumer zero or more times to provide the replacement elements.

This is an [intermediate operation](_package.md).

If the [consumer](../java.util.function/LongConsumer.md) argument is used outside the scope of its application to the mapping function, the results are undefined.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [BiConsumer](../java.util.function/BiConsumer.md)\<inT,in [LongConsumer](../java.util.function/LongConsumer.md)!\>!:a [non-interfering](_package.md), [stateless](_package.md) function that generates replacement elements |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](LongStream.md)! | the new stream |

**See Also**

- [#mapMulti](Stream.md)) 

### mapToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToDouble(mapper: ToDoubleFunction<in T>!): DoubleStream!
```

Returns a`DoubleStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [ToDoubleFunction](../java.util.function/ToDoubleFunction.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------|
| [DoubleStream](DoubleStream.md)! | the new stream |

### mapToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToInt(mapper: ToIntFunction<in T>!): IntStream!
```

Returns an`IntStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [ToIntFunction](../java.util.function/ToIntFunction.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element |

| Return ||
|-----------------------------------------------------------------------------------------|----------------|
| [IntStream](IntStream.md)! | the new stream |

### mapToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun mapToLong(mapper: ToLongFunction<in T>!): LongStream!
```

Returns a`LongStream`consisting of the results of applying the given function to the elements of this stream.

This is an [intermediate operation](_package.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [ToLongFunction](../java.util.function/ToLongFunction.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) function to apply to each element |

| Return ||
|-------------------------------------------------------------------------------------------|----------------|
| [LongStream](LongStream.md)! | the new stream |

### max

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun max(comparator: Comparator<in T>!): Optional<T>!
```

Returns the maximum element of this stream according to the provided`Comparator`. This is a special case of a [reduction](_package.md).

This is a [terminal operation](_package.md).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java.util/Comparator.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md)`Comparator`to compare elements of this stream |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)<T>! | an`Optional`describing the maximum element of this stream, or an empty`Optional`if the stream is empty |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the maximum element is null |

### min

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun min(comparator: Comparator<in T>!): Optional<T>!
```

Returns the minimum element of this stream according to the provided`Comparator`. This is a special case of a [reduction](_package.md).

This is a [terminal operation](_package.md).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java.util/Comparator.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md)`Comparator`to compare elements of this stream |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)<T>! | an`Optional`describing the minimum element of this stream, or an empty`Optional`if the stream is empty |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the minimum element is null |

### noneMatch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun noneMatch(predicate: Predicate<in T>!): Boolean
```

Returns whether no elements of this stream match the provided predicate. May not evaluate the predicate on all elements if not necessary for determining the result. If the stream is empty then`true`is returned and the predicate is not evaluated.

This is a [short-circuiting terminal operation](_package.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to elements of this stream |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if either no elements of the stream match the provided predicate or the stream is empty, otherwise`false` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> of(t: T): Stream<T>!
```

Returns a sequential`Stream`containing a single element.

| Parameters ||
|-------|-----------------------------|
| `t` | T:the single element |
| `<T>` | the type of stream elements |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------|
| [Stream](Stream.md)<T>! | a singleton sequential stream |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <T : Any!> of(vararg values: T): Stream<T>!
```

Returns a sequential ordered stream whose elements are the specified values.

| Parameters ||
|----------|----------------------------------|
| `<T>` | the type of stream elements |
| `values` | T:the elements of the new stream |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### ofNullable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> ofNullable(t: T): Stream<T>!
```

Returns a sequential`Stream`containing a single element, if non-null, otherwise returns an empty`Stream`.

| Parameters ||
|-------|-----------------------------|
| `t` | T:the single element |
| `<T>` | the type of stream elements |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Stream](Stream.md)<T>! | a stream with a single element if the specified element is non-null, otherwise an empty stream |

### peek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(action: Consumer<in T>!): Stream<T>!
```

Returns a stream consisting of the elements of this stream, additionally performing the provided action on each element as elements are consumed from the resulting stream.

This is an [intermediate operation](_package.md).

For parallel stream pipelines, the action may be called at whatever time and in whatever thread the element is made available by the upstream operation. If the action modifies shared state, it is responsible for providing the required synchronization.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:a [non-interfering](_package.md) action to perform on the elements as they are consumed from the stream |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(accumulator: BinaryOperator<T>!): Optional<T>!
```

Performs a [reduction](_package.md) on the elements of this stream, using an [associative](_package.md) accumulation function, and returns an`Optional`describing the reduced value, if any. This is equivalent to: 

```kotlin
<code>boolean foundAny = false;
      T result = null;
      for (T element : this stream) {
          if (!foundAny) {
              foundAny = true;
              result = element;
          }
          else
              result = accumulator.apply(result, element);
      }
      return foundAny ? Optional.of(result) : Optional.empty();
  </code>
```
but is not constrained to execute sequentially.

<br />

The`accumulator`function must be an [associative](_package.md) function.

This is a [terminal operation](_package.md).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accumulator` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<T\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function for combining two values |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Optional](../java.util/Optional.md)<T>! | an [Optional](../java.util/Optional.md) describing the result of the reduction |

| Exceptions ||
|----------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if the result of the reduction is null |

**See Also**

- [#reduce(Object, BinaryOperator)](Stream.md))
- [#min(Comparator)](Stream.md))
- [#max(Comparator)](Stream.md)) 

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reduce(
    identity: T, 
    accumulator: BinaryOperator<T>!
): T
```

Performs a [reduction](_package.md) on the elements of this stream, using the provided identity value and an [associative](_package.md) accumulation function, and returns the reduced value. This is equivalent to: 

```kotlin
<code>T result = identity;
      for (T element : this stream)
          result = accumulator.apply(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the accumulator function. This means that for all`t`,`accumulator.apply(identity, t)`is equal to`t`. The`accumulator`function must be an [associative](_package.md) function.

This is a [terminal operation](_package.md).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | T:the identity value for the accumulating function |
| `accumulator` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<T\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function for combining two values |

| Return ||
|---|-----------------------------|
| T | the result of the reduction |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <U : Any!> reduce(
    identity: U, 
    accumulator: BiFunction<U, in T, U>!, 
    combiner: BinaryOperator<U>!
): U
```

Performs a [reduction](_package.md) on the elements of this stream, using the provided identity, accumulation and combining functions. This is equivalent to: 

```kotlin
<code>U result = identity;
      for (T element : this stream)
          result = accumulator.apply(result, element)
      return result;
  </code>
```
but is not constrained to execute sequentially.

<br />

The`identity`value must be an identity for the combiner function. This means that for all`u`,`combiner(identity, u)`is equal to`u`. Additionally, the`combiner`function must be compatible with the`accumulator`function; for all`u`and`t`, the following must hold: 

```kotlin
<code>combiner.apply(u, accumulator.apply(identity, t)) == accumulator.apply(u, t)
  </code>
```

This is a [terminal operation](_package.md).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | The type of the result |
| `identity` | U:the identity value for the combiner function |
| `accumulator` | [BiFunction](../java.util.function/BiFunction.md)\<U,inT,U\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function for incorporating an additional element into a result |
| --- | --- |
| `combiner` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<U\>!:an [associative](_package.md), [non-interfering](_package.md), [stateless](_package.md) function for combining two values, which must be compatible with the accumulator function |

| Return ||
|---|-----------------------------|
| U | the result of the reduction |

**See Also**

- [#reduce(BinaryOperator)](Stream.md))
- [#reduce(Object, BinaryOperator)](Stream.md)) 

### skip

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun skip(n: Long): Stream<T>!
```

Returns a stream consisting of the remaining elements of this stream after discarding the first`n`elements of the stream. If this stream contains fewer than`n`elements then an empty stream will be returned.

This is a [stateful intermediate operation](_package.md).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of leading elements to skip |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

| Exceptions ||
|--------------------------------------|------------------|
| `java.lang.IllegalArgumentException` | if`n`is negative |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(): Stream<T>!
```

Returns a stream consisting of the elements of this stream, sorted according to natural order. If the elements of this stream are not`Comparable`, a`java.lang.ClassCastException`may be thrown when the terminal operation is executed.

For ordered streams, the sort is stable. For unordered streams, no stability guarantees are made.

This is a [stateful intermediate operation](_package.md).

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### sorted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sorted(comparator: Comparator<in T>!): Stream<T>!
```

Returns a stream consisting of the elements of this stream, sorted according to the provided`Comparator`.

For ordered streams, the sort is stable. For unordered streams, no stability guarantees are made.

This is a [stateful intermediate operation](_package.md).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java.util/Comparator.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md)`Comparator`to be used to compare stream elements |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### takeWhile

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takeWhile(predicate: Predicate<in T>!): Stream<T>!
```

Returns, if this stream is ordered, a stream consisting of the longest prefix of elements taken from this stream that match the given predicate. Otherwise returns, if this stream is unordered, a stream consisting of a subset of elements taken from this stream that match the given predicate.

If this stream is ordered then the longest prefix is a contiguous sequence of elements of this stream that match the given predicate. The first element of the sequence is the first element of this stream, and the element immediately following the last element of the sequence does not match the given predicate.

If this stream is unordered, and some (but not all) elements of this stream match the given predicate, then the behavior of this operation is nondeterministic; it is free to take any subset of matching elements (which includes the empty set).

Independent of whether this stream is ordered or unordered if all elements of this stream match the given predicate then this operation takes all elements (the result is the same as the input), or if no elements of the stream match the given predicate then no elements are taken (the result is an empty stream).

This is a [short-circuiting stateful intermediate operation](_package.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:a [non-interfering](_package.md), [stateless](_package.md) predicate to apply to elements to determine the longest prefix of elements. |

| Return ||
|---------------------------------------------------------------------------------------|----------------|
| [Stream](Stream.md)<T>! | the new stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): Array<Any!>!
```

Returns an array containing the elements of this stream.

This is a [terminal operation](_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array, whose [type](../java.lang/Class.md))is`Object`, containing the elements of this stream |

### toArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : Any!> toArray(generator: IntFunction<Array<A>!>!): Array<A>!
```

Returns an array containing the elements of this stream, using the provided`generator`function to allocate the returned array, as well as any additional arrays that might be required for a partitioned execution or for resizing.

This is a [terminal operation](_package.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | the component type of the resulting array |
| `generator` | [IntFunction](../java.util.function/IntFunction.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<A\>!\>!:a function which produces a new array of the desired type and the provided length |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<A>! | an array containing the elements in this stream |

| Exceptions ||
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of any element of this stream is not assignable to the [runtime component type](../java.lang/Class.md))of the generated array |

### toList

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toList(): MutableList<T>!
```

Accumulates the elements of this stream into a`List`. The elements in the list will be in this stream's encounter order, if one exists. The returned List is unmodifiable; calls to any mutator method will always cause`UnsupportedOperationException`to be thrown. There are no guarantees on the implementation type or serializability of the returned List.

The returned instance may be [value-based](https://developer.android.com//reference/java/lang/doc-files/ValueBased.html). Callers should make no assumptions about the identity of the returned instances. Identity-sensitive operations on these instances (reference equality (`==`), identity hash code, and synchronization) are unreliable and should be avoided.

This is a [terminal operation](_package.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>! | a List containing the stream elements |
