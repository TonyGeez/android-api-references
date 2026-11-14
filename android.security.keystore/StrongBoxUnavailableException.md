# StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StrongBoxUnavailableException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/StrongBoxUnavailableException "View this page in Java") 

```
open class StrongBoxUnavailableException : ProviderException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.security.ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException.html#) ||
| | | | | ↳ | [android.security.keystore.StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException#) |

Indicates that an operation could not be performed because the requested security hardware is not available.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException#StrongBoxUnavailableException())`()` <br /> |
| [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException#StrongBoxUnavailableException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException#StrongBoxUnavailableException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException#StrongBoxUnavailableException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StrongBoxUnavailableException()
```  

### StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StrongBoxUnavailableException(message: String!)
```  

### StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StrongBoxUnavailableException(
    message: String!, 
    cause: Throwable!)
```  

### StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StrongBoxUnavailableException(cause: Throwable!)
```
