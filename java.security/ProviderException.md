# ProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderException

```
open class ProviderException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.security.ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException#) |

| Known Direct Subclasses [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException.html#), [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException.html#), [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException.html#) |-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException.html#) | Indicates a transient error that prevented a key operation from being created. | | [SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException.html#) | Indicates that the Keystore does not support securely importing wrapped keys. | | [StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException.html#) | Indicates that an operation could not be performed because the requested security hardware is not available. | |

A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException#ProviderException())`()` Constructs a ProviderException with no detail message. |
| [ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException#ProviderException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a ProviderException with the specified detail message. |
| [ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException#ProviderException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`ProviderException`with the specified detail message and cause. |
| [ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException#ProviderException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`ProviderException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### ProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderException()
```

Constructs a ProviderException with no detail message. A detail message is a String that describes this particular exception. 

### ProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderException(s: String!)
```

Constructs a ProviderException with the specified detail message. A detail message is a String that describes this particular exception.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### ProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderException(
    message: String!, 
    cause: Throwable!)
```

Creates a`ProviderException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### ProviderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderException(cause: Throwable!)
```

Creates a`ProviderException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
