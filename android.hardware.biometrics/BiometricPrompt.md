Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BiometricPrompt

```
open class BiometricPrompt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.biometrics.BiometricPrompt](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#) |

A class that manages a system-provided biometric dialog.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback` Callback structure provided to `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)` or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.hardware.biometrics.BiometricPrompt.CryptoObject,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)`. |
| open | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationResult` Container for callback data from `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)` and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.hardware.biometrics.BiometricPrompt.CryptoObject,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)`. |
| open | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder` A builder that collects arguments to be shown on the system-provided biometric dialog. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.CryptoObject` A wrapper class for the cryptographic operations supported by BiometricPrompt. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#AUTHENTICATION_RESULT_TYPE_BIOMETRIC:kotlin.Int` Authentication type reported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationResult` when the user authenticated by presenting some form of biometric (e.g. fingerprint or face). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#AUTHENTICATION_RESULT_TYPE_DEVICE_CREDENTIAL:kotlin.Int` Authentication type reported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationResult` when the user authenticated by entering their device PIN, pattern, or password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_GOOD:kotlin.Int` The image acquired was good. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_IMAGER_DIRTY:kotlin.Int` The biometric image was too noisy due to suspected or detected dirt on the sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_INSUFFICIENT:kotlin.Int` The biometric image was too noisy to process due to a detected condition or a possibly dirty sensor (See `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_IMAGER_DIRTY:kotlin.Int`). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_PARTIAL:kotlin.Int` Only a partial biometric image was detected. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_TOO_FAST:kotlin.Int` The biometric image was incomplete due to quick motion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_TOO_SLOW:kotlin.Int` The biometric image was unreadable due to lack of motion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_CANCELED:kotlin.Int` The operation was canceled because the biometric sensor is unavailable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_HW_NOT_PRESENT:kotlin.Int` The device does not have a biometric sensor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_HW_UNAVAILABLE:kotlin.Int` The hardware is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_IDENTITY_CHECK_NOT_ACTIVE:kotlin.Int` Identity Check is currently not active. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_LOCKOUT:kotlin.Int` The operation was canceled because the API is locked out due to too many attempts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_LOCKOUT_PERMANENT:kotlin.Int` The operation was canceled because BIOMETRIC_ERROR_LOCKOUT occurred too many times. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS:kotlin.Int` Biometrics is not allowed to verify the user in apps. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_NO_BIOMETRICS:kotlin.Int` The user does not have any biometrics enrolled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_NO_DEVICE_CREDENTIAL:kotlin.Int` The device does not have pin, pattern, or password set up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_NO_SPACE:kotlin.Int` Error state returned for operations like enrollment; the operation cannot be completed because there's not enough storage remaining to complete the operation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED:kotlin.Int` A security vulnerability has been discovered and the sensor is unavailable until a security update has addressed this issue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_TIMEOUT:kotlin.Int` Error state returned when the current request has been running too long. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_UNABLE_TO_PROCESS:kotlin.Int` Error state returned when the sensor was unable to process the current image. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_USER_CANCELED:kotlin.Int` The user canceled the operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ERROR_VENDOR:kotlin.Int` OEMs should use this constant if there are conditions that do not fit under any of the other publicly defined constants, and must provide appropriate strings for these errors to the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)` callback. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_NO_AUTHENTICATION:kotlin.Long` Returned from `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getLastAuthenticationTime(kotlin.Int)` when there has been no successful authentication for the given authenticator since boot. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.hardware.biometrics.BiometricPrompt.CryptoObject,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)(crypto: https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.CryptoObject, cancel: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback)` This call warms up the biometric hardware, displays a system-provided dialog, and starts scanning for a biometric. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)(cancel: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback)` This call warms up the biometric hardware, displays a system-provided dialog, and starts scanning for a biometric. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getAllowedAuthenticators()()` Gets the type(s) of authenticators that may be invoked by the prompt to authenticate the user, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setAllowedAuthenticators(kotlin.Int)`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getAuthenticationPurpose()()` Gets the authentication purpose for the prompt. |
| open [PromptContentView](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentView)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getContentView()()` Gets the content view for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setContentView(android.hardware.biometrics.PromptContentView)`. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getDescription()()` Gets the description for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setDescription(kotlin.CharSequence)`. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FallbackOption](https://developer.android.com/reference/kotlin/android/hardware/biometrics/FallbackOption)!\> | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getFallbackOptions()()` Gets the fallback options for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#addFallbackOption(kotlin.CharSequence,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getLogoBitmap()()` Gets the logo bitmap for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoBitmap(android.graphics.Bitmap)`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getLogoDescription()()` Gets the logo description for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoDescription(kotlin.String)`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getLogoRes()()` Gets the drawable resource of the logo for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoRes(kotlin.Int)`. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getMaxFallbackOptions()()` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getNegativeButtonText()()` Gets the negative button text for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setNegativeButton(kotlin.CharSequence,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getSubtitle()()` Gets the subtitle for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setSubtitle(kotlin.CharSequence)`. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#getTitle()()` Gets the title for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setTitle(kotlin.CharSequence)`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#isConfirmationRequired()()` Determines if explicit user confirmation is required by the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setConfirmationRequired(kotlin.Boolean)`. |
| --- | --- |

## Constants

### AUTHENTICATION_RESULT_TYPE_BIOMETRIC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATION_RESULT_TYPE_BIOMETRIC: Int
```

Authentication type reported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationResult` when the user authenticated by presenting some form of biometric (e.g. fingerprint or face).

 Value: 2

### AUTHENTICATION_RESULT_TYPE_DEVICE_CREDENTIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHENTICATION_RESULT_TYPE_DEVICE_CREDENTIAL: Int
```

Authentication type reported by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationResult` when the user authenticated by entering their device PIN, pattern, or password.

 Value: 1

### BIOMETRIC_ACQUIRED_GOOD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_GOOD: Int
```

The image acquired was good.

 Value: 0

### BIOMETRIC_ACQUIRED_IMAGER_DIRTY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_IMAGER_DIRTY: Int
```

The biometric image was too noisy due to suspected or detected dirt on the sensor. For example, it's reasonable return this after multiple `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_INSUFFICIENT:kotlin.Int` or actual detection of dirt on the sensor (stuck pixels, swaths, etc.). The user is expected to take action to clean the sensor when this is returned.

 Value: 3

### BIOMETRIC_ACQUIRED_INSUFFICIENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_INSUFFICIENT: Int
```

The biometric image was too noisy to process due to a detected condition or a possibly dirty sensor (See `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#BIOMETRIC_ACQUIRED_IMAGER_DIRTY:kotlin.Int`).

 Value: 2

### BIOMETRIC_ACQUIRED_PARTIAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_PARTIAL: Int
```

Only a partial biometric image was detected. During enrollment, the user should be informed on what needs to happen to resolve this problem, e.g. "press firmly on sensor." (for fingerprint)

 Value: 1

### BIOMETRIC_ACQUIRED_TOO_FAST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_TOO_FAST: Int
```

The biometric image was incomplete due to quick motion. For example, this could also happen if the user moved during acquisition. The user should be asked to repeat the operation more slowly.

 Value: 5

### BIOMETRIC_ACQUIRED_TOO_SLOW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ACQUIRED_TOO_SLOW: Int
```

The biometric image was unreadable due to lack of motion.

 Value: 4

### BIOMETRIC_ERROR_CANCELED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_CANCELED: Int
```

The operation was canceled because the biometric sensor is unavailable. For example, this may happen when the user is switched, the device is locked or another pending operation prevents or disables it.

 Value: 5

### BIOMETRIC_ERROR_HW_NOT_PRESENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_HW_NOT_PRESENT: Int
```

The device does not have a biometric sensor.

 Value: 12

### BIOMETRIC_ERROR_HW_UNAVAILABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### BIOMETRIC_ERROR_LOCKOUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_LOCKOUT: Int
```

The operation was canceled because the API is locked out due to too many attempts. This occurs after 5 failed attempts, and lasts for 30 seconds.

 Value: 7

### BIOMETRIC_ERROR_LOCKOUT_PERMANENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_LOCKOUT_PERMANENT: Int
```

The operation was canceled because BIOMETRIC_ERROR_LOCKOUT occurred too many times. Biometric authentication is disabled until the user unlocks with strong authentication (PIN/Pattern/Password)

 Value: 9

### BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NOT_ENABLED_FOR_APPS: Int
```

Biometrics is not allowed to verify the user in apps.

 Value: 21

### BIOMETRIC_ERROR_NO_BIOMETRICS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NO_BIOMETRICS: Int
```

The user does not have any biometrics enrolled.

 Value: 11

### BIOMETRIC_ERROR_NO_DEVICE_CREDENTIAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NO_DEVICE_CREDENTIAL: Int
```

The device does not have pin, pattern, or password set up. See `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setAllowedAuthenticators(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#canAuthenticate(kotlin.Int)`.

 Value: 14

### BIOMETRIC_ERROR_NO_SPACE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_NO_SPACE: Int
```

Error state returned for operations like enrollment; the operation cannot be completed because there's not enough storage remaining to complete the operation.

 Value: 4

### BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_SECURITY_UPDATE_REQUIRED: Int
```

A security vulnerability has been discovered and the sensor is unavailable until a security update has addressed this issue. This error can be received if for example, authentication was requested with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int`, but the sensor's strength can currently only meet `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int`.

 Value: 15

### BIOMETRIC_ERROR_TIMEOUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_TIMEOUT: Int
```

Error state returned when the current request has been running too long. This is intended to prevent programs from waiting for the biometric sensor indefinitely. The timeout is platform and sensor-specific, but is generally on the order of 30 seconds.

 Value: 3

### BIOMETRIC_ERROR_UNABLE_TO_PROCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_UNABLE_TO_PROCESS: Int
```

Error state returned when the sensor was unable to process the current image.

 Value: 2

### BIOMETRIC_ERROR_USER_CANCELED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_USER_CANCELED: Int
```

The user canceled the operation. Upon receiving this, applications should use alternate authentication (e.g. a password). The application should also provide the means to return to biometric authentication, such as a "use " button.

 Value: 10

### BIOMETRIC_ERROR_VENDOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_ERROR_VENDOR: Int
```

OEMs should use this constant if there are conditions that do not fit under any of the other publicly defined constants, and must provide appropriate strings for these errors to the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)` callback. OEMs should expect that the error message will be shown to users.

 Value: 8

### BIOMETRIC_NO_AUTHENTICATION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BIOMETRIC_NO_AUTHENTICATION: Long
```

Returned from `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#getLastAuthenticationTime(kotlin.Int)` when there has been no successful authentication for the given authenticator since boot.

 Value: -1L

## Public methods

### authenticate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun authenticate(
    crypto: BiometricPrompt.CryptoObject, 
    cancel: CancellationSignal, 
    executor: Executor, 
    callback: BiometricPrompt.AuthenticationCallback
): Unit
```

This call warms up the biometric hardware, displays a system-provided dialog, and starts scanning for a biometric. It terminates when `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)` is called, when `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationSucceeded(android.hardware.biometrics.BiometricPrompt.AuthenticationResult)`, or when the user dismisses the system-provided dialog, at which point the crypto object becomes invalid. This operation can be canceled by using the provided cancel object. The application will receive authentication errors through `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback`, and button events through the corresponding callback set in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setNegativeButton(kotlin.CharSequence,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)` or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#addFallbackOption(kotlin.CharSequence,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`. It is safe to reuse the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#` object, and calling `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)` while an existing authentication attempt is occurring will stop the previous client and start a new authentication. The interrupted client will receive a cancelled notification through `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)`.

Note: Applications generally should not cancel and start authentication in quick succession. For example, to properly handle authentication across configuration changes, it's recommended to use BiometricPrompt in a fragment with setRetainInstance(true). By doing so, the application will not need to cancel/restart authentication during the configuration change.

Per the Android CDD, only biometric authenticators that meet or exceed the requirements for **Strong** are permitted to integrate with Keystore to perform related cryptographic operations. Therefore, it is an error to call this method after explicitly calling `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setAllowedAuthenticators(kotlin.Int)` with any biometric strength other than `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String`

| Parameters ||
|---|---|
| `crypto` | [BiometricPrompt.CryptoObject](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.CryptoObject): A cryptographic operation to be unlocked after successful authentication. This value cannot be `null`. |
| `cancel` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#): An object that can be used to cancel authentication. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): An executor to handle callback events. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [BiometricPrompt.AuthenticationCallback](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback): An object to receive authentication events. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If any argument is null, or if the allowed biometric authenticator strength is explicitly set to `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int`. Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, this exception is also thrown if `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setDeviceCredentialAllowed(kotlin.Boolean)` was explicitly set to true. |

### authenticate

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun authenticate(
    cancel: CancellationSignal, 
    executor: Executor, 
    callback: BiometricPrompt.AuthenticationCallback
): Unit
```

This call warms up the biometric hardware, displays a system-provided dialog, and starts scanning for a biometric. It terminates when `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)` is called, when `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationSucceeded(android.hardware.biometrics.BiometricPrompt.AuthenticationResult)` is called, or when the user dismisses the system-provided dialog. This operation can be canceled by using the provided cancel object. The application will receive authentication errors through `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback`, and button events through the corresponding callback set in `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setNegativeButton(kotlin.CharSequence,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)` or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#addFallbackOption(kotlin.CharSequence,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`. It is safe to reuse the `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#` object, and calling `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt#authenticate(android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.hardware.biometrics.BiometricPrompt.AuthenticationCallback)` while an existing authentication attempt is occurring will stop the previous client and start a new authentication. The interrupted client will receive a cancelled notification through `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback#onAuthenticationError(kotlin.Int,%20kotlin.CharSequence)`.

Note: Applications generally should not cancel and start authentication in quick succession. For example, to properly handle authentication across configuration changes, it's recommended to use BiometricPrompt in a fragment with setRetainInstance(true). By doing so, the application will not need to cancel/restart authentication during the configuration change. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#USE_BIOMETRIC:kotlin.String`

| Parameters ||
|---|---|
| `cancel` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#): An object that can be used to cancel authentication. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): An executor to handle callback events. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BiometricPrompt.AuthenticationCallback](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.AuthenticationCallback): An object to receive authentication events. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If any of the arguments are null. |

### getAllowedAuthenticators

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedAuthenticators(): Int
```

Gets the type(s) of authenticators that may be invoked by the prompt to authenticate the user, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setAllowedAuthenticators(kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bit field representing the type(s) of authenticators that may be invoked by the prompt (as defined by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators`), or 0 if this field was not set. This value may be `null`. |

### getAuthenticationPurpose

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthenticationPurpose(): Int
```

Gets the authentication purpose for the prompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The authentication purpose. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_PAYMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_LOGIN:kotlin.Int` |

### getContentView

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentView(): PromptContentView?
```

Gets the content view for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setContentView(android.hardware.biometrics.PromptContentView)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentView?` | The content view for the prompt, or null if the prompt has no content view. |

### getDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDescription(): CharSequence?
```

Gets the description for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setDescription(kotlin.CharSequence)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The description for the prompt, or null if the prompt has no description. |

### getFallbackOptions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFallbackOptions(): MutableList<FallbackOption!>
```

Gets the fallback options for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#addFallbackOption(kotlin.CharSequence,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/biometrics/FallbackOption!>` | The fallback options for the prompt. This value cannot be `null`. |

### getLogoBitmap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLogoBitmap(): Bitmap?
```

Gets the logo bitmap for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoBitmap(android.graphics.Bitmap)`. Currently for system applications use only. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | The logo bitmap of the prompt, or null if the prompt has no logo bitmap set. |

### getLogoDescription

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLogoDescription(): String?
```

Gets the logo description for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoDescription(kotlin.String)`. Currently for system applications use only. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The logo description of the prompt, or null if the prompt has no logo description set. |

### getLogoRes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLogoRes(): Int
```

Gets the drawable resource of the logo for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setLogoRes(kotlin.Int)`. Currently for system applications use only. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The drawable resource of the logo, or 0 if the prompt has no logo resource set. |

### getMaxFallbackOptions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMaxFallbackOptions(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum amount of fallback options that can be added to the prompt |

### getNegativeButtonText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNegativeButtonText(): CharSequence?
```

Gets the negative button text for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setNegativeButton(kotlin.CharSequence,%20java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The negative button text for the prompt, or null if no negative button text was set. |

### getSubtitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubtitle(): CharSequence?
```

Gets the subtitle for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setSubtitle(kotlin.CharSequence)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The subtitle for the prompt, or null if the prompt has no subtitle. |

### getTitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTitle(): CharSequence
```

Gets the title for the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setTitle(kotlin.CharSequence)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | The title of the prompt, which is guaranteed to be non-null. |

### isConfirmationRequired

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isConfirmationRequired(): Boolean
```

Determines if explicit user confirmation is required by the prompt, as set by `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder#setConfirmationRequired(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if explicit user confirmation is required, or false otherwise. |
