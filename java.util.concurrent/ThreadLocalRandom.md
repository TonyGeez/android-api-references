# ThreadLocalRandom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadLocalRandom

```
class ThreadLocalRandom : Random
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Random](../java/util/Random.md) ||
| | ↳ | [java.util.concurrent.ThreadLocalRandom](../java/util/concurrent/ThreadLocalRandom.md) |

A random number generator (with period 264) isolated to the current thread. Like the global [java.util.Random](../java/util/Random.md) generator used by the [java.lang.Math](../java/lang/Math.md) class, a`ThreadLocalRandom`is initialized with an internally generated seed that may not otherwise be modified. When applicable, use of`ThreadLocalRandom`rather than shared`Random`objects in concurrent programs will typically encounter much less overhead and contention. Use of`ThreadLocalRandom`is particularly appropriate when multiple tasks (for example, each a [ForkJoinTask](../java/util/concurrent/ForkJoinTask.md)) use random numbers in parallel in thread pools.

Usages of this class should typically be of the form:`ThreadLocalRandom.current().nextX(...)`(where`X`is`Int`,`Long`, etc). When all usages are of this form, it is never possible to accidentally share a`ThreadLocalRandom`across multiple threads.

This class also provides additional commonly used bounded random generation methods.

Instances of`ThreadLocalRandom`are not cryptographically secure. Consider instead using [java.security.SecureRandom](../java/security/SecureRandom.md) in security-sensitive applications. Additionally, default-constructed instances do not use a cryptographically random seed unless the java.lang.System#getProperty`java.util.secureRandomSeed`is set to`true`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ThreadLocalRandom](../java/util/concurrent/ThreadLocalRandom.md)! | [current](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the current thread's`ThreadLocalRandom`object. |
| [DoubleStream](../java/util/stream/DoubleStream.md)! | [doubles](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns an effectively unlimited stream of pseudorandom`double`values, each between zero (inclusive) and one (exclusive). |
| [DoubleStream](../java/util/stream/DoubleStream.md)! | [doubles](../java/util/concurrent/ThreadLocalRandom.md))`(`randomNumberOrigin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `randomNumberBound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns an effectively unlimited stream of pseudorandom`double`values, each conforming to the given origin (inclusive) and bound (exclusive). |
| --- | --- |
| [DoubleStream](../java/util/stream/DoubleStream.md)! | [doubles](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`double`values, each between zero (inclusive) and one (exclusive). |
| [DoubleStream](../java/util/stream/DoubleStream.md)! | [doubles](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `randomNumberBound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`double`values, each conforming to the given origin (inclusive) and bound (exclusive). |
| [IntStream](../java/util/stream/IntStream.md)! | [ints](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns an effectively unlimited stream of pseudorandom`int`values. |
| --- | --- |
| [IntStream](../java/util/stream/IntStream.md)! | [ints](../java/util/concurrent/ThreadLocalRandom.md))`(`randomNumberOrigin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `randomNumberBound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an effectively unlimited stream of pseudorandom`int`values, each conforming to the given origin (inclusive) and bound (exclusive). |
| [IntStream](../java/util/stream/IntStream.md)! | [ints](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`int`values. |
| [IntStream](../java/util/stream/IntStream.md)! | [ints](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `randomNumberBound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`int`values, each conforming to the given origin (inclusive) and bound (exclusive). |
| --- | --- |
| [LongStream](../java/util/stream/LongStream.md)! | [longs](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns an effectively unlimited stream of pseudorandom`long`values. |
| [LongStream](../java/util/stream/LongStream.md)! | [longs](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`long`values. |
| [LongStream](../java/util/stream/LongStream.md)! | [longs](../java/util/concurrent/ThreadLocalRandom.md))`(`randomNumberOrigin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberBound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an effectively unlimited stream of pseudorandom`long`values, each conforming to the given origin (inclusive) and bound (exclusive). |
| --- | --- |
| [LongStream](../java/util/stream/LongStream.md)! | [longs](../java/util/concurrent/ThreadLocalRandom.md))`(`streamSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberOrigin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `randomNumberBound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a stream producing the given`streamSize`number of pseudorandom`long`, each conforming to the given origin (inclusive) and bound (exclusive). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextBoolean](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the next pseudorandom, uniformly distributed`boolean`value from this random number generator's sequence. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the next pseudorandom, uniformly distributed`double`value between`0.0`and`1.0`from this random number generator's sequence. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](../java/util/concurrent/ThreadLocalRandom.md))`(`bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a pseudorandomly chosen`double`value between zero (inclusive) and the specified bound (exclusive). |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](../java/util/concurrent/ThreadLocalRandom.md))`(`origin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns a pseudorandomly chosen`double`value between the specified origin (inclusive) and the specified bound (exclusive). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the next pseudorandom, uniformly distributed`float`value between`0.0`and`1.0`from this random number generator's sequence. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](../java/util/concurrent/ThreadLocalRandom.md))`(`bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns a pseudorandomly chosen`float`value between zero (inclusive) and the specified bound (exclusive). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](../java/util/concurrent/ThreadLocalRandom.md))`(`origin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns a pseudorandomly chosen`float`value between the specified origin (inclusive) and the specified bound (exclusive). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the next pseudorandom, uniformly distributed`int`value from this random number generator's sequence. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](../java/util/concurrent/ThreadLocalRandom.md))`(`bound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pseudorandom, uniformly distributed`int`value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](../java/util/concurrent/ThreadLocalRandom.md))`(`origin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pseudorandomly chosen`int`value between the specified origin (inclusive) and the specified bound (exclusive). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](../java/util/concurrent/ThreadLocalRandom.md))`()` Returns the next pseudorandom, uniformly distributed`long`value from this random number generator's sequence. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](../java/util/concurrent/ThreadLocalRandom.md))`(`bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a pseudorandomly chosen`long`value between zero (inclusive) and the specified bound (exclusive). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](../java/util/concurrent/ThreadLocalRandom.md))`(`origin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a pseudorandomly chosen`long`value between the specified origin (inclusive) and the specified bound (exclusive). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSeed](../java/util/concurrent/ThreadLocalRandom.md))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Throws`UnsupportedOperationException`. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](../java/util/concurrent/ThreadLocalRandom.md))`(`bits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates a pseudorandom number with the indicated number of low-order bits. |

| Inherited functions ||
|---|---|
| From class [Random](../java/util/Random.md) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Random](../java/util/Random.md)! | [from](../java/util/Random.md))`(`generator:` ` [RandomGenerator](../java/util/random/RandomGenerator.md)!`)` <br /> Returns an instance of`Random`that delegates method calls to the [RandomGenerator](../java/util/random/RandomGenerator.md) argument. If the generator is an instance of`Random`, it is returned. Otherwise, this method returns an instance of`Random`that delegates all methods except`setSeed`to the generator. The returned instance's`setSeed`method always throws [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md). The returned instance is not serializable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [nextBytes](../java/util/Random.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Generates random bytes and places them into a user-supplied byte array. The number of random bytes produced is equal to the length of the byte array. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextGaussian](../java/util/Random.md))`()` <br /> Returns the next pseudorandom, Gaussian ("normally") distributed`double`value with mean`0.0`and standard deviation`1.0`from this random number generator's sequence. The general contract of`nextGaussian`is that one`double`value, chosen from (approximately) the usual normal distribution with mean`0.0`and standard deviation`1.0`, is pseudorandomly generated and returned. <br /> | ||
| From class [RandomGenerator](../java/util/random/RandomGenerator.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeprecated](../java/util/random/RandomGenerator.md))`()` <br /> Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](../java/util/random/RandomGenerator.md))`(`bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Returns a pseudorandomly chosen`double`value between zero (inclusive) and the specified bound (exclusive). <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](../java/util/random/RandomGenerator.md))`(`origin:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `bound:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Returns a pseudorandomly chosen`double`value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextExponential](../java/util/random/RandomGenerator.md))`()` <br /> Returns a nonnegative`double`value pseudorandomly chosen from an exponential distribution whose mean is 1. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](../java/util/random/RandomGenerator.md))`(`bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Returns a pseudorandomly chosen`float`value between zero (inclusive) and the specified bound (exclusive). <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [nextFloat](../java/util/random/RandomGenerator.md))`(`origin:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bound:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Returns a pseudorandomly chosen`float`value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextGaussian](../java/util/random/RandomGenerator.md))`(`mean:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `stddev:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Returns a`double`value pseudorandomly chosen from a Gaussian (normal) distribution with a mean and standard deviation specified by the arguments. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextInt](../java/util/random/RandomGenerator.md))`(`origin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bound:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a pseudorandomly chosen`int`value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](../java/util/random/RandomGenerator.md))`(`bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Returns a pseudorandomly chosen`long`value between zero (inclusive) and the specified bound (exclusive). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [nextLong](../java/util/random/RandomGenerator.md))`(`origin:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `bound:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Returns a pseudorandomly chosen`long`value between the specified origin (inclusive) and the specified bound (exclusive). <br /> | ||

## Public methods

### current

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun current(): ThreadLocalRandom!
```

Returns the current thread's`ThreadLocalRandom`object. Methods of this object should be called only by the current thread, not by other threads.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ThreadLocalRandom](../java/util/concurrent/ThreadLocalRandom.md)! | the current thread's`ThreadLocalRandom` |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doubles(): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandom`double`values, each between zero (inclusive) and one (exclusive).

A pseudorandom`double`value is generated as if it's the result of calling the method [nextDouble()](../java/util/Random.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a stream of pseudorandom`double`values |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doubles(
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns an effectively unlimited stream of pseudorandom`double`values, each conforming to the given origin (inclusive) and bound (exclusive).

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the bound (exclusive) of each random value |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a stream of pseudorandom`double`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is not finite, or`randomNumberBound`is not finite, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doubles(streamSize: Long): DoubleStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`double`values, each between zero (inclusive) and one (exclusive).

A pseudorandom`double`value is generated as if it's the result of calling the method [nextDouble()](../java/util/Random.md)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a stream of`double`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### doubles

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doubles(
    streamSize: Long, 
    randomNumberOrigin: Double, 
    randomNumberBound: Double
): DoubleStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`double`values, each conforming to the given origin (inclusive) and bound (exclusive).

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [DoubleStream](../java/util/stream/DoubleStream.md)! | a stream of pseudorandom`double`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is not finite, or`randomNumberBound`is not finite, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ints(): IntStream!
```

Returns an effectively unlimited stream of pseudorandom`int`values.

A pseudorandom`int`value is generated as if it's the result of calling the method [nextInt()](../java/util/Random.md)).

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| [IntStream](../java/util/stream/IntStream.md)! | a stream of pseudorandom`int`values |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ints(
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns an effectively unlimited stream of pseudorandom`int`values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom`int`value is generated as if it's the result of calling the following method with the origin and bound: 

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
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bound (exclusive) of each random value |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [IntStream](../java/util/stream/IntStream.md)! | a stream of pseudorandom`int`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ints(streamSize: Long): IntStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`int`values.

A pseudorandom`int`value is generated as if it's the result of calling the method [nextInt()](../java/util/Random.md)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| [IntStream](../java/util/stream/IntStream.md)! | a stream of pseudorandom`int`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### ints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ints(
    streamSize: Long, 
    randomNumberOrigin: Int, 
    randomNumberBound: Int
): IntStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`int`values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom`int`value is generated as if it's the result of calling the following method with the origin and bound: 

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
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [IntStream](../java/util/stream/IntStream.md)! | a stream of pseudorandom`int`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun longs(): LongStream!
```

Returns an effectively unlimited stream of pseudorandom`long`values.

A pseudorandom`long`value is generated as if it's the result of calling the method [nextLong()](../java/util/Random.md)).

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a stream of pseudorandom`long`values |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun longs(streamSize: Long): LongStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`long`values.

A pseudorandom`long`value is generated as if it's the result of calling the method [nextLong()](../java/util/Random.md)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a stream of pseudorandom`long`values |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun longs(
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns an effectively unlimited stream of pseudorandom`long`values, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom`long`value is generated as if it's the result of calling the following method with the origin and bound: 

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
|----------------------|--------------------------------------------------------------------------------------------------------------------------|
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the bound (exclusive) of each random value |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a stream of pseudorandom`long`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### longs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun longs(
    streamSize: Long, 
    randomNumberOrigin: Long, 
    randomNumberBound: Long
): LongStream!
```

Returns a stream producing the given`streamSize`number of pseudorandom`long`, each conforming to the given origin (inclusive) and bound (exclusive).

A pseudorandom`long`value is generated as if it's the result of calling the following method with the origin and bound: 

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
|----------------------|--------------------------------------------------------------------------------------------------------------------------|
| `streamSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of values to generate |
| `randomNumberOrigin` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the origin (inclusive) of each random value |
| `randomNumberBound` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the bound (exclusive) of each random value |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [LongStream](../java/util/stream/LongStream.md)! | a stream of pseudorandom`long`values, each with the given origin (inclusive) and bound (exclusive) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`streamSize`is less than zero, or`randomNumberOrigin`is greater than or equal to`randomNumberBound` |

### nextBoolean

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextBoolean(): Boolean
```

Returns the next pseudorandom, uniformly distributed`boolean`value from this random number generator's sequence. The general contract of`nextBoolean`is that one`boolean`value is pseudorandomly generated and returned. The values`true`and`false`are produced with (approximately) equal probability.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the next pseudorandom, uniformly distributed`boolean`value from this random number generator's sequence |

### nextDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextDouble(): Double
```

Returns the next pseudorandom, uniformly distributed`double`value between`0.0`and`1.0`from this random number generator's sequence.

The general contract of`nextDouble`is that one`double`value, chosen (approximately) uniformly from the range`0.0d`(inclusive) to`1.0d`(exclusive), is pseudorandomly generated and returned.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the next pseudorandom, uniformly distributed`double`value between`0.0`and`1.0`from this random number generator's sequence |

### nextDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextDouble(bound: Double): Double
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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextDouble(
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

### nextFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextFloat(): Float
```

Returns the next pseudorandom, uniformly distributed`float`value between`0.0`and`1.0`from this random number generator's sequence.

The general contract of`nextFloat`is that one`float`value, chosen (approximately) uniformly from the range`0.0f`(inclusive) to`1.0f`(exclusive), is pseudorandomly generated and returned. All 224 possible`float`values of the form*m x* 2-24, where*m*is a positive integer less than 224, are produced with (approximately) equal probability.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the next pseudorandom, uniformly distributed`float`value between`0.0f`and`1.0f`from this random number generator's sequence |

### nextFloat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextFloat(bound: Float): Float
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
fun nextFloat(
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

### nextInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextInt(): Int
```

Returns the next pseudorandom, uniformly distributed`int`value from this random number generator's sequence. The general contract of`nextInt`is that one`int`value is pseudorandomly generated and returned. All 232 possible`int`values are produced with (approximately) equal probability.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next pseudorandom, uniformly distributed`int`value from this random number generator's sequence |

### nextInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextInt(bound: Int): Int
```

Returns a pseudorandom, uniformly distributed`int`value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence. The general contract of`nextInt`is that one`int`value in the specified range is pseudorandomly generated and returned. All`bound`possible`int`values are produced with (approximately) equal probability.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `bound` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the upper bound (exclusive). Must be positive. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next pseudorandom, uniformly distributed`int`value between zero (inclusive) and`bound`(exclusive) from this random number generator's sequence |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if bound is not positive |

### nextInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextInt(
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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextLong(): Long
```

Returns the next pseudorandom, uniformly distributed`long`value from this random number generator's sequence. The general contract of`nextLong`is that one`long`value is pseudorandomly generated and returned.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the next pseudorandom, uniformly distributed`long`value from this random number generator's sequence |

### nextLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextLong(bound: Long): Long
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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun nextLong(
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

### setSeed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSeed(seed: Long): Unit
```

Throws`UnsupportedOperationException`. Setting seeds in this generator is not supported.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the seed value |

| Exceptions ||
|-------------------------------------------|--------|
| `java.lang.UnsupportedOperationException` | always |

## Protected methods

### next

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun next(bits: Int): Int
```

Generates a pseudorandom number with the indicated number of low-order bits. Because this class has no subclasses, this method cannot be invoked or overridden.

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `bits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):random bits |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next pseudorandom value from this random number generator's sequence |
