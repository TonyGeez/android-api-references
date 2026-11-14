# SecureKeyImportUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureKeyImportUnavailableException

Kotlin| [Java](SecureKeyImportUnavailableException.md) 
| --- | --- |

```
open class SecureKeyImportUnavailableException : ProviderException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.ProviderException](../java.security/ProviderException.md) ||
| | | | | ↳ | [android.security.keystore.SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md) |

Indicates that the Keystore does not support securely importing wrapped keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md))`()` <br /> |
| [SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [SecureKeyImportUnavailableException](SecureKeyImportUnavailableException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
