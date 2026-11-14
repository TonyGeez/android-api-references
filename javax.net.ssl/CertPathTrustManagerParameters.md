# CertPathTrustManagerParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathTrustManagerParameters

```
open class CertPathTrustManagerParameters : ManagerFactoryParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.CertPathTrustManagerParameters](../javax/net/ssl/CertPathTrustManagerParameters.md) |

A wrapper for CertPathParameters. This class is used to pass validation settings to CertPath based [TrustManager](../javax/net/ssl/TrustManager.md) s using the [TrustManagerFactory.init()](../javax/net/ssl/TrustManagerFactory.md))method.

Instances of this class are immutable.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathTrustManagerParameters](../javax/net/ssl/CertPathTrustManagerParameters.md))`(`parameters:` ` [CertPathParameters](../java/security/cert/CertPathParameters.md)!`)` Construct new CertPathTrustManagerParameters from the specified parameters. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CertPathParameters](../java/security/cert/CertPathParameters.md)! | [getParameters](../javax/net/ssl/CertPathTrustManagerParameters.md))`()` Return a clone of the CertPathParameters encapsulated by this class. |

## Public constructors

### CertPathTrustManagerParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathTrustManagerParameters(parameters: CertPathParameters!)
```

Construct new CertPathTrustManagerParameters from the specified parameters. The parameters are cloned to protect against subsequent modification.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [CertPathParameters](../java/security/cert/CertPathParameters.md)!:the CertPathParameters to be used |

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
| [CertPathParameters](../java/security/cert/CertPathParameters.md)! | a clone of the CertPathParameters encapsulated by this class. |
