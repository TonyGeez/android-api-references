# CertPathBuilderSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathBuilderSpi

```
abstract class CertPathBuilderSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.CertPathBuilderSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi#) |

The*Service Provider Interface* (**SPI** ) for the [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder) class. All`CertPathBuilder`implementations must include a class (the SPI class) that extends this class (`CertPathBuilderSpi`) and implements all of its methods. In general, instances of this class should only be accessed through the`CertPathBuilder`class. For details, see the Java Cryptography Architecture.

**Concurrent Access**

Instances of this class need not be protected against concurrent access from multiple threads. Threads that need to access a single`CertPathBuilderSpi`instance concurrently should synchronize amongst themselves and provide the necessary locking before calling the wrapping`CertPathBuilder`object.

However, implementations of`CertPathBuilderSpi`may still encounter concurrency issues, since multiple threads each manipulating a different`CertPathBuilderSpi`instance need not synchronize.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathBuilderSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi#CertPathBuilderSpi())`()` The default constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderResult)! | [engineBuild](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi#engineBuild(java.security.cert.CertPathParameters))`(`params:` ` [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!`)` Attempts to build a certification path using the specified algorithm parameter set. |
| open [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | [engineGetRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi#engineGetRevocationChecker())`()` Returns a`CertPathChecker`that this implementation uses to check the revocation status of certificates. |

## Public constructors

### CertPathBuilderSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathBuilderSpi()
```

The default constructor.

## Public methods

### engineBuild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineBuild(params: CertPathParameters!): CertPathBuilderResult!
```

Attempts to build a certification path using the specified algorithm parameter set.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!:the algorithm parameters |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [CertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderResult)! | the result of the build algorithm |

| Exceptions ||
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.security.cert.CertPathBuilderException` | if the builder is unable to construct a certification path that satisfies the specified parameters |
| `java.security.InvalidAlgorithmParameterException` | if the specified parameters are inappropriate for this`CertPathBuilder` |

### engineGetRevocationChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGetRevocationChecker(): CertPathChecker!
```

Returns a`CertPathChecker`that this implementation uses to check the revocation status of certificates. A PKIX implementation returns objects of type`PKIXRevocationChecker`.

The primary purpose of this method is to allow callers to specify additional input parameters and options specific to revocation checking. See the class description of`CertPathBuilder`for an example.

This method was added to version 1.8 of the Java Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be abstract and by default throws an`UnsupportedOperationException`.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | a`CertPathChecker`that this implementation uses to check the revocation status of certificates |

| Exceptions ||
|-------------------------------------------|---------------------------------|
| `java.lang.UnsupportedOperationException` | if this method is not supported |
