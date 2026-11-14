# KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyExpiredException

Kotlin| [Java](KeyExpiredException.md) 
| --- | --- |

```
open class KeyExpiredException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java.security/KeyException.md) |||
| | | | | ↳ | [java.security.InvalidKeyException](../java.security/InvalidKeyException.md) ||
| | | | | | ↳ | [android.security.keystore.KeyExpiredException](KeyExpiredException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that a cryptographic operation failed because the employed key's validity end date is in the past.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyExpiredException](KeyExpiredException.md))`()` Constructs a new`KeyExpiredException`without detail message and cause. |
| [KeyExpiredException](KeyExpiredException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`KeyExpiredException`with the provided detail message and no cause. |
| [KeyExpiredException](KeyExpiredException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`KeyExpiredException`with the provided detail message and cause. |

## Public constructors

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException()
```

Constructs a new`KeyExpiredException`without detail message and cause. 

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException(message: String!)
```

Constructs a new`KeyExpiredException`with the provided detail message and no cause. 

### KeyExpiredException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyExpiredException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`KeyExpiredException`with the provided detail message and cause.
