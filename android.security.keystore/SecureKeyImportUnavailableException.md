# SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureKeyImportUnavailableException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/SecureKeyImportUnavailableException "View this page in Java") 
| --- | --- |

```
open class SecureKeyImportUnavailableException : ProviderException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException.html#) ||
| | | | | ↳ | [android.security.keystore.SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException#) |

Indicates that the Keystore does not support securely importing wrapped keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException#SecureKeyImportUnavailableException())`()` <br /> |
| [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException#SecureKeyImportUnavailableException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException#SecureKeyImportUnavailableException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException#SecureKeyImportUnavailableException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureKeyImportUnavailableException()
```  

### SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureKeyImportUnavailableException(message: String!)
```  

### SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureKeyImportUnavailableException(
    message: String!, 
    cause: Throwable!)
```  

### SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SecureKeyImportUnavailableException(cause: Throwable!)
```
