# ChaCha20ParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChaCha20ParameterSpec

```
class ChaCha20ParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.ChaCha20ParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/ChaCha20ParameterSpec#) |

This class specifies the parameters used with the [*ChaCha20*](https://tools.ietf.org/html/rfc7539) algorithm.

The parameters consist of a 12-byte nonce and an initial counter value expressed as a 32-bit integer.

This class can be used to initialize a`Cipher`object that implements the*ChaCha20*algorithm.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ChaCha20ParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/ChaCha20ParameterSpec#ChaCha20ParameterSpec(kotlin.ByteArray,%20kotlin.Int))`(`nonce:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `counter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for ChaCha20 from the given nonce and counter. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCounter](https://developer.android.com/reference/kotlin/javax/crypto/spec/ChaCha20ParameterSpec#getCounter())`()` Returns the configured counter value. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getNonce](https://developer.android.com/reference/kotlin/javax/crypto/spec/ChaCha20ParameterSpec#getNonce())`()` Returns the nonce value. |

## Public constructors

### ChaCha20ParameterSpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ChaCha20ParameterSpec(
    nonce: ByteArray!, 
    counter: Int)
```

Constructs a parameter set for ChaCha20 from the given nonce and counter.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `nonce` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a 12-byte nonce value |
| `counter` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial counter value |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if`nonce`is`null` |
| `java.lang.IllegalArgumentException` | if`nonce`is not 12 bytes in length |

## Public methods

### getCounter

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCounter(): Int
```

Returns the configured counter value.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the counter value |

### getNonce

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNonce(): ByteArray!
```

Returns the nonce value.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the nonce value. This method returns a new array each time this method is called. |
