# MicrophoneInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MicrophoneInfo

Kotlin| [Java](MicrophoneInfo.md) 
| --- | --- |

```
class MicrophoneInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MicrophoneInfo](MicrophoneInfo.md) |

Class providing information on a microphone. It indicates the location and orientation of the microphone on the device as well as useful information like frequency response and sensitivity. It can be used by applications implementing special pre processing effects like noise suppression of beam forming that need to know about precise microphone characteristics in order to adapt their algorithms.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------|
| | [Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md) <br /> |

| Constants ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MAPPING_DIRECT](MicrophoneInfo.md) The channel contains raw audio from this microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MAPPING_PROCESSED](MicrophoneInfo.md) The channel contains processed audio from this microphone and possibly another microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_BI_DIRECTIONAL](MicrophoneInfo.md) Microphone directionality type: bi-directional. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_CARDIOID](MicrophoneInfo.md) Microphone directionality type: cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_HYPER_CARDIOID](MicrophoneInfo.md) Microphone directionality type: hyper cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_OMNI](MicrophoneInfo.md) Microphone directionality type: omni. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_SUPER_CARDIOID](MicrophoneInfo.md) Microphone directionality type: super cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_UNKNOWN](MicrophoneInfo.md) Unknown microphone directionality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GROUP_UNKNOWN](MicrophoneInfo.md) Value used for when the group of the microphone is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INDEX_IN_THE_GROUP_UNKNOWN](MicrophoneInfo.md) Value used for when the index in the group of the microphone is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_MAINBODY](MicrophoneInfo.md) A microphone that locate on main body of the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_MAINBODY_MOVABLE](MicrophoneInfo.md) A microphone that locate on a movable main body of the device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_PERIPHERAL](MicrophoneInfo.md) A microphone that locate on a peripheral. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_UNKNOWN](MicrophoneInfo.md) A microphone that the location is unknown. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [SENSITIVITY_UNKNOWN](MicrophoneInfo.md) Value used for when the sensitivity of the microphone is unknown. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [SPL_UNKNOWN](MicrophoneInfo.md) Value used for when the SPL of the microphone is unknown. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAddress](MicrophoneInfo.md))`()` Returns The "address" string of the microphone that corresponds to the address returned by [AudioDeviceInfo.getAddress()](AudioDeviceInfo.md)) |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](../android.util/Pair.md)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>! | [getChannelMapping](MicrophoneInfo.md))`()` Returns a [android.util.Pair](../android.util/Pair.md) list for channel mapping, which indicating how this microphone is used by each channels or a capture stream. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](MicrophoneInfo.md))`()` Returns alphanumeric code that uniquely identifies the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirectionality](MicrophoneInfo.md))`()` Returns the directionality of microphone. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](../android.util/Pair.md)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!\>! | [getFrequencyResponse](MicrophoneInfo.md))`()` Returns a [android.util.Pair](../android.util/Pair.md) list of frequency responses. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroup](MicrophoneInfo.md))`()` Returns A device group id that can be used to group together microphones on the same peripheral, attachments or logical groups. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](MicrophoneInfo.md))`()` Returns The system unique device ID that corresponds to the id returned by [AudioDeviceInfo.getId()](AudioDeviceInfo.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexInTheGroup](MicrophoneInfo.md))`()` Returns unique index for device within its group. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocation](MicrophoneInfo.md))`()` Returns the location of the microphone. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxSpl](MicrophoneInfo.md))`()` Returns the level in dB of the maximum SPL supported by the device at 1000Hz. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinSpl](MicrophoneInfo.md))`()` Returns the level in dB of the minimum SPL that can be registered by the device at 1000Hz. |
| [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | [getOrientation](MicrophoneInfo.md))`()` Returns A [Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md) object that represents the orientation of microphone. |
| --- | --- |
| [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | [getPosition](MicrophoneInfo.md))`()` Returns A [Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md) object that represents the geometric location of microphone in meters. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSensitivity](MicrophoneInfo.md))`()` Returns the level in dBFS produced by a 1000Hz tone at 94 dB SPL. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](MicrophoneInfo.md))`()` Returns the device type identifier of the microphone (e.g AudioDeviceInfo.TYPE_BUILTIN_MIC). |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | [ORIENTATION_UNKNOWN](MicrophoneInfo.md) Value used for when the orientation of the microphone is unknown. |
| static [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | [POSITION_UNKNOWN](MicrophoneInfo.md) Value used for when the position of the microphone is unknown. |

## Constants

### CHANNEL_MAPPING_DIRECT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_MAPPING_DIRECT: Int
```

The channel contains raw audio from this microphone. 

 Value: 1

### CHANNEL_MAPPING_PROCESSED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_MAPPING_PROCESSED: Int
```

The channel contains processed audio from this microphone and possibly another microphone. 

 Value: 2

### DIRECTIONALITY_BI_DIRECTIONAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_BI_DIRECTIONAL: Int
```

Microphone directionality type: bi-directional. 

 Value: 2

### DIRECTIONALITY_CARDIOID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_CARDIOID: Int
```

Microphone directionality type: cardioid. 

 Value: 3

### DIRECTIONALITY_HYPER_CARDIOID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_HYPER_CARDIOID: Int
```

Microphone directionality type: hyper cardioid. 

 Value: 4

### DIRECTIONALITY_OMNI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_OMNI: Int
```

Microphone directionality type: omni. 

 Value: 1

### DIRECTIONALITY_SUPER_CARDIOID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_SUPER_CARDIOID: Int
```

Microphone directionality type: super cardioid. 

 Value: 5

### DIRECTIONALITY_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTIONALITY_UNKNOWN: Int
```

Unknown microphone directionality. 

 Value: 0

### GROUP_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GROUP_UNKNOWN: Int
```

Value used for when the group of the microphone is unknown. 

 Value: -1

### INDEX_IN_THE_GROUP_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INDEX_IN_THE_GROUP_UNKNOWN: Int
```

Value used for when the index in the group of the microphone is unknown. 

 Value: -1

### LOCATION_MAINBODY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_MAINBODY: Int
```

A microphone that locate on main body of the device. 

 Value: 1

### LOCATION_MAINBODY_MOVABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_MAINBODY_MOVABLE: Int
```

A microphone that locate on a movable main body of the device. 

 Value: 2

### LOCATION_PERIPHERAL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_PERIPHERAL: Int
```

A microphone that locate on a peripheral. 

 Value: 3

### LOCATION_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_UNKNOWN: Int
```

A microphone that the location is unknown. 

 Value: 0

### SENSITIVITY_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SENSITIVITY_UNKNOWN: Float
```

Value used for when the sensitivity of the microphone is unknown. 

 Value: -3.4028235E38f

### SPL_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPL_UNKNOWN: Float
```

Value used for when the SPL of the microphone is unknown. This value could be used when maximum SPL or minimum SPL is unknown. 

 Value: -3.4028235E38f

## Public methods

### getAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): String
```

Returns The "address" string of the microphone that corresponds to the address returned by [AudioDeviceInfo.getAddress()](AudioDeviceInfo.md))

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the address of the microphone This value cannot be`null`. |

### getChannelMapping

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelMapping(): MutableList<Pair<Int!, Int!>!>!
```

Returns a [android.util.Pair](../android.util/Pair.md) list for channel mapping, which indicating how this microphone is used by each channels or a capture stream. For each [android.util.Pair](../android.util/Pair.md), the first value is channel index, the second value is channel mapping type, which could be either [CHANNEL_MAPPING_DIRECT](MicrophoneInfo.md) or [CHANNEL_MAPPING_PROCESSED](MicrophoneInfo.md). If a channel has contributions from more than one microphone, it is likely the HAL did some extra processing to combine the sources, but this is to be inferred by the user. Empty list when the MicrophoneInfo is returned by AudioManager.getMicrophones(). At least one entry when the MicrophoneInfo is returned by AudioRecord.getActiveMicrophones().

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Pair](../android.util/Pair.md)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!>! | a [android.util.Pair](../android.util/Pair.md) list for channel mapping |

### getDescription

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String!
```

Returns alphanumeric code that uniquely identifies the device.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the description of the microphone |

### getDirectionality

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDirectionality(): Int
```

Returns the directionality of microphone. The return value is one of [DIRECTIONALITY_UNKNOWN](MicrophoneInfo.md), [DIRECTIONALITY_OMNI](MicrophoneInfo.md), [DIRECTIONALITY_BI_DIRECTIONAL](MicrophoneInfo.md), [DIRECTIONALITY_CARDIOID](MicrophoneInfo.md), [DIRECTIONALITY_HYPER_CARDIOID](MicrophoneInfo.md), or [DIRECTIONALITY_SUPER_CARDIOID](MicrophoneInfo.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the directionality of microphone Value is either`0`or a combination of [android.media.MicrophoneInfo#DIRECTIONALITY_UNKNOWN](MicrophoneInfo.md), [android.media.MicrophoneInfo#DIRECTIONALITY_OMNI](MicrophoneInfo.md), [android.media.MicrophoneInfo#DIRECTIONALITY_BI_DIRECTIONAL](MicrophoneInfo.md), [android.media.MicrophoneInfo#DIRECTIONALITY_CARDIOID](MicrophoneInfo.md), [android.media.MicrophoneInfo#DIRECTIONALITY_HYPER_CARDIOID](MicrophoneInfo.md), and [android.media.MicrophoneInfo#DIRECTIONALITY_SUPER_CARDIOID](MicrophoneInfo.md) |

### getFrequencyResponse

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequencyResponse(): MutableList<Pair<Float!, Float!>!>!
```

Returns a [android.util.Pair](../android.util/Pair.md) list of frequency responses. For every [android.util.Pair](../android.util/Pair.md) in the list, the first value represents frequency in Hz, and the second value represents response in dB.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Pair](../android.util/Pair.md)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!>! | the frequency response of the microphone |

### getGroup

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGroup(): Int
```

Returns A device group id that can be used to group together microphones on the same peripheral, attachments or logical groups. Main body is usually group 0.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the group of the microphone or [GROUP_UNKNOWN](MicrophoneInfo.md) if the group is unknown |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Returns The system unique device ID that corresponds to the id returned by [AudioDeviceInfo.getId()](AudioDeviceInfo.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the microphone's id |

### getIndexInTheGroup

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIndexInTheGroup(): Int
```

Returns unique index for device within its group.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the microphone's index in its group or [INDEX_IN_THE_GROUP_UNKNOWN](MicrophoneInfo.md) if the index in the group is unknown |

### getLocation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocation(): Int
```

Returns the location of the microphone. The return value is one of [LOCATION_UNKNOWN](MicrophoneInfo.md), [LOCATION_MAINBODY](MicrophoneInfo.md), [LOCATION_MAINBODY_MOVABLE](MicrophoneInfo.md), or [LOCATION_PERIPHERAL](MicrophoneInfo.md).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the location of the microphone Value is either`0`or a combination of [android.media.MicrophoneInfo#LOCATION_UNKNOWN](MicrophoneInfo.md), [android.media.MicrophoneInfo#LOCATION_MAINBODY](MicrophoneInfo.md), [android.media.MicrophoneInfo#LOCATION_MAINBODY_MOVABLE](MicrophoneInfo.md), and [android.media.MicrophoneInfo#LOCATION_PERIPHERAL](MicrophoneInfo.md) |

### getMaxSpl

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSpl(): Float
```

Returns the level in dB of the maximum SPL supported by the device at 1000Hz.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the maximum level in dB or [SPL_UNKNOWN](MicrophoneInfo.md) if maximum SPL is unknown |

### getMinSpl

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinSpl(): Float
```

Returns the level in dB of the minimum SPL that can be registered by the device at 1000Hz.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the minimum level in dB or [SPL_UNKNOWN](MicrophoneInfo.md) if minimum SPL is unknown |

### getOrientation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrientation(): MicrophoneInfo.Coordinate3F!
```

Returns A [Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md) object that represents the orientation of microphone. X-axis, Y-axis and Z-axis show as the x, y, z value. The orientation will be normalized such as sqrt(x\^2 + y\^2 + z\^2) equals 1.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | the orientation of the microphone or [ORIENTATION_UNKNOWN](MicrophoneInfo.md) if orientation is unknown |

### getPosition

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): MicrophoneInfo.Coordinate3F!
```

Returns A [Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md) object that represents the geometric location of microphone in meters. X-axis, Y-axis and Z-axis show as the x, y, z values. For mobile devices, the axes originate from the bottom-left-back corner of the appliance. In devices with [android.content.pm.PackageManager#FEATURE_AUTOMOTIVE](../android.content.pm/PackageManager.md), axes are defined with respect to the vehicle body frame, originating from the center of the vehicle's rear axle.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MicrophoneInfo.Coordinate3F](../android/media/MicrophoneInfo.Coordinate3F.md)! | the geometric location of the microphone or [POSITION_UNKNOWN](MicrophoneInfo.md) if the geometric location is unknown |

**See Also**

### getSensitivity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSensitivity(): Float
```

Returns the level in dBFS produced by a 1000Hz tone at 94 dB SPL.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the sensitivity of the microphone or [SENSITIVITY_UNKNOWN](MicrophoneInfo.md) if the sensitivity is unknown |

### getType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the device type identifier of the microphone (e.g AudioDeviceInfo.TYPE_BUILTIN_MIC).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device type of the microphone |

## Properties

### ORIENTATION_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_UNKNOWN: MicrophoneInfo.Coordinate3F!
```

Value used for when the orientation of the microphone is unknown. 

### POSITION_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_UNKNOWN: MicrophoneInfo.Coordinate3F!
```

Value used for when the position of the microphone is unknown.
