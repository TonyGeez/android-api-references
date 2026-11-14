# UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPresenceUnavailableException

Kotlin| [Java](UserPresenceUnavailableException.md) 
| --- | --- |

```
open class UserPresenceUnavailableException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java.security/KeyException.md) |||
| | | | | ↳ | [java.security.InvalidKeyException](../java.security/InvalidKeyException.md) ||
| | | | | | ↳ | [android.security.keystore.UserPresenceUnavailableException](UserPresenceUnavailableException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates the condition that a proof of user-presence was requested but this proof was not presented.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserPresenceUnavailableException](UserPresenceUnavailableException.md))`()` Constructs a`UserPresenceUnavailableException`without a detail message or cause. |
| [UserPresenceUnavailableException](UserPresenceUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`UserPresenceUnavailableException`using the provided detail message but no cause. |
| [UserPresenceUnavailableException](UserPresenceUnavailableException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`UserPresenceUnavailableException`using the provided detail message and cause. |

## Public constructors

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException()
```

Constructs a`UserPresenceUnavailableException`without a detail message or cause. 

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException(message: String!)
```

Constructs a`UserPresenceUnavailableException`using the provided detail message but no cause. 

### UserPresenceUnavailableException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPresenceUnavailableException(
    message: String!, 
    cause: Throwable!)
```

Constructs a`UserPresenceUnavailableException`using the provided detail message and cause.
