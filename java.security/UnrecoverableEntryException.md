# UnrecoverableEntryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnrecoverableEntryException

```
open class UnrecoverableEntryException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.security.GeneralSecurityException](../java/security/GeneralSecurityException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.security.UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md) |

| Known Direct Subclasses [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) |---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) | This exception is thrown if a key in the keystore cannot be recovered. | |
| --- | --- | --- | --- | --- | --- | --- |

This exception is thrown if an entry in the keystore cannot be recovered.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md))`()` Constructs an UnrecoverableEntryException with no detail message. |
| [UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an UnrecoverableEntryException with the specified detail message, which provides more information about why this exception has been thrown. |

## Public constructors

### UnrecoverableEntryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnrecoverableEntryException()
```

Constructs an UnrecoverableEntryException with no detail message. 

### UnrecoverableEntryException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnrecoverableEntryException(msg: String!)
```

Constructs an UnrecoverableEntryException with the specified detail message, which provides more information about why this exception has been thrown.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
