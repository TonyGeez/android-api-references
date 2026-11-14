# UsbInterface

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbInterface

Kotlin| [Java](https://developer.android.com/reference/android/hardware/usb/UsbInterface "View this page in Java") 
| --- | --- |

```
open class UsbInterface : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#) |

A class representing an interface on a [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice). USB devices can have one or more interfaces, each one providing a different piece of functionality, separate from the other interfaces. An interface will have one or more [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) s, which are the channels by which the host transfers data with the device.
|
| ### Developer Guides
|
| For more information about communicating with USB hardware, read the [USB](https://developer.android.com/guide/topics/usb/index.html) developer guide.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlternateSetting](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getAlternateSetting())`()` Returns the interface's bAlternateSetting field. |
| open [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)! | [getEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getEndpoint(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [android.hardware.usb.UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndpointCount](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getEndpointCount())`()` Returns the number of [android.hardware.usb.UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) s this interface contains. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getId())`()` Returns the interface's bInterfaceNumber field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInterfaceClass](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getInterfaceClass())`()` Returns the interface's class field. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInterfaceProtocol](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getInterfaceProtocol())`()` Returns the interface's protocol field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInterfaceSubclass](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getInterfaceSubclass())`()` Returns the interface's subclass field. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#getName())`()` Returns the interface's name. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAlternateSetting

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlternateSetting(): Int
```

Returns the interface's bAlternateSetting field. This is an integer that along with the ID uniquely identifies the interface on the device. [UsbDeviceConnection.setInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection#setInterface(android.hardware.usb.UsbInterface))can be used to switch between two interfaces with the same ID but different alternate setting.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the interface's alternate setting |

### getEndpoint

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEndpoint(index: Int): UsbEndpoint!
```

Returns the [android.hardware.usb.UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) at the given index.

| Return ||
|-------------------------------------------------------------------------------------------------|--------------|
| [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)! | the endpoint |

### getEndpointCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEndpointCount(): Int
```

Returns the number of [android.hardware.usb.UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) s this interface contains.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of endpoints |

### getId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): Int
```

Returns the interface's bInterfaceNumber field. This is an integer that along with the alternate setting uniquely identifies the interface on the device.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the interface's ID |

### getInterfaceClass

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterfaceClass(): Int
```

Returns the interface's class field. Some useful constants for USB classes can be found in [UsbConstants](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants)

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the interface's class |

### getInterfaceProtocol

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterfaceProtocol(): Int
```

Returns the interface's protocol field.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the interface's protocol |

### getInterfaceSubclass

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterfaceSubclass(): Int
```

Returns the interface's subclass field.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the interface's subclass |

### getName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String?
```

Returns the interface's name.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the interface's name, or`null`if the property could not be read |

### toString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<UsbInterface!>
```
