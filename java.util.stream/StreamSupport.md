# StreamSupport

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamSupport

```
class StreamSupport
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.stream.StreamSupport](StreamSupport.md) |

Low-level utility methods for creating and manipulating streams.

This class is mostly for library writers presenting stream views of data structures; most static stream methods intended for end users are in the various`Stream`classes.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DoubleStream](DoubleStream.md)! | [doubleStream](StreamSupport.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` ` [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`DoubleStream`from a`Supplier`of`Spliterator.OfDouble`. |
| static [DoubleStream](DoubleStream.md)! | [doubleStream](StreamSupport.md))`(`spliterator:` ` [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`DoubleStream`from a`Spliterator.OfDouble`. |
| static [IntStream](IntStream.md)! | [intStream](StreamSupport.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` ` [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`IntStream`from a`Supplier`of`Spliterator.OfInt`. |
| --- | --- |
| static [IntStream](IntStream.md)! | [intStream](StreamSupport.md))`(`spliterator:` ` [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`IntStream`from a`Spliterator.OfInt`. |
| static [LongStream](LongStream.md)! | [longStream](StreamSupport.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` ` [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`LongStream`from a`Supplier`of`Spliterator.OfLong`. |
| static [LongStream](LongStream.md)! | [longStream](StreamSupport.md))`(`spliterator:` ` [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`LongStream`from a`Spliterator.OfLong`. |
| --- | --- |
| static [Stream](Stream.md)\<T\>! | [stream](StreamSupport.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` ` [Spliterator](../java.util/Spliterator.md)<T>!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`Stream`from a`Supplier`of`Spliterator`. |
| static [Stream](Stream.md)\<T\>! | [stream](StreamSupport.md))`(`spliterator:` ` [Spliterator](../java.util/Spliterator.md)<T>!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`Stream`from a`Spliterator`. |

## Public methods

### doubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun doubleStream(
    supplier: Supplier<out Spliterator.OfDouble!>!, 
    characteristics: Int, 
    parallel: Boolean
): DoubleStream!
```

Creates a new sequential or parallel`DoubleStream`from a`Supplier`of`Spliterator.OfDouble`.

The [Supplier.get()](../java.util.function/Supplier.md))method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](../java.util/Spliterator.md), it is likely more efficient to use [doubleStream(java.util.Spliterator.OfDouble,boolean)](StreamSupport.md))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](_package.md) for more details.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!\>!:A`Supplier`of a`Spliterator.OfDouble` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfDouble`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](DoubleStream.md)! | a new sequential or parallel`DoubleStream` |

**See Also**

- [#doubleStream(java.util.Spliterator.OfDouble, boolean)](StreamSupport.md)) 

### doubleStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun doubleStream(
    spliterator: Spliterator.OfDouble!, 
    parallel: Boolean
): DoubleStream!
```

Creates a new sequential or parallel`DoubleStream`from a`Spliterator.OfDouble`.

The spliterator is only traversed, split, or queried for estimated size after the terminal operation of the stream pipeline commences.

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](../java.util/Spliterator.md). Otherwise, [doubleStream(java.util.function.Supplier,int,boolean)](StreamSupport.md))should be used to reduce the scope of potential interference with the source. See [Non-Interference](_package.md) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!:A`Spliterator.OfDouble`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](DoubleStream.md)! | a new sequential or parallel`DoubleStream` |

### intStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun intStream(
    supplier: Supplier<out Spliterator.OfInt!>!, 
    characteristics: Int, 
    parallel: Boolean
): IntStream!
```

Creates a new sequential or parallel`IntStream`from a`Supplier`of`Spliterator.OfInt`.

The [Supplier.get()](../java.util.function/Supplier.md))method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](../java.util/Spliterator.md), it is likely more efficient to use [intStream(java.util.Spliterator.OfInt,boolean)](StreamSupport.md))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](_package.md) for more details.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!\>!:a`Supplier`of a`Spliterator.OfInt` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfInt`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------|
| [IntStream](IntStream.md)! | a new sequential or parallel`IntStream` |

**See Also**

- [#intStream(java.util.Spliterator.OfInt, boolean)](StreamSupport.md)) 

### intStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun intStream(
    spliterator: Spliterator.OfInt!, 
    parallel: Boolean
): IntStream!
```

Creates a new sequential or parallel`IntStream`from a`Spliterator.OfInt`.

The spliterator is only traversed, split, or queried for estimated size after the terminal operation of the stream pipeline commences.

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](../java.util/Spliterator.md). Otherwise, [intStream(java.util.function.Supplier,int,boolean)](StreamSupport.md))should be used to reduce the scope of potential interference with the source. See [Non-Interference](_package.md) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!:a`Spliterator.OfInt`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------|
| [IntStream](IntStream.md)! | a new sequential or parallel`IntStream` |

### longStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun longStream(
    supplier: Supplier<out Spliterator.OfLong!>!, 
    characteristics: Int, 
    parallel: Boolean
): LongStream!
```

Creates a new sequential or parallel`LongStream`from a`Supplier`of`Spliterator.OfLong`.

The [Supplier.get()](../java.util.function/Supplier.md))method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](../java.util/Spliterator.md), it is likely more efficient to use [longStream(java.util.Spliterator.OfLong,boolean)](StreamSupport.md))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](_package.md) for more details.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!\>!:a`Supplier`of a`Spliterator.OfLong` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfLong`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------|
| [LongStream](LongStream.md)! | a new sequential or parallel`LongStream` |

**See Also**

- [#longStream(java.util.Spliterator.OfLong, boolean)](StreamSupport.md)) 

### longStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun longStream(
    spliterator: Spliterator.OfLong!, 
    parallel: Boolean
): LongStream!
```

Creates a new sequential or parallel`LongStream`from a`Spliterator.OfLong`.

The spliterator is only traversed, split, or queried for estimated size after the terminal operation of the stream pipeline commences.

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](../java.util/Spliterator.md). Otherwise, [longStream(java.util.function.Supplier,int,boolean)](StreamSupport.md))should be used to reduce the scope of potential interference with the source. See [Non-Interference](_package.md) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!:a`Spliterator.OfLong`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------|
| [LongStream](LongStream.md)! | a new sequential or parallel`LongStream` |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> stream(
    supplier: Supplier<out Spliterator<T>!>!, 
    characteristics: Int, 
    parallel: Boolean
): Stream<T>!
```

Creates a new sequential or parallel`Stream`from a`Supplier`of`Spliterator`.

The [Supplier.get()](../java.util.function/Supplier.md))method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](../java.util/Spliterator.md), it is likely more efficient to use [stream(java.util.Spliterator,boolean)](StreamSupport.md))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](_package.md) for more details.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out [Spliterator](../java.util/Spliterator.md)\<T\>!\>!:a`Supplier`of a`Spliterator` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| --- | --- |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](Stream.md)<T>! | a new sequential or parallel`Stream` |

**See Also**

- [#stream(java.util.Spliterator, boolean)](StreamSupport.md)) 

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> stream(
    spliterator: Spliterator<T>!, 
    parallel: Boolean
): Stream<T>!
```

Creates a new sequential or parallel`Stream`from a`Spliterator`.

The spliterator is only traversed, split, or queried for estimated size after the terminal operation of the stream pipeline commences.

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](../java.util/Spliterator.md). Otherwise, [stream(java.util.function.Supplier,int,boolean)](StreamSupport.md))should be used to reduce the scope of potential interference with the source. See [Non-Interference](_package.md) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `spliterator` | [Spliterator](../java.util/Spliterator.md)\<T\>!:a`Spliterator`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](Stream.md)<T>! | a new sequential or parallel`Stream` |
