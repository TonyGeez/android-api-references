# Control

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Control

Kotlin| [Java](Control.md) 
| --- | --- |

```
class Control : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.Control](Control.md) |

Represents a physical object that can be represented by a [ControlTemplate](../android.service.controls.templates/ControlTemplate.md) and whose properties may be modified through a [ControlAction](../android.service.controls.actions/ControlAction.md). The information is provided by a [ControlsProviderService](ControlsProviderService.md) and represents static information (not current status) about the device.

Each control needs a unique (per provider) identifier that is persistent across reboots of the system.

Each [Control](Control.md) will have a name, a subtitle and will optionally belong to a structure and zone. Some of these values are defined by the user and/or the [ControlsProviderService](ControlsProviderService.md) and will be used to display the control as well as group them for management.

Each object will have an associated [DeviceTypes](DeviceTypes.md). This will determine the icons and colors used to display it.

An [Intent](../android.content/Intent.md) linking to the provider Activity that expands on this [Control](Control.md) and allows for further actions should be provided.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) Builder class for [Control](Control.md) that contains state information. |
| | [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) Builder class for [Control](Control.md). |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_DISABLED](Control.md) The [Control](Control.md) is currently disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](Control.md) Used to indicate that there was a temporary error while loading the device state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NOT_FOUND](Control.md) The device corresponding to the [Control](Control.md) cannot be found or was removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](Control.md) Used to indicate that the state of the device was successfully retrieved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_UNKNOWN](Control.md) Reserved for use with the [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md), and while loading. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](Control.md))`()` <br /> |
| [PendingIntent](../android.app/PendingIntent.md) | [getAppIntent](Control.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getControlId](Control.md))`()` <br /> |
| --- | --- |
| [ControlTemplate](../android.service.controls.templates/ControlTemplate.md) | [getControlTemplate](Control.md))`()` <br /> |
| [ColorStateList](../android.content.res/ColorStateList.md)? | [getCustomColor](Control.md))`()` Optional color to be shown with the [Control](Control.md). |
| [Icon](../android.graphics.drawable/Icon.md)? | [getCustomIcon](Control.md))`()` Optional icon to be shown with the [Control](Control.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceType](Control.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](Control.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getStatusText](Control.md))`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getStructure](Control.md))`()` Optional top-level group to help define the [Control](Control.md)'s location, visible to the user. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getSubtitle](Control.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getTitle](Control.md))`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getZone](Control.md))`()` Optional group name to help define the [Control](Control.md)'s location within a structure, visible to the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthRequired](Control.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Control.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Control](Control.md)!\> | [CREATOR](Control.md) <br /> |

## Constants

### STATUS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_DISABLED: Int
```

The [Control](Control.md) is currently disabled. A default error message will be displayed in place of any custom text that was set through [StatefulBuilder.setStatusText](../android/service/controls/Control.StatefulBuilder.md)). 

 Value: 4

### STATUS_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ERROR: Int
```

Used to indicate that there was a temporary error while loading the device state. A default error message will be displayed in place of any custom text that was set through [StatefulBuilder.setStatusText](../android/service/controls/Control.StatefulBuilder.md)). 

 Value: 3

### STATUS_NOT_FOUND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_NOT_FOUND: Int
```

The device corresponding to the [Control](Control.md) cannot be found or was removed. The user will be alerted and directed to the application to resolve. 

 Value: 2

### STATUS_OK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_OK: Int
```

Used to indicate that the state of the device was successfully retrieved. This includes all scenarios where the device may have a warning for the user, such as "Lock jammed", or "Vacuum stuck". Any information for the user should be set through [StatefulBuilder.setStatusText](../android/service/controls/Control.StatefulBuilder.md)). 

 Value: 1

### STATUS_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_UNKNOWN: Int
```

Reserved for use with the [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md), and while loading. When state is requested via [ControlsProviderService.createPublisherFor](ControlsProviderService.md)), use other status codes to indicate the proper device state. 

 Value: 0

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getAppIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppIntent(): PendingIntent
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](../android.app/PendingIntent.md) | a [PendingIntent](../android.app/PendingIntent.md) linking to an Activity for the [Control](Control.md) This value cannot be`null`. |

### getControlId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlId(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the identifier for the [Control](Control.md) This value cannot be`null`. |

### getControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlTemplate(): ControlTemplate
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](../android.service.controls.templates/ControlTemplate.md) | instance of [ControlTemplate](../android.service.controls.templates/ControlTemplate.md), that defines how the [Control](Control.md) will behave and what interactions are available to the user This value cannot be`null`. |

### getCustomColor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomColor(): ColorStateList?
```

Optional color to be shown with the [Control](Control.md). It is highly recommended to let the system default the color unless the default is not suitable for the application.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ColorStateList](../android.content.res/ColorStateList.md)? | background color to use This value may be`null`. |

### getCustomIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomIcon(): Icon?
```

Optional icon to be shown with the [Control](Control.md). It is highly recommended to let the system default the icon unless the default icon is not suitable.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------|
| [Icon](../android.graphics.drawable/Icon.md)? | icon to show This value may be`null`. |

### getDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | type of device represented by this [Control](Control.md), used to determine the default icon and color Value is [android.service.controls.DeviceTypes#TYPE_GENERIC_ON_OFF](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_START_STOP](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_OPEN_CLOSE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_LOCK_UNLOCK](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_ARM_DISARM](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_TEMP_SETTING](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_VIEWSTREAM](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_UNKNOWN](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AC_HEATER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AC_UNIT](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AIR_FRESHENER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AIR_PURIFIER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_COFFEE_MAKER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DEHUMIDIFIER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DISPLAY](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_FAN](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HOOD](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HUMIDIFIER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_KETTLE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_LIGHT](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MICROWAVE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_OUTLET](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_RADIATOR](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_REMOTE_CONTROL](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SET_TOP](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_STANDMIXER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_STYLER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SWITCH](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_TV](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WATER_HEATER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DISHWASHER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DRYER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MOP](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MOWER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MULTICOOKER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SHOWER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SPRINKLER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WASHER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_VACUUM](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AWNING](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_BLINDS](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CLOSET](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CURTAIN](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DOOR](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DRAWER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GARAGE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GATE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_PERGOLA](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SHUTTER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WINDOW](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_VALVE](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_LOCK](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SECURITY_SYSTEM](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HEATER](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_REFRIGERATOR](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_THERMOSTAT](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CAMERA](DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DOORBELL](DeviceTypes.md), or [android.service.controls.DeviceTypes#TYPE_ROUTINE](DeviceTypes.md) |

### getStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | status of the [Control](Control.md), used to convey information about the attempt to fetch the current state Value is [android.service.controls.Control#STATUS_UNKNOWN](Control.md), [android.service.controls.Control#STATUS_OK](Control.md), [android.service.controls.Control#STATUS_NOT_FOUND](Control.md), [android.service.controls.Control#STATUS_ERROR](Control.md), or [android.service.controls.Control#STATUS_DISABLED](Control.md) |

### getStatusText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatusText(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | user-facing text description of the [Control](Control.md)'s status, describing its current state This value cannot be`null`. |

### getStructure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStructure(): CharSequence?
```

Optional top-level group to help define the [Control](Control.md)'s location, visible to the user. If not present, the application name will be used as the top-level group. A structure contains zones which contains controls.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | name of the structure containing the control This value may be`null`. |

### getSubtitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubtitle(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | additional information about the [Control](Control.md), to appear underneath the title This value cannot be`null`. |

### getTitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the user facing name of the [Control](Control.md) This value cannot be`null`. |

### getZone

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZone(): CharSequence?
```

Optional group name to help define the [Control](Control.md)'s location within a structure, visible to the user. A structure contains zones which contains controls.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | name of the zone containing the control This value may be`null`. |

### isAuthRequired

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAuthRequired(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the control can not be interacted with until the device is unlocked |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Control!>
```
