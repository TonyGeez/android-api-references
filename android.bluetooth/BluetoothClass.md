# BluetoothClass

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothClass

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothClass "View this page in Java") 
| --- | --- |

```
class BluetoothClass : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#) |

Represents a Bluetooth class, which describes general characteristics and capabilities of a device. For example, a Bluetooth class will specify the general device type such as a phone, a computer, or headset, and whether it's capable of services such as audio or telephony.

Every Bluetooth class is composed of zero or more service classes, and exactly one device class. The device class is further broken down into major and minor device class components.

[BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#) is useful as a hint to roughly describe a device (for example to show an icon in the UI), but does not reliably describe which Bluetooth profiles or services are actually supported by a device. Accurate service discovery is done through SDP requests, which are automatically performed when creating an RFCOMM socket with [android.bluetooth.BluetoothDevice#createRfcommSocketToServiceRecord](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID))and [android.bluetooth.BluetoothAdapter#listenUsingRfcommWithServiceRecord](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID))

Use [BluetoothDevice.getBluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getBluetoothClass())to retrieve the class for a remote device.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------|
| | [Device](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Device) Defines all device class constants. |
| | [Service](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Service) Defines all service class constants. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROFILE_A2DP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#PROFILE_A2DP:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROFILE_HEADSET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#PROFILE_HEADSET:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROFILE_HID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#PROFILE_HID:kotlin.Int) <br /> |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doesClassMatch](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#doesClassMatch(kotlin.Int))`(`profile:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Check class bits for possible bluetooth profile support. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#getDeviceClass())`()` Return the (major and minor) device class component of this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMajorDeviceClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#getMajorDeviceClass())`()` Return the major device class component of this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#hasService(kotlin.Int))`(`service:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the specified service class is supported by this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### PROFILE_A2DP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROFILE_A2DP: Int
```  

 Value: 1

### PROFILE_HEADSET

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROFILE_HEADSET: Int
```  

 Value: 0

### PROFILE_HID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROFILE_HID: Int
```  

 Value: 3

## Public methods

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### doesClassMatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doesClassMatch(profile: Int): Boolean
```

Check class bits for possible bluetooth profile support. This is a simple heuristic that tries to guess if a device with the given class bits might support specified profile. It is not accurate for all devices. It tries to err on the side of false positives.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------|
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the profile to be checked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether this device supports specified profile |

### equals

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
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

### getDeviceClass

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceClass(): Int
```

Return the (major and minor) device class component of this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#).

Values returned from this function can be compared with the public constants in [BluetoothClass.Device](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Device) to determine which device class is encoded in this Bluetooth class.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | device class component |

### getMajorDeviceClass

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMajorDeviceClass(): Int
```

Return the major device class component of this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#).

Values returned from this function can be compared with the public constants in [BluetoothClass.Device.Major](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Device.Major) to determine which major class is encoded in this Bluetooth class.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | major device class component |

### hasService

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasService(service: Int): Boolean
```

Return true if the specified service class is supported by this [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass#).

Valid service classes are the public constants in [BluetoothClass.Service](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Service). For example, [BluetoothClass.Service.AUDIO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass.Service#AUDIO:kotlin.Int).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------|
| `service` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):valid service class |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the service class is supported |

### hashCode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothClass!>
```
