# NoSuchAlgorithmException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchAlgorithmException

```
open class NoSuchAlgorithmException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException#) |

This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException#NoSuchAlgorithmException())`()` Constructs a NoSuchAlgorithmException with no detail message. |
| [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException#NoSuchAlgorithmException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a NoSuchAlgorithmException with the specified detail message. |
| [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException#NoSuchAlgorithmException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`NoSuchAlgorithmException`with the specified detail message and cause. |
| [NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException#NoSuchAlgorithmException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`NoSuchAlgorithmException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### NoSuchAlgorithmException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchAlgorithmException()
```

Constructs a NoSuchAlgorithmException with no detail message. A detail message is a String that describes this particular exception. 

### NoSuchAlgorithmException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchAlgorithmException(msg: String!)
```

Constructs a NoSuchAlgorithmException with the specified detail message. A detail message is a String that describes this particular exception, which may, for example, specify which algorithm is not available.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### NoSuchAlgorithmException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchAlgorithmException(
    message: String!, 
    cause: Throwable!)
```

Creates a`NoSuchAlgorithmException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### NoSuchAlgorithmException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchAlgorithmException(cause: Throwable!)
```

Creates a`NoSuchAlgorithmException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
