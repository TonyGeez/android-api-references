# UnrecoverableKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnrecoverableKeyException

```
open class UnrecoverableKeyException : UnrecoverableEntryException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md) ||
| | | | | ↳ | [java.security.UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) |

This exception is thrown if a key in the keystore cannot be recovered.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md))`()` Constructs an UnrecoverableKeyException with no detail message. |
| [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an UnrecoverableKeyException with the specified detail message, which provides more information about why this exception has been thrown. |

## Public constructors

### UnrecoverableKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnrecoverableKeyException()
```

Constructs an UnrecoverableKeyException with no detail message. 

### UnrecoverableKeyException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnrecoverableKeyException(msg: String!)
```

Constructs an UnrecoverableKeyException with the specified detail message, which provides more information about why this exception has been thrown.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
