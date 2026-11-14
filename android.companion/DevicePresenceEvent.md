# DevicePresenceEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DevicePresenceEvent

Kotlin| [Java](https://developer.android.com/reference/android/companion/DevicePresenceEvent "View this page in Java") 
| --- | --- |

```
class DevicePresenceEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.DevicePresenceEvent](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#) |

Event for observing device presence.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_ASSOCIATION_REMOVED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_ASSOCIATION_REMOVED:kotlin.Int) A companion app will receives the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))with this event when the [AssociationInfo](https://developer.android.com/reference/kotlin/android/companion/AssociationInfo) is removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_BLE_APPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BLE_APPEARED:kotlin.Int) Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the device comes into BLE range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_BLE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BLE_DISAPPEARED:kotlin.Int) Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the device is no longer in BLE range. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_BT_CONNECTED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BT_CONNECTED:kotlin.Int) Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event when the bluetooth device is connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_BT_DISCONNECTED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BT_DISCONNECTED:kotlin.Int) Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the bluetooth device is disconnected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_SELF_MANAGED_APPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_SELF_MANAGED_APPEARED:kotlin.Int) A companion app for a self-managed device will receive the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))if it reports that a device has appeared on its own. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_SELF_MANAGED_DISAPPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_SELF_MANAGED_DISAPPEARED:kotlin.Int) A companion app for a self-managed device will receive the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))if it reports that a device has disappeared on its own. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_ASSOCIATION](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#NO_ASSOCIATION:kotlin.Int) Indicate observing device presence base on the ParcelUuid but not association id. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DevicePresenceEvent](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#DevicePresenceEvent(kotlin.Int,%20kotlin.Int,%20android.os.ParcelUuid))`(`associationId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uuid:` ` [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)?`)` Create a new DevicePresenceEvent. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAssociationId](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#getAssociationId())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvent](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#getEvent())`()` <br /> |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getUuid](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#getUuid())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [DevicePresenceEvent](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EVENT_ASSOCIATION_REMOVED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ASSOCIATION_REMOVED: Int
```

A companion app will receives the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))with this event when the [AssociationInfo](https://developer.android.com/reference/kotlin/android/companion/AssociationInfo) is removed. 

 Value: 6

### EVENT_BLE_APPEARED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_BLE_APPEARED: Int
```

Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the device comes into BLE range. 

 Value: 0

### EVENT_BLE_DISAPPEARED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_BLE_DISAPPEARED: Int
```

Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the device is no longer in BLE range. 

 Value: 1

### EVENT_BT_CONNECTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_BT_CONNECTED: Int
```

Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event when the bluetooth device is connected. 

 Value: 2

### EVENT_BT_DISCONNECTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_BT_DISCONNECTED: Int
```

Companion app receives [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))callback with this event if the bluetooth device is disconnected. 

 Value: 3

### EVENT_SELF_MANAGED_APPEARED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_SELF_MANAGED_APPEARED: Int
```

A companion app for a self-managed device will receive the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))if it reports that a device has appeared on its own. 

 Value: 4

### EVENT_SELF_MANAGED_DISAPPEARED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_SELF_MANAGED_DISAPPEARED: Int
```

A companion app for a self-managed device will receive the callback [CompanionDeviceService.onDevicePresenceEvent(DevicePresenceEvent)](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService#onDevicePresenceEvent(android.companion.DevicePresenceEvent))if it reports that a device has disappeared on its own. 

 Value: 5

### NO_ASSOCIATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_ASSOCIATION: Int
```

Indicate observing device presence base on the ParcelUuid but not association id. 

 Value: -1

## Public constructors

### DevicePresenceEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DevicePresenceEvent(
    associationId: Int, 
    event: Int, 
    uuid: ParcelUuid?)
```

Create a new DevicePresenceEvent.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.companion.DevicePresenceEvent#EVENT_BLE_APPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BLE_APPEARED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_BLE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BLE_DISAPPEARED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_BT_CONNECTED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BT_CONNECTED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_BT_DISCONNECTED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_BT_DISCONNECTED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_SELF_MANAGED_APPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_SELF_MANAGED_APPEARED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_SELF_MANAGED_DISAPPEARED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_SELF_MANAGED_DISAPPEARED:kotlin.Int), [android.companion.DevicePresenceEvent#EVENT_ASSOCIATION_REMOVED](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#EVENT_ASSOCIATION_REMOVED:kotlin.Int), android.companion.DevicePresenceEvent.EVENT_SELF_MANAGED_NEARBY, or android.companion.DevicePresenceEvent.EVENT_SELF_MANAGED_NOT_NEARBY |
| `uuid` | [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getAssociationId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAssociationId(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The association id has been used to observe device presence. Caller will receive the valid association id if only if using [ObservingDevicePresenceRequest.Builder.setAssociationId(int)](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest.Builder#setAssociationId(kotlin.Int)), otherwise return [NO_ASSOCIATION](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent#NO_ASSOCIATION:kotlin.Int). |

**See Also**

- [android.companion.ObservingDevicePresenceRequest.Builder#setAssociationId(int)](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest.Builder#setAssociationId(kotlin.Int)) 

### getEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEvent(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Associated companion device's event. |

### getUuid

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUuid(): ParcelUuid?
```

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | The ParcelUuid has been used to observe device presence. Caller will receive the ParcelUuid if only if using [ObservingDevicePresenceRequest.Builder.setUuid(ParcelUuid)](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest.Builder#setUuid(android.os.ParcelUuid)), otherwise return null. |

**See Also**

- [android.companion.ObservingDevicePresenceRequest.Builder#setUuid(ParcelUuid)](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest.Builder#setUuid(android.os.ParcelUuid)) 

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<DevicePresenceEvent!>
```
