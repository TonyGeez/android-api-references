# SipErrorCode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipErrorCode

Kotlin| [Java](SipErrorCode.md) 
| --- | --- |

```
open class SipErrorCode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipErrorCode](SipErrorCode.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Defines error codes returned during SIP actions. For example, during [onRegistrationFailed()](SipRegistrationListener.md)), [onError()](../android/net/sip/SipSession.Listener.md)), [onCallChangeFailed()](../android/net/sip/SipSession.Listener.md))and [onRegistrationFailed()](../android/net/sip/SipSession.Listener.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLIENT_ERROR](SipErrorCode.md) When some error occurs on the device, possibly due to a bug. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CROSS_DOMAIN_AUTHENTICATION](SipErrorCode.md) Cross-domain authentication required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_CONNECTION_LOST](SipErrorCode.md) When data connection is lost. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_CREDENTIALS](SipErrorCode.md) When invalid credentials are provided. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_REMOTE_URI](SipErrorCode.md) When the remote URI is not valid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IN_PROGRESS](SipErrorCode.md) The client is in a transaction and cannot initiate a new one. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_ERROR](SipErrorCode.md) Not an error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEER_NOT_REACHABLE](SipErrorCode.md) When the peer is not reachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVER_ERROR](SipErrorCode.md) When server responds with an error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVER_UNREACHABLE](SipErrorCode.md) When the server is not reachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_ERROR](SipErrorCode.md) When some socket error occurs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_OUT](SipErrorCode.md) When the transaction gets timed out. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_TERMINTED](SipErrorCode.md) When transaction is terminated unexpectedly. |

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](SipErrorCode.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Constants

### CLIENT_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLIENT_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

When some error occurs on the device, possibly due to a bug. 

 Value: -4

### CROSS_DOMAIN_AUTHENTICATION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CROSS_DOMAIN_AUTHENTICATION: Int
```

**Deprecated:** *Deprecated in Java.*

Cross-domain authentication required. 

 Value: -11

### DATA_CONNECTION_LOST

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_CONNECTION_LOST: Int
```

**Deprecated:** *Deprecated in Java.*

When data connection is lost. 

 Value: -10

### INVALID_CREDENTIALS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_CREDENTIALS: Int
```

**Deprecated:** *Deprecated in Java.*

When invalid credentials are provided. 

 Value: -8

### INVALID_REMOTE_URI

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_REMOTE_URI: Int
```

**Deprecated:** *Deprecated in Java.*

When the remote URI is not valid. 

 Value: -6

### IN_PROGRESS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IN_PROGRESS: Int
```

**Deprecated:** *Deprecated in Java.*

The client is in a transaction and cannot initiate a new one. 

 Value: -9

### NO_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Not an error. 

 Value: 0

### PEER_NOT_REACHABLE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEER_NOT_REACHABLE: Int
```

**Deprecated:** *Deprecated in Java.*

When the peer is not reachable. 

 Value: -7

### SERVER_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVER_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

When server responds with an error. 

 Value: -2

### SERVER_UNREACHABLE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVER_UNREACHABLE: Int
```

**Deprecated:** *Deprecated in Java.*

When the server is not reachable. 

 Value: -12

### SOCKET_ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

When some socket error occurs. 

 Value: -1

### TIME_OUT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIME_OUT: Int
```

**Deprecated:** *Deprecated in Java.*

When the transaction gets timed out. 

 Value: -5

### TRANSACTION_TERMINTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_TERMINTED: Int
```

**Deprecated:** *Deprecated in Java.*

When transaction is terminated unexpectedly. 

 Value: -3

## Public methods

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toString(errorCode: Int): String!
```

**Deprecated:** *Deprecated in Java.*
