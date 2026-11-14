# CertPathTrustManagerParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathTrustManagerParameters

```
open class CertPathTrustManagerParameters : ManagerFactoryParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.net.ssl.CertPathTrustManagerParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters#) |

A wrapper for CertPathParameters. This class is used to pass validation settings to CertPath based [TrustManager](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManager) s using the [TrustManagerFactory.init()](https://developer.android.com/reference/kotlin/javax/net/ssl/TrustManagerFactory#init(javax.net.ssl.ManagerFactoryParameters))method.

Instances of this class are immutable.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathTrustManagerParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters#CertPathTrustManagerParameters(java.security.cert.CertPathParameters))`(`parameters:` ` [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters.html#)!`)` Construct new CertPathTrustManagerParameters from the specified parameters. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters.html#)! | [getParameters](https://developer.android.com/reference/kotlin/javax/net/ssl/CertPathTrustManagerParameters#getParameters())`()` Return a clone of the CertPathParameters encapsulated by this class. |

## Public constructors

### CertPathTrustManagerParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathTrustManagerParameters(parameters: CertPathParameters!)
```

Construct new CertPathTrustManagerParameters from the specified parameters. The parameters are cloned to protect against subsequent modification.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters.html#)!:the CertPathParameters to be used |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if parameters is null |

## Public methods

### getParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameters(): CertPathParameters!
```

Return a clone of the CertPathParameters encapsulated by this class.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters.html#)! | a clone of the CertPathParameters encapsulated by this class. |
