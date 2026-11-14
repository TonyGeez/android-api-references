# BluetoothSocketException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothSocketException

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothSocketException "View this page in Java") 

```
open class BluetoothSocketException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [android.bluetooth.BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#) |

Thrown when an error occurs during a Bluetooth Socket related exception.

This is currently intended to be thrown for a failure during [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) operations.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLUETOOTH_OFF_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BLUETOOTH_OFF_FAILURE:kotlin.Int) Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because Bluetooth is turned off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_ACL_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_ACL_FAILURE:kotlin.Int) Error code during connect when there is an ACL connection failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_CLIENT_SECURITY_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE:kotlin.Int) Error code during connect when security clearance fails on the client during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INSUFFICIENT_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION:kotlin.Int) Error code during connect when authentication fails on the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INSUFFICIENT_AUTHORIZATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION:kotlin.Int) Error code during connect when authorization fails on the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INSUFFICIENT_ENCRYPTION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION:kotlin.Int) Error code during connect for insufficient encryption from the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE:kotlin.Int) Error code during connect indicating insufficient encryption key size on the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INVALID_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_PARAMETERS:kotlin.Int) Error code during connect for invalid parameters from the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_INVALID_SOURCE_CID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_SOURCE_CID:kotlin.Int) Error code during connect for invalid Channel ID from the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_NO_PSM_AVAILABLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE:kotlin.Int) Error code during connect when no PSM is available for L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_NO_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_RESOURCES:kotlin.Int) Error code during connect when no resources are available for L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_SOURCE_CID_ALREADY_ALLOCATED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED:kotlin.Int) Error code during connect for already allocated Channel ID from the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_TIMEOUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_TIMEOUT:kotlin.Int) Error code during connect when L2CAP connection timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_UNACCEPTABLE_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS:kotlin.Int) Error code during connect for unacceptable Parameters from the peer device during L2CAP connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L2CAP_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNKNOWN:kotlin.Int) Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a L2CAP-related socket operation that failed for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NULL_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#NULL_DEVICE:kotlin.Int) Error code during connect when null device attempts to do socket connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RPC_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#RPC_FAILURE:kotlin.Int) Error code during connect when a Runtime RPC exception occurs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_CLOSED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CLOSED:kotlin.Int) Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because the socket has been closed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_CONNECTION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CONNECTION_FAILURE:kotlin.Int) Error code during connect for generic socket connection failures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOCKET_MANAGER_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_MANAGER_FAILURE:kotlin.Int) Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because socket manager is not available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNIX_FILE_SOCKET_CREATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE:kotlin.Int) Error code during connect when the UNIX socket connection creation fails. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSPECIFIED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNSPECIFIED:kotlin.Int) Error code representing a failure during [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BluetoothSocketException(kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#) with an error code. |
| [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BluetoothSocketException(kotlin.Int,%20kotlin.String))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#) with an error code and custom error message. |

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#getErrorCode())`()` Returns the error code associated to this failure. |

## Constants

### BLUETOOTH_OFF_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLUETOOTH_OFF_FAILURE: Int
```

Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because Bluetooth is turned off. 

 Value: 15

### L2CAP_ACL_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_ACL_FAILURE: Int
```

Error code during connect when there is an ACL connection failure. 

 Value: 2

### L2CAP_CLIENT_SECURITY_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_CLIENT_SECURITY_FAILURE: Int
```

Error code during connect when security clearance fails on the client during L2CAP connection. 

 Value: 3

### L2CAP_INSUFFICIENT_AUTHENTICATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INSUFFICIENT_AUTHENTICATION: Int
```

Error code during connect when authentication fails on the peer device during L2CAP connection. 

 Value: 4

### L2CAP_INSUFFICIENT_AUTHORIZATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INSUFFICIENT_AUTHORIZATION: Int
```

Error code during connect when authorization fails on the peer device during L2CAP connection. 

 Value: 5

### L2CAP_INSUFFICIENT_ENCRYPTION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INSUFFICIENT_ENCRYPTION: Int
```

Error code during connect for insufficient encryption from the peer device during L2CAP connection. 

 Value: 7

### L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE: Int
```

Error code during connect indicating insufficient encryption key size on the peer device during L2CAP connection. 

 Value: 6

### L2CAP_INVALID_PARAMETERS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INVALID_PARAMETERS: Int
```

Error code during connect for invalid parameters from the peer device during L2CAP connection. 

 Value: 11

### L2CAP_INVALID_SOURCE_CID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_INVALID_SOURCE_CID: Int
```

Error code during connect for invalid Channel ID from the peer device during L2CAP connection. 

 Value: 8

### L2CAP_NO_PSM_AVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_NO_PSM_AVAILABLE: Int
```

Error code during connect when no PSM is available for L2CAP connection. 

 Value: 13

### L2CAP_NO_RESOURCES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_NO_RESOURCES: Int
```

Error code during connect when no resources are available for L2CAP connection. 

 Value: 12

### L2CAP_SOURCE_CID_ALREADY_ALLOCATED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_SOURCE_CID_ALREADY_ALLOCATED: Int
```

Error code during connect for already allocated Channel ID from the peer device during L2CAP connection. 

 Value: 9

### L2CAP_TIMEOUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_TIMEOUT: Int
```

Error code during connect when L2CAP connection timeout. 

 Value: 14

### L2CAP_UNACCEPTABLE_PARAMETERS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_UNACCEPTABLE_PARAMETERS: Int
```

Error code during connect for unacceptable Parameters from the peer device during L2CAP connection. 

 Value: 10

### L2CAP_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L2CAP_UNKNOWN: Int
```

Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a L2CAP-related socket operation that failed for an unknown reason. 

 Value: 1

### NULL_DEVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULL_DEVICE: Int
```

Error code during connect when null device attempts to do socket connection. 

 Value: 19

### RPC_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RPC_FAILURE: Int
```

Error code during connect when a Runtime RPC exception occurs. 

 Value: 20

### SOCKET_CLOSED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_CLOSED: Int
```

Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because the socket has been closed. 

 Value: 17

### SOCKET_CONNECTION_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_CONNECTION_FAILURE: Int
```

Error code during connect for generic socket connection failures. 

 Value: 18

### SOCKET_MANAGER_FAILURE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_MANAGER_FAILURE: Int
```

Error code returned by [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) during a socket operation that failed because socket manager is not available. 

 Value: 16

### UNIX_FILE_SOCKET_CREATION_FAILURE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNIX_FILE_SOCKET_CREATION_FAILURE: Int
```

Error code during connect when the UNIX socket connection creation fails. 

 Value: 21

### UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNSPECIFIED: Int
```

Error code representing a failure during [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket). The reason for failure isn't specified. 

 Value: 0

## Public constructors

### BluetoothSocketException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothSocketException(code: Int)
```

Create a [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#) with an error code. A generic error message is generated based on the`code`provided.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):: error code representing the reason for failure. Value is [android.bluetooth.BluetoothSocketException#UNSPECIFIED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNSPECIFIED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNKNOWN:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_ACL_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_ACL_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_SOURCE_CID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_SOURCE_CID:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_RESOURCES:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_TIMEOUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_TIMEOUT:kotlin.Int), [android.bluetooth.BluetoothSocketException#BLUETOOTH_OFF_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BLUETOOTH_OFF_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_MANAGER_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_MANAGER_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CLOSED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CLOSED:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CONNECTION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CONNECTION_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#NULL_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#NULL_DEVICE:kotlin.Int), [android.bluetooth.BluetoothSocketException#RPC_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#RPC_FAILURE:kotlin.Int), or [android.bluetooth.BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE:kotlin.Int) |

### BluetoothSocketException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothSocketException(
    code: Int, 
    msg: String)
```

Create a [BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#) with an error code and custom error message.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):: error code representing the reason for failure. Value is [android.bluetooth.BluetoothSocketException#UNSPECIFIED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNSPECIFIED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNKNOWN:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_ACL_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_ACL_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_SOURCE_CID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_SOURCE_CID:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_RESOURCES:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_TIMEOUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_TIMEOUT:kotlin.Int), [android.bluetooth.BluetoothSocketException#BLUETOOTH_OFF_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BLUETOOTH_OFF_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_MANAGER_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_MANAGER_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CLOSED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CLOSED:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CONNECTION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CONNECTION_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#NULL_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#NULL_DEVICE:kotlin.Int), [android.bluetooth.BluetoothSocketException#RPC_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#RPC_FAILURE:kotlin.Int), or [android.bluetooth.BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE:kotlin.Int) |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):: Custom error message associated to the failure. This value cannot be`null`. |

## Public methods

### getErrorCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorCode(): Int
```

Returns the error code associated to this failure.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothSocketException#UNSPECIFIED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNSPECIFIED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNKNOWN:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_ACL_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_ACL_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_CLIENT_SECURITY_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHENTICATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_AUTHORIZATION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPT_KEY_SIZE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INSUFFICIENT_ENCRYPTION:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_SOURCE_CID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_SOURCE_CID:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_SOURCE_CID_ALREADY_ALLOCATED:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_UNACCEPTABLE_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_INVALID_PARAMETERS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_INVALID_PARAMETERS:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_RESOURCES](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_RESOURCES:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_NO_PSM_AVAILABLE:kotlin.Int), [android.bluetooth.BluetoothSocketException#L2CAP_TIMEOUT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#L2CAP_TIMEOUT:kotlin.Int), [android.bluetooth.BluetoothSocketException#BLUETOOTH_OFF_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#BLUETOOTH_OFF_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_MANAGER_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_MANAGER_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CLOSED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CLOSED:kotlin.Int), [android.bluetooth.BluetoothSocketException#SOCKET_CONNECTION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#SOCKET_CONNECTION_FAILURE:kotlin.Int), [android.bluetooth.BluetoothSocketException#NULL_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#NULL_DEVICE:kotlin.Int), [android.bluetooth.BluetoothSocketException#RPC_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#RPC_FAILURE:kotlin.Int), or [android.bluetooth.BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException#UNIX_FILE_SOCKET_CREATION_FAILURE:kotlin.Int) |
