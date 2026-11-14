# BluetoothGattDescriptor

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattDescriptor

Kotlin| [Java](../android/bluetooth/BluetoothGattDescriptor.md) 
| --- | --- |

```
open class BluetoothGattDescriptor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattDescriptor](../android/bluetooth/BluetoothGattDescriptor.md) |

Represents a Bluetooth GATT Descriptor

GATT Descriptors contain additional information and attributes of a GATT characteristic, [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md). They can be used to describe the characteristic's features or to control certain behaviours of the characteristic.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor read permission |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow encrypted read operations |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_READ_ENCRYPTED_MITM](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow reading with person-in-the-middle protection |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor write permission |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow encrypted writes |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_ENCRYPTED_MITM](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow encrypted writes with person-in-the-middle protection |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow signed write operations |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERMISSION_WRITE_SIGNED_MITM](../android/bluetooth/BluetoothGattDescriptor.md) Descriptor permission: Allow signed write operations with person-in-the-middle protection |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothGattDescriptor](../android/bluetooth/BluetoothGattDescriptor.md))`(`uuid:` ` [UUID](../java/util/UUID.md)!`, `permissions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new BluetoothGattDescriptor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/bluetooth/BluetoothGattDescriptor.md))`()` <br /> |
| open [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)! | [getCharacteristic](../android/bluetooth/BluetoothGattDescriptor.md))`()` Returns the characteristic this descriptor belongs to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPermissions](../android/bluetooth/BluetoothGattDescriptor.md))`()` Returns the permissions for this descriptor. |
| --- | --- |
| open [UUID](../java/util/UUID.md)! | [getUuid](../android/bluetooth/BluetoothGattDescriptor.md))`()` Returns the UUID of this descriptor. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getValue](../android/bluetooth/BluetoothGattDescriptor.md))`()` Returns the stored value for this descriptor |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setValue](../android/bluetooth/BluetoothGattDescriptor.md))`(`value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the locally stored value of this descriptor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/bluetooth/BluetoothGattDescriptor.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothGattDescriptor](../android/bluetooth/BluetoothGattDescriptor.md)!\> | [CREATOR](../android/bluetooth/BluetoothGattDescriptor.md) <br /> |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [DISABLE_NOTIFICATION_VALUE](../android/bluetooth/BluetoothGattDescriptor.md) Value used to disable notifications or indications |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [ENABLE_INDICATION_VALUE](../android/bluetooth/BluetoothGattDescriptor.md) Value used to enable indication for a client configuration descriptor |
| --- | --- |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [ENABLE_NOTIFICATION_VALUE](../android/bluetooth/BluetoothGattDescriptor.md) Value used to enable notification for a client configuration descriptor |

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
| `uuid` | [UUID](../java/util/UUID.md)!:The UUID for this descriptor |
| `permissions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Permissions for this descriptor |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristic(): BluetoothGattCharacteristic!
```

Returns the characteristic this descriptor belongs to.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)! | The characteristic. |

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
| [UUID](../java/util/UUID.md)! | UUID of this descriptor |

### getValue

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): ByteArray!
```

**Deprecated:** *Use [BluetoothGatt.readDescriptor(BluetoothGattDescriptor)](../android/bluetooth/BluetoothGatt.md))instead*

Returns the stored value for this descriptor

This function returns the stored value for this descriptor as retrieved by calling [android.bluetooth.BluetoothGatt#readDescriptor](../android/bluetooth/BluetoothGatt.md)). The cached value of the descriptor is updated as a result of a descriptor read operation.

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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
