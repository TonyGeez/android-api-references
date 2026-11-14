Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureRandom

```
open class SecureRandom : Random
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Random](../java.util/Random.md) ||
| | ↳ | [java.security.SecureRandom](SecureRandom.md) |

This class provides a cryptographically strong random number generator (RNG).

A cryptographically strong random number minimally complies with the statistical random number generator tests specified in [*FIPS 140-2, Security Requirements for Cryptographic Modules*](http://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.140-2.pdf), section 4.9.1. Additionally, `SecureRandom` must produce non-deterministic output. Therefore any seed material passed to a `SecureRandom` object must be unpredictable, and all `SecureRandom` output sequences must be cryptographically strong, as described in [*RFC 4086: Randomness Requirements for Security*](http://tools.ietf.org/html/rfc4086).

Many `SecureRandom` implementations are in the form of a pseudo-random number generator (PRNG, also known as deterministic random bits generator or DRBG), which means they use a deterministic algorithm to produce a pseudo-random sequence from a random seed. Other implementations may produce true random numbers, and yet others may use a combination of both techniques.

A caller obtains a `SecureRandom` instance via the no-argument constructor or one of the `getInstance` methods. For example:

```kotlin
SecureRandom r1 = new SecureRandom();
  SecureRandom r2 = SecureRandom.getInstance("NativePRNG");
  SecureRandom r3 = SecureRandom.getInstance("DRBG",
          DrbgParameters.instantiation(128, RESEED_ONLY, null));
```

The third statement above returns a `SecureRandom` object of the specific algorithm supporting the specific instantiate parameters. The implementation's effective instantiated parameters must match this minimum request but is not necessarily the same. For example, even if the request does not require a certain feature, the actual instantiation can provide the feature. An implementation may lazily instantiate a `SecureRandom` until it's actually used, but the effective instantiate parameters must be determined right after it's created and getParameters should always return the same result unchanged.

Typical callers of `SecureRandom` invoke the following methods to retrieve random bytes:

```kotlin
SecureRandom random = new SecureRandom();
  byte[] bytes = new byte[20];
  random.nextBytes(bytes);
```

Callers may also invoke the generateSeed method to generate a given number of seed bytes (to seed other random number generators, for example):

```kotlin
byte[] seed = random.generateSeed(20);
```

A newly created PRNG `SecureRandom` object is not seeded (except if it is created by SecureRandom). The first call to `nextBytes` will force it to seed itself from an implementation- specific entropy source. This self-seeding will not occur if `setSeed` was previously called.

A `SecureRandom` can be reseeded at any time by calling the `reseed` or `setSeed` method. The `reseed` method reads entropy input from its entropy source to reseed itself. The `setSeed` method requires the caller to provide the seed.

Please note that `reseed` may not be supported by all `SecureRandom` implementations.

Some `SecureRandom` implementations may accept a SecureRandomParameters parameter in its nextBytes and reseed methods to further control the behavior of the methods.

Note: Depending on the implementation, the `generateSeed`, `reseed` and `nextBytes` methods may block as entropy is being gathered, for example, if the entropy source is /dev/random on various Unix-like operating systems.

## Thread safety

`SecureRandom` objects are safe for use by multiple concurrent threads.

## Summary

| Public constructors ||
|---|---|
| SecureRandom Constructs a secure random number generator (RNG) implementing the default random number algorithm. |
| SecureRandom Constructs a secure random number generator (RNG) implementing the default random number algorithm. |

| Protected constructors ||
|---|---|
| SecureRandom Creates a `SecureRandom` object. |

| Public methods ||
|---|---|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | generateSeed Returns the given number of seed bytes, computed using the seed generation algorithm that this class uses to seed itself. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getAlgorithm Returns the name of the algorithm implemented by this `SecureRandom` object. |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm. |
| --- | --- |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm. |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm. |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request. |
| --- | --- |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request. |
| open static [SecureRandom](SecureRandom.md)! | getInstance Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request. |
| open static [SecureRandom](SecureRandom.md)! | getInstanceStrong Returns a `SecureRandom` object. |
| --- | --- |
| open [SecureRandomParameters](SecureRandomParameters.md)! | getParameters Returns the effective SecureRandomParameters for this `SecureRandom` instance. |
| [Provider](Provider.md)! | getProvider Returns the provider of this `SecureRandom` object. |
| open static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | getSeed Returns the given number of seed bytes, computed using the seed generation algorithm that this class uses to seed itself. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | nextBytes Generates a user-specified number of random bytes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | nextBytes Generates a user-specified number of random bytes with additional parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reseed Reseeds this `SecureRandom` with entropy input read from its entropy source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reseed Reseeds this `SecureRandom` with entropy input read from its entropy source with additional parameters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSeed Reseeds this random object with the given seed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSeed Reseeds this random object, using the eight bytes contained in the given `long seed`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a Human-readable string representation of this `SecureRandom`. |

| Protected methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | next Generates an integer containing the user-specified number of pseudo-random bits (right justified, with leading zeros). |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/util/Random.html#` `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.html#!` doubles

<br />

Returns an effectively unlimited stream of pseudorandom `double` values, each between zero (inclusive) and one (exclusive).

A pseudorandom `double` value is generated as if it's the result of calling the method nextDouble.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.html#!` doubles

<br />

Returns an effectively unlimited stream of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive).

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.html#!` doubles

<br />

Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each between zero (inclusive) and one (exclusive).

A pseudorandom `double` value is generated as if it's the result of calling the method nextDouble.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.html#!` doubles

<br />

Returns a stream producing the given `streamSize` number of pseudorandom `double` values, each conforming to the given origin (inclusive) and bound (exclusive).

<br />

`https://developer.android.com/reference/kotlin/java/util/Random.html#!` from

<br />

Returns an instance of `Random` that delegates method calls to the `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator.html#` argument. If the generator is an instance of `Random`, it is returned. Otherwise, this method returns an instance of `Random` that delegates all methods except `setSeed` to the generator. The returned instance's `setSeed` method always throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. The returned instance is not serializable.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#!` ints

<br />

Returns an effectively unlimited stream of pseudorandom `int` values.

A pseudorandom `int` value is generated as if it's the result of calling the method nextInt.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#!` ints

<br />

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

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#!` ints

<br />

Returns a stream producing the given `streamSize` number of pseudorandom `int` values.

A pseudorandom `int` value is generated as if it's the result of calling the method nextInt.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#!` ints

<br />

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

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/LongStream.html#!` longs

<br />

Returns an effectively unlimited stream of pseudorandom `long` values.

A pseudorandom `long` value is generated as if it's the result of calling the method nextLong.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/LongStream.html#!` longs

<br />

Returns a stream producing the given `streamSize` number of pseudorandom `long` values.

A pseudorandom `long` value is generated as if it's the result of calling the method nextLong.

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/LongStream.html#!` longs

<br />

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

<br />

`https://developer.android.com/reference/kotlin/java/util/stream/LongStream.html#!` longs

<br />

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

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` nextBoolean

<br />

Returns the next pseudorandom, uniformly distributed `boolean` value from this random number generator's sequence. The general contract of `nextBoolean` is that one `boolean` value is pseudorandomly generated and returned. The values `true` and `false` are produced with (approximately) equal probability.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextDouble

<br />

Returns the next pseudorandom, uniformly distributed `double` value between `0.0` and `1.0` from this random number generator's sequence.

The general contract of `nextDouble` is that one `double` value, chosen (approximately) uniformly from the range `0.0d` (inclusive) to `1.0d` (exclusive), is pseudorandomly generated and returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` nextFloat

<br />

Returns the next pseudorandom, uniformly distributed `float` value between `0.0` and `1.0` from this random number generator's sequence.

The general contract of `nextFloat` is that one `float` value, chosen (approximately) uniformly from the range `0.0f` (inclusive) to `1.0f` (exclusive), is pseudorandomly generated and returned. All 224 possible `float` values of the form *m x* 2-24, where *m* is a positive integer less than 224, are produced with (approximately) equal probability.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextGaussian

<br />

Returns the next pseudorandom, Gaussian ("normally") distributed `double` value with mean `0.0` and standard deviation `1.0` from this random number generator's sequence.

The general contract of `nextGaussian` is that one `double` value, chosen from (approximately) the usual normal distribution with mean `0.0` and standard deviation `1.0`, is pseudorandomly generated and returned.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` nextInt

<br />

Returns the next pseudorandom, uniformly distributed `int` value from this random number generator's sequence. The general contract of `nextInt` is that one `int` value is pseudorandomly generated and returned. All 232 possible `int` values are produced with (approximately) equal probability.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` nextInt

<br />

Returns a pseudorandom, uniformly distributed `int` value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence. The general contract of `nextInt` is that one `int` value in the specified range is pseudorandomly generated and returned. All `bound` possible `int` values are produced with (approximately) equal probability.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` nextLong

<br />

Returns the next pseudorandom, uniformly distributed `long` value from this random number generator's sequence. The general contract of `nextLong` is that one `long` value is pseudorandomly generated and returned.

<br />

From class `https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator.html#` `https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.html#!` equiDoubles

<br />

Returns an effectively unlimited stream of pseudorandomly chosen `double` values, where each value is between the specified `left` boundary and the specified `right` boundary. The `left` boundary is included as indicated by `isLeftIncluded`; similarly, the `right` boundary is included as indicated by `isRightIncluded`.

The stream potentially produces all multiples *k* δ (*k* integer) lying in the interval specified by the parameters, where δ \> 0 is the smallest number for which all these multiples are exact `double`s. They are therefore all equidistant. The uniformity of the distribution of the `double`s produced by the stream depends on the quality of the underlying nextLong.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` isDeprecated

<br />

Return true if the implementation of RandomGenerator (algorithm) has been marked for deprecation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextDouble

<br />

Returns a pseudorandomly chosen `double` value between zero (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextDouble

<br />

Returns a pseudorandomly chosen `double` value between the specified origin (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextExponential

<br />

Returns a nonnegative `double` value pseudorandomly chosen from an exponential distribution whose mean is 1.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` nextFloat

<br />

Returns a pseudorandomly chosen `float` value between zero (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` nextFloat

<br />

Returns a pseudorandomly chosen `float` value between the specified origin (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` nextGaussian

<br />

Returns a `double` value pseudorandomly chosen from a Gaussian (normal) distribution with a mean and standard deviation specified by the arguments.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` nextInt

<br />

Returns a pseudorandomly chosen `int` value between the specified origin (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` nextLong

<br />

Returns a pseudorandomly chosen `long` value between zero (inclusive) and the specified bound (exclusive).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` nextLong

<br />

Returns a pseudorandomly chosen `long` value between the specified origin (inclusive) and the specified bound (exclusive).

<br />

## Public constructors

### SecureRandom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SecureRandom()
```

Constructs a secure random number generator (RNG) implementing the default random number algorithm.

This constructor traverses the list of registered security Providers, starting with the most preferred Provider. A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the first Provider that supports a `SecureRandom` (RNG) algorithm is returned. If none of the Providers support a RNG algorithm, then an implementation-specific default is returned.

Note that the list of registered providers may be retrieved via the getProviders method.

See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names.

### SecureRandom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SecureRandom(seed: ByteArray!)
```

Constructs a secure random number generator (RNG) implementing the default random number algorithm. The `SecureRandom` instance is seeded with the specified seed bytes.

This constructor traverses the list of registered security Providers, starting with the most preferred Provider. A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the first Provider that supports a `SecureRandom` (RNG) algorithm is returned. If none of the Providers support a RNG algorithm, then an implementation-specific default is returned.

Note that the list of registered providers may be retrieved via the getProviders method.

See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names.

| Parameters ||
|---|---|
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the seed. |

## Protected constructors

### SecureRandom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SecureRandom(
    secureRandomSpi: SecureRandomSpi!, 
    provider: Provider!)
```

Creates a `SecureRandom` object.

| Parameters ||
|---|---|
| `secureRandomSpi` | [SecureRandomSpi](SecureRandomSpi.md)!: the `SecureRandom` implementation. |
| `provider` | [Provider](Provider.md)!: the provider. |

## Public methods

### generateSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateSeed(numBytes: Int): ByteArray!
```

Returns the given number of seed bytes, computed using the seed generation algorithm that this class uses to seed itself. This call may be used to seed other random number generators.

| Parameters ||
|---|---|
| `numBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of seed bytes to generate. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the seed bytes. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `numBytes` is negative |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlgorithm(): String!
```

Returns the name of the algorithm implemented by this `SecureRandom` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the algorithm or `unknown` if the algorithm name cannot be determined. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(algorithm: String!): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the getProviders method.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if no `Provider` supports a `SecureRandomSpi` implementation for the specified algorithm |

**See Also**

- Provider

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm.

A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the getProviders method.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the provider. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provider name is `null` or empty |
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if a `SecureRandomSpi` implementation for the specified algorithm is not available from the specified provider |
| --- | --- |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |

**See Also**

- Provider

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm.

A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the specified `Provider` object is returned. Note that the specified `Provider` object does not have to be registered in the provider list.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |
| `provider` | [Provider](Provider.md)!: the provider. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified provider is `null` |
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if a `SecureRandomSpi` implementation for the specified algorithm is not available from the specified `Provider` object |
| --- | --- |

**See Also**

- Provider

### getInstance

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    algorithm: String!, 
    params: SecureRandomParameters!
): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the first Provider that supports the specified algorithm and the specified `SecureRandomParameters` is returned.

Note that the list of registered providers may be retrieved via the getProviders method.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |
| `params` | [SecureRandomParameters](SecureRandomParameters.md)!: the `SecureRandomParameters` the newly created `SecureRandom` object must support. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified params is `null` |
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if no Provider supports a `SecureRandomSpi` implementation for the specified algorithm and parameters |
| --- | --- |

**See Also**

- Provider

### getInstance

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    algorithm: String!, 
    params: SecureRandomParameters!, 
    provider: String!
): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request.

A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the getProviders method.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |
| `params` | [SecureRandomParameters](SecureRandomParameters.md)!: the `SecureRandomParameters` the newly created `SecureRandom` object must support. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the provider. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provider name is `null` or empty, or params is `null` |
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if the specified provider does not support a `SecureRandomSpi` implementation for the specified algorithm and parameters |
| --- | --- |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |

**See Also**

- Provider

### getInstance

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    algorithm: String!, 
    params: SecureRandomParameters!, 
    provider: Provider!
): SecureRandom!
```

Returns a `SecureRandom` object that implements the specified Random Number Generator (RNG) algorithm and supports the specified `SecureRandomParameters` request.

A new `SecureRandom` object encapsulating the `SecureRandomSpi` implementation from the specified `Provider` object is returned. Note that the specified `Provider` object does not have to be registered in the provider list.

| Parameters ||
|---|---|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the RNG algorithm. See the `SecureRandom` section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#securerandom-number-generation-algorithms) for information about standard RNG algorithm names. |
| `params` | [SecureRandomParameters](SecureRandomParameters.md)!: the `SecureRandomParameters` the newly created `SecureRandom` object must support. |
| `provider` | [Provider](Provider.md)!: the provider. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | the new `SecureRandom` object |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified provider or params is `null` |
| `java.lang.NullPointerException` | if `algorithm` is `null` |
| `java.security.NoSuchAlgorithmException` | if the specified provider does not support a `SecureRandomSpi` implementation for the specified algorithm and parameters |
| --- | --- |

**See Also**

- Provider

### getInstanceStrong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstanceStrong(): SecureRandom!
```

Returns a `SecureRandom` object. In Android this is equivalent to get a SHA1PRNG from AndroidOpenSSL. Some situations require strong random values, such as when creating high-value/long-lived secrets like RSA public/private keys. To help guide applications in selecting a suitable strong `SecureRandom` implementation, Java distributions include a list of known strong `SecureRandom` implementations in the `securerandom.strongAlgorithms` Security property.

Every implementation of the Java platform is required to support at least one strong `SecureRandom` implementation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandom#!` | a strong `SecureRandom` implementation |

| Exceptions ||
|---|---|
| `java.security.NoSuchAlgorithmException` | if no algorithm is available |

**See Also**

- getProperty

### getParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParameters(): SecureRandomParameters!
```

Returns the effective SecureRandomParameters for this `SecureRandom` instance.

The returned value can be different from the `SecureRandomParameters` object passed into a `getInstance` method, but it cannot change during the lifetime of this `SecureRandom` object.

A caller can use the returned value to find out what features this `SecureRandom` supports.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/SecureRandomParameters!` | the effective SecureRandomParameters parameters, or `null` if no parameters were used. |

**See Also**

- SecureRandomSpi

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProvider(): Provider!
```

Returns the provider of this `SecureRandom` object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Provider!` | the provider of this `SecureRandom` object. |

### getSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSeed(numBytes: Int): ByteArray!
```

Returns the given number of seed bytes, computed using the seed generation algorithm that this class uses to seed itself. This call may be used to seed other random number generators.

This method is only included for backwards compatibility. The caller is encouraged to use one of the alternative `getInstance` methods to obtain a `SecureRandom` object, and then call the `generateSeed` method to obtain seed bytes from that object.

| Parameters ||
|---|---|
| `numBytes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of seed bytes to generate. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the seed bytes. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `numBytes` is negative |

**See Also**

### nextBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextBytes(bytes: ByteArray!): Unit
```

Generates a user-specified number of random bytes.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the array to be filled in with random bytes. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the byte array is null |

### nextBytes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextBytes(
    bytes: ByteArray!, 
    params: SecureRandomParameters!
): Unit
```

Generates a user-specified number of random bytes with additional parameters.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the array to be filled in with random bytes |
| `params` | [SecureRandomParameters](SecureRandomParameters.md)!: additional parameters |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `params` is `null`, illegal or unsupported by this `SecureRandom` |
| `java.lang.NullPointerException` | if `bytes` is null |
| `java.lang.UnsupportedOperationException` | if the underlying provider implementation has not overridden this method |
| --- | --- |

### reseed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reseed(): Unit
```

Reseeds this `SecureRandom` with entropy input read from its entropy source.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the underlying provider implementation has not overridden this method. |

### reseed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reseed(params: SecureRandomParameters!): Unit
```

Reseeds this `SecureRandom` with entropy input read from its entropy source with additional parameters.

Note that entropy is obtained from an entropy source. While some data in `params` may contain entropy, its main usage is to provide diversity.

| Parameters ||
|---|---|
| `params` | [SecureRandomParameters](SecureRandomParameters.md)!: extra parameters |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `params` is `null`, illegal or unsupported by this `SecureRandom` |
| `java.lang.UnsupportedOperationException` | if the underlying provider implementation has not overridden this method. |

### setSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSeed(seed: ByteArray!): Unit
```

Reseeds this random object with the given seed. The seed supplements, rather than replaces, the existing seed. Thus, repeated calls are guaranteed never to reduce randomness.

A PRNG `SecureRandom` will not seed itself automatically if `setSeed` is called before any `nextBytes` or `reseed` calls. The caller should make sure that the `seed` argument contains enough entropy for the security of this `SecureRandom`.

| Parameters ||
|---|---|
| `seed` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the seed. |

**See Also**

- getSeed

### setSeed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSeed(seed: Long): Unit
```

Reseeds this random object, using the eight bytes contained in the given `long seed`. The given seed supplements, rather than replaces, the existing seed. Thus, repeated calls are guaranteed never to reduce randomness.

This method is defined for compatibility with `java.util.Random`.

| Parameters ||
|---|---|
| `seed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seed. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `setSeed` operation is not supported by this random number generator |

**See Also**

- getSeed

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a Human-readable string representation of this `SecureRandom`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string representation |

## Protected methods

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun next(numBits: Int): Int
```

Generates an integer containing the user-specified number of pseudo-random bits (right justified, with leading zeros). This method overrides a `java.util.Random` method, and serves to provide a source of random bits to all of the methods inherited from that class (for example, `nextInt`, `nextLong`, and `nextFloat`).

| Parameters ||
|---|---|
| `bits` | random bits |
| `numBits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of pseudo-random bits to be generated, where `0 <= numBits <= 32`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an `int` containing the user-specified number of pseudo-random bits (right justified, with leading zeros). |
