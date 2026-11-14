# Control

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Control

Kotlin| [Java](https://developer.android.com/reference/android/service/controls/Control "View this page in Java") 

```
class Control : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.controls.Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) |

Represents a physical object that can be represented by a [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) and whose properties may be modified through a [ControlAction](https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction). The information is provided by a [ControlsProviderService](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService) and represents static information (not current status) about the device.

Each control needs a unique (per provider) identifier that is persistent across reboots of the system.

Each [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) will have a name, a subtitle and will optionally belong to a structure and zone. Some of these values are defined by the user and/or the [ControlsProviderService](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService) and will be used to display the control as well as group them for management.

Each object will have an associated [DeviceTypes](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes). This will determine the icons and colors used to display it.

An [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) linking to the provider Activity that expands on this [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) and allows for further actions should be provided.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [StatefulBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder) Builder class for [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) that contains state information. |
| | [StatelessBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatelessBuilder) Builder class for [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#). |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_DISABLED](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_DISABLED:kotlin.Int) The [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) is currently disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_ERROR:kotlin.Int) Used to indicate that there was a temporary error while loading the device state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NOT_FOUND](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_NOT_FOUND:kotlin.Int) The device corresponding to the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) cannot be found or was removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_OK:kotlin.Int) Used to indicate that the state of the device was successfully retrieved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_UNKNOWN:kotlin.Int) Reserved for use with the [StatelessBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatelessBuilder), and while loading. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/controls/Control#describeContents())`()` <br /> |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | [getAppIntent](https://developer.android.com/reference/kotlin/android/service/controls/Control#getAppIntent())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getControlId](https://developer.android.com/reference/kotlin/android/service/controls/Control#getControlId())`()` <br /> |
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | [getControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/Control#getControlTemplate())`()` <br /> |
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | [getCustomColor](https://developer.android.com/reference/kotlin/android/service/controls/Control#getCustomColor())`()` Optional color to be shown with the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#). |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | [getCustomIcon](https://developer.android.com/reference/kotlin/android/service/controls/Control#getCustomIcon())`()` Optional icon to be shown with the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceType](https://developer.android.com/reference/kotlin/android/service/controls/Control#getDeviceType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](https://developer.android.com/reference/kotlin/android/service/controls/Control#getStatus())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getStatusText](https://developer.android.com/reference/kotlin/android/service/controls/Control#getStatusText())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getStructure](https://developer.android.com/reference/kotlin/android/service/controls/Control#getStructure())`()` Optional top-level group to help define the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)'s location, visible to the user. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getSubtitle](https://developer.android.com/reference/kotlin/android/service/controls/Control#getSubtitle())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getTitle](https://developer.android.com/reference/kotlin/android/service/controls/Control#getTitle())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getZone](https://developer.android.com/reference/kotlin/android/service/controls/Control#getZone())`()` Optional group name to help define the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)'s location within a structure, visible to the user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAuthRequired](https://developer.android.com/reference/kotlin/android/service/controls/Control#isAuthRequired())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/controls/Control#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/controls/Control#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STATUS_DISABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_DISABLED: Int
```

The [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) is currently disabled. A default error message will be displayed in place of any custom text that was set through [StatefulBuilder.setStatusText](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder#setStatusText(kotlin.CharSequence)). 

 Value: 4

### STATUS_ERROR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ERROR: Int
```

Used to indicate that there was a temporary error while loading the device state. A default error message will be displayed in place of any custom text that was set through [StatefulBuilder.setStatusText](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder#setStatusText(kotlin.CharSequence)). 

 Value: 3

### STATUS_NOT_FOUND

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_NOT_FOUND: Int
```

The device corresponding to the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) cannot be found or was removed. The user will be alerted and directed to the application to resolve. 

 Value: 2

### STATUS_OK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_OK: Int
```

Used to indicate that the state of the device was successfully retrieved. This includes all scenarios where the device may have a warning for the user, such as "Lock jammed", or "Vacuum stuck". Any information for the user should be set through [StatefulBuilder.setStatusText](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatefulBuilder#setStatusText(kotlin.CharSequence)). 

 Value: 1

### STATUS_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_UNKNOWN: Int
```

Reserved for use with the [StatelessBuilder](https://developer.android.com/reference/kotlin/android/service/controls/Control.StatelessBuilder), and while loading. When state is requested via [ControlsProviderService.createPublisherFor](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService#createPublisherFor(kotlin.collections.MutableList)), use other status codes to indicate the proper device state. 

 Value: 0

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAppIntent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppIntent(): PendingIntent
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) | a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) linking to an Activity for the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) This value cannot be`null`. |

### getControlId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlId(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the identifier for the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) This value cannot be`null`. |

### getControlTemplate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getControlTemplate(): ControlTemplate
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate) | instance of [ControlTemplate](https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate), that defines how the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) will behave and what interactions are available to the user This value cannot be`null`. |

### getCustomColor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomColor(): ColorStateList?
```

Optional color to be shown with the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#). It is highly recommended to let the system default the color unless the default is not suitable for the application.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | background color to use This value may be`null`. |

### getCustomIcon

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomIcon(): Icon?
```

Optional icon to be shown with the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#). It is highly recommended to let the system default the icon unless the default icon is not suitable.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)? | icon to show This value may be`null`. |

### getDeviceType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceType(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | type of device represented by this [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#), used to determine the default icon and color Value is [android.service.controls.DeviceTypes#TYPE_GENERIC_ON_OFF](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_ON_OFF:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_START_STOP](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_START_STOP:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_OPEN_CLOSE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_OPEN_CLOSE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_LOCK_UNLOCK](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_LOCK_UNLOCK:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_ARM_DISARM](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_ARM_DISARM:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_TEMP_SETTING](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_TEMP_SETTING:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GENERIC_VIEWSTREAM](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GENERIC_VIEWSTREAM:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_UNKNOWN:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_AC_HEATER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_AC_HEATER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_AC_UNIT](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_AC_UNIT:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_AIR_FRESHENER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_AIR_FRESHENER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_AIR_PURIFIER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_AIR_PURIFIER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_COFFEE_MAKER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_COFFEE_MAKER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DEHUMIDIFIER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DEHUMIDIFIER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DISPLAY](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DISPLAY:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_FAN](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_FAN:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_HOOD](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_HOOD:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_HUMIDIFIER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_HUMIDIFIER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_KETTLE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_KETTLE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_LIGHT](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_LIGHT:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_MICROWAVE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_MICROWAVE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_OUTLET](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_OUTLET:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_RADIATOR](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_RADIATOR:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_REMOTE_CONTROL](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_REMOTE_CONTROL:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SET_TOP](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SET_TOP:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_STANDMIXER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_STANDMIXER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_STYLER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_STYLER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SWITCH](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SWITCH:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_TV](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_TV:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_WATER_HEATER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_WATER_HEATER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DISHWASHER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DISHWASHER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DRYER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DRYER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_MOP](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_MOP:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_MOWER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_MOWER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_MULTICOOKER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_MULTICOOKER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SHOWER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SHOWER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SPRINKLER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SPRINKLER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_WASHER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_WASHER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_VACUUM](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_VACUUM:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_AWNING](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_AWNING:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_BLINDS](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_BLINDS:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_CLOSET](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_CLOSET:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_CURTAIN](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_CURTAIN:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DOOR](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DOOR:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DRAWER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DRAWER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GARAGE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GARAGE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_GATE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_GATE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_PERGOLA](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_PERGOLA:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SHUTTER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SHUTTER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_WINDOW](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_WINDOW:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_VALVE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_VALVE:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_LOCK](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_LOCK:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_SECURITY_SYSTEM](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_SECURITY_SYSTEM:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_HEATER](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_HEATER:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_REFRIGERATOR](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_REFRIGERATOR:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_THERMOSTAT](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_THERMOSTAT:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_CAMERA](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_CAMERA:kotlin.Int), [android.service.controls.DeviceTypes#TYPE_DOORBELL](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_DOORBELL:kotlin.Int), or [android.service.controls.DeviceTypes#TYPE_ROUTINE](https://developer.android.com/reference/kotlin/android/service/controls/DeviceTypes#TYPE_ROUTINE:kotlin.Int) |

### getStatus

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | status of the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#), used to convey information about the attempt to fetch the current state Value is [android.service.controls.Control#STATUS_UNKNOWN](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_UNKNOWN:kotlin.Int), [android.service.controls.Control#STATUS_OK](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_OK:kotlin.Int), [android.service.controls.Control#STATUS_NOT_FOUND](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_NOT_FOUND:kotlin.Int), [android.service.controls.Control#STATUS_ERROR](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_ERROR:kotlin.Int), or [android.service.controls.Control#STATUS_DISABLED](https://developer.android.com/reference/kotlin/android/service/controls/Control#STATUS_DISABLED:kotlin.Int) |

### getStatusText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatusText(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | user-facing text description of the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)'s status, describing its current state This value cannot be`null`. |

### getStructure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStructure(): CharSequence?
```

Optional top-level group to help define the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)'s location, visible to the user. If not present, the application name will be used as the top-level group. A structure contains zones which contains controls.

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
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | additional information about the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#), to appear underneath the title This value cannot be`null`. |

### getTitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTitle(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the user facing name of the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#) This value cannot be`null`. |

### getZone

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZone(): CharSequence?
```

Optional group name to help define the [Control](https://developer.android.com/reference/kotlin/android/service/controls/Control#)'s location within a structure, visible to the user. A structure contains zones which contains controls.

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Control!>
```
