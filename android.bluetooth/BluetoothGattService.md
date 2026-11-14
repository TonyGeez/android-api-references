# BluetoothGattService

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothGattService

Kotlin| [Java](../android/bluetooth/BluetoothGattService.md) 
| --- | --- |

```
open class BluetoothGattService : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothGattService](../android/bluetooth/BluetoothGattService.md) |

Represents a Bluetooth GATT Service

Gatt Service contains a collection of [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md), as well as referenced services.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_PRIMARY](../android/bluetooth/BluetoothGattService.md) Primary service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_SECONDARY](../android/bluetooth/BluetoothGattService.md) Secondary service (included by primary services) |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothGattService](../android/bluetooth/BluetoothGattService.md))`(`uuid:` ` [UUID](../java/util/UUID.md)!`, `serviceType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new BluetoothGattService. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addCharacteristic](../android/bluetooth/BluetoothGattService.md))`(`characteristic:` ` [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!`)` Add a characteristic to this service. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addService](../android/bluetooth/BluetoothGattService.md))`(`service:` ` [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!`)` Add an included service to this service. |
| open [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)! | [getCharacteristic](../android/bluetooth/BluetoothGattService.md))`(`uuid:` ` [UUID](../java/util/UUID.md)!`)` Returns a characteristic with a given UUID out of the list of characteristics offered by this service. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!\>! | [getCharacteristics](../android/bluetooth/BluetoothGattService.md))`()` Returns a list of characteristics included in this service. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!\>! | [getIncludedServices](../android/bluetooth/BluetoothGattService.md))`()` Get the list of included GATT services for this service. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInstanceId](../android/bluetooth/BluetoothGattService.md))`()` Returns the instance ID for this service |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/bluetooth/BluetoothGattService.md))`()` Get the type of this service (primary/secondary) |
| open [UUID](../java/util/UUID.md)! | [getUuid](../android/bluetooth/BluetoothGattService.md))`()` Returns the UUID of this service |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/bluetooth/BluetoothGattService.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!\> | [CREATOR](../android/bluetooth/BluetoothGattService.md) <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!\>! | [mCharacteristics](../android/bluetooth/BluetoothGattService.md) List of characteristics included in this service. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!\>! | [mIncludedServices](../android/bluetooth/BluetoothGattService.md) List of included services for this service. |
| --- | --- |

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
| `uuid` | [UUID](../java/util/UUID.md)!:The UUID for this service |
| `serviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of this service, [android.bluetooth.BluetoothGattService#SERVICE_TYPE_PRIMARY](../android/bluetooth/BluetoothGattService.md) or [android.bluetooth.BluetoothGattService#SERVICE_TYPE_SECONDARY](../android/bluetooth/BluetoothGattService.md) |

## Public methods

### addCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCharacteristic(characteristic: BluetoothGattCharacteristic!): Boolean
```

Add a characteristic to this service.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `characteristic` | [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!:The characteristics to be added |

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
| `service` | [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!:The service to be added |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the included service was added to the service |

### getCharacteristic

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristic(uuid: UUID!): BluetoothGattCharacteristic!
```

Returns a characteristic with a given UUID out of the list of characteristics offered by this service.

This is a convenience function to allow access to a given characteristic without enumerating over the list returned by [getCharacteristics](../android/bluetooth/BluetoothGattService.md))manually.

If a remote service offers multiple characteristics with the same UUID, the first instance of a characteristic with the given UUID is returned.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)! | GATT characteristic object or null if no characteristic with the given UUID was found. |

### getCharacteristics

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacteristics(): MutableList<BluetoothGattCharacteristic!>!
```

Returns a list of characteristics included in this service.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattCharacteristic](../android/bluetooth/BluetoothGattCharacteristic.md)!>! | Characteristics included in this service |

### getIncludedServices

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIncludedServices(): MutableList<BluetoothGattService!>!
```

Get the list of included GATT services for this service.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothGattService](../android/bluetooth/BluetoothGattService.md)!>! | List of included services or empty list if no included services were discovered. |

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
| [UUID](../java/util/UUID.md)! | UUID of this service |

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
