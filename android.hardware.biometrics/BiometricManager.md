Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiometricManager

```
open class BiometricManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.biometrics.BiometricManager](BiometricManager.md) |

A class that contains biometric utilities. For authentication, see `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt`. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators` Types of authenticators, defined at a level of granularity supported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#` and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt`. |
| open | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Strings` Provides localized strings for an application that uses `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt` to authenticate the user. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_LOGIN:kotlin.Int` Authentication purpose representing a login use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_PAYMENT:kotlin.Int` Authentication purpose representing a payment use case. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_UNKNOWN:kotlin.Int` Unknown authentication purpose. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` The hardware is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE:kotlin.Int` Identity Check is currently not active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NONE_ENROLLED:kotlin.Int` The user does not have any biometrics enrolled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS:kotlin.Int` Biometrics is not allowed to verify the user in apps. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NO_HARDWARE:kotlin.Int` There is no biometric hardware. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED:kotlin.Int` A security vulnerability has been discovered and the sensor is unavailable until a security update has addressed this issue. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_NO_AUTHENTICATION:kotlin.Long` Returned from `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getLastAuthenticationTime(kotlin.Int)` when no matching successful authentication has been performed since boot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` No error detected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_ACCOUNT:kotlin.Int` An icon representing a user account. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_GENERIC:kotlin.Int` A generic icon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_MESSAGE:kotlin.Int` An icon representing a message or chat option, such as to contact support or an administrator. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_PASSWORD:kotlin.Int` An icon representing a password. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_QR_CODE:kotlin.Int` An icon representing a QR code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_RESET:kotlin.Int` An icon representing a password reset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_SETTING:kotlin.Int` An icon representing settings (a gear). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#ICON_TYPE_SUPERVISED:kotlin.Int` An icon representing a supervised account. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#canAuthenticate()()` Determine if biometrics can be used. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#canAuthenticate(kotlin.Int)(authenticators: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine if any of the provided authenticators can be used. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getBiometricSensorStrengths()()` Returns a map of biometric modalities to their sensor security strengths. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getLastAuthenticationTime(kotlin.Int)(authenticators: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the last time the user successfully authenticated using one of the given authenticators. |
| open [BiometricManager.Strings](../android/hardware/biometrics/BiometricManager.Strings.md) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getStrings(kotlin.Int)(authenticators: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Produces an instance of the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Strings` class, which provides localized strings for an application, given a set of allowed authenticator types. |

## Constants

### AUTHENTICATION_PURPOSE_LOGIN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATION_PURPOSE_LOGIN: Int
```

Authentication purpose representing a login use case.

 Value: 2

### AUTHENTICATION_PURPOSE_PAYMENT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATION_PURPOSE_PAYMENT: Int
```

Authentication purpose representing a payment use case.

 Value: 1

### AUTHENTICATION_PURPOSE_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATION_PURPOSE_UNKNOWN: Int
```

Unknown authentication purpose.

 Value: 0

### BIOMETRIC_ERROR_HW_UNAVAILABLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_HW_UNAVAILABLE: Int
```

The hardware is unavailable. Try again later.

 Value: 1

### BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE: Int
```

Identity Check is currently not active. This device either doesn't have this feature enabled, or it's not considered in a high-risk environment that requires extra security measures for accessing sensitive data.

 Value: 20

### BIOMETRIC_ERROR_NONE_ENROLLED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NONE_ENROLLED: Int
```

The user does not have any biometrics enrolled.

 Value: 11

### BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS: Int
```

Biometrics is not allowed to verify the user in apps.

 Value: 21

### BIOMETRIC_ERROR_NO_HARDWARE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NO_HARDWARE: Int
```

There is no biometric hardware.

 Value: 12

### BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED: Int
```

A security vulnerability has been discovered and the sensor is unavailable until a security update has addressed this issue. This error can be received if for example, authentication was requested with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int`, but the sensor's strength can currently only meet `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int`.

 Value: 15

### BIOMETRIC_NO_AUTHENTICATION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_NO_AUTHENTICATION: Long
```

Returned from `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getLastAuthenticationTime(kotlin.Int)` when no matching successful authentication has been performed since boot.

 Value: -1L

### BIOMETRIC_SUCCESS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_SUCCESS: Int
```

No error detected.

 Value: 0

### ICON_TYPE_ACCOUNT

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_ACCOUNT: Int
```

An icon representing a user account.

 Value: 2

### ICON_TYPE_GENERIC

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_GENERIC: Int
```

A generic icon.

 Value: 3

### ICON_TYPE_MESSAGE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_MESSAGE: Int
```

An icon representing a message or chat option, such as to contact support or an administrator.

 Value: 6

### ICON_TYPE_PASSWORD

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_PASSWORD: Int
```

An icon representing a password.

 Value: 0

### ICON_TYPE_QR_CODE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_QR_CODE: Int
```

An icon representing a QR code.

 Value: 1

### ICON_TYPE_RESET

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_RESET: Int
```

An icon representing a password reset.

 Value: 5

### ICON_TYPE_SETTING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_SETTING: Int
```

An icon representing settings (a gear).

 Value: 4

### ICON_TYPE_SUPERVISED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ICON_TYPE_SUPERVISED: Int
```

An icon representing a supervised account.

 Value: 7

## Public methods

### canAuthenticate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canAuthenticate(): Int
```

**Deprecated:** *See `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#canAuthenticate(kotlin.Int)`.*

Determine if biometrics can be used. In other words, determine if `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt` can be expected to be shown (hardware available, templates enrolled, user-enabled). This is the equivalent of `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#canAuthenticate(kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NONE_ENROLLED:kotlin.Int` if the user does not have any strong biometrics enrolled, or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` if none are currently supported/enabled. Returns `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` if a strong biometric can currently be used (enrolled and available). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NONE_ENROLLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NO_HARDWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE:kotlin.Int` |

### canAuthenticate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canAuthenticate(authenticators: Int): Int
```

Determine if any of the provided authenticators can be used. In other words, determine if `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt` can be expected to be shown (hardware available, templates enrolled, user-enabled). For biometric authenticators, determine if the device can currently authenticate with at least the requested strength. For example, invoking this API with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int` on a device that currently only has `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` enrolled will return `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int`. Invoking this API with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` can be used to determine if the user has a PIN/Pattern/Password set up. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String`

| Parameters ||
|---|---|
| `authenticators` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field consisting of constants defined in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators`. If multiple authenticators are queried, a logical OR will be applied. For example, if `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` is queried and only `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` is set up, this API will return `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#IDENTITY_CHECK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NONE_ENROLLED:kotlin.Int` if the user does not have any of the requested authenticators enrolled, or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` if none are currently supported/enabled. Returns `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` if one of the requested authenticators can currently be used (enrolled and available). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NONE_ENROLLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_NO_HARDWARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE:kotlin.Int` |

### getBiometricSensorStrengths

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBiometricSensorStrengths(): MutableMap<Int!, Int!>
```

Returns a map of biometric modalities to their sensor security strengths.

Note that this API is intended exclusively for use by applications that hold a qualifying Android role (currently only `android.app.role.RoleManager#ROLE_WALLET` or `android.app.role.RoleManager#ROLE_DEVICE_POLICY_MANAGEMENT`) and are currently running in the foreground.

The returned map links each biometric modality available on the device (e.g., `TYPE_FINGERPRINT` for fingerprint or `TYPE_FACE` for face) to its corresponding sensor strength (e.g., `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` for Class-3 or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#LESS_THAN_STRONG:kotlin.Int` for unknown/unexposed cases). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_BIOMETRIC_SENSOR_STRENGTHS:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | This value cannot be `null`. |

### getLastAuthenticationTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLastAuthenticationTime(authenticators: Int): Long
```

Gets the last time the user successfully authenticated using one of the given authenticators. The returned value is time in `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` (time since boot, including sleep).

`https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_NO_AUTHENTICATION:kotlin.Long` is returned in the case where there has been no successful authentication using any of the given authenticators since boot.

Currently, only `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` are accepted. `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if `authenticators` contains other authenticator types.

Note that this may return successful authentication times even if the device is currently locked. You may use `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#isDeviceLocked()` to determine if the device is unlocked or not. Additionally, this method may return valid times for an authentication method that is no longer available. For instance, if the user unlocked the device with a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` authenticator but then deleted that authenticator (e.g., fingerprint data), this method will still return the time of that unlock for `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` if it is the most recent successful event. The caveat is that `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_NO_AUTHENTICATION:kotlin.Long` will be returned if the device no longer has a secure lock screen at all, even if there were successful authentications performed before the lock screen was made insecure. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String` 
Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base.

| Parameters ||
|---|---|
| `authenticators` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit field consisting of constants defined in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#IDENTITY_CHECK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the time of last authentication or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#BIOMETRIC_NO_AUTHENTICATION:kotlin.Long` Value is a non-negative timestamp in the `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()` time base. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `authenticators` contains values other than `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` or is 0. |

### getStrings

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrings(authenticators: Int): BiometricManager.Strings
```

Produces an instance of the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Strings` class, which provides localized strings for an application, given a set of allowed authenticator types. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String`

| Parameters ||
|---|---|
| `authenticators` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bit field representing the types of `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators` that may be used for authentication. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#IDENTITY_CHECK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Strings` | A `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Strings` collection for the given allowed authenticator types. This value cannot be `null`. |
