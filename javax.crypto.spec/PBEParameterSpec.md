# PBEParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PBEParameterSpec

```
open class PBEParameterSpec : AlgorithmParameterSpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.spec.PBEParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#) |

This class specifies the set of parameters used with password-based encryption (PBE), as defined in the [PKCS #5](http://www.ietf.org/rfc/rfc2898.txt) standard.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PBEParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#PBEParameterSpec(kotlin.ByteArray,%20kotlin.Int))`(`salt:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `iterationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a parameter set for password-based encryption as defined in the PKCS #5 standard. |
| [PBEParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#PBEParameterSpec(kotlin.ByteArray,%20kotlin.Int,%20java.security.spec.AlgorithmParameterSpec))`(`salt:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `iterationCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paramSpec:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`)` Constructs a parameter set for password-based encryption as defined in the PKCS #5 standard. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIterationCount](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#getIterationCount())`()` Returns the iteration count. |
| open [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | [getParameterSpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#getParameterSpec())`()` Returns the cipher algorithm parameter specification. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSalt](https://developer.android.com/reference/kotlin/javax/crypto/spec/PBEParameterSpec#getSalt())`()` Returns the salt. |
| --- | --- |

## Public constructors

### PBEParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PBEParameterSpec(
    salt: ByteArray!, 
    iterationCount: Int)
```

Constructs a parameter set for password-based encryption as defined in the PKCS #5 standard.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `salt` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the salt. The contents of`salt`are copied to protect against subsequent modification. |
| `iterationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the iteration count. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`salt`is null. |

### PBEParameterSpec

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PBEParameterSpec(
    salt: ByteArray!, 
    iterationCount: Int, 
    paramSpec: AlgorithmParameterSpec!)
```

Constructs a parameter set for password-based encryption as defined in the PKCS #5 standard.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `salt` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the salt. The contents of`salt`are copied to protect against subsequent modification. |
| `iterationCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the iteration count. |
| `paramSpec` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the cipher algorithm parameter specification, which may be null. |
| --- | --- |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`salt`is null. |

## Public methods

### getIterationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIterationCount(): Int
```

Returns the iteration count.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the iteration count |

### getParameterSpec

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameterSpec(): AlgorithmParameterSpec!
```

Returns the cipher algorithm parameter specification.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)! | the parameter specification, or null if none was set. |

### getSalt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSalt(): ByteArray!
```

Returns the salt.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the salt. Returns a new array each time this method is called. |
