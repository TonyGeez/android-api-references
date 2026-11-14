# KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyNotYetValidException

Kotlin| [Java](KeyNotYetValidException.md) 
| --- | --- |

```
open class KeyNotYetValidException : InvalidKeyException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||||
| --- | --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||||
| | | ↳ | [java.security.GeneralSecurityException](../java.security/GeneralSecurityException.md) ||||
| --- | --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.KeyException](../java.security/KeyException.md) |||
| | | | | ↳ | [java.security.InvalidKeyException](../java.security/InvalidKeyException.md) ||
| | | | | | ↳ | [android.security.keystore.KeyNotYetValidException](KeyNotYetValidException.md) |
| --- | --- | --- | --- | --- | --- | --- |

Indicates that a cryptographic operation failed because the employed key's validity start date is in the future.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyNotYetValidException](KeyNotYetValidException.md))`()` Constructs a new`KeyNotYetValidException`without detail message and cause. |
| [KeyNotYetValidException](KeyNotYetValidException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`KeyNotYetValidException`with the provided detail message and no cause. |
| [KeyNotYetValidException](KeyNotYetValidException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new`KeyNotYetValidException`with the provided detail message and cause. |

## Public constructors

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException()
```

Constructs a new`KeyNotYetValidException`without detail message and cause. 

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException(message: String!)
```

Constructs a new`KeyNotYetValidException`with the provided detail message and no cause. 

### KeyNotYetValidException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyNotYetValidException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new`KeyNotYetValidException`with the provided detail message and cause.
