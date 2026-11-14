# MicrophoneInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MicrophoneInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/MicrophoneInfo "View this page in Java") 
| --- | --- |

```
class MicrophoneInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MicrophoneInfo](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#) |

Class providing information on a microphone. It indicates the location and orientation of the microphone on the device as well as useful information like frequency response and sensitivity. It can be used by applications implementing special pre processing effects like noise suppression of beam forming that need to know about precise microphone characteristics in order to adapt their algorithms.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------|
| | [Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F) <br /> |

| Constants ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MAPPING_DIRECT](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#CHANNEL_MAPPING_DIRECT:kotlin.Int) The channel contains raw audio from this microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MAPPING_PROCESSED](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#CHANNEL_MAPPING_PROCESSED:kotlin.Int) The channel contains processed audio from this microphone and possibly another microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_BI_DIRECTIONAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_BI_DIRECTIONAL:kotlin.Int) Microphone directionality type: bi-directional. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_CARDIOID:kotlin.Int) Microphone directionality type: cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_HYPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_HYPER_CARDIOID:kotlin.Int) Microphone directionality type: hyper cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_OMNI](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_OMNI:kotlin.Int) Microphone directionality type: omni. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_SUPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_SUPER_CARDIOID:kotlin.Int) Microphone directionality type: super cardioid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTIONALITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_UNKNOWN:kotlin.Int) Unknown microphone directionality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GROUP_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#GROUP_UNKNOWN:kotlin.Int) Value used for when the group of the microphone is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INDEX_IN_THE_GROUP_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#INDEX_IN_THE_GROUP_UNKNOWN:kotlin.Int) Value used for when the index in the group of the microphone is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_MAINBODY](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY:kotlin.Int) A microphone that locate on main body of the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_MAINBODY_MOVABLE](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY_MOVABLE:kotlin.Int) A microphone that locate on a movable main body of the device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_PERIPHERAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_PERIPHERAL:kotlin.Int) A microphone that locate on a peripheral. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_UNKNOWN:kotlin.Int) A microphone that the location is unknown. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [SENSITIVITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#SENSITIVITY_UNKNOWN:kotlin.Float) Value used for when the sensitivity of the microphone is unknown. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [SPL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#SPL_UNKNOWN:kotlin.Float) Value used for when the SPL of the microphone is unknown. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAddress](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getAddress())`()` Returns The "address" string of the microphone that corresponds to the address returned by [AudioDeviceInfo.getAddress()](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getAddress()) |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>! | [getChannelMapping](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getChannelMapping())`()` Returns a [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) list for channel mapping, which indicating how this microphone is used by each channels or a capture stream. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getDescription())`()` Returns alphanumeric code that uniquely identifies the device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirectionality](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getDirectionality())`()` Returns the directionality of microphone. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)\< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!\>! | [getFrequencyResponse](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getFrequencyResponse())`()` Returns a [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) list of frequency responses. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroup](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getGroup())`()` Returns A device group id that can be used to group together microphones on the same peripheral, attachments or logical groups. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getId())`()` Returns The system unique device ID that corresponds to the id returned by [AudioDeviceInfo.getId()](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getId()). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndexInTheGroup](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getIndexInTheGroup())`()` Returns unique index for device within its group. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocation](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getLocation())`()` Returns the location of the microphone. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaxSpl](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getMaxSpl())`()` Returns the level in dB of the maximum SPL supported by the device at 1000Hz. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinSpl](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getMinSpl())`()` Returns the level in dB of the minimum SPL that can be registered by the device at 1000Hz. |
| [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | [getOrientation](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getOrientation())`()` Returns A [Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F) object that represents the orientation of microphone. |
| --- | --- |
| [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | [getPosition](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getPosition())`()` Returns A [Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F) object that represents the geometric location of microphone in meters. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSensitivity](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getSensitivity())`()` Returns the level in dBFS produced by a 1000Hz tone at 94 dB SPL. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#getType())`()` Returns the device type identifier of the microphone (e.g AudioDeviceInfo.TYPE_BUILTIN_MIC). |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | [ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#ORIENTATION_UNKNOWN:android.media.MicrophoneInfo.Coordinate3F) Value used for when the orientation of the microphone is unknown. |
| static [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | [POSITION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#POSITION_UNKNOWN:android.media.MicrophoneInfo.Coordinate3F) Value used for when the position of the microphone is unknown. |

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

Returns The "address" string of the microphone that corresponds to the address returned by [AudioDeviceInfo.getAddress()](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getAddress())

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the address of the microphone This value cannot be`null`. |

### getChannelMapping

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelMapping(): MutableList<Pair<Int!, Int!>!>!
```

Returns a [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) list for channel mapping, which indicating how this microphone is used by each channels or a capture stream. For each [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#), the first value is channel index, the second value is channel mapping type, which could be either [CHANNEL_MAPPING_DIRECT](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#CHANNEL_MAPPING_DIRECT:kotlin.Int) or [CHANNEL_MAPPING_PROCESSED](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#CHANNEL_MAPPING_PROCESSED:kotlin.Int). If a channel has contributions from more than one microphone, it is likely the HAL did some extra processing to combine the sources, but this is to be inferred by the user. Empty list when the MicrophoneInfo is returned by AudioManager.getMicrophones(). At least one entry when the MicrophoneInfo is returned by AudioRecord.getActiveMicrophones().

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!>! | a [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) list for channel mapping |

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

Returns the directionality of microphone. The return value is one of [DIRECTIONALITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_UNKNOWN:kotlin.Int), [DIRECTIONALITY_OMNI](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_OMNI:kotlin.Int), [DIRECTIONALITY_BI_DIRECTIONAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_BI_DIRECTIONAL:kotlin.Int), [DIRECTIONALITY_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_CARDIOID:kotlin.Int), [DIRECTIONALITY_HYPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_HYPER_CARDIOID:kotlin.Int), or [DIRECTIONALITY_SUPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_SUPER_CARDIOID:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the directionality of microphone Value is either`0`or a combination of [android.media.MicrophoneInfo#DIRECTIONALITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_UNKNOWN:kotlin.Int), [android.media.MicrophoneInfo#DIRECTIONALITY_OMNI](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_OMNI:kotlin.Int), [android.media.MicrophoneInfo#DIRECTIONALITY_BI_DIRECTIONAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_BI_DIRECTIONAL:kotlin.Int), [android.media.MicrophoneInfo#DIRECTIONALITY_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_CARDIOID:kotlin.Int), [android.media.MicrophoneInfo#DIRECTIONALITY_HYPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_HYPER_CARDIOID:kotlin.Int), and [android.media.MicrophoneInfo#DIRECTIONALITY_SUPER_CARDIOID](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#DIRECTIONALITY_SUPER_CARDIOID:kotlin.Int) |

### getFrequencyResponse

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrequencyResponse(): MutableList<Pair<Float!, Float!>!>!
```

Returns a [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) list of frequency responses. For every [android.util.Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#) in the list, the first value represents frequency in Hz, and the second value represents response in dB.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html#)< [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!>! | the frequency response of the microphone |

### getGroup

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGroup(): Int
```

Returns A device group id that can be used to group together microphones on the same peripheral, attachments or logical groups. Main body is usually group 0.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the group of the microphone or [GROUP_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#GROUP_UNKNOWN:kotlin.Int) if the group is unknown |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Returns The system unique device ID that corresponds to the id returned by [AudioDeviceInfo.getId()](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getId()).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the microphone's index in its group or [INDEX_IN_THE_GROUP_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#INDEX_IN_THE_GROUP_UNKNOWN:kotlin.Int) if the index in the group is unknown |

### getLocation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocation(): Int
```

Returns the location of the microphone. The return value is one of [LOCATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_UNKNOWN:kotlin.Int), [LOCATION_MAINBODY](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY:kotlin.Int), [LOCATION_MAINBODY_MOVABLE](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY_MOVABLE:kotlin.Int), or [LOCATION_PERIPHERAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_PERIPHERAL:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the location of the microphone Value is either`0`or a combination of [android.media.MicrophoneInfo#LOCATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_UNKNOWN:kotlin.Int), [android.media.MicrophoneInfo#LOCATION_MAINBODY](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY:kotlin.Int), [android.media.MicrophoneInfo#LOCATION_MAINBODY_MOVABLE](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_MAINBODY_MOVABLE:kotlin.Int), and [android.media.MicrophoneInfo#LOCATION_PERIPHERAL](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#LOCATION_PERIPHERAL:kotlin.Int) |

### getMaxSpl

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSpl(): Float
```

Returns the level in dB of the maximum SPL supported by the device at 1000Hz.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the maximum level in dB or [SPL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#SPL_UNKNOWN:kotlin.Float) if maximum SPL is unknown |

### getMinSpl

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinSpl(): Float
```

Returns the level in dB of the minimum SPL that can be registered by the device at 1000Hz.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the minimum level in dB or [SPL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#SPL_UNKNOWN:kotlin.Float) if minimum SPL is unknown |

### getOrientation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrientation(): MicrophoneInfo.Coordinate3F!
```

Returns A [Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F) object that represents the orientation of microphone. X-axis, Y-axis and Z-axis show as the x, y, z value. The orientation will be normalized such as sqrt(x\^2 + y\^2 + z\^2) equals 1.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | the orientation of the microphone or [ORIENTATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#ORIENTATION_UNKNOWN:android.media.MicrophoneInfo.Coordinate3F) if orientation is unknown |

### getPosition

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): MicrophoneInfo.Coordinate3F!
```

Returns A [Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F) object that represents the geometric location of microphone in meters. X-axis, Y-axis and Z-axis show as the x, y, z values. For mobile devices, the axes originate from the bottom-left-back corner of the appliance. In devices with [android.content.pm.PackageManager#FEATURE_AUTOMOTIVE](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUTOMOTIVE:kotlin.String), axes are defined with respect to the vehicle body frame, originating from the center of the vehicle's rear axle.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MicrophoneInfo.Coordinate3F](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo.Coordinate3F)! | the geometric location of the microphone or [POSITION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#POSITION_UNKNOWN:android.media.MicrophoneInfo.Coordinate3F) if the geometric location is unknown |

**See Also**

### getSensitivity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSensitivity(): Float
```

Returns the level in dBFS produced by a 1000Hz tone at 94 dB SPL.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the sensitivity of the microphone or [SENSITIVITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo#SENSITIVITY_UNKNOWN:kotlin.Float) if the sensitivity is unknown |

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
