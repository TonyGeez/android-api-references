# Control

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Control

Kotlin| [Java](../android/service/controls/Control.md) 
| --- | --- |

```
class Control : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.controls.Control](../android/service/controls/Control.md) |

Represents a physical object that can be represented by a [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) and whose properties may be modified through a [ControlAction](../android/service/controls/actions/ControlAction.md). The information is provided by a [ControlsProviderService](../android/service/controls/ControlsProviderService.md) and represents static information (not current status) about the device.

Each control needs a unique (per provider) identifier that is persistent across reboots of the system.

Each [Control](../android/service/controls/Control.md) will have a name, a subtitle and will optionally belong to a structure and zone. Some of these values are defined by the user and/or the [ControlsProviderService](../android/service/controls/ControlsProviderService.md) and will be used to display the control as well as group them for management.

Each object will have an associated [DeviceTypes](../android/service/controls/DeviceTypes.md). This will determine the icons and colors used to display it.

An [Intent](../android/content/Intent.md) linking to the provider Activity that expands on this [Control](../android/service/controls/Control.md) and allows for further actions should be provided.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [StatefulBuilder](../android/service/controls/Control.StatefulBuilder.md) Builder class for [Control](../android/service/controls/Control.md) that contains state information. |
| | [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md) Builder class for [Control](../android/service/controls/Control.md). |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_DISABLED](../android/service/controls/Control.md) The [Control](../android/service/controls/Control.md) is currently disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](../android/service/controls/Control.md) Used to indicate that there was a temporary error while loading the device state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NOT_FOUND](../android/service/controls/Control.md) The device corresponding to the [Control](../android/service/controls/Control.md) cannot be found or was removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](../android/service/controls/Control.md) Used to indicate that the state of the device was successfully retrieved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_UNKNOWN](../android/service/controls/Control.md) Reserved for use with the [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md), and while loading. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/controls/Control.md))`()` <br /> |
| [PendingIntent](../android/app/PendingIntent.md) | [getAppIntent](../android/service/controls/Control.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getControlId](../android/service/controls/Control.md))`()` <br /> |
| --- | --- |
| [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | [getControlTemplate](../android/service/controls/Control.md))`()` <br /> |
| [ColorStateList](../android/content/res/ColorStateList.md)? | [getCustomColor](../android/service/controls/Control.md))`()` Optional color to be shown with the [Control](../android/service/controls/Control.md). |
| [Icon](../android/graphics/drawable/Icon.md)? | [getCustomIcon](../android/service/controls/Control.md))`()` Optional icon to be shown with the [Control](../android/service/controls/Control.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceType](../android/service/controls/Control.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](../android/service/controls/Control.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getStatusText](../android/service/controls/Control.md))`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getStructure](../android/service/controls/Control.md))`()` Optional top-level group to help define the [Control](../android/service/controls/Control.md)'s location, visible to the user. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getSubtitle](../android/service/controls/Control.md))`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getTitle](../android/service/controls/Control.md))`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getZone](../android/service/controls/Control.md))`()` Optional group name to help define the [Control](../android/service/controls/Control.md)'s location within a structure, visible to the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthRequired](../android/service/controls/Control.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/controls/Control.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Control](../android/service/controls/Control.md)!\> | [CREATOR](../android/service/controls/Control.md) <br /> |

## Constants

### STATUS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_DISABLED: Int
```

The [Control](../android/service/controls/Control.md) is currently disabled. A default error message will be displayed in place of any custom text that was set through [StatefulBuilder.setStatusText](../android/service/controls/Control.StatefulBuilder.md)). 

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

The device corresponding to the [Control](../android/service/controls/Control.md) cannot be found or was removed. The user will be alerted and directed to the application to resolve. 

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

Reserved for use with the [StatelessBuilder](../android/service/controls/Control.StatelessBuilder.md), and while loading. When state is requested via [ControlsProviderService.createPublisherFor](../android/service/controls/ControlsProviderService.md)), use other status codes to indicate the proper device state. 

 Value: 0

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAppIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppIntent(): PendingIntent
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](../android/app/PendingIntent.md) | a [PendingIntent](../android/app/PendingIntent.md) linking to an Activity for the [Control](../android/service/controls/Control.md) This value cannot be`null`. |

### getControlId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlId(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the identifier for the [Control](../android/service/controls/Control.md) This value cannot be`null`. |

### getControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlTemplate(): ControlTemplate
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](../android/service/controls/templates/ControlTemplate.md) | instance of [ControlTemplate](../android/service/controls/templates/ControlTemplate.md), that defines how the [Control](../android/service/controls/Control.md) will behave and what interactions are available to the user This value cannot be`null`. |

### getCustomColor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomColor(): ColorStateList?
```

Optional color to be shown with the [Control](../android/service/controls/Control.md). It is highly recommended to let the system default the color unless the default is not suitable for the application.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md)? | background color to use This value may be`null`. |

### getCustomIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomIcon(): Icon?
```

Optional icon to be shown with the [Control](../android/service/controls/Control.md). It is highly recommended to let the system default the icon unless the default icon is not suitable.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------|
| [Icon](../android/graphics/drawable/Icon.md)? | icon to show This value may be`null`. |

### getDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | type of device represented by this [Control](../android/service/controls/Control.md), used to determine the default icon and color Value is [android.service.controls.DeviceTypes#TYPE_GENERIC_ON_OFF](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_START_STOP](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_OPEN_CLOSE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_LOCK_UNLOCK](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_ARM_DISARM](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_TEMP_SETTING](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GENERIC_VIEWSTREAM](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_UNKNOWN](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AC_HEATER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AC_UNIT](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AIR_FRESHENER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AIR_PURIFIER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_COFFEE_MAKER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DEHUMIDIFIER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DISPLAY](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_FAN](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HOOD](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HUMIDIFIER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_KETTLE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_LIGHT](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MICROWAVE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_OUTLET](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_RADIATOR](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_REMOTE_CONTROL](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SET_TOP](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_STANDMIXER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_STYLER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SWITCH](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_TV](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WATER_HEATER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DISHWASHER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DRYER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MOP](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MOWER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_MULTICOOKER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SHOWER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SPRINKLER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WASHER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_VACUUM](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_AWNING](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_BLINDS](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CLOSET](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CURTAIN](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DOOR](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DRAWER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GARAGE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_GATE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_PERGOLA](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SHUTTER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_WINDOW](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_VALVE](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_LOCK](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_SECURITY_SYSTEM](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_HEATER](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_REFRIGERATOR](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_THERMOSTAT](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_CAMERA](../android/service/controls/DeviceTypes.md), [android.service.controls.DeviceTypes#TYPE_DOORBELL](../android/service/controls/DeviceTypes.md), or [android.service.controls.DeviceTypes#TYPE_ROUTINE](../android/service/controls/DeviceTypes.md) |

### getStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | status of the [Control](../android/service/controls/Control.md), used to convey information about the attempt to fetch the current state Value is [android.service.controls.Control#STATUS_UNKNOWN](../android/service/controls/Control.md), [android.service.controls.Control#STATUS_OK](../android/service/controls/Control.md), [android.service.controls.Control#STATUS_NOT_FOUND](../android/service/controls/Control.md), [android.service.controls.Control#STATUS_ERROR](../android/service/controls/Control.md), or [android.service.controls.Control#STATUS_DISABLED](../android/service/controls/Control.md) |

### getStatusText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatusText(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | user-facing text description of the [Control](../android/service/controls/Control.md)'s status, describing its current state This value cannot be`null`. |

### getStructure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStructure(): CharSequence?
```

Optional top-level group to help define the [Control](../android/service/controls/Control.md)'s location, visible to the user. If not present, the application name will be used as the top-level group. A structure contains zones which contains controls.

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
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | additional information about the [Control](../android/service/controls/Control.md), to appear underneath the title This value cannot be`null`. |

### getTitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the user facing name of the [Control](../android/service/controls/Control.md) This value cannot be`null`. |

### getZone

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZone(): CharSequence?
```

Optional group name to help define the [Control](../android/service/controls/Control.md)'s location within a structure, visible to the user. A structure contains zones which contains controls.

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Control!>
```
