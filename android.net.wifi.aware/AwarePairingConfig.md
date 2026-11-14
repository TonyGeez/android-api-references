# AwarePairingConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AwarePairingConfig

Kotlin| [Java](AwarePairingConfig.md) 
| --- | --- |

```
class AwarePairingConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.aware.AwarePairingConfig](AwarePairingConfig.md) |

The config for the Aware Pairing. Set to [PublishConfig.Builder.setPairingConfig(AwarePairingConfig)](../android/net/wifi/aware/PublishConfig.Builder.md))and [SubscribeConfig.Builder.setPairingConfig(AwarePairingConfig)](../android/net/wifi/aware/SubscribeConfig.Builder.md)). Only valid when [Characteristics.isAwarePairingSupported()](Characteristics.md))is true.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/wifi/aware/AwarePairingConfig.Builder.md) Builder used to build [AwarePairingConfig](AwarePairingConfig.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_NFC_READER](AwarePairingConfig.md) Aware Pairing bootstrapping method NFC reader |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_NFC_TAG](AwarePairingConfig.md) Aware Pairing bootstrapping method NFC tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](AwarePairingConfig.md) Aware Pairing bootstrapping method opportunistic |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](AwarePairingConfig.md) Aware Pairing bootstrapping method passphrase display |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](AwarePairingConfig.md) Aware Pairing bootstrapping method passphrase keypad |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](AwarePairingConfig.md) Aware Pairing bootstrapping method pin-code display |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](AwarePairingConfig.md) Aware Pairing bootstrapping method pin-code keypad |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_QR_DISPLAY](AwarePairingConfig.md) Aware Pairing bootstrapping method QR-code display |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_QR_SCAN](AwarePairingConfig.md) Aware Pairing bootstrapping method QR-code scan |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](AwarePairingConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AwarePairingConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBootstrappingMethods](AwarePairingConfig.md))`()` Get the supported bootstrapping methods in this config. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSupportedCipherSuites](AwarePairingConfig.md))`()` Get the supported cipher suites in this config. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AwarePairingConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingCacheEnabled](AwarePairingConfig.md))`()` Check if the NPK/NIK cache is support in the config |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingSetupEnabled](AwarePairingConfig.md))`()` Check if the Aware Pairing setup is support in the config. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPairingVerificationEnabled](AwarePairingConfig.md))`()` Check if the Aware Pairing verification is support in the config. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](AwarePairingConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AwarePairingConfig](AwarePairingConfig.md)!\> | [CREATOR](AwarePairingConfig.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_OPPORTUNISTIC](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_DISPLAY](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_DISPLAY](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_DISPLAY](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_TAG](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PIN_CODE_KEYPAD](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_PASSPHRASE_KEYPAD](AwarePairingConfig.md), [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_QR_SCAN](AwarePairingConfig.md), and [android.net.wifi.aware.AwarePairingConfig#PAIRING_BOOTSTRAPPING_NFC_READER](AwarePairingConfig.md) |

### getSupportedCipherSuites

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedCipherSuites(): Int
```

Get the supported cipher suites in this config.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_128](Characteristics.md), and [android.net.wifi.aware.Characteristics#WIFI_AWARE_CIPHER_SUITE_NCS_PK_PASN_256](Characteristics.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AwarePairingConfig!>
```
