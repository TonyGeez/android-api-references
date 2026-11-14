# BluetoothGattCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattCharacteristic

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothGattCharacteristic "View this page in Java") 
| --- | --- |

```
open class BluetoothGattCharacteristic : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#) |

Represents a Bluetooth GATT Characteristic

A GATT characteristic is a basic data element used to construct a GATT service, [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService). The characteristic contains a value as well as additional information and optional GATT descriptors, [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_FLOAT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_FLOAT:kotlin.Int) Characteristic value format type float (32-bit float) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SFLOAT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_SFLOAT:kotlin.Int) Characteristic value format type sfloat (16-bit float) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SINT16](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_SINT16:kotlin.Int) Characteristic value format type sint16 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SINT32](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_SINT32:kotlin.Int) Characteristic value format type sint32 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SINT8](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_SINT8:kotlin.Int) Characteristic value format type sint8 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_UINT16](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_UINT16:kotlin.Int) Characteristic value format type uint16 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_UINT32](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_UINT32:kotlin.Int) Characteristic value format type uint32 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_UINT8](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_UINT8:kotlin.Int) Characteristic value format type uint8 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_READ:kotlin.Int) Characteristic read permission |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_READ_ENCRYPTED:kotlin.Int) Characteristic permission: Allow encrypted read operations |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_READ_ENCRYPTED_MITM:kotlin.Int) Characteristic permission: Allow reading with person-in-the-middle protection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_WRITE:kotlin.Int) Characteristic write permission |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_WRITE_ENCRYPTED:kotlin.Int) Characteristic permission: Allow encrypted writes |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_WRITE_ENCRYPTED_MITM:kotlin.Int) Characteristic permission: Allow encrypted writes with person-in-the-middle protection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_WRITE_SIGNED:kotlin.Int) Characteristic permission: Allow signed write operations |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PERMISSION_WRITE_SIGNED_MITM:kotlin.Int) Characteristic permission: Allow signed write operations with person-in-the-middle protection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_BROADCAST](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_BROADCAST:kotlin.Int) Characteristic property: Characteristic is broadcastable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_EXTENDED_PROPS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_EXTENDED_PROPS:kotlin.Int) Characteristic property: Characteristic has extended properties |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_INDICATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_INDICATE:kotlin.Int) Characteristic property: Characteristic supports indication |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_NOTIFY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_NOTIFY:kotlin.Int) Characteristic property: Characteristic supports notification |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_READ](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_READ:kotlin.Int) Characteristic property: Characteristic is readable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_SIGNED_WRITE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_SIGNED_WRITE:kotlin.Int) Characteristic property: Characteristic supports write with signature |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_WRITE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_WRITE:kotlin.Int) Characteristic property: Characteristic can be written. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROPERTY_WRITE_NO_RESPONSE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#PROPERTY_WRITE_NO_RESPONSE:kotlin.Int) Characteristic property: Characteristic can be written without response. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WRITE_TYPE_DEFAULT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT:kotlin.Int) Write characteristic, requesting acknowledgement by the remote device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WRITE_TYPE_NO_RESPONSE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE:kotlin.Int) Write characteristic without requiring a response by the remote device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WRITE_TYPE_SIGNED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_SIGNED:kotlin.Int) Write characteristic including authentication signature |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#BluetoothGattCharacteristic(java.util.UUID,%20kotlin.Int,%20kotlin.Int))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`, `properties:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `permissions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new BluetoothGattCharacteristic. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#addDescriptor(android.bluetooth.BluetoothGattDescriptor))`(`descriptor:` ` [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!`)` Adds a descriptor to this characteristic. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#describeContents())`()` <br /> |
| open [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)! | [getDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getDescriptor(java.util.UUID))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`)` Returns a descriptor with a given UUID out of the list of descriptors for this characteristic. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!\>! | [getDescriptors](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getDescriptors())`()` Returns a list of descriptors for this characteristic. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [getFloatValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getFloatValue(kotlin.Int,%20kotlin.Int))`(`formatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the stored value of this characteristic. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInstanceId](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getInstanceId())`()` Returns the instance ID for this characteristic. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [getIntValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getIntValue(kotlin.Int,%20kotlin.Int))`(`formatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the stored value of this characteristic. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPermissions](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getPermissions())`()` Returns the permissions for this characteristic. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProperties](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getProperties())`()` Returns the properties of this characteristic. |
| --- | --- |
| open [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)! | [getService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getService())`()` Returns the service this characteristic belongs to. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStringValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getStringValue(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the stored value of this characteristic. |
| open [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [getUuid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getUuid())`()` Returns the UUID of this characteristic |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getValue())`()` Get the stored value for this characteristic. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWriteType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getWriteType())`()` Gets the write type for this characteristic. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.ByteArray))`(`value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the locally stored value of this characteristic. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `formatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the locally stored value of this characteristic. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`mantissa:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exponent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `formatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the locally stored value of this characteristic. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the locally stored value of this characteristic. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWriteType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setWriteType(kotlin.Int))`(`writeType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the write type for this characteristic |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#CREATOR:android.os.Parcelable.Creator) <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!\>! | [mDescriptors](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#mDescriptors:kotlin.collections.MutableList) List of descriptors included in this characteristic. |

## Constants

### FORMAT_FLOAT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_FLOAT: Int
```

Characteristic value format type float (32-bit float) 

 Value: 52

### FORMAT_SFLOAT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SFLOAT: Int
```

Characteristic value format type sfloat (16-bit float) 

 Value: 50

### FORMAT_SINT16

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SINT16: Int
```

Characteristic value format type sint16 

 Value: 34

### FORMAT_SINT32

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SINT32: Int
```

Characteristic value format type sint32 

 Value: 36

### FORMAT_SINT8

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SINT8: Int
```

Characteristic value format type sint8 

 Value: 33

### FORMAT_UINT16

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_UINT16: Int
```

Characteristic value format type uint16 

 Value: 18

### FORMAT_UINT32

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_UINT32: Int
```

Characteristic value format type uint32 

 Value: 20

### FORMAT_UINT8

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_UINT8: Int
```

Characteristic value format type uint8 

 Value: 17

### PERMISSION_READ

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ: Int
```

Characteristic read permission 

 Value: 1

### PERMISSION_READ_ENCRYPTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ_ENCRYPTED: Int
```

Characteristic permission: Allow encrypted read operations 

 Value: 2

### PERMISSION_READ_ENCRYPTED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ_ENCRYPTED_MITM: Int
```

Characteristic permission: Allow reading with person-in-the-middle protection 

 Value: 4

### PERMISSION_WRITE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE: Int
```

Characteristic write permission 

 Value: 16

### PERMISSION_WRITE_ENCRYPTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_ENCRYPTED: Int
```

Characteristic permission: Allow encrypted writes 

 Value: 32

### PERMISSION_WRITE_ENCRYPTED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_ENCRYPTED_MITM: Int
```

Characteristic permission: Allow encrypted writes with person-in-the-middle protection 

 Value: 64

### PERMISSION_WRITE_SIGNED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_SIGNED: Int
```

Characteristic permission: Allow signed write operations 

 Value: 128

### PERMISSION_WRITE_SIGNED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_SIGNED_MITM: Int
```

Characteristic permission: Allow signed write operations with person-in-the-middle protection 

 Value: 256

### PROPERTY_BROADCAST

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_BROADCAST: Int
```

Characteristic property: Characteristic is broadcastable. 

 Value: 1

### PROPERTY_EXTENDED_PROPS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_EXTENDED_PROPS: Int
```

Characteristic property: Characteristic has extended properties 

 Value: 128

### PROPERTY_INDICATE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_INDICATE: Int
```

Characteristic property: Characteristic supports indication 

 Value: 32

### PROPERTY_NOTIFY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_NOTIFY: Int
```

Characteristic property: Characteristic supports notification 

 Value: 16

### PROPERTY_READ

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_READ: Int
```

Characteristic property: Characteristic is readable. 

 Value: 2

### PROPERTY_SIGNED_WRITE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_SIGNED_WRITE: Int
```

Characteristic property: Characteristic supports write with signature 

 Value: 64

### PROPERTY_WRITE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_WRITE: Int
```

Characteristic property: Characteristic can be written. 

 Value: 8

### PROPERTY_WRITE_NO_RESPONSE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_WRITE_NO_RESPONSE: Int
```

Characteristic property: Characteristic can be written without response. 

 Value: 4

### WRITE_TYPE_DEFAULT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRITE_TYPE_DEFAULT: Int
```

Write characteristic, requesting acknowledgement by the remote device 

 Value: 2

### WRITE_TYPE_NO_RESPONSE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRITE_TYPE_NO_RESPONSE: Int
```

Write characteristic without requiring a response by the remote device 

 Value: 1

### WRITE_TYPE_SIGNED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRITE_TYPE_SIGNED: Int
```

Write characteristic including authentication signature 

 Value: 4

## Public constructors

### BluetoothGattCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothGattCharacteristic(
    uuid: UUID!, 
    properties: Int, 
    permissions: Int)
```

Create a new BluetoothGattCharacteristic.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!:The UUID for this characteristic |
| `properties` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Properties of this characteristic |
| `permissions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Permissions for this characteristic |
| --- | --- |

## Public methods

### addDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addDescriptor(descriptor: BluetoothGattDescriptor!): Boolean
```

Adds a descriptor to this characteristic.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `descriptor` | [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!:Descriptor to be added to this characteristic. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the descriptor was added to the characteristic |

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescriptor(uuid: UUID!): BluetoothGattDescriptor!
```

Returns a descriptor with a given UUID out of the list of descriptors for this characteristic.

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)! | GATT descriptor object or null if no descriptor with the given UUID was found. |

### getDescriptors

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescriptors(): MutableList<BluetoothGattDescriptor!>!
```

Returns a list of descriptors for this characteristic.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor)!>! | Descriptors for this characteristic |

### getFloatValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFloatValue(
    formatType: Int, 
    offset: Int
): Float!
```

**Deprecated:** *Use [BluetoothGatt.readCharacteristic(BluetoothGattCharacteristic)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic))to get the characteristic value*

Return the stored value of this characteristic.

See [getValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getValue())for details.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `formatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The format type used to interpret the characteristic value. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which the float value can be found. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | Cached value of the characteristic at a given offset or null if the requested offset exceeds the value size. |

### getInstanceId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInstanceId(): Int
```

Returns the instance ID for this characteristic.

If a remote device offers multiple characteristics with the same UUID, the instance ID is used to distinguish between characteristics.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Instance ID of this characteristic |

### getIntValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntValue(
    formatType: Int, 
    offset: Int
): Int!
```

**Deprecated:** *Use [BluetoothGatt.readCharacteristic(BluetoothGattCharacteristic)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic))to get the characteristic value*

Return the stored value of this characteristic.

The formatType parameter determines how the characteristic value is to be interpreted. For example, setting formatType to [FORMAT_UINT16](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#FORMAT_UINT16:kotlin.Int) specifies that the first two bytes of the characteristic value at the given offset are interpreted to generate the return value.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `formatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The format type used to interpret the characteristic value. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which the integer value can be found. |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | Cached value of the characteristic or null of offset exceeds value size. |

### getPermissions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermissions(): Int
```

Returns the permissions for this characteristic.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Permissions of this characteristic |

### getProperties

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): Int
```

Returns the properties of this characteristic.

The properties contain a bit mask of property flags indicating the features of this characteristic.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Properties of this characteristic |

### getService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getService(): BluetoothGattService!
```

Returns the service this characteristic belongs to.

| Return ||
|----------------------------------------------------------------------------------------------------------------|------------------------|
| [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService)! | The associated service |

### getStringValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStringValue(offset: Int): String!
```

**Deprecated:** *Use [BluetoothGatt.readCharacteristic(BluetoothGattCharacteristic)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic))to get the characteristic value*

Return the stored value of this characteristic.

See [getValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#getValue())for details.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which the string value can be found. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Cached value of the characteristic |

### getUuid

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUuid(): UUID!
```

Returns the UUID of this characteristic

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | UUID of this characteristic |

### getValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): ByteArray!
```

**Deprecated:** *Use [BluetoothGatt.readCharacteristic(BluetoothGattCharacteristic)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic))instead*

Get the stored value for this characteristic.

This function returns the stored value for this characteristic as retrieved by calling [BluetoothGatt.readCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readCharacteristic(android.bluetooth.BluetoothGattCharacteristic)). The cached value of the characteristic is updated as a result of a read characteristic operation or if a characteristic update notification has been received.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | Cached value of the characteristic |

### getWriteType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWriteType(): Int
```

Gets the write type for this characteristic.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Write type for this characteristic Value is [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT:kotlin.Int), [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE:kotlin.Int), or [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_SIGNED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_SIGNED:kotlin.Int) |

### setValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(value: ByteArray!): Boolean
```

**Deprecated:** *Pass the characteristic value directly into[android.bluetooth.BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,byte[],int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int))*

Updates the locally stored value of this characteristic.

This function modifies the locally stored cached value of this characteristic. To send the value to the remote device, call android.bluetooth.BluetoothGatt#writeCharacteristic to send the value to the remote device.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:New value for this characteristic |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locally stored value has been set, false if the requested value could not be stored locally. |

### setValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(
    value: Int, 
    formatType: Int, 
    offset: Int
): Boolean
```

**Deprecated:** *Pass the characteristic value directly into[android.bluetooth.BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,byte[],int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int))*

Set the locally stored value of this characteristic.

See[setValue(byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.ByteArray))for details.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):New value for this characteristic |
| `formatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Integer format type used to transform the value parameter |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which the value should be placed |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locally stored value has been set |

### setValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(
    mantissa: Int, 
    exponent: Int, 
    formatType: Int, 
    offset: Int
): Boolean
```

**Deprecated:** *Pass the characteristic value directly into[android.bluetooth.BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,byte[],int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int))*

Set the locally stored value of this characteristic.

See[setValue(byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.ByteArray))for details.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `mantissa` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Mantissa for this characteristic |
| `exponent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):exponent value for this characteristic |
| `formatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Float format type used to transform the value parameter |
| --- | --- |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset at which the value should be placed |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locally stored value has been set |

### setValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(value: String!): Boolean
```

**Deprecated:** *Pass the characteristic value directly into[android.bluetooth.BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,byte[],int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int))*

Set the locally stored value of this characteristic.

See[setValue(byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#setValue(kotlin.ByteArray))for details.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:New value for this characteristic |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locally stored value has been set |

### setWriteType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWriteType(writeType: Int): Unit
```

Set the write type for this characteristic

Setting the write type of a characteristic determines how the[android.bluetooth.BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,byte[],int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeCharacteristic(android.bluetooth.BluetoothGattCharacteristic,%20kotlin.ByteArray,%20kotlin.Int))function write this characteristic.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `writeType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The write type to for this characteristic. Value is [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_DEFAULT:kotlin.Int), [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_NO_RESPONSE:kotlin.Int), or [android.bluetooth.BluetoothGattCharacteristic#WRITE_TYPE_SIGNED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic#WRITE_TYPE_SIGNED:kotlin.Int) |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
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

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothGattCharacteristic!>
```  

### mDescriptors

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mDescriptors: MutableList<BluetoothGattDescriptor!>!
```

List of descriptors included in this characteristic.
