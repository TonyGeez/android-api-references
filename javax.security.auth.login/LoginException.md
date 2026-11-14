# LoginException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoginException

```
open class LoginException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [javax.security.auth.login.LoginException](https://developer.android.com/reference/kotlin/javax/security/auth/login/LoginException#) |

This is the basic login exception.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LoginException](https://developer.android.com/reference/kotlin/javax/security/auth/login/LoginException#LoginException())`()` Constructs a LoginException with no detail message. |
| [LoginException](https://developer.android.com/reference/kotlin/javax/security/auth/login/LoginException#LoginException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a LoginException with the specified detail message. |

## Public constructors

### LoginException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LoginException()
```

Constructs a LoginException with no detail message. A detail message is a String that describes this particular exception. 

### LoginException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LoginException(msg: String!)
```

Constructs a LoginException with the specified detail message. A detail message is a String that describes this particular exception.

<br />

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
