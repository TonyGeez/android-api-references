# SipRegistrationListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipRegistrationListener

Kotlin| [Java](../android/net/sip/SipRegistrationListener.md) 
| --- | --- |

```
interface SipRegistrationListener
```

| [android.net.sip.SipRegistrationListener](../android/net/sip/SipRegistrationListener.md) |

| **This interface was deprecated in API level 31.**
|
| [android.net.sip.SipManager](../android/net/sip/SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Listener for SIP registration events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistering](../android/net/sip/SipRegistrationListener.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when a registration request is sent. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationDone](../android/net/sip/SipRegistrationListener.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expiryTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called when the registration succeeded. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](../android/net/sip/SipRegistrationListener.md))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when the registration failed. |
| --- | --- |

## Public methods

### onRegistering

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRegistering(localProfileUri: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a registration request is sent.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the URI string of the SIP profile to register with |

### onRegistrationDone

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRegistrationDone(
    localProfileUri: String!, 
    expiryTime: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the registration succeeded.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the URI string of the SIP profile to register with |
| `expiryTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):duration in seconds before the registration expires |

### onRegistrationFailed

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRegistrationFailed(
    localProfileUri: String!, 
    errorCode: Int, 
    errorMessage: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the registration failed.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `localProfileUri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the URI string of the SIP profile to register with |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):error code of this error |
| `errorMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:error message |
| --- | --- |

**See Also**

- [android.net.sip.SipErrorCode](../android/net/sip/SipErrorCode.md)
