# CertPathParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathParameters

```
interface CertPathParameters : Cloneable
```

| [java.security.cert.CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters#) |

| Known Direct Subclasses [PKIXParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------| | [PKIXParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters) | Parameters used as input for the PKIX`CertPathValidator`algorithm. | |

| Known Indirect Subclasses [PKIXBuilderParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXBuilderParameters) |------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------| | [PKIXBuilderParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXBuilderParameters) | Parameters used as input for the PKIX`CertPathBuilder`algorithm. | |

A specification of certification path algorithm parameters. The purpose of this interface is to group (and provide type safety for) all`CertPath`parameter specifications. All`CertPath`parameter specifications must implement this interface.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters#clone())`()` Makes a copy of this`CertPathParameters`. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

Makes a copy of this`CertPathParameters`. Changes to the copy will not affect the original and vice versa.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`CertPathParameters` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
