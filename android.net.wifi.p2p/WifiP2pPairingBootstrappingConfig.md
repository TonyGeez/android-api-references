# WifiP2pPairingBootstrappingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pPairingBootstrappingConfig

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig "View this page in Java") 
| --- | --- |

```
class WifiP2pPairingBootstrappingConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#) |

A class representing Wi-Fi Direct pairing bootstrapping configuration.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE:kotlin.Int) Pairing bootstrapping method display passphrase - The passphrase is displayed on the connection initiating device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE:kotlin.Int) Pairing bootstrapping method display pin-code - The pin-code is displayed on the connection initiating device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int) Pairing bootstrapping method keypad passphrase - The passphrase is displayed on the other device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int) Pairing bootstrapping method keypad pin-code - The pin-code is displayed on the other device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC:kotlin.Int) Pairing bootstrapping method opportunistic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND:kotlin.Int) Pairing bootstrapping done out of band (For example: Over Bluetooth LE. Refer Wi-Fi Alliance Wi-Fi Direct R2 specification Section 3.9 for the details). |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pPairingBootstrappingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#WifiP2pPairingBootstrappingConfig(kotlin.Int,%20kotlin.String))`(`method:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructor for a WifiP2pPairingBootstrappingConfig. |

| Public methods ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#describeContents())`()` Implement the Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPairingBootstrappingMethod](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#getPairingBootstrappingMethod())`()` Gets the current pairing bootstrapping method. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPairingBootstrappingPassword](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#getPairingBootstrappingPassword())`()` Retrieves the PIN or password used for the current pairing bootstrapping method. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#toString())`()` Generates a string of all the defined elements. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WifiP2pPairingBootstrappingConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

## Constants

### PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE: Int
```

Pairing bootstrapping method display passphrase - The passphrase is displayed on the connection initiating device. The user enters the displayed passphrase on the other device. 

 Value: 4

### PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE: Int
```

Pairing bootstrapping method display pin-code - The pin-code is displayed on the connection initiating device. The user enters the displayed pin-code on the other device. 

 Value: 2

### PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE: Int
```

Pairing bootstrapping method keypad passphrase - The passphrase is displayed on the other device. The user enters the displayed passphrase on the connection initiating device. 

 Value: 16

### PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE: Int
```

Pairing bootstrapping method keypad pin-code - The pin-code is displayed on the other device. The user enters the displayed pin-code on the connection initiating device. 

 Value: 8

### PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC: Int
```

Pairing bootstrapping method opportunistic 

 Value: 1

### PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND: Int
```

Pairing bootstrapping done out of band (For example: Over Bluetooth LE. Refer Wi-Fi Alliance Wi-Fi Direct R2 specification Section 3.9 for the details). 

 Value: 32

## Public constructors

### WifiP2pPairingBootstrappingConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pPairingBootstrappingConfig(
    method: Int, 
    password: String?)
```

Constructor for a WifiP2pPairingBootstrappingConfig.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `method` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the`PAIRING_BOOTSTRAPPING_METHOD_*`. Value is either`0`or a combination of [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int), and [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND:kotlin.Int) |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Password or PIN for pairing setup. if`method`is [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE:kotlin.Int), the password must be a string containing 4 or more digits (0-9). For example: "1234", "56789". if`method`is [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE:kotlin.Int) or [PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND:kotlin.Int), the password must be a UTF-8 string of minimum of 1 character. The password must be set to null if the`method`is [PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC:kotlin.Int), [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int) or [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int). |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if a non-null password is set for pairing bootstrapping method [PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC:kotlin.Int), [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int) or [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int). |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getPairingBootstrappingMethod

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPairingBootstrappingMethod(): Int
```

Gets the current pairing bootstrapping method.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current pairing bootstrapping method. Value is either`0`or a combination of [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OPPORTUNISTIC:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int), [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int), and [android.net.wifi.p2p.WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_OUT_OF_BAND:kotlin.Int) |

### getPairingBootstrappingPassword

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPairingBootstrappingPassword(): String?
```

Retrieves the PIN or password used for the current pairing bootstrapping method.

The specific type and format of the returned value depend on the active pairing bootstrapping method:

If the method is [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PINCODE:kotlin.Int) or [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PINCODE:kotlin.Int), this method returns a PIN. A PIN is a string consisting of 4 or more digits (0-9).

If the method is [PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_DISPLAY_PASSPHRASE:kotlin.Int) or [PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pPairingBootstrappingConfig#PAIRING_BOOTSTRAPPING_METHOD_KEYPAD_PASSPHRASE:kotlin.Int) this method returns a password. A password is a UTF-8 encoded string with a minimum length of 1 character.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The PIN or password as a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#), or`null`if not applicable for the current pairing bootstrapping method. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Generates a string of all the defined elements.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a compiled string representing all elements |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WifiP2pPairingBootstrappingConfig!>
```

Implement the Parcelable interface
