# AccessControlException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessControlException

```
open class AccessControlException : SecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.SecurityException](../java.lang/SecurityException.md) ||
| | | | | ↳ | [java.security.AccessControlException](AccessControlException.md) |

This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied.

The reason to deny access can vary. For example, the requested permission might be of an incorrect type, contain an invalid value, or request access that is not allowed according to the security policy. Such information should be given whenever possible at the time the exception is thrown.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessControlException](AccessControlException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`AccessControlException`with the specified, detailed message. |
| [AccessControlException](AccessControlException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `p:` ` [Permission](Permission.md)!`)` Constructs an`AccessControlException`with the specified, detailed message, and the requested permission that caused the exception. |

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Permission](Permission.md)! | [getPermission](AccessControlException.md))`()` Gets the Permission object associated with this exception, or null if there was no corresponding Permission object. |

## Public constructors

### AccessControlException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessControlException(s: String!)
```

Constructs an`AccessControlException`with the specified, detailed message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### AccessControlException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessControlException(
    s: String!, 
    p: Permission!)
```

Constructs an`AccessControlException`with the specified, detailed message, and the requested permission that caused the exception.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
| `p` | [Permission](Permission.md)!:the permission that caused the exception. |

## Public methods

### getPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermission(): Permission!
```

Gets the Permission object associated with this exception, or null if there was no corresponding Permission object.

| Return ||
|----------------------------------------------------------------------------------------|------------------------|
| [Permission](Permission.md)! | the Permission object. |
