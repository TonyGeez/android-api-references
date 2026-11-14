# BaseStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseStream

```
interface BaseStream<T : Any!, S : BaseStream<T, S>!> : AutoCloseable
```

| [java.util.stream.BaseStream](../java/util/stream/BaseStream.md) |

| Known Direct Subclasses [DoubleStream](../java/util/stream/DoubleStream.md), [IntStream](../java/util/stream/IntStream.md), [LongStream](../java/util/stream/LongStream.md), [Stream](../java/util/stream/Stream.md) |----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------| | [DoubleStream](../java/util/stream/DoubleStream.md) | A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. | | [IntStream](../java/util/stream/IntStream.md) | A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. | | [LongStream](../java/util/stream/LongStream.md) | A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. | | [Stream](../java/util/stream/Stream.md) | A sequence of elements supporting sequential and parallel aggregate operations. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations. The following example illustrates an aggregate operation using the stream types [Stream](../java/util/stream/Stream.md) and [IntStream](../java/util/stream/IntStream.md), computing the sum of the weights of the red widgets: 

```kotlin
<code>int sum = widgets.stream()
                       .filter(w -&gt; w.getColor() == RED)
                       .mapToInt(w -&gt; w.getWeight())
                       .sum();
  </code>
```
See the class documentation for [Stream](../java/util/stream/Stream.md) and the package documentation for [java.util.stream](../java/util/stream/_package.md) for additional specification of streams, stream operations, stream pipelines, and parallelism, which governs the behavior of all stream types.

<br />

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/stream/BaseStream.md))`()` Closes this stream, causing all close handlers for this stream pipeline to be called. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](../java/util/stream/BaseStream.md))`()` Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\>! | [iterator](../java/util/stream/BaseStream.md))`()` Returns an iterator for the elements of this stream. |
| --- | --- |
| abstractS | [onClose](../java/util/stream/BaseStream.md))`(`closeHandler:` ` [Runnable](../java/lang/Runnable.md)!`)` Returns an equivalent stream with an additional close handler. |
| abstractS | [parallel](../java/util/stream/BaseStream.md))`()` Returns an equivalent stream that is parallel. |
| abstractS | [sequential](../java/util/stream/BaseStream.md))`()` Returns an equivalent stream that is sequential. |
| --- | --- |
| abstract [Spliterator](../java/util/Spliterator.md)\<T\>! | [spliterator](../java/util/stream/BaseStream.md))`()` Returns a spliterator for the elements of this stream. |
| abstractS | [unordered](../java/util/stream/BaseStream.md))`()` Returns an equivalent stream that is [unordered](../java/util/stream/_package.md). |

## Public methods

### close

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this stream, causing all close handlers for this stream pipeline to be called.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

**See Also**

- [java.lang.AutoCloseable#close()](../java/lang/AutoCloseable.md)) 

### isParallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isParallel(): Boolean
```

Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. Calling this method after invoking an terminal stream operation method may yield unpredictable results.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this stream would execute in parallel if executed |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<T>!
```

Returns an iterator for the elements of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>! | the element iterator for this stream |

### onClose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClose(closeHandler: Runnable!): S
```

Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](../java/util/stream/BaseStream.md))method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself.

This is an [intermediate operation](../java/util/stream/_package.md).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------|
| `closeHandler` | [Runnable](../java/lang/Runnable.md)!:A task to execute when the stream is closed |

| Return ||
|---|-------------------------------------------------------------|
| S | a stream with a handler that is run if the stream is closed |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): S
```

Returns an equivalent stream that is parallel. May return itself, either because the stream was already parallel, or because the underlying stream state was modified to be parallel.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|---|-------------------|
| S | a parallel stream |

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): S
```

Returns an equivalent stream that is sequential. May return itself, either because the stream was already sequential, or because the underlying stream state was modified to be sequential.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|---|---------------------|
| S | a sequential stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator<T>!
```

Returns a spliterator for the elements of this stream.

This is a [terminal operation](../java/util/stream/_package.md).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<T>! | the element spliterator for this stream |

### unordered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unordered(): S
```

Returns an equivalent stream that is [unordered](../java/util/stream/_package.md). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered.

This is an [intermediate operation](../java/util/stream/_package.md).

| Return ||
|---|---------------------|
| S | an unordered stream |
