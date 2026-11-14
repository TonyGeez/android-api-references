# StreamSupport

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamSupport

```
class StreamSupport
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.stream.StreamSupport](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#) |

Low-level utility methods for creating and manipulating streams.

This class is mostly for library writers presenting stream views of data structures; most static stream methods intended for end users are in the various`Stream`classes.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [doubleStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#doubleStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` ` [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`DoubleStream`from a`Supplier`of`Spliterator.OfDouble`. |
| static [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | [doubleStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#doubleStream(java.util.Spliterator.OfDouble,%20kotlin.Boolean))`(`spliterator:` ` [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`DoubleStream`from a`Spliterator.OfDouble`. |
| static [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | [intStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#intStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` ` [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`IntStream`from a`Supplier`of`Spliterator.OfInt`. |
| --- | --- |
| static [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | [intStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#intStream(java.util.Spliterator.OfInt,%20kotlin.Boolean))`(`spliterator:` ` [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`IntStream`from a`Spliterator.OfInt`. |
| static [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [longStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#longStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` ` [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`LongStream`from a`Supplier`of`Spliterator.OfLong`. |
| static [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [longStream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#longStream(java.util.Spliterator.OfLong,%20kotlin.Boolean))`(`spliterator:` ` [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`LongStream`from a`Spliterator.OfLong`. |
| --- | --- |
| static [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<T\>! | [stream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#stream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<out` ` [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)<T>!>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`Stream`from a`Supplier`of`Spliterator`. |
| static [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<T\>! | [stream](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#stream(java.util.Spliterator,%20kotlin.Boolean))`(`spliterator:` ` [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)<T>!`, `parallel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new sequential or parallel`Stream`from a`Spliterator`. |

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

The [Supplier.get()](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#get())method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding), it is likely more efficient to use [doubleStream(java.util.Spliterator.OfDouble,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#doubleStream(java.util.Spliterator.OfDouble,%20kotlin.Boolean))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<out [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)!\>!:A`Supplier`of a`Spliterator.OfDouble` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfDouble`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | a new sequential or parallel`DoubleStream` |

**See Also**

- [#doubleStream(java.util.Spliterator.OfDouble, boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#doubleStream(java.util.Spliterator.OfDouble,%20kotlin.Boolean)) 

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

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding). Otherwise, [doubleStream(java.util.function.Supplier,int,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#doubleStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))should be used to reduce the scope of potential interference with the source. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble.html#)!:A`Spliterator.OfDouble`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [DoubleStream](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream)! | a new sequential or parallel`DoubleStream` |

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

The [Supplier.get()](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#get())method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding), it is likely more efficient to use [intStream(java.util.Spliterator.OfInt,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#intStream(java.util.Spliterator.OfInt,%20kotlin.Boolean))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<out [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)!\>!:a`Supplier`of a`Spliterator.OfInt` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfInt`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | a new sequential or parallel`IntStream` |

**See Also**

- [#intStream(java.util.Spliterator.OfInt, boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#intStream(java.util.Spliterator.OfInt,%20kotlin.Boolean)) 

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

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding). Otherwise, [intStream(java.util.function.Supplier,int,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#intStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))should be used to reduce the scope of potential interference with the source. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfInt](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt.html#)!:a`Spliterator.OfInt`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | a new sequential or parallel`IntStream` |

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

The [Supplier.get()](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#get())method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding), it is likely more efficient to use [longStream(java.util.Spliterator.OfLong,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#longStream(java.util.Spliterator.OfLong,%20kotlin.Boolean))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<out [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)!\>!:a`Supplier`of a`Spliterator.OfLong` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator.OfLong`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | a new sequential or parallel`LongStream` |

**See Also**

- [#longStream(java.util.Spliterator.OfLong, boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#longStream(java.util.Spliterator.OfLong,%20kotlin.Boolean)) 

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

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding). Otherwise, [longStream(java.util.function.Supplier,int,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#longStream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))should be used to reduce the scope of potential interference with the source. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfLong](https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong.html#)!:a`Spliterator.OfLong`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | a new sequential or parallel`LongStream` |

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

The [Supplier.get()](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#get())method will be invoked on the supplier no more than once, and only after the terminal operation of the stream pipeline commences.

For spliterators that report a characteristic of`IMMUTABLE`or`CONCURRENT`, or that are [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding), it is likely more efficient to use [stream(java.util.Spliterator,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#stream(java.util.Spliterator,%20kotlin.Boolean))instead.

The use of a`Supplier`in this form provides a level of indirection that reduces the scope of potential interference with the source. Since the supplier is only invoked after the terminal operation commences, any modifications to the source up to the start of the terminal operation are reflected in the stream result. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<out [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)\<T\>!\>!:a`Supplier`of a`Spliterator` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Spliterator characteristics of the supplied`Spliterator`. The characteristics must be equal to`supplier.get().characteristics()`, otherwise undefined behavior may occur when terminal operation commences. |
| --- | --- |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<T>! | a new sequential or parallel`Stream` |

**See Also**

- [#stream(java.util.Spliterator, boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#stream(java.util.Spliterator,%20kotlin.Boolean)) 

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

It is strongly recommended the spliterator report a characteristic of`IMMUTABLE`or`CONCURRENT`, or be [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#binding). Otherwise, [stream(java.util.function.Supplier,int,boolean)](https://developer.android.com/reference/kotlin/java/util/stream/StreamSupport#stream(java.util.function.Supplier,%20kotlin.Int,%20kotlin.Boolean))should be used to reduce the scope of potential interference with the source. See [Non-Interference](https://developer.android.com/reference/kotlin/java/util/stream/package-summary#NonInterference) for more details.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of stream elements |
| `spliterator` | [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#)\<T\>!:a`Spliterator`describing the stream elements |
| `parallel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`then the returned stream is a parallel stream; if`false`the returned stream is a sequential stream. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<T>! | a new sequential or parallel`Stream` |
