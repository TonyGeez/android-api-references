# StrongBoxUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StrongBoxUnavailableException

Kotlin| [Java](StrongBoxUnavailableException.md) 
| --- | --- |

```
open class StrongBoxUnavailableException : ProviderException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.ProviderException](../java.security/ProviderException.md) ||
| | | | | ↳ | [android.security.keystore.StrongBoxUnavailableException](StrongBoxUnavailableException.md) |

Indicates that an operation could not be performed because the requested security hardware is not available.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StrongBoxUnavailableException](StrongBoxUnavailableException.md))`()` <br /> |
| [StrongBoxUnavailableException](StrongBoxUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [StrongBoxUnavailableException](StrongBoxUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [StrongBoxUnavailableException](StrongBoxUnavailableException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
