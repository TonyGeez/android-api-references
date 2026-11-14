# java.util.stream

# java.util.stream

## Interfaces

| [BaseStream](../java/util/stream/BaseStream.md) | Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations. |
| --- | --- |
| [Collector](../java/util/stream/Collector.md) | A [mutable reduction operation](../java/util/stream/_package.md) that accumulates input elements into a mutable result container, optionally transforming the accumulated result into a final representation after all input elements have been processed. |
| [DoubleStream](../java/util/stream/DoubleStream.md) | A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. |
| [Gatherer](../java/util/stream/Gatherer.md) | An intermediate operation that transforms a stream of input elements into a stream of output elements, optionally applying a final action when the end of the upstream is reached. |
| --- | --- |
| [IntStream](../java/util/stream/IntStream.md) | A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. |
| [LongStream](../java/util/stream/LongStream.md) | A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. |
| [Stream](../java/util/stream/Stream.md) | A sequence of elements supporting sequential and parallel aggregate operations. |
| --- | --- |

## Classes

| [Collectors](../java/util/stream/Collectors.md) | Implementations of [Collector](../java/util/stream/Collector.md) that implement various useful reduction operations, such as accumulating elements into collections, summarizing elements according to various criteria, etc. |
| --- | --- |
| [Gatherers](../java/util/stream/Gatherers.md) | Implementations of [Gatherer](../java/util/stream/Gatherer.md) that provide useful intermediate operations, such as windowing functions, folding functions, transforming elements concurrently, etc. |
| [StreamSupport](../java/util/stream/StreamSupport.md) | Low-level utility methods for creating and manipulating streams. |
