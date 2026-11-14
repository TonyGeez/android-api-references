# KeyStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyStoreException

```
open class KeyStoreException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyStoreException](KeyStoreException.md) |

This is the generic KeyStore exception.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyStoreException](KeyStoreException.md))`()` Constructs a KeyStoreException with no detail message. |
| [KeyStoreException](KeyStoreException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a KeyStoreException with the specified detail message. |
| [KeyStoreException](KeyStoreException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`KeyStoreException`with the specified detail message and cause. |
| [KeyStoreException](KeyStoreException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`KeyStoreException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### KeyStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreException()
```

Constructs a KeyStoreException with no detail message. (A detail message is a String that describes this particular exception.) 

### KeyStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreException(msg: String!)
```

Constructs a KeyStoreException with the specified detail message. (A detail message is a String that describes this particular exception.)

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### KeyStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreException(
    message: String!, 
    cause: Throwable!)
```

Creates a`KeyStoreException`with the specified detail message and cause.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### KeyStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyStoreException(cause: Throwable!)
```

Creates a`KeyStoreException`with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
