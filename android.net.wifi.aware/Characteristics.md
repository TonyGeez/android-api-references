Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Characteristics

```
class Characteristics : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.Characteristics](Characteristics.md) |

The characteristics of the Wi-Fi Aware implementation.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_128:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS PK 2WDH 128: 128 bit public-key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_256:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS 2WDH 256: 256 bit public-key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS PASN 128: 128 bit public-key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS PASN 256: 256 bit public-key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_128:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS SK 128: 128 bit shared-key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_256:kotlin.Int` Wi-Fi Aware supported cipher suite representing NCS SK 256: 256 bit shared-key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NONE:kotlin.Int` Wi-Fi Aware supported open (unencrypted) data-path. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getMaxMatchFilterLength()()` Returns the maximum length of byte array that can be used to specify a Aware match filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getMaxServiceNameLength()()` Returns the maximum string length that can be used to specify a Aware service name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getMaxServiceSpecificInfoLength()()` Returns the maximum length of byte array that can be used to specify a Aware service specific information field: the arbitrary load used in discovery or the message length of Aware message exchange. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getNumberOfSupportedDataInterfaces()()` Returns the maximum number of Aware data interfaces supported by the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getNumberOfSupportedDataPaths()()` Returns the maximum number of Aware data paths(also known as NDPs - NAN Data Paths) supported by the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getNumberOfSupportedPublishSessions()()` Returns the maximum number of Aware publish sessions supported by the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getNumberOfSupportedSubscribeSessions()()` Returns the maximum number of Aware subscribe session supported by the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getSupportedCipherSuites()()` Returns the set of cipher suites supported by the device for use in Wi-Fi Aware data-paths. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getSupportedOffloadBootstrappingMethods()()` Returns the supported bootstrapping methods for framework offloaded auto-pairing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#getSupportedPairingCipherSuites()()` Returns the set of cipher suites supported by the device for use in Wi-Fi Aware pairing. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#isAwarePairingSupported()()` Check if the Aware Pairing and all associated security features as defined in Wi-Fi Alliance (WFA) Wi-Fi Aware Specification version 4. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#isInstantCommunicationModeSupported()()` Check if instant communication mode is supported by device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#isSuspensionSupported()()` Check if Aware Suspension is supported. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Characteristics](Characteristics.md)!\> | `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### WIFI_AWARE_CIPHER_SUITE_NCS_PK_128

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_PK_128: Int
```

Wi-Fi Aware supported cipher suite representing NCS PK 2WDH 128: 128 bit public-key.

 Value: 4

### WIFI_AWARE_CIPHER_SUITE_NCS_PK_256

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_PK_256: Int
```

Wi-Fi Aware supported cipher suite representing NCS 2WDH 256: 256 bit public-key.

 Value: 8

### WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128: Int
```

Wi-Fi Aware supported cipher suite representing NCS PASN 128: 128 bit public-key.

 Value: 16

### WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256: Int
```

Wi-Fi Aware supported cipher suite representing NCS PASN 256: 256 bit public-key.

 Value: 32

### WIFI_AWARE_CIPHER_SUITE_NCS_SK_128

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_SK_128: Int
```

Wi-Fi Aware supported cipher suite representing NCS SK 128: 128 bit shared-key.

 Value: 1

### WIFI_AWARE_CIPHER_SUITE_NCS_SK_256

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NCS_SK_256: Int
```

Wi-Fi Aware supported cipher suite representing NCS SK 256: 256 bit shared-key.

 Value: 2

### WIFI_AWARE_CIPHER_SUITE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIFI_AWARE_CIPHER_SUITE_NONE: Int
```

Wi-Fi Aware supported open (unencrypted) data-path.

 Value: 0

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getMaxMatchFilterLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxMatchFilterLength(): Int
```

Returns the maximum length of byte array that can be used to specify a Aware match filter. Restricts the parameters of the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setMatchFilter(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setMatchFilter(kotlin.collections.MutableList)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum length of byte array for Aware discovery match filter. |

### getMaxServiceNameLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxServiceNameLength(): Int
```

Returns the maximum string length that can be used to specify a Aware service name. Restricts the parameters of the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setServiceName(kotlin.String)` and `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setServiceName(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum string length of Aware service name. |

### getMaxServiceSpecificInfoLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxServiceSpecificInfoLength(): Int
```

Returns the maximum length of byte array that can be used to specify a Aware service specific information field: the arbitrary load used in discovery or the message length of Aware message exchange. Restricts the parameters of the `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray)`, `https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setServiceSpecificInfo(kotlin.ByteArray)`, and `https://developer.android.com/reference/kotlin/android/net/wifi/aware/DiscoverySession#sendMessage(android.net.wifi.aware.PeerHandle,%20kotlin.Int,%20kotlin.ByteArray)` variants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum length of byte array for Aware messaging. |

### getNumberOfSupportedDataInterfaces

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumberOfSupportedDataInterfaces(): Int
```

Returns the maximum number of Aware data interfaces supported by the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum number of Aware data interfaces supported by the device. Value is 1 or greater |

### getNumberOfSupportedDataPaths

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumberOfSupportedDataPaths(): Int
```

Returns the maximum number of Aware data paths(also known as NDPs - NAN Data Paths) supported by the device. Use `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailableDataPathsCount()` to get the number of available Aware data paths which are not currently used by any app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum number of Aware data paths supported by the device. Value is 1 or greater |

### getNumberOfSupportedPublishSessions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumberOfSupportedPublishSessions(): Int
```

Returns the maximum number of Aware publish sessions supported by the device. Use `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailablePublishSessionsCount()` to get the number of available publish sessions which are not currently used by any app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum number of publish sessions supported by the device. Value is 1 or greater |

### getNumberOfSupportedSubscribeSessions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumberOfSupportedSubscribeSessions(): Int
```

Returns the maximum number of Aware subscribe session supported by the device. Use `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwareResources#getAvailableSubscribeSessionsCount()` to get the number of available subscribe sessions which are not currently used by any app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A positive integer, maximum number of subscribe sessions supported by the device. Value is 1 or greater |

### getSupportedCipherSuites

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedCipherSuites(): Int
```

Returns the set of cipher suites supported by the device for use in Wi-Fi Aware data-paths. The device automatically picks the strongest cipher suite when initiating a data-path setup.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A set of flags from `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_128:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_256:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_128:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_256:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_SK_256:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_256:kotlin.Int` |

### getSupportedOffloadBootstrappingMethods

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedOffloadBootstrappingMethods(): Int
```

Returns the supported bootstrapping methods for framework offloaded auto-pairing. Returns a combination of the `PAIRING_BOOTSTRAPPING_*` bitmask constants from `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int` |

### getSupportedPairingCipherSuites

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedPairingCipherSuites(): Int
```

Returns the set of cipher suites supported by the device for use in Wi-Fi Aware pairing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A set of flags from `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int` |

### isAwarePairingSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAwarePairingSupported(): Boolean
```

Check if the Aware Pairing and all associated security features as defined in Wi-Fi Alliance (WFA) Wi-Fi Aware Specification version 4.0 are supported. This includes:

1. NAN Pairing (as in Wi-Fi Aware Specification Version 4.0 section 7.6) with NIK caching
2. NDP unicast data frame encryption (as in Wi-Fi Aware Specification Version 4.0 section 7.3.1)
3. Group addressed data frame encryption (as in Wi-Fi Aware Specification Version 4.0 section 7.3.3)
4. Management frame protection (as in Wi-Fi Aware Specification Version 4.0 section 7.3.2 for both unicast and multicast frames)
5. Beacon integrity protection (as in Wi-Fi Aware Specification Version 4.0 section 7.3.4)

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if supported, false otherwise. |

### isInstantCommunicationModeSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInstantCommunicationModeSupported(): Boolean
```

Check if instant communication mode is supported by device. The instant communication mode is defined as per Wi-Fi Alliance (WFA) Wi-Fi Aware specifications version 3.1 Section 12.3.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if supported, false otherwise. |

### isSuspensionSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSuspensionSupported(): Boolean
```

Check if Aware Suspension is supported. Aware Suspension is a mechanism of putting an Aware connection in and out of a low-power mode while preserving the discovery sessions and data paths.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if supported, false otherwise. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Characteristics!>
```
