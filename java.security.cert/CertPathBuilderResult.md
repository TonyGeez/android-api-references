# CertPathBuilderResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathBuilderResult

```
interface CertPathBuilderResult : Cloneable
```

| [java.security.cert.CertPathBuilderResult](../java/security/cert/CertPathBuilderResult.md) |

| Known Direct Subclasses [PKIXCertPathBuilderResult](../java/security/cert/PKIXCertPathBuilderResult.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [PKIXCertPathBuilderResult](../java/security/cert/PKIXCertPathBuilderResult.md) | This class represents the successful result of the PKIX certification path builder algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

A specification of the result of a certification path builder algorithm. All results returned by the [CertPathBuilder.build](../java/security/cert/CertPathBuilder.md))method must implement this interface.

At a minimum, a`CertPathBuilderResult`contains the`CertPath`built by the`CertPathBuilder`instance. Implementations of this interface may add methods to return implementation or algorithm specific information, such as debugging information or certification path validation results.

**Concurrent Access**

Unless otherwise specified, the methods defined in this interface are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/security/cert/CertPathBuilderResult.md))`()` Makes a copy of this`CertPathBuilderResult`. |
| abstract [CertPath](../java/security/cert/CertPath.md)! | [getCertPath](../java/security/cert/CertPathBuilderResult.md))`()` Returns the built certification path. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Makes a copy of this`CertPathBuilderResult`. Changes to the copy will not affect the original and vice versa.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`CertPathBuilderResult` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCertPath(): CertPath!
```

Returns the built certification path.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [CertPath](../java/security/cert/CertPath.md)! | the certification path (never`null`) |
