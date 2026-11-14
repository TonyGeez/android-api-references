# RandomGeneratorFactory

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RandomGeneratorFactory

```
class RandomGeneratorFactory<T : RandomGenerator!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.random.RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) |

This is a factory class for generating multiple random number generators of a specific [algorithm](../java/util/random/_package.md). [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) also provides methods for selecting random number generator algorithms. A specific [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) can be located by using the [RandomGeneratorFactory.of(String)](../java/util/random/RandomGeneratorFactory.md))method, where the argument string is the name of the [algorithm](../java/util/random/_package.md) required. The method [RandomGeneratorFactory.all()](../java/util/random/RandomGeneratorFactory.md))produces a non-empty [Stream](../java/util/stream/Stream.md) of all available [RandomGeneratorFactorys](../java/util/random/RandomGeneratorFactory.md) that can be searched to locate a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) suitable to the task. There are three methods for constructing a RandomGenerator instance, depending on the type of initial seed required. [RandomGeneratorFactory.create(long)](../java/util/random/RandomGeneratorFactory.md))is used for long seed construction,[RandomGeneratorFactory.create(byte[])](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create(kotlin.ByteArray))is used for byte\[\] seed construction, and [RandomGeneratorFactory.create()](../java/util/random/RandomGeneratorFactory.md))is used for random seed construction. Example; 

```kotlin
<code>RandomGeneratorFactory&lt;RandomGenerator&gt; factory = RandomGeneratorFactory.of("Random");
 
      for (int i = 0; i &lt; 10; i++) {
          new Thread(() -&gt; {
              RandomGenerator random = factory.create(100L);
              System.out.println(random.nextDouble());
          }).start();
      }
  </code>
```
RandomGeneratorFactory also provides methods describing the attributes (or properties) of a generator and can be used to select random number generator [algorithms](../java/util/random/_package.md). These methods are typically used in conjunction with [RandomGeneratorFactory.all()](../java/util/random/RandomGeneratorFactory.md)). In this example, the code locates the [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) that produces [RandomGenerators](../java/util/random/RandomGenerator.md) with the highest number of state bits. 

```kotlin
<code>RandomGeneratorFactory&lt;RandomGenerator&gt; best = RandomGeneratorFactory.all()
          .sorted(Comparator.comparingInt(RandomGenerator::stateBits).reversed())
          .findFirst()
          .orElse(RandomGeneratorFactory.of("Random"));
      System.out.println(best.name() + " in " + best.group() + " was selected");
 
      RandomGenerator rng = best.create();
      System.out.println(rng.nextLong());
  </code>
```

<br />

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Stream](../java/util/stream/Stream.md)\< [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)\< [RandomGenerator](../java/util/random/RandomGenerator.md)!\>!\>! | [all](../java/util/random/RandomGeneratorFactory.md))`()` Returns a non-empty stream of available [RandomGeneratorFactory(s)](../java/util/random/RandomGeneratorFactory.md). |
| T | [create](../java/util/random/RandomGeneratorFactory.md))`()` Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen. |
| T | [create](../java/util/random/RandomGeneratorFactory.md))`(`seed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen providing a starting byte\[\] seed. |
| --- | --- |
| T | [create](../java/util/random/RandomGeneratorFactory.md))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen providing a starting long seed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [equidistribution](../java/util/random/RandomGeneratorFactory.md))`()` Returns the equidistribution of the [algorithm](../java/util/random/_package.md). |
| static [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)\< [RandomGenerator](../java/util/random/RandomGenerator.md)!\>! | [getDefault](../java/util/random/RandomGeneratorFactory.md))`()` Returns a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) meeting the minimal requirement of having an algorithm whose state bits are greater than or equal 64. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [group](../java/util/random/RandomGeneratorFactory.md))`()` Return the group name of the [algorithm](../java/util/random/_package.md) used by the random number generator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isArbitrarilyJumpable](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator can jump an arbitrarily specified distant point in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeprecated](../java/util/random/RandomGeneratorFactory.md))`()` Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHardware](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator uses a hardware device (HRNG) to produce entropic input. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isJumpable](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator can jump a specified distant point in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapable](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator is jumpable and can leap to a very distant point in the state cycle. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSplittable](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator can be cloned into a separate object with the same properties but positioned further in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStatistical](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator is computed using an arithmetic [algorithm](../java/util/random/_package.md) and is statistically deterministic. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStochastic](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator is computed using external or entropic sources as inputs. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStreamable](../java/util/random/RandomGeneratorFactory.md))`()` Return true if random generator can be used to create [Streams](../java/util/stream/Stream.md) of random numbers. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/util/random/RandomGeneratorFactory.md))`()` Return the name of the [algorithm](../java/util/random/_package.md) used by the random number generator. |
| static [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)\<T\>! | [of](../java/util/random/RandomGeneratorFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) that can produce instances of [RandomGenerator](../java/util/random/RandomGenerator.md) that utilize the`name` [algorithm](../java/util/random/_package.md). |
| --- | --- |
| [BigInteger](../java/math/BigInteger.md)! | [period](../java/util/random/RandomGeneratorFactory.md))`()` Return the period of the [algorithm](../java/util/random/_package.md) used by the random number generator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [stateBits](../java/util/random/RandomGeneratorFactory.md))`()` Returns number of bits used by the [algorithm](../java/util/random/_package.md) to maintain state of seed. |

## Public methods

### all

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun all(): Stream<RandomGeneratorFactory<RandomGenerator!>!>!
```

Returns a non-empty stream of available [RandomGeneratorFactory(s)](../java/util/random/RandomGeneratorFactory.md). RandomGenerators that are marked as deprecated are not included in the result.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)< [RandomGenerator](../java/util/random/RandomGenerator.md)!>!>! | a non-empty stream of all available [RandomGeneratorFactory(s)](../java/util/random/RandomGeneratorFactory.md). |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(): T
```

Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen.

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](../java/util/random/RandomGenerator.md). |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(seed: ByteArray!): T
```

Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen providing a starting byte\[\] seed. If byte\[\] seed is not supported by an [algorithm](../java/util/random/_package.md) then the no argument form of create is used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array random seed value. |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](../java/util/random/RandomGenerator.md). |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if seed is null. |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(seed: Long): T
```

Create an instance of [RandomGenerator](../java/util/random/RandomGenerator.md) based on [algorithm](../java/util/random/_package.md) chosen providing a starting long seed. If long seed is not supported by an algorithm then the no argument form of create is used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):long random seed value. |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](../java/util/random/RandomGenerator.md). |

### equidistribution

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equidistribution(): Int
```

Returns the equidistribution of the [algorithm](../java/util/random/_package.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the equidistribution of the [algorithm](../java/util/random/_package.md). |

### getDefault

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(): RandomGeneratorFactory<RandomGenerator!>!
```

Returns a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) meeting the minimal requirement of having an algorithm whose state bits are greater than or equal 64.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)< [RandomGenerator](../java/util/random/RandomGenerator.md)!>! | a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) |

### group

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun group(): String!
```

Return the group name of the [algorithm](../java/util/random/_package.md) used by the random number generator.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Group name of the [algorithm](../java/util/random/_package.md). |

### isArbitrarilyJumpable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isArbitrarilyJumpable(): Boolean
```

Return true if random generator can jump an arbitrarily specified distant point in the state cycle.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is arbitrarily jumpable. |

### isDeprecated

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDeprecated(): Boolean
```

Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the implementation of RandomGenerator (algorithm) has been marked for deprecation |

### isHardware

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHardware(): Boolean
```

Return true if random generator uses a hardware device (HRNG) to produce entropic input.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is generated by hardware. |

### isJumpable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isJumpable(): Boolean
```

Return true if random generator can jump a specified distant point in the state cycle.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is jumpable. |

### isLeapable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLeapable(): Boolean
```

Return true if random generator is jumpable and can leap to a very distant point in the state cycle.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is leapable. |

### isSplittable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSplittable(): Boolean
```

Return true if random generator can be cloned into a separate object with the same properties but positioned further in the state cycle.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is splittable. |

### isStatistical

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStatistical(): Boolean
```

Return true if random generator is computed using an arithmetic [algorithm](../java/util/random/_package.md) and is statistically deterministic.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is statistical. |

### isStochastic

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStochastic(): Boolean
```

Return true if random generator is computed using external or entropic sources as inputs.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is stochastic. |

### isStreamable

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStreamable(): Boolean
```

Return true if random generator can be used to create [Streams](../java/util/stream/Stream.md) of random numbers.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is streamable. |

### name

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun name(): String!
```

Return the name of the [algorithm](../java/util/random/_package.md) used by the random number generator.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Name of the [algorithm](../java/util/random/_package.md). |

### of

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : RandomGenerator!> of(name: String!): RandomGeneratorFactory<T>!
```

Returns a [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) that can produce instances of [RandomGenerator](../java/util/random/RandomGenerator.md) that utilize the`name` [algorithm](../java/util/random/_package.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of random number generator [algorithm](../java/util/random/_package.md) |
| `<T>` | Sub-interface of [RandomGenerator](../java/util/random/RandomGenerator.md) to produce |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md)<T>! | [RandomGeneratorFactory](../java/util/random/RandomGeneratorFactory.md) of [RandomGenerator](../java/util/random/RandomGenerator.md) |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if name is null |
| `java.lang.IllegalArgumentException` | if the named algorithm is not found |

### period

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun period(): BigInteger!
```

Return the period of the [algorithm](../java/util/random/_package.md) used by the random number generator. Returns BigInteger.ZERO if period is not determinable.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java/math/BigInteger.md)! | BigInteger period. |

### stateBits

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stateBits(): Int
```

Returns number of bits used by the [algorithm](../java/util/random/_package.md) to maintain state of seed.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of bits used by the [algorithm](../java/util/random/_package.md) to maintain state of seed. |
