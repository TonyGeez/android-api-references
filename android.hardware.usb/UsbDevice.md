# UsbDevice

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbDevice

Kotlin| [Java](https://developer.android.com/reference/android/hardware/usb/UsbDevice "View this page in Java") 
| --- | --- |

```
open class UsbDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#) |

This class represents a USB device attached to the android device with the android device acting as the USB host. Each device contains one or more [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) s, each of which contains a number of [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) s (the channels via which data is transmitted over USB).

This class contains information (along with [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) and [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)) that describes the capabilities of the USB device. To communicate with the device, you open a [UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection) for the device and use [UsbRequest](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest) to send and receive data on an endpoint. android.hardware.usb.UsbDeviceConnection#controlTransfer is used for control requests on endpoint zero.
|
| ### Developer Guides
|
| For more information about communicating with USB hardware, read the [USB](https://developer.android.com/guide/topics/connectivity/usb/index.html) developer guide.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) | [getConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getConfiguration(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConfigurationCount](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getConfigurationCount())`()` Returns the number of [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) s this device contains. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceClass](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceClass())`()` Returns the devices's class field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceId())`()` Returns a unique integer ID for the device. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceId(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDeviceName](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceName())`()` Returns the name of the device. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDeviceName](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceName(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceProtocol](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceProtocol())`()` Returns the device's protocol field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceSubclass](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getDeviceSubclass())`()` Returns the device's subclass field. |
| open [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) | [getInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getInterface(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) at the given index. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInterfaceCount](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getInterfaceCount())`()` Returns the number of [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) s this device contains. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getManufacturerName](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getManufacturerName())`()` Returns the manufacturer name of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProductId](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getProductId())`()` Returns a product ID for the device. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getProductName](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getProductName())`()` Returns the product name of the device. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSerialNumber](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getSerialNumber())`()` Returns the serial number of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVendorId](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getVendorId())`()` Returns a vendor ID for the device. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#getVersion())`()` Returns the version number of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#hashCode())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#toString())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getConfiguration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConfiguration(index: Int): UsbConfiguration
```

Returns the [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) at the given index.

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) | the configuration This value cannot be`null`. |

### getConfigurationCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConfigurationCount(): Int
```

Returns the number of [UsbConfiguration](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration) s this device contains.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of configurations |

### getDeviceClass

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceClass(): Int
```

Returns the devices's class field. Some useful constants for USB device classes can be found in [UsbConstants](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants).

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the devices's class |

### getDeviceId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceId(): Int
```

Returns a unique integer ID for the device. This is a convenience for clients that want to use an integer to represent the device, rather than the device name. IDs are not persistent across USB disconnects.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device ID |

### getDeviceId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDeviceId(name: String!): Int
```  

### getDeviceName

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceName(): String
```

Returns the name of the device. In the standard implementation, this is the path of the device file for the device in the usbfs file system.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the device name This value cannot be`null`. |

### getDeviceName

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDeviceName(id: Int): String!
```  

### getDeviceProtocol

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceProtocol(): Int
```

Returns the device's protocol field.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device's protocol |

### getDeviceSubclass

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceSubclass(): Int
```

Returns the device's subclass field.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device's subclass |

### getInterface

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterface(index: Int): UsbInterface
```

Returns the [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) at the given index. For devices with multiple configurations, you will probably want to use [UsbConfiguration.getInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration#getInterface(kotlin.Int))instead.

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) | the interface This value cannot be`null`. |

### getInterfaceCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterfaceCount(): Int
```

Returns the number of [UsbInterface](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface) s this device contains. For devices with multiple configurations, you will probably want to use [UsbConfiguration.getInterfaceCount](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConfiguration#getInterfaceCount())instead.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of interfaces |

### getManufacturerName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getManufacturerName(): String?
```

Returns the manufacturer name of the device.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the manufacturer name, or`null`if the property could not be read |

### getProductId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProductId(): Int
```

Returns a product ID for the device.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device product ID |

### getProductName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProductName(): String?
```

Returns the product name of the device.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the product name, or`null`if the property could not be read |

### getSerialNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSerialNumber(): String?
```

Returns the serial number of the device.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the serial number name, or`null`if the property could not be read |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if the app targets SDK \>= {@value android.os.Build.VERSION_CODES#Q} and the app does not have permission to read from the device. |

### getVendorId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVendorId(): Int
```

Returns a vendor ID for the device.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device vendor ID |

### getVersion

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVersion(): String
```

Returns the version number of the device.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the device version This value cannot be`null`. |

### hashCode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

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
static val CREATOR: Parcelable.Creator<UsbDevice!>
```
