Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathValidatorSpi

```
abstract class CertPathValidatorSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertPathValidatorSpi](CertPathValidatorSpi.md) |

The *Service Provider Interface* (**SPI** ) for the `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator` class. All `CertPathValidator` implementations must include a class (the SPI class) that extends this class (`CertPathValidatorSpi`) and implements all of its methods. In general, instances of this class should only be accessed through the `CertPathValidator` class. For details, see the Java Cryptography Architecture.

**Concurrent Access**

Instances of this class need not be protected against concurrent access from multiple threads. Threads that need to access a single `CertPathValidatorSpi` instance concurrently should synchronize amongst themselves and provide the necessary locking before calling the wrapping `CertPathValidator` object.

However, implementations of `CertPathValidatorSpi` may still encounter concurrency issues, since multiple threads each manipulating a different `CertPathValidatorSpi` instance need not synchronize.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi#CertPathValidatorSpi()()` The default constructor. |

| Public methods ||
|---|---|
| open [CertPathChecker](CertPathChecker.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi#engineGetRevocationChecker()()` Returns a `CertPathChecker` that this implementation uses to check the revocation status of certificates. |
| abstract [CertPathValidatorResult](CertPathValidatorResult.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi#engineValidate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters)(certPath: https://developer.android.com/reference/kotlin/java/security/cert/CertPath!, params: https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters!)` Validates the specified certification path using the specified algorithm parameter set. |

## Public constructors

### CertPathValidatorSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorSpi()
```

The default constructor.

## Public methods

### engineGetRevocationChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun engineGetRevocationChecker(): CertPathChecker!
```

Returns a `CertPathChecker` that this implementation uses to check the revocation status of certificates. A PKIX implementation returns objects of type `PKIXRevocationChecker`.

The primary purpose of this method is to allow callers to specify additional input parameters and options specific to revocation checking. See the class description of `CertPathValidator` for an example.

This method was added to version 1.8 of the Java Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be abstract and by default throws an `UnsupportedOperationException`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker!` | a `CertPathChecker` that this implementation uses to check the revocation status of certificates |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this method is not supported |

### engineValidate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun engineValidate(
    certPath: CertPath!, 
    params: CertPathParameters!
): CertPathValidatorResult!
```

Validates the specified certification path using the specified algorithm parameter set.

The `CertPath` specified must be of a type that is supported by the validation algorithm, otherwise an `InvalidAlgorithmParameterException` will be thrown. For example, a `CertPathValidator` that implements the PKIX algorithm validates `CertPath` objects of type X.509.

| Parameters ||
|---|---|
| `certPath` | [CertPath](CertPath.md)!: the `CertPath` to be validated |
| `params` | [CertPathParameters](CertPathParameters.md)!: the algorithm parameters |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult!` | the result of the validation algorithm |

| Exceptions ||
|---|---|
| `java.security.InvalidAlgorithmParameterException` | if the specified parameters or the type of the specified `CertPath` are inappropriate for this `CertPathValidator` |
| `java.security.cert.CertPathValidatorException` | if the `CertPath` does not validate |
