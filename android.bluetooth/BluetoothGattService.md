# BluetoothGattService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattService

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothGattService "View this page in Java") 

```
open class BluetoothGattService : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#) |

Represents a Bluetooth GATT Service

Gatt Service contains a collection of [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic), as well as referenced services.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#SERVICE_TYPE_PRIMARY:kotlin.Int) Primary service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_SECONDARY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#SERVICE_TYPE_SECONDARY:kotlin.Int) Secondary service (included by primary services) |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#BluetoothGattService(java.util.UUID,%20kotlin.Int))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`, `serviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new BluetoothGattService. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#addCharacteristic(android.bluetooth.BluetoothGattCharacteristic))`(`characteristic:` ` [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!`)` Add a characteristic to this service. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#addService(android.bluetooth.BluetoothGattService))`(`service:` ` [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!`)` Add an included service to this service. |
| open [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)! | [getCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getCharacteristic(java.util.UUID))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`)` Returns a characteristic with a given UUID out of the list of characteristics offered by this service. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!\>! | [getCharacteristics](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getCharacteristics())`()` Returns a list of characteristics included in this service. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!\>! | [getIncludedServices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getIncludedServices())`()` Get the list of included GATT services for this service. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInstanceId](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getInstanceId())`()` Returns the instance ID for this service |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getType())`()` Get the type of this service (primary/secondary) |
| open [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [getUuid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getUuid())`()` Returns the UUID of this service |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#CREATOR:android.os.Parcelable.Creator) <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!\>! | [mCharacteristics](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#mCharacteristics:kotlin.collections.MutableList) List of characteristics included in this service. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!\>! | [mIncludedServices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#mIncludedServices:kotlin.collections.MutableList) List of included services for this service. |

## Constants

### SERVICE_TYPE_PRIMARY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_PRIMARY: Int
```

Primary service 

 Value: 0

### SERVICE_TYPE_SECONDARY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_SECONDARY: Int
```

Secondary service (included by primary services) 

 Value: 1

## Public constructors

### BluetoothGattService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothGattService(
    uuid: UUID!, 
    serviceType: Int)
```

Create a new BluetoothGattService.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!:The UUID for this service |
| `serviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of this service, [android.bluetooth.BluetoothGattService#SERVICE_TYPE_PRIMARY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#SERVICE_TYPE_PRIMARY:kotlin.Int) or [android.bluetooth.BluetoothGattService#SERVICE_TYPE_SECONDARY](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#SERVICE_TYPE_SECONDARY:kotlin.Int) |

## Public methods

### addCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCharacteristic(characteristic: BluetoothGattCharacteristic!): Boolean
```

Add a characteristic to this service.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `characteristic` | [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!:The characteristics to be added |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the characteristic was added to the service |

### addService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addService(service: BluetoothGattService!): Boolean
```

Add an included service to this service.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!:The service to be added |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the included service was added to the service |

### getCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristic(uuid: UUID!): BluetoothGattCharacteristic!
```

Returns a characteristic with a given UUID out of the list of characteristics offered by this service.

This is a convenience function to allow access to a given characteristic without enumerating over the list returned by [getCharacteristics](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#getCharacteristics())manually.

If a remote service offers multiple characteristics with the same UUID, the first instance of a characteristic with the given UUID is returned.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)! | GATT characteristic object or null if no characteristic with the given UUID was found. |

### getCharacteristics

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristics(): MutableList<BluetoothGattCharacteristic!>!
```

Returns a list of characteristics included in this service.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattCharacteristic](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCharacteristic)!>! | Characteristics included in this service |

### getIncludedServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIncludedServices(): MutableList<BluetoothGattService!>!
```

Get the list of included GATT services for this service.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattService](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattService#)!>! | List of included services or empty list if no included services were discovered. |

### getInstanceId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInstanceId(): Int
```

Returns the instance ID for this service

If a remote device offers multiple services with the same UUID (ex. multiple battery services for different batteries), the instance ID is used to distinguish services.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Instance ID of this service |

### getType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

Get the type of this service (primary/secondary) 

### getUuid

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUuid(): UUID!
```

Returns the UUID of this service

| Return ||
|------------------------------------------------------------------------------|----------------------|
| [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | UUID of this service |

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
static val CREATOR: Parcelable.Creator<BluetoothGattService!>
```  

### mCharacteristics

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mCharacteristics: MutableList<BluetoothGattCharacteristic!>!
```

List of characteristics included in this service. 

### mIncludedServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mIncludedServices: MutableList<BluetoothGattService!>!
```

List of included services for this service.
