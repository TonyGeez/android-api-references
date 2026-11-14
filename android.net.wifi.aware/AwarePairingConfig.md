# AwarePairingConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AwarePairingConfig

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/aware/AwarePairingConfig "View this page in Java") 
| --- | --- |

```
class AwarePairingConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.AwarePairingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#) |

The config for the Aware Pairing. Set to [PublishConfig.Builder.setPairingConfig(AwarePairingConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/PublishConfig.Builder#setPairingConfig(android.net.wifi.aware.AwarePairingConfig))and [SubscribeConfig.Builder.setPairingConfig(AwarePairingConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/aware/SubscribeConfig.Builder#setPairingConfig(android.net.wifi.aware.AwarePairingConfig)). Only valid when [Characteristics.isAwarePairingSupported()](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#isAwarePairingSupported())is true.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig.Builder) Builder used to build [AwarePairingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_NFC_READER](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER:kotlin.Int) Aware Pairing bootstrapping method NFC reader |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_NFC_TAG](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG:kotlin.Int) Aware Pairing bootstrapping method NFC tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC:kotlin.Int) Aware Pairing bootstrapping method opportunistic |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int) Aware Pairing bootstrapping method passphrase display |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int) Aware Pairing bootstrapping method passphrase keypad |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int) Aware Pairing bootstrapping method pin-code display |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int) Aware Pairing bootstrapping method pin-code keypad |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_QR_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY:kotlin.Int) Aware Pairing bootstrapping method QR-code display |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_QR_SCAN](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN:kotlin.Int) Aware Pairing bootstrapping method QR-code scan |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBootstrappingMethods](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#getBootstrappingMethods())`()` Get the supported bootstrapping methods in this config. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSupportedCipherSuites](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#getSupportedCipherSuites())`()` Get the supported cipher suites in this config. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingCacheEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#isPairingCacheEnabled())`()` Check if the NPK/NIK cache is support in the config |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingSetupEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#isPairingSetupEnabled())`()` Check if the Aware Pairing setup is support in the config. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingVerificationEnabled](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#isPairingVerificationEnabled())`()` Check if the Aware Pairing verification is support in the config. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AwarePairingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### PAIRING_BOOTSTRAPPING_NFC_READER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_NFC_READER: Int
```

Aware Pairing bootstrapping method NFC reader 

 Value: 256

### PAIRING_BOOTSTRAPPING_NFC_TAG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_NFC_TAG: Int
```

Aware Pairing bootstrapping method NFC tag 

 Value: 16

### PAIRING_BOOTSTRAPPING_OPPORTUNISTIC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_OPPORTUNISTIC: Int
```

Aware Pairing bootstrapping method opportunistic 

 Value: 1

### PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY: Int
```

Aware Pairing bootstrapping method passphrase display 

 Value: 4

### PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD: Int
```

Aware Pairing bootstrapping method passphrase keypad 

 Value: 64

### PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY: Int
```

Aware Pairing bootstrapping method pin-code display 

 Value: 2

### PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD: Int
```

Aware Pairing bootstrapping method pin-code keypad 

 Value: 32

### PAIRING_BOOTSTRAPPING_QR_DISPLAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_QR_DISPLAY: Int
```

Aware Pairing bootstrapping method QR-code display 

 Value: 8

### PAIRING_BOOTSTRAPPING_QR_SCAN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_QR_SCAN: Int
```

Aware Pairing bootstrapping method QR-code scan 

 Value: 128

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBootstrappingMethods

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBootstrappingMethods(): Int
```

Get the supported bootstrapping methods in this config. Set of the PAIRING_BOOTSTRAPPING_ values.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD:kotlin.Int), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN:kotlin.Int), and [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER](https://developer.android.com/reference/kotlin/android/net/wifi/aware/AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER:kotlin.Int) |

### getSupportedCipherSuites

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedCipherSuites(): Int
```

Get the supported cipher suites in this config.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128:kotlin.Int), and [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256](https://developer.android.com/reference/kotlin/android/net/wifi/aware/Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256:kotlin.Int) |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isPairingCacheEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPairingCacheEnabled(): Boolean
```

Check if the NPK/NIK cache is support in the config 

### isPairingSetupEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPairingSetupEnabled(): Boolean
```

Check if the Aware Pairing setup is support in the config. Setup is the first time for two device establish Aware Pairing 

### isPairingVerificationEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPairingVerificationEnabled(): Boolean
```

Check if the Aware Pairing verification is support in the config. Verification is for two device already paired and re-establish with cached NPK/NIK 

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AwarePairingConfig!>
```
