Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceHandle

Kotlin | [Java](DeviceHandle.md)
| --- | --- |

```
class DeviceHandle : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.ranging.oob.DeviceHandle](DeviceHandle.md) |

Represents a handle to a ranging device, containing information about the device and a transport handle for out-of-band communication.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle.Builder` Builder class for creating instances of `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [BluetoothDevice](../android.bluetooth/BluetoothDevice.md)? | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#getBluetoothDevice()()` Returns the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` object of the device associated with this `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#`. |
| [RangingDevice](../android.ranging/RangingDevice.md) | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#getRangingDevice()()` Returns the ranging device associated with this handle. |
| --- | --- |
| [TransportHandle](TransportHandle.md) | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#getTransportHandle()()` Returns the transport handle, if set, for communication. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [DeviceHandle](DeviceHandle.md)!\> | `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBluetoothDevice

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBluetoothDevice(): BluetoothDevice?
```

Returns the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` object of the device associated with this `https://developer.android.com/reference/kotlin/android/ranging/oob/DeviceHandle#`. This Bluetooth Device is used for BLE RSSI and Channel Sounding ranging.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#?` | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#` This value may be `null`. |

### getRangingDevice

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRangingDevice(): RangingDevice
```

Returns the ranging device associated with this handle.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/RangingDevice.html#` | The `https://developer.android.com/reference/kotlin/android/ranging/RangingDevice.html#` instance. This value cannot be `null`. |

### getTransportHandle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransportHandle(): TransportHandle
```

Returns the transport handle, if set, for communication.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle` | The `https://developer.android.com/reference/kotlin/android/ranging/oob/TransportHandle` instance. This value cannot be `null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<DeviceHandle!>
```
