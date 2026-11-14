Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Random

```
open class Random : RandomGenerator, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Random](Random.md) |

| Known Direct Subclasses [SecureRandom](../java.security/SecureRandom.md), [ThreadLocalRandom](../java.util.concurrent/ThreadLocalRandom.md) |---|---| | [SecureRandom](../java.security/SecureRandom.md) | This class provides a cryptographically strong random number generator (RNG). | | [ThreadLocalRandom](../java.util.concurrent/ThreadLocalRandom.md) | A random number generator (with period 264) isolated to the current thread. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An instance of this class is used to generate a stream of pseudorandom numbers; its period is only 248. The class uses a 48-bit seed, which is modified using a linear congruential formula. (See Donald E. Knuth, The Art of Computer Programming, Volume 2, Third edition: Seminumerical Algorithms, Section 3.2.1.)

If two instances of `Random` are created with the same seed, and the same sequence of method calls is made for each, they will generate and return identical sequences of numbers. In order to guarantee this property, particular algorithms are specified for the class `Random`. Java implementations must use all the algorithms shown here for the class `Random`, for the sake of absolute portability of Java code. However, subclasses of class `Random` are permitted to use other algorithms, so long as they adhere to the general contracts for all the methods.

The algorithms implemented by class `Random` use a `protected` utility method that on each invocation can supply up to 32 pseudorandomly generated bits.

Many applications will find the method `https://developer.android.com/reference/kotlin/java/lang/Math.html#random()` simpler to use.

Instances of `java.util.Random` are threadsafe. However, the concurrent use of the same `java.util.Random` instance across threads may encounter contention and consequent poor performance. Consider instead using `https://developer.android.com/reference/kotlin/java/util/concurrent/ThreadLocalRandom` in multithreaded designs.

Instances of `java.util.Random` are not cryptographically secure. Consider instead using `https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#` to get a cryptographically secure pseudo-random number generator for use by security-sensitive applications.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Random#Random()()` Creates a new random number generator. |
| `https://developer.android.com/reference/kotlin/java/util/Random#Random(kotlin.Long)(seed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Creates a new random number generator using a single `long` seed. |

| Public methods ||
|---|---|
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#doubles()()` Returns an effectively unlimited stream of pseudorandom `double` values, each between zero (inclusive) and one (exclusive). |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#doubles(kotlin.Double,%20kotlin.Double)(randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns an effectively unlimited stream of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive). |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#doubles(kotlin.Long)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each between zero (inclusive) and one (exclusive). |
| --- | --- |
| open [DoubleStream](../java.util.stream/DoubleStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#doubles(kotlin.Long,%20kotlin.Double,%20kotlin.Double)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive). |
| open static [Random](Random.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#from(java.util.random.RandomGenerator)(generator: https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator!)` Returns an instance of `Random` that delegates method calls to the `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator` argument. |
| open [IntStream](../java.util.stream/IntStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#ints()()` Returns an effectively unlimited stream of pseudorandom `int` values. |
| --- | --- |
| open [IntStream](../java.util.stream/IntStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#ints(kotlin.Int,%20kotlin.Int)(randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns an effectively unlimited stream of pseudorandom `int` values, each conforming to the given origin (inclusive) and bound (exclusive). |
| open [IntStream](../java.util.stream/IntStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#ints(kotlin.Long)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `int` values. |
| open [IntStream](../java.util.stream/IntStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#ints(kotlin.Long,%20kotlin.Int,%20kotlin.Int)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `int` values, each conforming to the given origin (inclusive) and bound (exclusive). |
| --- | --- |
| open [LongStream](../java.util.stream/LongStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#longs()()` Returns an effectively unlimited stream of pseudorandom `long` values. |
| open [LongStream](../java.util.stream/LongStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#longs(kotlin.Long)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `long` values. |
| open [LongStream](../java.util.stream/LongStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#longs(kotlin.Long,%20kotlin.Long)(randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns an effectively unlimited stream of pseudorandom `long` values, each conforming to the given origin (inclusive) and bound (exclusive). |
| --- | --- |
| open [LongStream](../java.util.stream/LongStream.md)! | `https://developer.android.com/reference/kotlin/java/util/Random#longs(kotlin.Long,%20kotlin.Long,%20kotlin.Long)(streamSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, randomNumberOrigin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, randomNumberBound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a stream producing the given `streamSize` number of pseudorandom `long`, each conforming to the given origin (inclusive) and bound (exclusive). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextBoolean()()` Returns the next pseudorandom, uniformly distributed `boolean` value from this random number generator's sequence. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextBytes(kotlin.ByteArray)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Generates random bytes and places them into a user-supplied byte array. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextDouble()()` Returns the next pseudorandom, uniformly distributed `double` value between `0.0` and `1.0` from this random number generator's sequence. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextFloat()()` Returns the next pseudorandom, uniformly distributed `float` value between `0.0` and `1.0` from this random number generator's sequence. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextGaussian()()` Returns the next pseudorandom, Gaussian ("normally") distributed `double` value with mean `0.0` and standard deviation `1.0` from this random number generator's sequence. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextInt()()` Returns the next pseudorandom, uniformly distributed `int` value from this random number generator's sequence. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextInt(kotlin.Int)(bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a pseudorandom, uniformly distributed `int` value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#nextLong()()` Returns the next pseudorandom, uniformly distributed `long` value from this random number generator's sequence. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#setSeed(kotlin.Long)(seed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets or updates the seed of this random number generator using the provided `long` seed value (optional operation). |

| Protected methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Random#next(kotlin.Int)(bits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Generates the next pseudorandom number. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator` |---|---| | `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream!` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#equiDoubles(kotlin.Double,%20kotlin.Double,%20kotlin.Boolean,%20kotlin.Boolean)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, isLeftIncluded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, isRightIncluded: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns an effectively unlimited stream of pseudorandomly chosen `double` values, where each value is between the specified `left` boundary and the specified `right` boundary. The `left` boundary is included as indicated by `isLeftIncluded`; similarly, the `right` boundary is included as indicated by `isRightIncluded`. The stream potentially produces all multiples *k* δ (*k* integer) lying in the interval specified by the parameters, where δ \> 0 is the smallest number for which all these multiples are exact `double`s. They are therefore all equidistant. The uniformity of the distribution of the `double`s produced by the stream depends on the quality of the underlying `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextLong(kotlin.Long)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#isDeprecated()()` Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextDouble(kotlin.Double)(bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns a pseudorandomly chosen `double` value between zero (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextDouble(kotlin.Double,%20kotlin.Double)(origin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns a pseudorandomly chosen `double` value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextExponential()()` Returns a nonnegative `double` value pseudorandomly chosen from an exponential distribution whose mean is 1. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextFloat(kotlin.Float)(bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a pseudorandomly chosen `float` value between zero (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextFloat(kotlin.Float,%20kotlin.Float)(origin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a pseudorandomly chosen `float` value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextGaussian(kotlin.Double,%20kotlin.Double)(mean: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, stddev: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns a `double` value pseudorandomly chosen from a Gaussian (normal) distribution with a mean and standard deviation specified by the arguments. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextInt(kotlin.Int,%20kotlin.Int)(origin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a pseudorandomly chosen `int` value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextLong(kotlin.Long)(bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a pseudorandomly chosen `long` value between zero (inclusive) and the specified bound (exclusive). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator#nextLong(kotlin.Long,%20kotlin.Long)(origin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, bound: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a pseudorandomly chosen `long` value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | ||

## Public constructors

### Random

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Random()
```

Creates a new random number generator. This constructor sets the seed of the random number generator to a value very likely to be distinct from any other invocation of this constructor.

### Random

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Random(seed: Long)
```

Creates a new random number generator using a single `long` seed. The seed is the initial value of the internal state of the pseudorandom number generator which is maintained by method `https://developer.android.com/reference/kotlin/java/util/Random#next(kotlin.Int)`.

| Parameters ||
|---|---|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the initial seed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Random#setSeed(kotlin.Long)`

## Public methods

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun doubles(): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandom `double` values, each between zero (inclusive) and one (exclusive).

A pseudorandom `double` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextDouble()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream!` | a stream of pseudorandom `double` values |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun doubles(
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive).

| Parameters ||
|---|---|
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the bound (exclusive) of each random value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream!` | a stream of pseudorandom `double` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `randomNumberOrigin` is not finite, or `randomNumberBound` is not finite, or `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun doubles(streamSize: Long): DoubleStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each between zero (inclusive) and one (exclusive).

A pseudorandom `double` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextDouble()`.

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream!` | a stream of `double` values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun doubles(
    streamSize: Long, 
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive).

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream!` | a stream of pseudorandom `double` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero, or `randomNumberOrigin` is not finite, or `randomNumberBound` is not finite, or `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### from

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun from(generator: RandomGenerator!): Random!
```

Returns an instance of `Random` that delegates method calls to the `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator` argument. If the generator is an instance of `Random`, it is returned. Otherwise, this method returns an instance of `Random` that delegates all methods except `setSeed` to the generator. The returned instance's `setSeed` method always throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. The returned instance is not serializable.

| Parameters ||
|---|---|
| `generator` | [RandomGenerator](../java.util.random/RandomGenerator.md)!: the `RandomGenerator` calls are delegated to |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Random#!` | the delegating `Random` instance |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if generator is null |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ints(): IntStream!
```

Returns an effectively unlimited stream of pseudorandom `int` values.

A pseudorandom `int` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextInt()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream!` | a stream of pseudorandom `int` values |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ints(
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns an effectively unlimited stream of pseudorandom `int` values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom `int` value is generated as if it's the result of calling the following method with the origin and bound:

```kotlin
<code>int nextInt(int origin, int bound) {
    int n = bound - origin;
    if (n &gt; 0) {
      return nextInt(n) + origin;
    }
    else {  // range not representable as int
      int r;
      do {
        r = nextInt();
      } while (r &lt; origin || r &gt;= bound);
      return r;
    }
  }</code>
```

| Parameters ||
|---|---|
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bound (exclusive) of each random value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream!` | a stream of pseudorandom `int` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ints(streamSize: Long): IntStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `int` values.

A pseudorandom `int` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextInt()`.

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream!` | a stream of pseudorandom `int` values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ints(
    streamSize: Long, 
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `int` values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom `int` value is generated as if it's the result of calling the following method with the origin and bound:

```kotlin
<code>int nextInt(int origin, int bound) {
    int n = bound - origin;
    if (n &gt; 0) {
      return nextInt(n) + origin;
    }
    else {  // range not representable as int
      int r;
      do {
        r = nextInt();
      } while (r &lt; origin || r &gt;= bound);
      return r;
    }
  }</code>
```

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream!` | a stream of pseudorandom `int` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero, or `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun longs(): LongStream!
```

Returns an effectively unlimited stream of pseudorandom `long` values.

A pseudorandom `long` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextLong()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/LongStream!` | a stream of pseudorandom `long` values |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun longs(streamSize: Long): LongStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `long` values.

A pseudorandom `long` value is generated as if it's the result of calling the method `https://developer.android.com/reference/kotlin/java/util/Random#nextLong()`.

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/LongStream!` | a stream of pseudorandom `long` values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun longs(
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns an effectively unlimited stream of pseudorandom `long` values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom `long` value is generated as if it's the result of calling the following method with the origin and bound:

```kotlin
<code>long nextLong(long origin, long bound) {
    long r = nextLong();
    long n = bound - origin, m = n - 1;
    if ((n &amp; m) == 0L)  // power of two
      r = (r &amp; m) + origin;
    else if (n &gt; 0L) {  // reject over-represented candidates
      for (long u = r &gt;&gt;&gt; 1;            // ensure nonnegative
           u + m - (r = u % n) &lt; 0L;    // rejection check
           u = nextLong() &gt;&gt;&gt; 1) // retry
          ;
      r += origin;
    }
    else {              // range not representable as long
      while (r &lt; origin || r &gt;= bound)
        r = nextLong();
    }
    return r;
  }</code>
```

| Parameters ||
|---|---|
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the bound (exclusive) of each random value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/LongStream!` | a stream of pseudorandom `long` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun longs(
    streamSize: Long, 
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns a stream producing the given `streamSize` number of pseudorandom `long`, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom `long` value is generated as if it's the result of calling the following method with the origin and bound:

```kotlin
<code>long nextLong(long origin, long bound) {
    long r = nextLong();
    long n = bound - origin, m = n - 1;
    if ((n &amp; m) == 0L)  // power of two
      r = (r &amp; m) + origin;
    else if (n &gt; 0L) {  // reject over-represented candidates
      for (long u = r &gt;&gt;&gt; 1;            // ensure nonnegative
           u + m - (r = u % n) &lt; 0L;    // rejection check
           u = nextLong() &gt;&gt;&gt; 1) // retry
          ;
      r += origin;
    }
    else {              // range not representable as long
      while (r &lt; origin || r &gt;= bound)
        r = nextLong();
    }
    return r;
  }</code>
```

| Parameters ||
|---|---|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of values to generate |
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the origin (inclusive) of each random value |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/LongStream!` | a stream of pseudorandom `long` values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `streamSize` is less than zero, or `randomNumberOrigin` is greater than or equal to `randomNumberBound` |

### nextBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextBoolean(): Boolean
```

Returns the next pseudorandom, uniformly distributed `boolean` value from this random number generator's sequence. The general contract of `nextBoolean` is that one `boolean` value is pseudorandomly generated and returned. The values `true` and `false` are produced with (approximately) equal probability.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the next pseudorandom, uniformly distributed `boolean` value from this random number generator's sequence |

### nextBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextBytes(bytes: ByteArray!): Unit
```

Generates random bytes and places them into a user-supplied byte array. The number of random bytes produced is equal to the length of the byte array.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the byte array to fill with random bytes |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the byte array is null |

### nextDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextDouble(): Double
```

Returns the next pseudorandom, uniformly distributed `double` value between `0.0` and `1.0` from this random number generator's sequence.

The general contract of `nextDouble` is that one `double` value, chosen (approximately) uniformly from the range `0.0d` (inclusive) to `1.0d` (exclusive), is pseudorandomly generated and returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the next pseudorandom, uniformly distributed `double` value between `0.0` and `1.0` from this random number generator's sequence |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Math.html#random()`

### nextFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextFloat(): Float
```

Returns the next pseudorandom, uniformly distributed `float` value between `0.0` and `1.0` from this random number generator's sequence.

The general contract of `nextFloat` is that one `float` value, chosen (approximately) uniformly from the range `0.0f` (inclusive) to `1.0f` (exclusive), is pseudorandomly generated and returned. All 224 possible `float` values of the form *m x* 2-24, where *m* is a positive integer less than 224, are produced with (approximately) equal probability.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the next pseudorandom, uniformly distributed `float` value between `0.0f` and `1.0f` from this random number generator's sequence |

### nextGaussian

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextGaussian(): Double
```

Returns the next pseudorandom, Gaussian ("normally") distributed `double` value with mean `0.0` and standard deviation `1.0` from this random number generator's sequence.

The general contract of `nextGaussian` is that one `double` value, chosen from (approximately) the usual normal distribution with mean `0.0` and standard deviation `1.0`, is pseudorandomly generated and returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the next pseudorandom, Gaussian ("normally") distributed `double` value with mean `0.0` and standard deviation `1.0` from this random number generator's sequence |

### nextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextInt(): Int
```

Returns the next pseudorandom, uniformly distributed `int` value from this random number generator's sequence. The general contract of `nextInt` is that one `int` value is pseudorandomly generated and returned. All 232 possible `int` values are produced with (approximately) equal probability.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next pseudorandom, uniformly distributed `int` value from this random number generator's sequence |

### nextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextInt(bound: Int): Int
```

Returns a pseudorandom, uniformly distributed `int` value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence. The general contract of `nextInt` is that one `int` value in the specified range is pseudorandomly generated and returned. All `bound` possible `int` values are produced with (approximately) equal probability.

| Parameters ||
|---|---|
| `bound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the upper bound (exclusive). Must be positive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next pseudorandom, uniformly distributed `int` value between zero (inclusive) and `bound` (exclusive) from this random number generator's sequence |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if bound is not positive |

### nextLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextLong(): Long
```

Returns the next pseudorandom, uniformly distributed `long` value from this random number generator's sequence. The general contract of `nextLong` is that one `long` value is pseudorandomly generated and returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the next pseudorandom, uniformly distributed `long` value from this random number generator's sequence |

### setSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSeed(seed: Long): Unit
```

Sets or updates the seed of this random number generator using the provided `long` seed value (optional operation).

| Parameters ||
|---|---|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seed value |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `setSeed` operation is not supported by this random number generator |

## Protected methods

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun next(bits: Int): Int
```

Generates the next pseudorandom number. This method returns an `int` value such that, if the argument `bits` is between `1` and `32` (inclusive), then that many low-order bits of the returned value will be (approximately) independently chosen bit values, each of which is (approximately) equally likely to be `0` or `1`.

| Parameters ||
|---|---|
| `bits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): random bits |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next pseudorandom value from this random number generator's sequence |
