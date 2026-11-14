# BluetoothGattDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattDescriptor

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothGattDescriptor "View this page in Java") 

```
open class BluetoothGattDescriptor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#) |

Represents a Bluetooth GATT Descriptor

GATT Descriptors contain additional information and attributes of a GATT characteristic, [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic). They can be used to describe the characteristic's features or to control certain behaviours of the characteristic.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_READ:kotlin.Int) Descriptor read permission |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_READ_ENCRYPTED:kotlin.Int) Descriptor permission: Allow encrypted read operations |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_READ_ENCRYPTED_MITM:kotlin.Int) Descriptor permission: Allow reading with person-in-the-middle protection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_WRITE:kotlin.Int) Descriptor write permission |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_WRITE_ENCRYPTED:kotlin.Int) Descriptor permission: Allow encrypted writes |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_WRITE_ENCRYPTED_MITM:kotlin.Int) Descriptor permission: Allow encrypted writes with person-in-the-middle protection |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_WRITE_SIGNED:kotlin.Int) Descriptor permission: Allow signed write operations |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED_MITM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#PERMISSION_WRITE_SIGNED_MITM:kotlin.Int) Descriptor permission: Allow signed write operations with person-in-the-middle protection |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#BluetoothGattDescriptor(java.util.UUID,%20kotlin.Int))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`, `permissions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new BluetoothGattDescriptor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#describeContents())`()` <br /> |
| open [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)! | [getCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#getCharacteristic())`()` Returns the characteristic this descriptor belongs to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPermissions](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#getPermissions())`()` Returns the permissions for this descriptor. |
| open [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [getUuid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#getUuid())`()` Returns the UUID of this descriptor. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#getValue())`()` Returns the stored value for this descriptor |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#setValue(kotlin.ByteArray))`(`value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the locally stored value of this descriptor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothGattDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#CREATOR:android.os.Parcelable.Creator) <br /> |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [DISABLE_NOTIFICATION_VALUE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#DISABLE_NOTIFICATION_VALUE:kotlin.ByteArray) Value used to disable notifications or indications |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [ENABLE_INDICATION_VALUE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#ENABLE_INDICATION_VALUE:kotlin.ByteArray) Value used to enable indication for a client configuration descriptor |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [ENABLE_NOTIFICATION_VALUE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattDescriptor#ENABLE_NOTIFICATION_VALUE:kotlin.ByteArray) Value used to enable notification for a client configuration descriptor |

## Constants

### PERMISSION_READ

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ: Int
```

Descriptor read permission 

 Value: 1

### PERMISSION_READ_ENCRYPTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ_ENCRYPTED: Int
```

Descriptor permission: Allow encrypted read operations 

 Value: 2

### PERMISSION_READ_ENCRYPTED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_READ_ENCRYPTED_MITM: Int
```

Descriptor permission: Allow reading with person-in-the-middle protection 

 Value: 4

### PERMISSION_WRITE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE: Int
```

Descriptor write permission 

 Value: 16

### PERMISSION_WRITE_ENCRYPTED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_ENCRYPTED: Int
```

Descriptor permission: Allow encrypted writes 

 Value: 32

### PERMISSION_WRITE_ENCRYPTED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_ENCRYPTED_MITM: Int
```

Descriptor permission: Allow encrypted writes with person-in-the-middle protection 

 Value: 64

### PERMISSION_WRITE_SIGNED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_SIGNED: Int
```

Descriptor permission: Allow signed write operations 

 Value: 128

### PERMISSION_WRITE_SIGNED_MITM

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERMISSION_WRITE_SIGNED_MITM: Int
```

Descriptor permission: Allow signed write operations with person-in-the-middle protection 

 Value: 256

## Public constructors

### BluetoothGattDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothGattDescriptor(
    uuid: UUID!, 
    permissions: Int)
```

Create a new BluetoothGattDescriptor.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!:The UUID for this descriptor |
| `permissions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Permissions for this descriptor |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristic(): BluetoothGattCharacteristic!
```

Returns the characteristic this descriptor belongs to.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)! | The characteristic. |

### getPermissions

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermissions(): Int
```

Returns the permissions for this descriptor.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Permissions of this descriptor |

### getUuid

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUuid(): UUID!
```

Returns the UUID of this descriptor.

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | UUID of this descriptor |

### getValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): ByteArray!
```

**Deprecated:** *Use [BluetoothGatt.readDescriptor(BluetoothGattDescriptor)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readDescriptor(android.bluetooth.BluetoothGattDescriptor))instead*

Returns the stored value for this descriptor

This function returns the stored value for this descriptor as retrieved by calling [android.bluetooth.BluetoothGatt#readDescriptor](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#readDescriptor(android.bluetooth.BluetoothGattDescriptor)). The cached value of the descriptor is updated as a result of a descriptor read operation.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | Cached value of the descriptor |

### setValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValue(value: ByteArray!): Boolean
```

**Deprecated:** *Pass the descriptor value directly into[android.bluetooth.BluetoothGatt#writeDescriptor(android.bluetooth.BluetoothGattDescriptor,byte[])](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt#writeDescriptor(android.bluetooth.BluetoothGattDescriptor,%20kotlin.ByteArray))*

Updates the locally stored value of this descriptor.

This function modifies the locally stored cached value of this descriptor. To send the value to the remote device, call android.bluetooth.BluetoothGatt#writeDescriptor to send the value to the remote device.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:New value for this descriptor |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locally stored value has been set, false if the requested value could not be stored locally. |

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
static val CREATOR: Parcelable.Creator<BluetoothGattDescriptor!>
```  

### DISABLE_NOTIFICATION_VALUE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISABLE_NOTIFICATION_VALUE: ByteArray!
```

Value used to disable notifications or indications 

### ENABLE_INDICATION_VALUE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENABLE_INDICATION_VALUE: ByteArray!
```

Value used to enable indication for a client configuration descriptor 

### ENABLE_NOTIFICATION_VALUE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENABLE_NOTIFICATION_VALUE: ByteArray!
```

Value used to enable notification for a client configuration descriptor
