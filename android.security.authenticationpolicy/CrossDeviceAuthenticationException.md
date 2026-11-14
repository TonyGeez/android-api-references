Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossDeviceAuthenticationException

```
class CrossDeviceAuthenticationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.security.authenticationpolicy.CrossDeviceAuthenticationException](CrossDeviceAuthenticationException.md) |
| --- | --- | --- | --- |

Exception thrown when cross-device authentication fails.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT:kotlin.Int` CompanionDeviceManager is not present on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_DECRYPTION_FAILED:kotlin.Int` Decryption of the payload failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_PACKAGE:kotlin.Int` The calling package is invalid or not allowlisted. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_TIMESTAMP:kotlin.Int` The request timestamp is invalid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_NOT_IN_FOREGROUND:kotlin.Int` The calling package was not visible in the foreground. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_SERIALIZATION_FAILED:kotlin.Int` Serialization or deserialization of the request failed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNAUTHORIZED:kotlin.Int` The request is not authorized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNKNOWN:kotlin.Int` Unknown error occurred. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#CrossDeviceAuthenticationException(kotlin.Int)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#CrossDeviceAuthenticationException(kotlin.Int,%20kotlin.String)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#CrossDeviceAuthenticationException(kotlin.Int,%20kotlin.String,%20kotlin.Throwable)(errorCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#getErrorCode()()` Returns the error code associated with this exception. |

## Constants

### ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT: Int
```

CompanionDeviceManager is not present on this device.

 Value: 7

### ERROR_DECRYPTION_FAILED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DECRYPTION_FAILED: Int
```

Decryption of the payload failed.

 Value: 2

### ERROR_INVALID_PACKAGE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_PACKAGE: Int
```

The calling package is invalid or not allowlisted.

 Value: 3

### ERROR_INVALID_TIMESTAMP

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_TIMESTAMP: Int
```

The request timestamp is invalid.

 Value: 4

### ERROR_NOT_IN_FOREGROUND

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NOT_IN_FOREGROUND: Int
```

The calling package was not visible in the foreground. Some form of foreground visibility is always required, but the exact definition of varies based on the device's form factor.

 Value: 6

### ERROR_SERIALIZATION_FAILED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_SERIALIZATION_FAILED: Int
```

Serialization or deserialization of the request failed.

 Value: 5

### ERROR_UNAUTHORIZED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNAUTHORIZED: Int
```

The request is not authorized. This error indicates that the user must take some action on the source device before the request can be fulfilled. The required conditions vary by form factor, but typically require that the has either unlocked the source device directly or has an an active connection to another trusted device. See the associated message for more details. A more specific error code from this class will be returned instead this error for common error conditions that do not vary.

 Value: 1

### ERROR_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN: Int
```

Unknown error occurred.

 Value: 0

## Public constructors

### CrossDeviceAuthenticationException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CrossDeviceAuthenticationException(errorCode: Int)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNAUTHORIZED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_DECRYPTION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_SERIALIZATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_NOT_IN_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT:kotlin.Int` |

### CrossDeviceAuthenticationException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CrossDeviceAuthenticationException(
    errorCode: Int, 
    message: String)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNAUTHORIZED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_DECRYPTION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_SERIALIZATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_NOT_IN_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### CrossDeviceAuthenticationException

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CrossDeviceAuthenticationException(
    errorCode: Int, 
    message: String, 
    cause: Throwable)
```

| Parameters ||
|---|---|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNAUTHORIZED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_DECRYPTION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_SERIALIZATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_NOT_IN_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): This value cannot be `null`. |
| --- | --- |

## Public methods

### getErrorCode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getErrorCode(): Int
```

Returns the error code associated with this exception.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_UNAUTHORIZED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_DECRYPTION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_PACKAGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_INVALID_TIMESTAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_SERIALIZATION_FAILED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_NOT_IN_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException#ERROR_COMPANION_DEVICE_MANAGER_NOT_PRESENT:kotlin.Int` |
