# SipRegistrationListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipRegistrationListener

Kotlin| [Java](https://developer.android.com/reference/android/net/sip/SipRegistrationListener "View this page in Java") 

```
interface SipRegistrationListener
```

| [android.net.sip.SipRegistrationListener](https://developer.android.com/reference/kotlin/android/net/sip/SipRegistrationListener#) |

| **This interface was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Listener for SIP registration events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistering](https://developer.android.com/reference/kotlin/android/net/sip/SipRegistrationListener#onRegistering(kotlin.String))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when a registration request is sent. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationDone](https://developer.android.com/reference/kotlin/android/net/sip/SipRegistrationListener#onRegistrationDone(kotlin.String,%20kotlin.Long))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expiryTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called when the registration succeeded. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRegistrationFailed](https://developer.android.com/reference/kotlin/android/net/sip/SipRegistrationListener#onRegistrationFailed(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`localProfileUri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called when the registration failed. |

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

**See Also**

- [android.net.sip.SipErrorCode](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode)
