# CertPathBuilderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathBuilderException

```
open class CertPathBuilderException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [java.security.cert.CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException#) |

An exception indicating one of a variety of problems encountered when building a certification path with a`CertPathBuilder`.

A`CertPathBuilderException`provides support for wrapping exceptions. The [getCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method returns the throwable, if any, that caused this exception to be thrown.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException#CertPathBuilderException())`()` Creates a`CertPathBuilderException`with`null`as its detail message. |
| [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException#CertPathBuilderException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CertPathBuilderException`with the given detail message. |
| [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException#CertPathBuilderException(kotlin.String,%20kotlin.Throwable))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertPathBuilderException`with the specified detail message and cause. |
| [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException#CertPathBuilderException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertPathBuilderException`that wraps the specified throwable. |

## Public constructors

### CertPathBuilderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathBuilderException()
```

Creates a`CertPathBuilderException`with`null`as its detail message. 

### CertPathBuilderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathBuilderException(msg: String!)
```

Creates a`CertPathBuilderException`with the given detail message. The detail message is a`String`that describes this particular exception in more detail.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

### CertPathBuilderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathBuilderException(
    msg: String!, 
    cause: Throwable!)
```

Creates a`CertPathBuilderException`with the specified detail message and cause.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CertPathBuilderException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertPathBuilderException(cause: Throwable!)
```

Creates a`CertPathBuilderException`that wraps the specified throwable. This allows any exception to be converted into a`CertPathBuilderException`, while retaining information about the wrapped exception, which may be useful for debugging. The detail message is set to (`cause==null ? null : cause.toString()`) (which typically contains the class and detail message of cause).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
