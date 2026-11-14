# CertPathValidatorResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathValidatorResult

```
interface CertPathValidatorResult : Cloneable
```

| [java.security.cert.CertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult#) |

| Known Direct Subclasses [PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------| | [PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult) | This class represents the successful result of the PKIX certification path validation algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult) | This class represents the successful result of the PKIX certification path builder algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

A specification of the result of a certification path validator algorithm.

The purpose of this interface is to group (and provide type safety for) all certification path validator results. All results returned by the [CertPathValidator.validate](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters))method must implement this interface.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult#clone())`()` Makes a copy of this`CertPathValidatorResult`. |

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
