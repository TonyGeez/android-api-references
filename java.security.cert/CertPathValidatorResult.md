# CertPathValidatorResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathValidatorResult

```
interface CertPathValidatorResult : Cloneable
```

| [java.security.cert.CertPathValidatorResult](CertPathValidatorResult.md) |

| Known Direct Subclasses [PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) | This class represents the successful result of the PKIX certification path validation algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) | This class represents the successful result of the PKIX certification path builder algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

A specification of the result of a certification path validator algorithm.

The purpose of this interface is to group (and provide type safety for) all certification path validator results. All results returned by the [CertPathValidator.validate](CertPathValidator.md))method must implement this interface.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](CertPathValidatorResult.md))`()` Makes a copy of this`CertPathValidatorResult`. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Makes a copy of this`CertPathValidatorResult`. Changes to the copy will not affect the original and vice versa.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`CertPathValidatorResult` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
