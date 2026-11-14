# java.util.stream

# java.util.stream

## Interfaces

| [BaseStream](BaseStream.md) | Base interface for streams, which are sequences of elements supporting sequential and parallel aggregate operations. |
| --- | --- |
| [Collector](Collector.md) | A [mutable reduction operation](_package.md) that accumulates input elements into a mutable result container, optionally transforming the accumulated result into a final representation after all input elements have been processed. |
| [DoubleStream](DoubleStream.md) | A sequence of primitive double-valued elements supporting sequential and parallel aggregate operations. |
| [Gatherer](Gatherer.md) | An intermediate operation that transforms a stream of input elements into a stream of output elements, optionally applying a final action when the end of the upstream is reached. |
| --- | --- |
| [IntStream](IntStream.md) | A sequence of primitive int-valued elements supporting sequential and parallel aggregate operations. |
| [LongStream](LongStream.md) | A sequence of primitive long-valued elements supporting sequential and parallel aggregate operations. |
| [Stream](Stream.md) | A sequence of elements supporting sequential and parallel aggregate operations. |
| --- | --- |

## Classes

| [Collectors](Collectors.md) | Implementations of [Collector](Collector.md) that implement various useful reduction operations, such as accumulating elements into collections, summarizing elements according to various criteria, etc. |
| --- | --- |
| [Gatherers](Gatherers.md) | Implementations of [Gatherer](Gatherer.md) that provide useful intermediate operations, such as windowing functions, folding functions, transforming elements concurrently, etc. |
| [StreamSupport](StreamSupport.md) | Low-level utility methods for creating and manipulating streams. |
