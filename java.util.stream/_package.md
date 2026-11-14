# java.util.stream

# java.util.stream

## Interfaces

| [BaseStream](https://developer.android.com/reference/kotlin/java/util/stream/BaseStream) | Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations. |
| --- | --- |
| [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector) | A [mutable reduction operation](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#Reduction) that accumulates input elements into a mutable result container, optionally transforming the accumulated result into a final representation after all input elements have been processed. |
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream) | A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. |
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer) | An intermediate operation that transforms a stream of input elements into a stream of output elements, optionally applying a final action when the end of the upstream is reached. |
| --- | --- |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream) | A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. |
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream) | A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. |
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) | A sequence of elements supporting sequential and parallel aggregate operations. |
| --- | --- |

## Classes

| [Collectors](https://developer.android.com/reference/kotlin/java/util/stream/Collectors) | Implementations of [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector) that implement various useful reduction operations, such as accumulating elements into collections, summarizing elements according to various criteria, etc. |
| --- | --- |
| [Gatherers](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers) | Implementations of [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer) that provide useful intermediate operations, such as windowing functions, folding functions, transforming elements concurrently, etc. |
| [StreamSupport](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport) | Low-level utility methods for creating and manipulating streams. |
