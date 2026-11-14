# UnsupportedCallbackException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedCallbackException

```
open class UnsupportedCallbackException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [javax.security.auth.callback.UnsupportedCallbackException](../javax/security/auth/callback/UnsupportedCallbackException.md) |
| --- | --- | --- | --- |

Signals that a`CallbackHandler`does not recognize a particular`Callback`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedCallbackException](../javax/security/auth/callback/UnsupportedCallbackException.md))`(`callback:` ` [Callback](../javax/security/auth/callback/Callback.md)!`)` Constructs a`UnsupportedCallbackException`with no detail message. |
| [UnsupportedCallbackException](../javax/security/auth/callback/UnsupportedCallbackException.md))`(`callback:` ` [Callback](../javax/security/auth/callback/Callback.md)!`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a UnsupportedCallbackException with the specified detail message. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Callback](../javax/security/auth/callback/Callback.md)! | [getCallback](../javax/security/auth/callback/UnsupportedCallbackException.md))`()` Get the unrecognized`Callback`. |

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
| `callback` | [Callback](../javax/security/auth/callback/Callback.md)!:the unrecognized`Callback`. |

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
| `callback` | [Callback](../javax/security/auth/callback/Callback.md)!:the unrecognized`Callback`. <br /> |
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
| [Callback](../javax/security/auth/callback/Callback.md)! | the unrecognized`Callback`. |
