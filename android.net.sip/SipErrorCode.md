# SipErrorCode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SipErrorCode

Kotlin| [Java](https://developer.android.com/reference/android/net/sip/SipErrorCode "View this page in Java") 
| --- | --- |

```
open class SipErrorCode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.sip.SipErrorCode](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

Defines error codes returned during SIP actions. For example, during [onRegistrationFailed()](https://developer.android.com/reference/kotlin/android/net/sip/SipRegistrationListener#onRegistrationFailed(kotlin.String,%20kotlin.Int,%20kotlin.String)), [onError()](https://developer.android.com/reference/kotlin/android/net/sip/SipSession.Listener#onError(android.net.sip.SipSession,%20kotlin.Int,%20kotlin.String)), [onCallChangeFailed()](https://developer.android.com/reference/kotlin/android/net/sip/SipSession.Listener#onCallChangeFailed(android.net.sip.SipSession,%20kotlin.Int,%20kotlin.String))and [onRegistrationFailed()](https://developer.android.com/reference/kotlin/android/net/sip/SipSession.Listener#onRegistrationFailed(android.net.sip.SipSession,%20kotlin.Int,%20kotlin.String)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLIENT_ERROR](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#CLIENT_ERROR:kotlin.Int) When some error occurs on the device, possibly due to a bug. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CROSS_DOMAIN_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#CROSS_DOMAIN_AUTHENTICATION:kotlin.Int) Cross-domain authentication required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_CONNECTION_LOST](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#DATA_CONNECTION_LOST:kotlin.Int) When data connection is lost. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_CREDENTIALS](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#INVALID_CREDENTIALS:kotlin.Int) When invalid credentials are provided. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_REMOTE_URI](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#INVALID_REMOTE_URI:kotlin.Int) When the remote URI is not valid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IN_PROGRESS](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#IN_PROGRESS:kotlin.Int) The client is in a transaction and cannot initiate a new one. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_ERROR](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#NO_ERROR:kotlin.Int) Not an error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEER_NOT_REACHABLE](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#PEER_NOT_REACHABLE:kotlin.Int) When the peer is not reachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVER_ERROR](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#SERVER_ERROR:kotlin.Int) When server responds with an error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVER_UNREACHABLE](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#SERVER_UNREACHABLE:kotlin.Int) When the server is not reachable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_ERROR](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#SOCKET_ERROR:kotlin.Int) When some socket error occurs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TIME_OUT](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#TIME_OUT:kotlin.Int) When the transaction gets timed out. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_TERMINTED](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#TRANSACTION_TERMINTED:kotlin.Int) When transaction is terminated unexpectedly. |

| Public methods ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](https://developer.android.com/reference/kotlin/android/net/sip/SipErrorCode#toString(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
