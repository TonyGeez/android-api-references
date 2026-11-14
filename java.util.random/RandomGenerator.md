# RandomGenerator

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RandomGenerator

```
interface RandomGenerator
```

| [java.util.random.RandomGenerator](RandomGenerator.md) |

| Known Direct Subclasses [Random](../java.util/Random.md), [RandomGenerator.StreamableGenerator](../java/util/random/RandomGenerator.StreamableGenerator.md), [SplittableRandom](../java.util/SplittableRandom.md) |--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Random](../java.util/Random.md) | An instance of this class is used to generate a stream of pseudorandom numbers; its period is only 248. | | [RandomGenerator.StreamableGenerator](../java/util/random/RandomGenerator.StreamableGenerator.md) | The [StreamableGenerator](../java/util/random/RandomGenerator.StreamableGenerator.md) interface augments the [RandomGenerator](RandomGenerator.md) interface to provide methods that return streams of [RandomGenerator](RandomGenerator.md) objects. | | [SplittableRandom](../java.util/SplittableRandom.md) | A generator of uniform pseudorandom values (with period 264) applicable for use in (among other contexts) isolated parallel computations that may generate subtasks. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RandomGenerator.ArbitrarilyJumpableGenerator](../java/util/random/RandomGenerator.ArbitrarilyJumpableGenerator.md), [RandomGenerator.JumpableGenerator](../java/util/random/RandomGenerator.JumpableGenerator.md), [RandomGenerator.LeapableGenerator](../java/util/random/RandomGenerator.LeapableGenerator.md), [RandomGenerator.SplittableGenerator](../java/util/random/RandomGenerator.SplittableGenerator.md), [SecureRandom](../java.security/SecureRandom.md), [SplittableRandom](../java.util/SplittableRandom.md), [ThreadLocalRandom](../java.util.concurrent/ThreadLocalRandom.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RandomGenerator.ArbitrarilyJumpableGenerator](../java/util/random/RandomGenerator.ArbitrarilyJumpableGenerator.md) | This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can easily*jump*forward, by an arbitrary amount, to a distant point in the state cycle. | | [RandomGenerator.JumpableGenerator](../java/util/random/RandomGenerator.JumpableGenerator.md) | This interface is designed to provide a common protocol for objects that generate pseudorandom values and can easily*jump*forward, by a moderate amount (ex. 2 | | [RandomGenerator.LeapableGenerator](../java/util/random/RandomGenerator.LeapableGenerator.md) | This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can easily not only jump but also*leap*forward, by a large amount (ex. 2 | | [RandomGenerator.SplittableGenerator](../java/util/random/RandomGenerator.SplittableGenerator.md) | This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can be*split*into two objects (the original one and a new one) each of which obey that same protocol (and therefore can be recursively split indefinitely). | | [SecureRandom](../java.security/SecureRandom.md) | This class provides a cryptographically strong random number generator (RNG). | | [SplittableRandom](../java.util/SplittableRandom.md) | A generator of uniform pseudorandom values (with period 264) applicable for use in (among other contexts) isolated parallel computations that may generate subtasks. | | [ThreadLocalRandom](../java.util.concurrent/ThreadLocalRandom.md) | A random number generator (with period 264) isolated to the current thread. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The [RandomGenerator](RandomGenerator.md) interface is designed to provide a common protocol for objects that generate random or (more typically) pseudorandom sequences of numbers (or Boolean values). Such a sequence may be obtained by either repeatedly invoking a method that returns a single pseudorandomly chosen value, or by invoking a method that returns a stream of pseudorandomly chosen values.

Ideally, given an implicitly or explicitly specified range of values, each value would be chosen independently and uniformly from that range. In practice, one may have to settle for some approximation to independence and uniformity.

In the case of`int`,`long`, and`boolean`values, if there is no explicit specification of range, then the range includes all possible values of the type. In the case of`float`and`double`values, first a value is always chosen uniformly from the set of 2*w* values between 0.0 (inclusive) and 1.0 (exclusive), where*w* is [Float.PRECISION](../java.lang/Float.md) for`float`values and [Double.PRECISION](../java.lang/Double.md) for`double`values, such that adjacent values differ by 2−*w* (notice that this set is a*subset* of the set of*all representable floating-point values*between 0.0 (inclusive) and 1.0 (exclusive)); then if an explicit range was specified, then the chosen number is computationally scaled and translated so as to appear to have been chosen approximately uniformly from that explicit range.

Each method that returns a stream produces a stream of values each of which is chosen in the same manner as for a method that returns a single pseudorandomly chosen value. For example, if`r`implements [RandomGenerator](RandomGenerator.md), then the method call`r.ints(100)`returns a stream of 100`int`values. These are not necessarily the exact same values that would have been returned if instead`r.nextInt()`had been called 100 times; all that is guaranteed is that each value in the stream is chosen in a similar pseudorandom manner from the same range.

Every object that implements the [RandomGenerator](RandomGenerator.md) interface by using a pseudorandom algorithm is assumed to contain a finite amount of state. Using such an object to generate a pseudorandomly chosen value alters its state by computing a new state as a function of the current state, without reference to any information other than the current state. The number of distinct possible states of such an object is called its*period* . (Some implementations of the [RandomGenerator](RandomGenerator.md) interface may be truly random rather than pseudorandom, for example relying on the statistical behavior of a physical object to derive chosen values. Such implementations do not have a fixed period.)

As a rule, objects that implement the [RandomGenerator](RandomGenerator.md) interface need not be thread-safe. It is recommended that multithreaded applications use either [ThreadLocalRandom](../java.util.concurrent/ThreadLocalRandom.md) or (preferably) pseudorandom number generators that implement the [SplittableGenerator](../java/util/random/RandomGenerator.SplittableGenerator.md) or [JumpableGenerator](../java/util/random/RandomGenerator.JumpableGenerator.md) interface.

Objects that implement [RandomGenerator](RandomGenerator.md) are typically not cryptographically secure. Consider instead using [SecureRandom](../java.security/SecureRandom.md) to get a cryptographically secure pseudorandom number generator for use by security-sensitive applications. Note, however, that [SecureRandom](../java.security/SecureRandom.md) does implement the [RandomGenerator](RandomGenerator.md) interface, so that instances of [SecureRandom](../java.security/SecureRandom.md) may be used interchangeably with other types of pseudorandom generators in applications that do not require a secure generator.

Unless explicit stated otherwise, the use of null for any method argument will cause a NullPointerException.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ArbitrarilyJumpableGenerator](../java/util/random/RandomGenerator.ArbitrarilyJumpableGenerator.md) This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can easily*jump*forward, by an arbitrary amount, to a distant point in the state cycle. |
| abstract | [JumpableGenerator](../java/util/random/RandomGenerator.JumpableGenerator.md) This interface is designed to provide a common protocol for objects that generate pseudorandom values and can easily*jump*forward, by a moderate amount (ex. 2 |
| abstract | [LeapableGenerator](../java/util/random/RandomGenerator.LeapableGenerator.md) This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can easily not only jump but also*leap*forward, by a large amount (ex. 2 |
| --- | --- |
| abstract | [SplittableGenerator](../java/util/random/RandomGenerator.SplittableGenerator.md) This interface is designed to provide a common protocol for objects that generate sequences of pseudorandom values and can be*split*into two objects (the original one and a new one) each of which obey that same protocol (and therefore can be recursively split indefinitely). |
| abstract | [StreamableGenerator](../java/util/random/RandomGenerator.StreamableGenerator.md) The [StreamableGenerator](../java/util/random/RandomGenerator.StreamableGenerator.md) interface augments the [RandomGenerator](RandomGenerator.md) interface to provide methods that return streams of [RandomGenerator](RandomGenerator.md) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | [doubles](RandomGenerator.md))`()` Returns an effectively unlimited stream of pseudorandomly chosen`double`values. |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | [doubles](RandomGenerator.md))`(`randomNumberOrigin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `randomNumberBound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns an effectively unlimited stream of pseudorandomly chosen`double`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | [doubles](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`double`values. |
| --- | --- |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | [doubles](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `randomNumberBound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`double`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| openstatic [RandomGenerator](RandomGenerator.md)! | [getDefault](RandomGenerator.md))`()` Returns a [RandomGenerator](RandomGenerator.md) meeting the minimal requirement of having an [algorithm](_package.md) whose state bits are greater than or equal 64. |
| open [IntStream](../java.util.stream/IntStream.md)! | [ints](RandomGenerator.md))`()` Returns an effectively unlimited stream of pseudorandomly chosen`int`values. |
| --- | --- |
| open [IntStream](../java.util.stream/IntStream.md)! | [ints](RandomGenerator.md))`(`randomNumberOrigin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `randomNumberBound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an effectively unlimited stream of pseudorandomly chosen`int`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| open [IntStream](../java.util.stream/IntStream.md)! | [ints](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`int`values. |
| open [IntStream](../java.util.stream/IntStream.md)! | [ints](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `randomNumberBound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`int`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeprecated](RandomGenerator.md))`()` Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation. |
| open [LongStream](../java.util.stream/LongStream.md)! | [longs](RandomGenerator.md))`()` Returns an effectively unlimited stream of pseudorandomly chosen`long`values. |
| open [LongStream](../java.util.stream/LongStream.md)! | [longs](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`long`values. |
| --- | --- |
| open [LongStream](../java.util.stream/LongStream.md)! | [longs](RandomGenerator.md))`(`randomNumberOrigin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberBound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an effectively unlimited stream of pseudorandomly chosen`long`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| open [LongStream](../java.util.stream/LongStream.md)! | [longs](RandomGenerator.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberBound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandomly chosen`long`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextBoolean](RandomGenerator.md))`()` Returns a pseudorandomly chosen`boolean`value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [nextBytes](RandomGenerator.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Fills a user-supplied byte array with generated byte values pseudorandomly chosen uniformly from the range of values between -128 (inclusive) and 127 (inclusive). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](RandomGenerator.md))`()` Returns a pseudorandom`double`value between zero (inclusive) and one (exclusive). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](RandomGenerator.md))`(`bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a pseudorandomly chosen`double`value between zero (inclusive) and the specified bound (exclusive). |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](RandomGenerator.md))`(`origin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a pseudorandomly chosen`double`value between the specified origin (inclusive) and the specified bound (exclusive). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextExponential](RandomGenerator.md))`()` Returns a nonnegative`double`value pseudorandomly chosen from an exponential distribution whose mean is 1. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](RandomGenerator.md))`()` Returns a pseudorandom`float`value between zero (inclusive) and one (exclusive). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](RandomGenerator.md))`(`bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns a pseudorandomly chosen`float`value between zero (inclusive) and the specified bound (exclusive). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](RandomGenerator.md))`(`origin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns a pseudorandomly chosen`float`value between the specified origin (inclusive) and the specified bound (exclusive). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextGaussian](RandomGenerator.md))`()` Returns a`double`value pseudorandomly chosen from a Gaussian (normal) distribution whose mean is 0 and whose standard deviation is 1. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextGaussian](RandomGenerator.md))`(`mean:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `stddev:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a`double`value pseudorandomly chosen from a Gaussian (normal) distribution with a mean and standard deviation specified by the arguments. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](RandomGenerator.md))`()` Returns a pseudorandomly chosen`int`value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](RandomGenerator.md))`(`bound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pseudorandomly chosen`int`value between zero (inclusive) and the specified bound (exclusive). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](RandomGenerator.md))`(`origin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pseudorandomly chosen`int`value between the specified origin (inclusive) and the specified bound (exclusive). |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](RandomGenerator.md))`()` Returns a pseudorandomly chosen`long`value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](RandomGenerator.md))`(`bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a pseudorandomly chosen`long`value between zero (inclusive) and the specified bound (exclusive). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](RandomGenerator.md))`(`origin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a pseudorandomly chosen`long`value between the specified origin (inclusive) and the specified bound (exclusive). |
| openstatic [RandomGenerator](RandomGenerator.md)! | [of](RandomGenerator.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an instance of [RandomGenerator](RandomGenerator.md) that utilizes the`name` [algorithm](_package.md). |

## Public methods

### doubles

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doubles(): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`double`values.

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [DoubleStream](../java.util.stream/DoubleStream.md)! | a stream of pseudorandomly chosen`double`values |

### doubles

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doubles(
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`double`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the least value that can be produced |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the upper bound (exclusive) for each value produced |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [DoubleStream](../java.util.stream/DoubleStream.md)! | a stream of pseudorandomly chosen`double`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is not finite, or`randomNumberBound`is not finite, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### doubles

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doubles(streamSize: Long): DoubleStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`double`values.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [DoubleStream](../java.util.stream/DoubleStream.md)! | a stream of pseudorandomly chosen`double`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### doubles

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doubles(
    streamSize: Long, 
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`double`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the least value that can be produced |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the upper bound (exclusive) for each value produced |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [DoubleStream](../java.util.stream/DoubleStream.md)! | a stream of pseudorandomly chosen`double`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is not finite, or`randomNumberBound`is not finite, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### getDefault

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): RandomGenerator!
```

Returns a [RandomGenerator](RandomGenerator.md) meeting the minimal requirement of having an [algorithm](_package.md) whose state bits are greater than or equal 64.

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [RandomGenerator](RandomGenerator.md)! | a [RandomGenerator](RandomGenerator.md) |

### ints

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ints(): IntStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`int`values.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| [IntStream](../java.util.stream/IntStream.md)! | a stream of pseudorandomly chosen`int`values |

### ints

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ints(
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`int`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the least value that can be produced |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the upper bound (exclusive) for each value produced |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [IntStream](../java.util.stream/IntStream.md)! | a stream of pseudorandomly chosen`int`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### ints

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ints(streamSize: Long): IntStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`int`values.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| [IntStream](../java.util.stream/IntStream.md)! | a stream of pseudorandomly chosen`int`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### ints

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ints(
    streamSize: Long, 
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`int`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the least value that can be produced |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the upper bound (exclusive) for each value produced |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [IntStream](../java.util.stream/IntStream.md)! | a stream of pseudorandomly chosen`int`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### isDeprecated

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDeprecated(): Boolean
```

Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the implementation of RandomGenerator (algorithm) has been marked for deprecation |

### longs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longs(): LongStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`long`values.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [LongStream](../java.util.stream/LongStream.md)! | a stream of pseudorandomly chosen`long`values |

### longs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longs(streamSize: Long): LongStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`long`values.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [LongStream](../java.util.stream/LongStream.md)! | a stream of pseudorandomly chosen`long`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### longs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longs(
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns an effectively unlimited stream of pseudorandomly chosen`long`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the least value that can be produced |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the upper bound (exclusive) for each value produced |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [LongStream](../java.util.stream/LongStream.md)! | a stream of pseudorandomly chosen`long`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### longs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun longs(
    streamSize: Long, 
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns a stream producing the given`streamSize`number of pseudorandomly chosen`long`values, where each value is between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the least value that can be produced |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the upper bound (exclusive) for each value produced |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [LongStream](../java.util.stream/LongStream.md)! | a stream of pseudorandomly chosen`long`values, each between the specified origin (inclusive) and the specified bound (exclusive) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### nextBoolean

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextBoolean(): Boolean
```

Returns a pseudorandomly chosen`boolean`value.

The default implementation tests the high-order bit (sign bit) of a value produced by [nextInt](RandomGenerator.md))(), on the grounds that some algorithms for pseudorandom number generation produce values whose high-order bits have better statistical quality than the low-order bits.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a pseudorandomly chosen`boolean`value |

### nextBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextBytes(bytes: ByteArray!): Unit
```

Fills a user-supplied byte array with generated byte values pseudorandomly chosen uniformly from the range of values between -128 (inclusive) and 127 (inclusive).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array to fill with pseudorandom bytes |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if bytes is null |

### nextDouble

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextDouble(): Double
```

Returns a pseudorandom`double`value between zero (inclusive) and one (exclusive).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a pseudorandom`double`value between zero (inclusive) and one (exclusive) |

### nextDouble

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextDouble(bound: Double): Double
```

Returns a pseudorandomly chosen`double`value between zero (inclusive) and the specified bound (exclusive).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the upper bound (exclusive) for the returned value. Must be positive and finite |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a pseudorandomly chosen`double`value between zero (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`bound`is not both positive and finite |

### nextDouble

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextDouble(
    origin: Double, 
    bound: Double
): Double
```

Returns a pseudorandomly chosen`double`value between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `origin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the least value that can be returned |
| `bound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the upper bound (exclusive) for the returned value |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a pseudorandomly chosen`double`value between the origin (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`origin`is not finite, or`bound`is not finite, or`origin`is greater than or equal to`bound` |

### nextExponential

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextExponential(): Double
```

Returns a nonnegative`double`value pseudorandomly chosen from an exponential distribution whose mean is 1.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a nonnegative`double`value pseudorandomly chosen from an exponential distribution |

### nextFloat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextFloat(): Float
```

Returns a pseudorandom`float`value between zero (inclusive) and one (exclusive).

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a pseudorandom`float`value between zero (inclusive) and one (exclusive) |

### nextFloat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextFloat(bound: Float): Float
```

Returns a pseudorandomly chosen`float`value between zero (inclusive) and the specified bound (exclusive).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bound` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the upper bound (exclusive) for the returned value. Must be positive and finite |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a pseudorandomly chosen`float`value between zero (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`bound`is not both positive and finite |

### nextFloat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextFloat(
    origin: Float, 
    bound: Float
): Float
```

Returns a pseudorandomly chosen`float`value between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `origin` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the least value that can be returned |
| `bound` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the upper bound (exclusive) |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a pseudorandomly chosen`float`value between the origin (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`origin`is not finite, or`bound`is not finite, or`origin`is greater than or equal to`bound` |

### nextGaussian

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextGaussian(): Double
```

Returns a`double`value pseudorandomly chosen from a Gaussian (normal) distribution whose mean is 0 and whose standard deviation is 1.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a`double`value pseudorandomly chosen from a Gaussian distribution |

### nextGaussian

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextGaussian(
    mean: Double, 
    stddev: Double
): Double
```

Returns a`double`value pseudorandomly chosen from a Gaussian (normal) distribution with a mean and standard deviation specified by the arguments.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mean` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the mean of the Gaussian distribution to be drawn from |
| `stddev` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the standard deviation (square root of the variance) of the Gaussian distribution to be drawn from |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a`double`value pseudorandomly chosen from the specified Gaussian distribution |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.IllegalArgumentException` | if`stddev`is negative |

### nextInt

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextInt(): Int
```

Returns a pseudorandomly chosen`int`value.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a pseudorandomly chosen`int`value |

### nextInt

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextInt(bound: Int): Int
```

Returns a pseudorandomly chosen`int`value between zero (inclusive) and the specified bound (exclusive).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `bound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the upper bound (exclusive) for the returned value. Must be positive. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a pseudorandomly chosen`int`value between zero (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if`bound`is not positive |

### nextInt

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextInt(
    origin: Int, 
    bound: Int
): Int
```

Returns a pseudorandomly chosen`int`value between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `origin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the least value that can be returned |
| `bound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the upper bound (exclusive) for the returned value |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a pseudorandomly chosen`int`value between the origin (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if`origin`is greater than or equal to`bound` |

### nextLong

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextLong(): Long
```

Returns a pseudorandomly chosen`long`value.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a pseudorandomly chosen`long`value |

### nextLong

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextLong(bound: Long): Long
```

Returns a pseudorandomly chosen`long`value between zero (inclusive) and the specified bound (exclusive).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `bound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the upper bound (exclusive) for the returned value. Must be positive. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a pseudorandomly chosen`long`value between zero (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if`bound`is not positive |

### nextLong

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextLong(
    origin: Long, 
    bound: Long
): Long
```

Returns a pseudorandomly chosen`long`value between the specified origin (inclusive) and the specified bound (exclusive).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `origin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the least value that can be returned |
| `bound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the upper bound (exclusive) for the returned value |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a pseudorandomly chosen`long`value between the origin (inclusive) and the bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if`origin`is greater than or equal to`bound` |

### of

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun of(name: String!): RandomGenerator!
```

Returns an instance of [RandomGenerator](RandomGenerator.md) that utilizes the`name` [algorithm](_package.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of random number generator [algorithm](_package.md) |

| Return ||
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [RandomGenerator](RandomGenerator.md)! | An instance of [RandomGenerator](RandomGenerator.md) |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if name is null |
| `java.lang.IllegalArgumentException` | if the named algorithm is not found |
