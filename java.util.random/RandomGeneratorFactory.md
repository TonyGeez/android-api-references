# RandomGeneratorFactory

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RandomGeneratorFactory

```
class RandomGeneratorFactory<T : RandomGenerator!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.random.RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) |

This is a factory class for generating multiple random number generators of a specific [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) also provides methods for selecting random number generator algorithms. A specific [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) can be located by using the [RandomGeneratorFactory.of(String)](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#of(kotlin.String))method, where the argument string is the name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) required. The method [RandomGeneratorFactory.all()](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#all())produces a non-empty [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) of all available [RandomGeneratorFactorys](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) that can be searched to locate a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) suitable to the task. There are three methods for constructing a RandomGenerator instance, depending on the type of initial seed required. [RandomGeneratorFactory.create(long)](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create(kotlin.Long))is used for long seed construction,[RandomGeneratorFactory.create(byte[])](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create(kotlin.ByteArray))is used for byte\[\] seed construction, and [RandomGeneratorFactory.create()](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create())is used for random seed construction. Example; 

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
RandomGeneratorFactory also provides methods describing the attributes (or properties) of a generator and can be used to select random number generator [algorithms](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). These methods are typically used in conjunction with [RandomGeneratorFactory.all()](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#all()). In this example, the code locates the [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) that produces [RandomGenerators](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) with the highest number of state bits. 

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
| static [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)\< [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)\< [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator)!\>!\>! | [all](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#all())`()` Returns a non-empty stream of available [RandomGeneratorFactory(s)](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#). |
| T | [create](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create())`()` Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen. |
| T | [create](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create(kotlin.ByteArray))`(`seed:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen providing a starting byte\[\] seed. |
| T | [create](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#create(kotlin.Long))`(`seed:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen providing a starting long seed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [equidistribution](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#equidistribution())`()` Returns the equidistribution of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). |
| static [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)\< [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator)!\>! | [getDefault](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#getDefault())`()` Returns a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) meeting the minimal requirement of having an algorithm whose state bits are greater than or equal 64. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [group](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#group())`()` Return the group name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isArbitrarilyJumpable](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isArbitrarilyJumpable())`()` Return true if random generator can jump an arbitrarily specified distant point in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDeprecated](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isDeprecated())`()` Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHardware](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isHardware())`()` Return true if random generator uses a hardware device (HRNG) to produce entropic input. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isJumpable](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isJumpable())`()` Return true if random generator can jump a specified distant point in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapable](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isLeapable())`()` Return true if random generator is jumpable and can leap to a very distant point in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSplittable](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isSplittable())`()` Return true if random generator can be cloned into a separate object with the same properties but positioned further in the state cycle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStatistical](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isStatistical())`()` Return true if random generator is computed using an arithmetic [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) and is statistically deterministic. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStochastic](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isStochastic())`()` Return true if random generator is computed using external or entropic sources as inputs. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStreamable](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#isStreamable())`()` Return true if random generator can be used to create [Streams](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) of random numbers. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#name())`()` Return the name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator. |
| static [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)\<T\>! | [of](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#of(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) that can produce instances of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) that utilize the`name` [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). |
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [period](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#period())`()` Return the period of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [stateBits](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#stateBits())`()` Returns number of bits used by the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) to maintain state of seed. |

## Public methods

### all

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun all(): Stream<RandomGeneratorFactory<RandomGenerator!>!>!
```

Returns a non-empty stream of available [RandomGeneratorFactory(s)](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#). RandomGenerators that are marked as deprecated are not included in the result.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)< [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)< [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator)!>!>! | a non-empty stream of all available [RandomGeneratorFactory(s)](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#). |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(): T
```

Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen.

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator). |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(seed: ByteArray!): T
```

Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen providing a starting byte\[\] seed. If byte\[\] seed is not supported by an [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) then the no argument form of create is used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:byte array random seed value. |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator). |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if seed is null. |

### create

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun create(seed: Long): T
```

Create an instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) based on [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) chosen providing a starting long seed. If long seed is not supported by an algorithm then the no argument form of create is used.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):long random seed value. |

| Return ||
|---|-----------------------------------------------------------------------------------------------------------------------|
| T | new in instance of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator). |

### equidistribution

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equidistribution(): Int
```

Returns the equidistribution of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the equidistribution of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). |

### getDefault

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(): RandomGeneratorFactory<RandomGenerator!>!
```

Returns a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) meeting the minimal requirement of having an algorithm whose state bits are greater than or equal 64.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)< [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator)!>! | a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) |

### group

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun group(): String!
```

Return the group name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Group name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). |

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

Return true if random generator is computed using an arithmetic [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) and is statistically deterministic.

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

Return true if random generator can be used to create [Streams](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) of random numbers.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if random generator is streamable. |

### name

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun name(): String!
```

Return the name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Name of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms). |

### of

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : RandomGenerator!> of(name: String!): RandomGeneratorFactory<T>!
```

Returns a [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) that can produce instances of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) that utilize the`name` [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of random number generator [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) |
| `<T>` | Sub-interface of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) to produce |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#)<T>! | [RandomGeneratorFactory](https://developer.android.com/reference/kotlin/java/util/random/RandomGeneratorFactory#) of [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator) |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if name is null |
| `java.lang.IllegalArgumentException` | if the named algorithm is not found |

### period

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun period(): BigInteger!
```

Return the period of the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) used by the random number generator. Returns BigInteger.ZERO if period is not determinable.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | BigInteger period. |

### stateBits

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stateBits(): Int
```

Returns number of bits used by the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) to maintain state of seed.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of bits used by the [algorithm](https://developer.android.com/reference/kotlin/java/util/random/package-summary#algorithms) to maintain state of seed. |
