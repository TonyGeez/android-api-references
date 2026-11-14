# Spliterators

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Spliterators

```
class Spliterators
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Spliterators](Spliterators.md) |

Static classes and methods for operating on or creating instances of [Spliterator](Spliterator.md) and its primitive specializations [Spliterator.OfInt](../java/util/Spliterator.OfInt.md), [Spliterator.OfLong](../java/util/Spliterator.OfLong.md), and [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md).

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AbstractDoubleSpliterator](../java/util/Spliterators.AbstractDoubleSpliterator.md) An abstract `Spliterator.OfDouble` that implements `trySplit` to permit limited parallelism. |
| abstract | [AbstractIntSpliterator](../java/util/Spliterators.AbstractIntSpliterator.md) An abstract `Spliterator.OfInt` that implements `trySplit` to permit limited parallelism. |
| abstract | [AbstractLongSpliterator](../java/util/Spliterators.AbstractLongSpliterator.md) An abstract `Spliterator.OfLong` that implements `trySplit` to permit limited parallelism. |
| --- | --- |
| abstract | [AbstractSpliterator](../java/util/Spliterators.AbstractSpliterator.md) An abstract `Spliterator` that implements `trySplit` to permit limited parallelism. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [emptyDoubleSpliterator](Spliterators.md))`()` Creates an empty `Spliterator.OfDouble` |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | [emptyIntSpliterator](Spliterators.md))`()` Creates an empty `Spliterator.OfInt` |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [emptyLongSpliterator](Spliterators.md))`()` Creates an empty `Spliterator.OfLong` |
| --- | --- |
| static [Spliterator](Spliterator.md)\<T\>! | [emptySpliterator](Spliterators.md))`()` Creates an empty `Spliterator` |
| static [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)! | [iterator](Spliterators.md))`(`spliterator:` ` [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!`)` Creates an `PrimitiveIterator.OfDouble` from a `Spliterator.OfDouble`. |
| static [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)! | [iterator](Spliterators.md))`(`spliterator:` ` [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!`)` Creates an `PrimitiveIterator.OfInt` from a `Spliterator.OfInt`. |
| --- | --- |
| static [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)! | [iterator](Spliterators.md))`(`spliterator:` ` [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!`)` Creates an `PrimitiveIterator.OfLong` from a `Spliterator.OfLong`. |
| static [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\>! | [iterator](Spliterators.md))`(`spliterator:` ` [Spliterator](Spliterator.md)<out` `T>!`)` Creates an `Iterator` from a `Spliterator`. |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [spliterator](Spliterators.md))`(`array:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfDouble` covering the elements of a given array, using a customized set of spliterator characteristics. |
| --- | --- |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [spliterator](Spliterators.md))`(`array:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfDouble` covering a range of elements of a given array, using a customized set of spliterator characteristics. |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | [spliterator](Spliterators.md))`(`array:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfInt` covering the elements of a given array, using a customized set of spliterator characteristics. |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | [spliterator](Spliterators.md))`(`array:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfInt` covering a range of elements of a given array, using a customized set of spliterator characteristics. |
| --- | --- |
| static [Spliterator](Spliterator.md)\<T\>! | [spliterator](Spliterators.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator` covering the elements of a given array, using a customized set of spliterator characteristics. |
| static [Spliterator](Spliterator.md)\<T\>! | [spliterator](Spliterators.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator` covering a range of elements of a given array, using a customized set of spliterator characteristics. |
| static [Spliterator](Spliterator.md)\<T\>! | [spliterator](Spliterators.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator` using the given collection's [iterator](Collection.md)) as the source of elements, and reporting its [size](Collection.md)) as its initial size. |
| --- | --- |
| static [Spliterator](Spliterator.md)\<T\>! | [spliterator](Spliterators.md))`(`iterator:` ` [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>!`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator` using a given `Iterator` as the source of elements, and with a given initially reported size. |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [spliterator](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)!`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfDouble` using a given `DoubleStream.DoubleIterator` as the source of elements, and with a given initially reported size. |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | [spliterator](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)!`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfInt` using a given `IntStream.IntIterator` as the source of elements, and with a given initially reported size. |
| --- | --- |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [spliterator](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)!`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfLong` using a given `LongStream.LongIterator` as the source of elements, and with a given initially reported size. |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [spliterator](Spliterators.md))`(`array:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfLong` covering the elements of a given array, using a customized set of spliterator characteristics. |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [spliterator](Spliterators.md))`(`array:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`, `fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `additionalCharacteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfLong` covering a range of elements of a given array, using a customized set of spliterator characteristics. |
| --- | --- |
| static [Spliterator](Spliterator.md)\<T\>! | [spliteratorUnknownSize](Spliterators.md))`(`iterator:` ` [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator` using a given `Iterator` as the source of elements, with no initial size estimate. |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | [spliteratorUnknownSize](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfDouble` using a given `DoubleStream.DoubleIterator` as the source of elements, with no initial size estimate. |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | [spliteratorUnknownSize](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfInt` using a given `IntStream.IntIterator` as the source of elements, with no initial size estimate. |
| --- | --- |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | [spliteratorUnknownSize](Spliterators.md))`(`iterator:` ` [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)!`, `characteristics:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a `Spliterator.OfLong` using a given `LongStream.LongIterator` as the source of elements, with no initial size estimate. |

## Public methods

### emptyDoubleSpliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun emptyDoubleSpliterator(): Spliterator.OfDouble!
```

Creates an empty `Spliterator.OfDouble`

The empty spliterator reports [Spliterator.SIZED](Spliterator.md) and [Spliterator.SUBSIZED](Spliterator.md). Calls to [java.util.Spliterator#trySplit()](Spliterator.md)) always return `null`.

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | An empty spliterator |

### emptyIntSpliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun emptyIntSpliterator(): Spliterator.OfInt!
```

Creates an empty `Spliterator.OfInt`

The empty spliterator reports [Spliterator.SIZED](Spliterator.md) and [Spliterator.SUBSIZED](Spliterator.md). Calls to [java.util.Spliterator#trySplit()](Spliterator.md)) always return `null`.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------|
| [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | An empty spliterator |

### emptyLongSpliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun emptyLongSpliterator(): Spliterator.OfLong!
```

Creates an empty `Spliterator.OfLong`

The empty spliterator reports [Spliterator.SIZED](Spliterator.md) and [Spliterator.SUBSIZED](Spliterator.md). Calls to [java.util.Spliterator#trySplit()](Spliterator.md)) always return `null`.

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | An empty spliterator |

### emptySpliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> emptySpliterator(): Spliterator<T>!
```

Creates an empty `Spliterator`

The empty spliterator reports [Spliterator.SIZED](Spliterator.md) and [Spliterator.SUBSIZED](Spliterator.md). Calls to [java.util.Spliterator#trySplit()](Spliterator.md)) always return `null`.

| Parameters ||
|-------|------------------|
| `<T>` | Type of elements |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------|
| [Spliterator](Spliterator.md)<T>! | An empty spliterator |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun iterator(spliterator: Spliterator.OfDouble!): PrimitiveIterator.OfDouble!
```

Creates an `PrimitiveIterator.OfDouble` from a `Spliterator.OfDouble`.

Traversal of elements should be accomplished through the iterator. The behaviour of traversal is undefined if the spliterator is operated after the iterator is returned.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)!: The spliterator |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------|
| [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)! | An iterator |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the given spliterator is `null` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun iterator(spliterator: Spliterator.OfInt!): PrimitiveIterator.OfInt!
```

Creates an `PrimitiveIterator.OfInt` from a `Spliterator.OfInt`.

Traversal of elements should be accomplished through the iterator. The behaviour of traversal is undefined if the spliterator is operated after the iterator is returned.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)!: The spliterator |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------|
| [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)! | An iterator |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the given spliterator is `null` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun iterator(spliterator: Spliterator.OfLong!): PrimitiveIterator.OfLong!
```

Creates an `PrimitiveIterator.OfLong` from a `Spliterator.OfLong`.

Traversal of elements should be accomplished through the iterator. The behaviour of traversal is undefined if the spliterator is operated after the iterator is returned.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------|
| `spliterator` | [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)!: The spliterator |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------|
| [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)! | An iterator |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the given spliterator is `null` |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> iterator(spliterator: Spliterator<out T>!): MutableIterator<T>!
```

Creates an `Iterator` from a `Spliterator`.

Traversal of elements should be accomplished through the iterator. The behaviour of traversal is undefined if the spliterator is operated after the iterator is returned.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `spliterator` | [Spliterator](Spliterator.md)\<out T\>!: The spliterator |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T>! | An iterator |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the given spliterator is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: DoubleArray!, 
    additionalCharacteristics: Int
): Spliterator.OfDouble!
```

Creates a `Spliterator.OfDouble` covering the elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(double[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.DoubleArray)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!: The array, assumed to be unmodified during use |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | A spliterator for an array |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |

**See Also**

- [java.util.Arrays#spliterator(double[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.DoubleArray)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: DoubleArray!, 
    fromIndex: Int, 
    toIndex: Int, 
    additionalCharacteristics: Int
): Spliterator.OfDouble!
```

Creates a `Spliterator.OfDouble` covering a range of elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(double[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.DoubleArray,%20kotlin.Int,%20kotlin.Int)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report. (For example, if it is known the array will not be further modified, specify `IMMUTABLE`; if the array data is considered to have an encounter order, specify `ORDERED`). The method [Arrays.spliterator(long[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray,%20kotlin.Int,%20kotlin.Int)) can often be used instead, which returns a spliterator that reports `SIZED`, `SUBSIZED`, `IMMUTABLE`, and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!: The array, assumed to be unmodified during use |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The least index (inclusive) to cover |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One past the greatest index to cover |
| --- | --- |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | A spliterator for an array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex` is negative, `toIndex` is less than `fromIndex`, or `toIndex` is greater than the array size |

**See Also**

- [java.util.Arrays#spliterator(double[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.DoubleArray,%20kotlin.Int,%20kotlin.Int)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: IntArray!, 
    additionalCharacteristics: Int
): Spliterator.OfInt!
```

Creates a `Spliterator.OfInt` covering the elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(int[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.IntArray)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The array, assumed to be unmodified during use |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | A spliterator for an array |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |

**See Also**

- [java.util.Arrays#spliterator(int[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.IntArray)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: IntArray!, 
    fromIndex: Int, 
    toIndex: Int, 
    additionalCharacteristics: Int
): Spliterator.OfInt!
```

Creates a `Spliterator.OfInt` covering a range of elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(int[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The array, assumed to be unmodified during use |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The least index (inclusive) to cover |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One past the greatest index to cover |
| --- | --- |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | A spliterator for an array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex` is negative, `toIndex` is less than `fromIndex`, or `toIndex` is greater than the array size |

**See Also**

- [java.util.Arrays#spliterator(int[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> spliterator(
    array: Array<Any!>!, 
    additionalCharacteristics: Int
): Spliterator<T>!
```

Creates a `Spliterator` covering the elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.Array)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The array, assumed to be unmodified during use |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [Spliterator](Spliterator.md)<T>! | A spliterator for an array |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |

**See Also**

- [java.util.Arrays#spliterator(Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.Array)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> spliterator(
    array: Array<Any!>!, 
    fromIndex: Int, 
    toIndex: Int, 
    additionalCharacteristics: Int
): Spliterator<T>!
```

Creates a `Spliterator` covering a range of elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.Array)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The array, assumed to be unmodified during use |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The least index (inclusive) to cover |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One past the greatest index to cover |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------|
| [Spliterator](Spliterator.md)<T>! | A spliterator for an array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex` is negative, `toIndex` is less than `fromIndex`, or `toIndex` is greater than the array size |

**See Also**

- [java.util.Arrays#spliterator(Object[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.Array,%20kotlin.Int,%20kotlin.Int)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> spliterator(
    c: MutableCollection<out T>!, 
    characteristics: Int
): Spliterator<T>!
```

Creates a `Spliterator` using the given collection's [iterator](Collection.md)) as the source of elements, and reporting its [size](Collection.md)) as its initial size.

The spliterator is * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the collection's iterator, and implements `trySplit` to permit limited parallelism.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out T\>!: The collection |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements. The characteristics `SIZED` and `SUBSIZED` are additionally reported unless `CONCURRENT` is supplied. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator](Spliterator.md)<T>! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if the given collection is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> spliterator(
    iterator: MutableIterator<T>!, 
    size: Long, 
    characteristics: Int
): Spliterator<T>!
```

Creates a `Spliterator` using a given `Iterator` as the source of elements, and with a given initially reported size.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned, or the initially reported size is not equal to the actual number of elements in the source.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `iterator` | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\>!: The iterator for the source |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of elements in the source, to be reported as initial `estimateSize` |
| --- | --- |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements. The characteristics `SIZED` and `SUBSIZED` are additionally reported unless `CONCURRENT` is supplied. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator](Spliterator.md)<T>! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    iterator: PrimitiveIterator.OfDouble!, 
    size: Long, 
    characteristics: Int
): Spliterator.OfDouble!
```

Creates a `Spliterator.OfDouble` using a given `DoubleStream.DoubleIterator` as the source of elements, and with a given initially reported size.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned, or the initially reported size is not equal to the actual number of elements in the source.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)!: The iterator for the source |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of elements in the source, to be reported as initial `estimateSize` |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements. The characteristics `SIZED` and `SUBSIZED` are additionally reported unless `CONCURRENT` is supplied. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    iterator: PrimitiveIterator.OfInt!, 
    size: Long, 
    characteristics: Int
): Spliterator.OfInt!
```

Creates a `Spliterator.OfInt` using a given `IntStream.IntIterator` as the source of elements, and with a given initially reported size.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned, or the initially reported size is not equal to the actual number of elements in the source.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)!: The iterator for the source |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of elements in the source, to be reported as initial `estimateSize`. |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements. The characteristics `SIZED` and `SUBSIZED` are additionally reported unless `CONCURRENT` is supplied. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    iterator: PrimitiveIterator.OfLong!, 
    size: Long, 
    characteristics: Int
): Spliterator.OfLong!
```

Creates a `Spliterator.OfLong` using a given `LongStream.LongIterator` as the source of elements, and with a given initially reported size.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned, or the initially reported size is not equal to the actual number of elements in the source.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)!: The iterator for the source |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of elements in the source, to be reported as initial `estimateSize`. |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements. The characteristics `SIZED` and `SUBSIZED` are additionally reported unless `CONCURRENT` is supplied. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: LongArray!, 
    additionalCharacteristics: Int
): Spliterator.OfLong!
```

Creates a `Spliterator.OfLong` covering the elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(long[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report; it is common to additionally specify `IMMUTABLE` and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: The array, assumed to be unmodified during use |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | A spliterator for an array |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |

**See Also**

- [java.util.Arrays#spliterator(long[])](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliterator(
    array: LongArray!, 
    fromIndex: Int, 
    toIndex: Int, 
    additionalCharacteristics: Int
): Spliterator.OfLong!
```

Creates a `Spliterator.OfLong` covering a range of elements of a given array, using a customized set of spliterator characteristics.

This method is provided as an implementation convenience for Spliterators which store portions of their elements in arrays, and need fine control over Spliterator characteristics. Most other situations in which a Spliterator for an array is needed should use [Arrays.spliterator(long[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray,%20kotlin.Int,%20kotlin.Int)).

The returned spliterator always reports the characteristics `SIZED` and `SUBSIZED`. The caller may provide additional characteristics for the spliterator to report. (For example, if it is known the array will not be further modified, specify `IMMUTABLE`; if the array data is considered to have an encounter order, specify `ORDERED`). The method [Arrays.spliterator(long[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray,%20kotlin.Int,%20kotlin.Int)) can often be used instead, which returns a spliterator that reports `SIZED`, `SUBSIZED`, `IMMUTABLE`, and `ORDERED`.

| Parameters ||
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: The array, assumed to be unmodified during use |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The least index (inclusive) to cover |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): One past the greatest index to cover |
| --- | --- |
| `additionalCharacteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional spliterator characteristics of this spliterator's source or elements beyond `SIZED` and `SUBSIZED` which are always reported |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | A spliterator for an array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given array is `null` |
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex` is negative, `toIndex` is less than `fromIndex`, or `toIndex` is greater than the array size |

**See Also**

- [java.util.Arrays#spliterator(long[], int, int)](https://developer.android.com/reference/kotlin/java/util/Arrays#spliterator(kotlin.LongArray,%20kotlin.Int,%20kotlin.Int)) 

### spliteratorUnknownSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> spliteratorUnknownSize(
    iterator: MutableIterator<T>!, 
    characteristics: Int
): Spliterator<T>!
```

Creates a `Spliterator` using a given `Iterator` as the source of elements, with no initial size estimate.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | Type of elements |
| `iterator` | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\>!: The iterator for the source |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements (`SIZED` and `SUBSIZED`, if supplied, are ignored and are not reported.) |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator](Spliterator.md)<T>! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliteratorUnknownSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliteratorUnknownSize(
    iterator: PrimitiveIterator.OfDouble!, 
    characteristics: Int
): Spliterator.OfDouble!
```

Creates a `Spliterator.OfDouble` using a given `DoubleStream.DoubleIterator` as the source of elements, with no initial size estimate.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md)!: The iterator for the source |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements (`SIZED` and `SUBSIZED`, if supplied, are ignored and are not reported.) |

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliteratorUnknownSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliteratorUnknownSize(
    iterator: PrimitiveIterator.OfInt!, 
    characteristics: Int
): Spliterator.OfInt!
```

Creates a `Spliterator.OfInt` using a given `IntStream.IntIterator` as the source of elements, with no initial size estimate.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md)!: The iterator for the source |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements (`SIZED` and `SUBSIZED`, if supplied, are ignored and are not reported.) |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfInt](../java/util/Spliterator.OfInt.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |

### spliteratorUnknownSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spliteratorUnknownSize(
    iterator: PrimitiveIterator.OfLong!, 
    characteristics: Int
): Spliterator.OfLong!
```

Creates a `Spliterator.OfLong` using a given `LongStream.LongIterator` as the source of elements, with no initial size estimate.

The spliterator is not * [late-binding](Spliterator.md)* , inherits the *fail-fast* properties of the iterator, and implements `trySplit` to permit limited parallelism.

Traversal of elements should be accomplished through the spliterator. The behaviour of splitting and traversal is undefined if the iterator is operated on after the spliterator is returned.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md)!: The iterator for the source |
| `characteristics` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Characteristics of this spliterator's source or elements (`SIZED` and `SUBSIZED`, if supplied, are ignored and are not reported.) |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------|
| [Spliterator.OfLong](../java/util/Spliterator.OfLong.md)! | A spliterator from an iterator |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the given iterator is `null` |
