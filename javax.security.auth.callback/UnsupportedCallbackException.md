# UnsupportedCallbackException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedCallbackException

```
open class UnsupportedCallbackException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [javax.security.auth.callback.UnsupportedCallbackException](https://developer.android.com/reference/kotlin/javax/security/auth/callback/UnsupportedCallbackException#) |
| --- | --- | --- | --- |

Signals that a`CallbackHandler`does not recognize a particular`Callback`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedCallbackException](https://developer.android.com/reference/kotlin/javax/security/auth/callback/UnsupportedCallbackException#UnsupportedCallbackException(javax.security.auth.callback.Callback))`(`callback:` ` [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)!`)` Constructs a`UnsupportedCallbackException`with no detail message. |
| [UnsupportedCallbackException](https://developer.android.com/reference/kotlin/javax/security/auth/callback/UnsupportedCallbackException#UnsupportedCallbackException(javax.security.auth.callback.Callback,%20kotlin.String))`(`callback:` ` [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)!`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a UnsupportedCallbackException with the specified detail message. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)! | [getCallback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/UnsupportedCallbackException#getCallback())`()` Get the unrecognized`Callback`. |

## Public constructors

### UnsupportedCallbackException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedCallbackException(callback: Callback!)
```

Constructs a`UnsupportedCallbackException`with no detail message.

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)!:the unrecognized`Callback`. |

### UnsupportedCallbackException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedCallbackException(
    callback: Callback!, 
    msg: String!)
```

Constructs a UnsupportedCallbackException with the specified detail message. A detail message is a String that describes this particular exception.

<br />

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)!:the unrecognized`Callback`. <br /> |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

## Public methods

### getCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCallback(): Callback!
```

Get the unrecognized`Callback`.

<br />

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [Callback](https://developer.android.com/reference/kotlin/javax/security/auth/callback/Callback)! | the unrecognized`Callback`. |
