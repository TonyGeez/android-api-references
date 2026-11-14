Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbEndpoint

Kotlin | [Java](https://developer.android.com/reference/android/hardware/usb/UsbEndpoint "View this page in Java")

```
open class UsbEndpoint : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.usb.UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#) |

A class representing an endpoint on a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface`. Endpoints are the channels for sending and receiving data over USB. Typically bulk endpoints are used for sending non-trivial amounts of data. Interrupt endpoints are used for sending small amounts of data, typically events, separately from the main data streams. The endpoint zero is a special endpoint for control messages sent from the host to device. Isochronous endpoints are currently unsupported.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getAddress()()` Returns the endpoint's address field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getAttributes()()` Returns the endpoint's attributes field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getDirection()()` Returns the endpoint's direction. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getEndpointNumber()()` Extracts the endpoint's endpoint number from its address |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getInterval()()` Returns the endpoint's interval field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getMaxPacketSize()()` Returns the endpoint's maximum packet size. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType()()` Returns the endpoint's type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#)!\> | `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAddress

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAddress(): Int
```

Returns the endpoint's address field. The address is a bitfield containing both the endpoint number as well as the data direction of the endpoint. the endpoint number and direction can also be accessed via `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getEndpointNumber()` and `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getDirection()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's address |

### getAttributes

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributes(): Int
```

Returns the endpoint's attributes field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's attributes |

### getDirection

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDirection(): Int
```

Returns the endpoint's direction. Returns `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_OUT:kotlin.Int` if the direction is host to device, and `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_IN:kotlin.Int` if the direction is device to host.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's direction |

**See Also**

- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_IN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_OUT:kotlin.Int`

### getEndpointNumber

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEndpointNumber(): Int
```

Extracts the endpoint's endpoint number from its address

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's endpoint number |

### getInterval

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInterval(): Int
```

Returns the endpoint's interval field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's interval |

### getMaxPacketSize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxPacketSize(): Int
```

Returns the endpoint's maximum packet size.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's maximum packet size |

### getType

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): Int
```

Returns the endpoint's type. Possible results are:

- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_CONTROL:kotlin.Int` (endpoint zero)
- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_ISOC:kotlin.Int` (isochronous endpoint)
- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_BULK:kotlin.Int` (bulk endpoint)
- `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_INT:kotlin.Int` (interrupt endpoint)

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the endpoint's type |

### toString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    parcel: Parcel, 
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

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<UsbEndpoint!>
```
