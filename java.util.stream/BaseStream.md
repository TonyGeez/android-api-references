# BaseStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseStream

```
interface BaseStream<T : Any!, S : BaseStream<T, S>!> : AutoCloseable
```

| [java.util.stream.BaseStream](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#) |

| Known Direct Subclasses [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream), [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream), [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream), [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) |----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------| | [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream) | A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. | | [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream) | A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. | | [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream) | A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. | | [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) | A sequence of elements supporting sequential and parallel aggregate operations. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations. The following example illustrates an aggregate operation using the stream types [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream), computing the sum of the weights of the red widgets: 

```kotlin
<code>int sum = widgets.stream()
                       .filter(w -&gt; w.getColor() == RED)
                       .mapToInt(w -&gt; w.getWeight())
                       .sum();
  </code>
```
See the class documentation for [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) and the package documentation for [java.util.stream](https://developer.android.com/reference/kotlin/java/util/stream/package-summary) for additional specification of streams, stream operations, stream pipelines, and parallelism, which governs the behavior of all stream types.

<br />

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())`()` Closes this stream, causing all close handlers for this stream pipeline to be called. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParallel](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#isParallel())`()` Returns whether this stream, if a terminal operation were to be executed, would execute in parallel. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\>! | [iterator](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#iterator())`()` Returns an iterator for the elements of this stream. |
| --- | --- |
| abstractS | [onClose](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#onClose(java.lang.Runnable))`(`closeHandler:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Returns an equivalent stream with an additional close handler. |
| abstractS | [parallel](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#parallel())`()` Returns an equivalent stream that is parallel. |
| abstractS | [sequential](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#sequential())`()` Returns an equivalent stream that is sequential. |
| --- | --- |
| abstract [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)\<T\>! | [spliterator](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#spliterator())`()` Returns a spliterator for the elements of this stream. |
| abstractS | [unordered](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#unordered())`()` Returns an equivalent stream that is [unordered](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Ordering). |

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

- [java.lang.AutoCloseable#close()](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close()) 

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

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>! | the element iterator for this stream |

### onClose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClose(closeHandler: Runnable!): S
```

Returns an equivalent stream with an additional close handler. Close handlers are run when the [close()](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close())method is called on the stream, and are executed in the order they were added. All close handlers are run, even if earlier close handlers throw exceptions. If any close handler throws an exception, the first exception thrown will be relayed to the caller of`close()`, with any remaining exceptions added to that exception as suppressed exceptions (unless one of the remaining exceptions is the same exception as the first exception, since an exception cannot suppress itself.) May return itself.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------|
| `closeHandler` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:A task to execute when the stream is closed |

| Return ||
|---|-------------------------------------------------------------|
| S | a stream with a handler that is run if the stream is closed |

### parallel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parallel(): S
```

Returns an equivalent stream that is parallel. May return itself, either because the stream was already parallel, or because the underlying stream state was modified to be parallel.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|---|-------------------|
| S | a parallel stream |

### sequential

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sequential(): S
```

Returns an equivalent stream that is sequential. May return itself, either because the stream was already sequential, or because the underlying stream state was modified to be sequential.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|---|---------------------|
| S | a sequential stream |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spliterator(): Spliterator<T>!
```

Returns a spliterator for the elements of this stream.

This is a [terminal operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------|
| [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)<T>! | the element spliterator for this stream |

### unordered

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unordered(): S
```

Returns an equivalent stream that is [unordered](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Ordering). May return itself, either because the stream was already unordered, or because the underlying stream state was modified to be unordered.

This is an [intermediate operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#StreamOps).

| Return ||
|---|---------------------|
| S | an unordered stream |
