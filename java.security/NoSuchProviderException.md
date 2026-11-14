# NoSuchProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchProviderException

```
open class NoSuchProviderException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException) ||
| | | | ↳ | [java.security.NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException#) |

This exception is thrown when a particular security provider is requested but is not available in the environment.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException#NoSuchProviderException())`()` Constructs a NoSuchProviderException with no detail message. |
| [NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException#NoSuchProviderException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a NoSuchProviderException with the specified detail message. |

## Public constructors

### NoSuchProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchProviderException()
```

Constructs a NoSuchProviderException with no detail message. A detail message is a String that describes this particular exception. 

### NoSuchProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchProviderException(msg: String!)
```

Constructs a NoSuchProviderException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
