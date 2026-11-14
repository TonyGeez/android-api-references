# CertStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertStoreException

```
open class CertStoreException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [java.security.cert.CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException#) |

An exception indicating one of a variety of problems retrieving certificates and CRLs from a`CertStore`.

A`CertStoreException`provides support for wrapping exceptions. The [getCause](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method returns the throwable, if any, that caused this exception to be thrown.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException#CertStoreException())`()` Creates a`CertStoreException`with`null`as its detail message. |
| [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException#CertStoreException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CertStoreException`with the given detail message. |
| [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException#CertStoreException(kotlin.String,%20kotlin.Throwable))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertStoreException`with the specified detail message and cause. |
| [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException#CertStoreException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`CertStoreException`that wraps the specified throwable. |

## Public constructors

### CertStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertStoreException()
```

Creates a`CertStoreException`with`null`as its detail message. 

### CertStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertStoreException(msg: String!)
```

Creates a`CertStoreException`with the given detail message. A detail message is a`String`that describes this particular exception.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |

### CertStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertStoreException(
    msg: String!, 
    cause: Throwable!)
```

Creates a`CertStoreException`with the specified detail message and cause.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CertStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertStoreException(cause: Throwable!)
```

Creates a`CertStoreException`that wraps the specified throwable. This allows any exception to be converted into a`CertStoreException`, while retaining information about the cause, which may be useful for debugging. The detail message is set to (`cause==null ? null : cause.toString()`) (which typically contains the class and detail message of cause).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
