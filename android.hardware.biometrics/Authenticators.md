# BiometricManager.Authenticators

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Authenticators

Kotlin| [Java](https://developer.android.com/reference/android/hardware/biometrics/BiometricManager.Authenticators "View this page in Java") 

```
interface Authenticators
```

| [android.hardware.biometrics.BiometricManager.Authenticators](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#) |

Types of authenticators, defined at a level of granularity supported by [BiometricManager](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager) and [BiometricPrompt](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt).

Types may combined via bitwise OR into a single integer representing multiple authenticators (e.g.`DEVICE_CREDENTIAL | BIOMETRIC_WEAK`).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int) Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIOMETRIC_WEAK](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int) Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_CREDENTIAL](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#DEVICE_CREDENTIAL:kotlin.Int) The non-biometric credential used to secure the device (i.e., PIN, pattern, or password). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDENTITY_CHECK](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#IDENTITY_CHECK:kotlin.Int) The bit is used to request for Identity Check. |

## Constants

### BIOMETRIC_STRONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOMETRIC_STRONG: Int
```

Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for**Class 3** (formerly**Strong**), as defined by the Android CDD.

This corresponds to [KeyProperties.AUTH_BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties.html#AUTH_BIOMETRIC_STRONG:kotlin.Int) during key generation. 

 Value: 15

**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#) 

### BIOMETRIC_WEAK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOMETRIC_WEAK: Int
```

Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for**Class 2** (formerly**Weak**), as defined by the Android CDD.

Note that this is a superset of [BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int) and is defined such that`BIOMETRIC_STRONG | BIOMETRIC_WEAK == BIOMETRIC_WEAK`. 

 Value: 255

### DEVICE_CREDENTIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_CREDENTIAL: Int
```

The non-biometric credential used to secure the device (i.e., PIN, pattern, or password). This should typically only be used in combination with a biometric auth type, such as [BIOMETRIC_WEAK](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_WEAK:kotlin.Int).

This corresponds to [KeyProperties.AUTH_DEVICE_CREDENTIAL](https://developer.android.com/reference/kotlin/android/security/keystore/KeyProperties.html#AUTH_DEVICE_CREDENTIAL:kotlin.Int) during key generation. 

 Value: 32768

**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder](https://developer.android.com/reference/kotlin/android/security/keystore/KeyGenParameterSpec.Builder.html#) 

### IDENTITY_CHECK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDENTITY_CHECK: Int
```

The bit is used to request for Identity Check. Identity Check is a feature which requires class 3 biometric authentication to access sensitive surfaces when the device is outside trusted places.

The requirements to trigger Identity Check are as follows: 1. User must have enabled the toggle for Identity Check in settings 2. User must have enrollments for at least one [BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int) sensor 3. The device is determined to be in a high risk environment, for example if it is outside of the user's trusted locations or fails to meet similar conditions. 4. The Identity Check requirements bit must be true

If all the above conditions are satisfied, only [BIOMETRIC_STRONG](https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.Authenticators#BIOMETRIC_STRONG:kotlin.Int) sensors will be eligible for authentication, and device credential fallback will be dropped. 

 Value: 65536
