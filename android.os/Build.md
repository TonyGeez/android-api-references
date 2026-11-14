Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Build

Kotlin | [Java](../android/os/Build.md)
| --- | --- |

```
open class Build
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Build](../android/os/Build.md) |

Information about the current build, extracted from system properties.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/os/Build.Partition` Build information for a particular device partition. |
| open | `https://developer.android.com/reference/kotlin/android/os/Build.VERSION` Various version strings. |
| open | `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES` Enumeration of the currently known SDK version codes. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES_FULL` Enumeration of the currently known SDK major and minor version codes. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_FIXED:kotlin.Int` The known issue is fixed on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_APPLICABLE:kotlin.Int` The known issue is not applicable to this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_FIXED:kotlin.Int` The known issue is not fixed on this device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_UNKNOWN:kotlin.Int` The status of the known issue on this device is not known. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#UNKNOWN:kotlin.String` Value used for when a build property is unknown. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Build#Build()()` <br /> |

| Public methods ||
|---|---|
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#getBackportedFixStatus(kotlin.Long)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` The status of the backported fix for a known issue on this device. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Build.Partition](../android/os/Build.Partition.md)!\> | `https://developer.android.com/reference/kotlin/android/os/Build#getFingerprintedPartitions()()` Get build information about partitions that have a separate fingerprint defined. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#getMajorSdkVersion(kotlin.Int)(sdkIntFull: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtain the major version encoded in a VERSION_CODES_FULL value. |
| --- | --- |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#getMinorSdkVersion(kotlin.Int)(sdkIntFull: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtain the minor version encoded in a VERSION_CODES_FULL value. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#getRadioVersion()()` Returns the version string for the radio firmware. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#getSerial()()` Gets the hardware serial number, if available. |
| --- | --- |

| Properties ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#BOARD:kotlin.String` The name of the underlying board, like "goldfish". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#BOOTLOADER:kotlin.String` The system bootloader version number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#BRAND:kotlin.String` The consumer-visible brand with which the product/hardware will be associated, if any. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#CPU_ABI:kotlin.String` The name of the instruction set (CPU type + ABI convention) of native code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#CPU_ABI2:kotlin.String` The name of the second instruction set (CPU type + ABI convention) of native code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#DEVICE:kotlin.String` The name of the industrial design. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#DISPLAY:kotlin.String` A build ID string meant for displaying to the user |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#FINGERPRINT:kotlin.String` A string that uniquely identifies this build. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#HARDWARE:kotlin.String` The name of the hardware (from the kernel command line or /proc). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#HOST:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#ID:kotlin.String` Either a changelist number, or a label like "M4-rc20". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#MANUFACTURER:kotlin.String` The manufacturer of the product/hardware. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#MODEL:kotlin.String` The end-user-visible name for the end product. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#ODM_SKU:kotlin.String` The SKU of the device as set by the original design manufacturer (ODM). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#PRODUCT:kotlin.String` The name of the overall product. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#RADIO:kotlin.String` The radio firmware version number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#SERIAL:kotlin.String` A hardware serial number, if available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#SKU:kotlin.String` The SKU of the hardware (from the kernel command line). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#SOC_MANUFACTURER:kotlin.String` The manufacturer of the device's primary system-on-chip. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#SOC_MODEL:kotlin.String` The model name of the device's primary system-on-chip. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#STRONGBOX_MANUFACTURER:kotlin.String` The manufacturer of the device's StrongBox chip. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#STRONGBOX_MODEL:kotlin.String` The model of the device's StrongBox chip. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_32_BIT_ABIS:kotlin.Array` An ordered list of **32 bit** ABIs supported by this device. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_64_BIT_ABIS:kotlin.Array` An ordered list of **64 bit** ABIs supported by this device. |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_ABIS:kotlin.Array` An ordered list of ABIs supported by this device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#TAGS:kotlin.String` Comma-separated tags describing the build, like "unsigned,debug". |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/Build#TIME:kotlin.Long` The time at which the build was produced, given in milliseconds since the UNIX epoch. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#TYPE:kotlin.String` The type of build, like "user" or "eng". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/Build#USER:kotlin.String` <br /> |

## Constants

### BACKPORTED_FIX_STATUS_FIXED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKPORTED_FIX_STATUS_FIXED: Int
```

The known issue is fixed on this device.

 Value: 1

### BACKPORTED_FIX_STATUS_NOT_APPLICABLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKPORTED_FIX_STATUS_NOT_APPLICABLE: Int
```

The known issue is not applicable to this device.

For example if the issue only affects a specific brand, devices from other brands would report not applicable.

 Value: 2

### BACKPORTED_FIX_STATUS_NOT_FIXED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKPORTED_FIX_STATUS_NOT_FIXED: Int
```

The known issue is not fixed on this device.

 Value: 3

### BACKPORTED_FIX_STATUS_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BACKPORTED_FIX_STATUS_UNKNOWN: Int
```

The status of the known issue on this device is not known.

 Value: 0

### UNKNOWN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN: String
```

Value used for when a build property is unknown.

 Value: "unknown"

## Public constructors

### Build

```
Build()
```

## Public methods

### getBackportedFixStatus

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getBackportedFixStatus(id: Long): Int
```

The status of the backported fix for a known issue on this device.

| Parameters ||
|---|---|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The id of the known issue to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_FIXED:kotlin.Int` if the known issue is fixed on this device, `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_FIXED:kotlin.Int` if the known issue is not fixed on this device, `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_APPLICABLE:kotlin.Int` if the known issue is is not applicable on this device, otherwise `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_UNKNOWN:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_FIXED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_APPLICABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/Build#BACKPORTED_FIX_STATUS_NOT_FIXED:kotlin.Int` |

### getFingerprintedPartitions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getFingerprintedPartitions(): MutableList<Build.Partition!>
```

Get build information about partitions that have a separate fingerprint defined. The list includes partitions that are suitable candidates for over-the-air updates. This is not an exhaustive list of partitions on the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/Build.Partition!>` | This value cannot be `null`. |

### getMajorSdkVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMajorSdkVersion(sdkIntFull: Int): Int
```

Obtain the major version encoded in a VERSION_CODES_FULL value. This value is guaranteed to be non-negative.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The major version encoded in a VERSION_CODES_FULL value |

### getMinorSdkVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getMinorSdkVersion(sdkIntFull: Int): Int
```

Obtain the minor version encoded in a VERSION_CODES_FULL value. This value is guaranteed to be non-negative.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The minor version encoded in a VERSION_CODES_FULL value |

### getRadioVersion

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getRadioVersion(): String!
```

Returns the version string for the radio firmware. May return null (if, for instance, the radio is not currently on).

### getSerial

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSerial(): String!
```

Gets the hardware serial number, if available.

**Note:** Root access may allow you to modify device identifiers, such as the hardware serial number. If you change these identifiers, you can not use [key attestation](../training/articles/security-key-attestation.md) to obtain proof of the device's original identifiers. KeyMint will reject an ID attestation request if the identifiers provided by the frameworks do not match the identifiers it was provisioned with.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](../training/articles/user-data-ids.md)). This method can be invoked if one of the following requirements is met:

- If the calling app has been granted the READ_PRIVILEGED_PHONE_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.
- If the calling app has carrier privileges (see `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#hasCarrierPrivileges()`) on any active subscription.
- If the calling app is the default SMS role holder (see `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#isRoleHeld(kotlin.String)`).
- If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#getEnrollmentSpecificId()`).

If the calling app does not meet one of these requirements then this method will behave as follows:

- If the calling app's target SDK is API level 28 or lower and the app has the READ_PHONE_STATE permission then `https://developer.android.com/reference/kotlin/android/os/Build#UNKNOWN:kotlin.String` is returned.
- If the calling app's target SDK is API level 28 or lower and the app does not have the READ_PHONE_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

. 
Requires android.Manifest.permission.READ_PRIVILEGED_PHONE_STATE

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The serial number if specified. |

## Properties

### BOARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOARD: String!
```

The name of the underlying board, like "goldfish".

### BOOTLOADER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOOTLOADER: String!
```

The system bootloader version number.

### BRAND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BRAND: String!
```

The consumer-visible brand with which the product/hardware will be associated, if any.

### CPU_ABI

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CPU_ABI: String!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_ABIS:kotlin.Array` instead.*

The name of the instruction set (CPU type + ABI convention) of native code.

### CPU_ABI2

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CPU_ABI2: String!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_ABIS:kotlin.Array` instead.*

The name of the second instruction set (CPU type + ABI convention) of native code.

### DEVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE: String!
```

The name of the industrial design.

### DISPLAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DISPLAY: String!
```

A build ID string meant for displaying to the user

### FINGERPRINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FINGERPRINT: String!
```

A string that uniquely identifies this build. Do not attempt to parse this value.

### HARDWARE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HARDWARE: String!
```

The name of the hardware (from the kernel command line or /proc).

### HOST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOST: String!
```

### ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ID: String!
```

Either a changelist number, or a label like "M4-rc20".

### MANUFACTURER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANUFACTURER: String!
```

The manufacturer of the product/hardware.

### MODEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODEL: String!
```

The end-user-visible name for the end product.

### ODM_SKU

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ODM_SKU: String
```

The SKU of the device as set by the original design manufacturer (ODM).

This is a runtime-initialized property set during startup to configure device services. If no value is set, this is reported as `https://developer.android.com/reference/kotlin/android/os/Build#UNKNOWN:kotlin.String`.

The ODM SKU may have multiple variants for the same system SKU in case a manufacturer produces variants of the same design. For example, the same build may be released with variations in physical keyboard and/or display hardware, each with a different ODM SKU.

### PRODUCT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRODUCT: String!
```

The name of the overall product.

### RADIO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RADIO: String!
```

**Deprecated:** *The radio firmware version is frequently not available when this class is initialized, leading to a blank or "unknown" value for this string. Use `https://developer.android.com/reference/kotlin/android/os/Build#getRadioVersion()` instead.*

The radio firmware version number.

### SERIAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERIAL: String!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/os/Build#getSerial()` instead.*

A hardware serial number, if available. Alphanumeric only, case-insensitive. This field is always set to `https://developer.android.com/reference/kotlin/android/os/Build#UNKNOWN:kotlin.String`.

### SKU

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SKU: String
```

The SKU of the hardware (from the kernel command line).

The SKU is reported by the bootloader to configure system software features. If no value is supplied by the bootloader, this is reported as `https://developer.android.com/reference/kotlin/android/os/Build#UNKNOWN:kotlin.String`.

### SOC_MANUFACTURER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOC_MANUFACTURER: String
```

The manufacturer of the device's primary system-on-chip.

### SOC_MODEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOC_MODEL: String
```

The model name of the device's primary system-on-chip.

### STRONGBOX_MANUFACTURER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRONGBOX_MANUFACTURER: String
```

The manufacturer of the device's StrongBox chip. If the device does not use StrongBox, this should be set to "unsupported".

### STRONGBOX_MODEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STRONGBOX_MODEL: String
```

The model of the device's StrongBox chip. If the device does not use StrongBox, this should be set to "unsupported".

### SUPPORTED_32_BIT_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPORTED_32_BIT_ABIS: Array<String!>!
```

An ordered list of **32 bit** ABIs supported by this device. The most preferred ABI is the first element in the list. See `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_ABIS:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_64_BIT_ABIS:kotlin.Array`.

### SUPPORTED_64_BIT_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPORTED_64_BIT_ABIS: Array<String!>!
```

An ordered list of **64 bit** ABIs supported by this device. The most preferred ABI is the first element in the list. See `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_ABIS:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_32_BIT_ABIS:kotlin.Array`.

### SUPPORTED_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUPPORTED_ABIS: Array<String!>!
```

An ordered list of ABIs supported by this device. The most preferred ABI is the first element in the list. See `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_32_BIT_ABIS:kotlin.Array` and `https://developer.android.com/reference/kotlin/android/os/Build#SUPPORTED_64_BIT_ABIS:kotlin.Array`.

### TAGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAGS: String!
```

Comma-separated tags describing the build, like "unsigned,debug".

### TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIME: Long
```

The time at which the build was produced, given in milliseconds since the UNIX epoch.

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE: String!
```

The type of build, like "user" or "eng".

### USER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USER: String!
```
