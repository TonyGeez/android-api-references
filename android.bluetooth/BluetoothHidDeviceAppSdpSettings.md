Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHidDeviceAppSdpSettings

Kotlin | [Java](BluetoothHidDeviceAppSdpSettings.md)
| --- | --- |

```
class BluetoothHidDeviceAppSdpSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHidDeviceAppSdpSettings](BluetoothHidDeviceAppSdpSettings.md) |

Represents the Service Discovery Protocol (SDP) settings for a Bluetooth HID Device application.

The BluetoothHidDevice framework adds the SDP record during app registration, so that the Android device can be discovered as a Bluetooth HID Device.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#BluetoothHidDeviceAppSdpSettings(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Byte,%20kotlin.ByteArray)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, description: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, provider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, subclass: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html, descriptors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Create a BluetoothHidDeviceAppSdpSettings object for the Bluetooth SDP record. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#getDescription()()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#getDescriptors()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#getName()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#getProvider()()` <br /> |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#getSubclass()()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothHidDeviceAppSdpSettings](BluetoothHidDeviceAppSdpSettings.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDeviceAppSdpSettings#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### BluetoothHidDeviceAppSdpSettings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BluetoothHidDeviceAppSdpSettings(
    name: String!, 
    description: String!, 
    provider: String!, 
    subclass: Byte, 
    descriptors: ByteArray!)
```

Create a BluetoothHidDeviceAppSdpSettings object for the Bluetooth SDP record.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of this Bluetooth HID device. Maximum length is 50 bytes. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Description for this Bluetooth HID device. Maximum length is 50 bytes. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Provider of this Bluetooth HID device. Maximum length is 50 bytes. |
| --- | --- |
| `subclass` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): Subclass of this Bluetooth HID device. See [www.usb.org/developers/hidpage/HID1_11.pdf Section 4.2](https://developer.android.com/static/reference/kotlin/android/bluetooth/www.usb.org/developers/hidpage/HID1_11.pdf) |
| `descriptors` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Descriptors of this Bluetooth HID device. See [www.usb.org/developers/hidpage/HID1_11.pdf Chapter 6](https://developer.android.com/static/reference/kotlin/android/bluetooth/www.usb.org/developers/hidpage/HID1_11.pdf) Maximum length is 2048 bytes. |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getDescription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): String!
```

### getDescriptors

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescriptors(): ByteArray!
```

### getName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

### getProvider

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProvider(): String!
```

### getSubclass

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubclass(): Byte
```

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<BluetoothHidDeviceAppSdpSettings!>
```
