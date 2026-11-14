# BiometricManager.Authenticators

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Authenticators

Kotlin| [Java](../android/hardware/biometrics/BiometricManager.Authenticators.md) 
| --- | --- |

```
interface Authenticators
```

| [android.hardware.biometrics.BiometricManager.Authenticators](../android/hardware/biometrics/BiometricManager.Authenticators.md) |

Types of authenticators, defined at a level of granularity supported by [BiometricManager](../android/hardware/biometrics/BiometricManager.md) and [BiometricPrompt](../android/hardware/biometrics/BiometricPrompt.md).

Types may combined via bitwise OR into a single integer representing multiple authenticators (e.g.`DEVICE_CREDENTIAL | BIOMETRIC_WEAK`).
| --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIOMETRIC_STRONG](../android/hardware/biometrics/BiometricManager.Authenticators.md) Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BIOMETRIC_WEAK](../android/hardware/biometrics/BiometricManager.Authenticators.md) Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_CREDENTIAL](../android/hardware/biometrics/BiometricManager.Authenticators.md) The non-biometric credential used to secure the device (i.e., PIN, pattern, or password). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDENTITY_CHECK](../android/hardware/biometrics/BiometricManager.Authenticators.md) The bit is used to request for Identity Check. |

## Constants

### BIOMETRIC_STRONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOMETRIC_STRONG: Int
```

Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for**Class 3** (formerly**Strong**), as defined by the Android CDD.

This corresponds to [KeyProperties.AUTH_BIOMETRIC_STRONG](../android/security/keystore/KeyProperties.md) during key generation. 

 Value: 15

**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder](../android/security/keystore/KeyGenParameterSpec.Builder.md) 

### BIOMETRIC_WEAK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOMETRIC_WEAK: Int
```

Any biometric (e.g. fingerprint, iris, or face) on the device that meets or exceeds the requirements for**Class 2** (formerly**Weak**), as defined by the Android CDD.

Note that this is a superset of [BIOMETRIC_STRONG](../android/hardware/biometrics/BiometricManager.Authenticators.md) and is defined such that`BIOMETRIC_STRONG | BIOMETRIC_WEAK == BIOMETRIC_WEAK`. 
| --- | --- |

 Value: 255

### DEVICE_CREDENTIAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_CREDENTIAL: Int
```

The non-biometric credential used to secure the device (i.e., PIN, pattern, or password). This should typically only be used in combination with a biometric auth type, such as [BIOMETRIC_WEAK](../android/hardware/biometrics/BiometricManager.Authenticators.md).

This corresponds to [KeyProperties.AUTH_DEVICE_CREDENTIAL](../android/security/keystore/KeyProperties.md) during key generation. 

 Value: 32768

**See Also**

- [android.security.keystore.KeyGenParameterSpec.Builder](../android/security/keystore/KeyGenParameterSpec.Builder.md) 

### IDENTITY_CHECK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDENTITY_CHECK: Int
```

The bit is used to request for Identity Check. Identity Check is a feature which requires class 3 biometric authentication to access sensitive surfaces when the device is outside trusted places.

The requirements to trigger Identity Check are as follows: 1. User must have enabled the toggle for Identity Check in settings 2. User must have enrollments for at least one [BIOMETRIC_STRONG](../android/hardware/biometrics/BiometricManager.Authenticators.md) sensor 3. The device is determined to be in a high risk environment, for example if it is outside of the user's trusted locations or fails to meet similar conditions. 4. The Identity Check requirements bit must be true

If all the above conditions are satisfied, only [BIOMETRIC_STRONG](../android/hardware/biometrics/BiometricManager.Authenticators.md) sensors will be eligible for authentication, and device credential fallback will be dropped. 

 Value: 65536
