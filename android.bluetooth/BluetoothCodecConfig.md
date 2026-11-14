# BluetoothCodecConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothCodecConfig

Kotlin| [Java](../android/bluetooth/BluetoothCodecConfig.md) 
| --- | --- |

```
class BluetoothCodecConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothCodecConfig](../android/bluetooth/BluetoothCodecConfig.md) |

Represents the codec configuration for a Bluetooth A2DP source device.

Contains the source codec type, the codec priority, the codec sample rate, the codec bits per sample, and the codec channel mode.

The source codec type values are the same as those supported by the device hardware.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/bluetooth/BluetoothCodecConfig.Builder.md) Builder for [BluetoothCodecConfig](../android/bluetooth/BluetoothCodecConfig.md). |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITS_PER_SAMPLE_16](../android/bluetooth/BluetoothCodecConfig.md) Codec bits per sample 16. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITS_PER_SAMPLE_24](../android/bluetooth/BluetoothCodecConfig.md) Codec bits per sample 24. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITS_PER_SAMPLE_32](../android/bluetooth/BluetoothCodecConfig.md) Codec bits per sample 32. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BITS_PER_SAMPLE_NONE](../android/bluetooth/BluetoothCodecConfig.md) Codec bits per sample 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MODE_MONO](../android/bluetooth/BluetoothCodecConfig.md) Codec channel mode MONO. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MODE_NONE](../android/bluetooth/BluetoothCodecConfig.md) Codec channel mode NONE. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_MODE_STEREO](../android/bluetooth/BluetoothCodecConfig.md) Codec channel mode STEREO. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODEC_PRIORITY_DEFAULT](../android/bluetooth/BluetoothCodecConfig.md) Codec priority default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODEC_PRIORITY_DISABLED](../android/bluetooth/BluetoothCodecConfig.md) Codec priority disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODEC_PRIORITY_HIGHEST](../android/bluetooth/BluetoothCodecConfig.md) Codec priority highest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_176400](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 176400 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_192000](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 192000 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_44100](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 44100 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_48000](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 48000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_88200](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 88200 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_96000](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 96000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_RATE_NONE](../android/bluetooth/BluetoothCodecConfig.md) Codec sample rate 0 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_AAC](../android/bluetooth/BluetoothCodecConfig.md) Source codec type AAC. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_APTX](../android/bluetooth/BluetoothCodecConfig.md) Source codec type APTX. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_APTX_HD](../android/bluetooth/BluetoothCodecConfig.md) Source codec type APTX HD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_INVALID](../android/bluetooth/BluetoothCodecConfig.md) Source codec type invalid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_LC3](../android/bluetooth/BluetoothCodecConfig.md) Source codec type LC3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_LDAC](../android/bluetooth/BluetoothCodecConfig.md) Source codec type LDAC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_OPUS](../android/bluetooth/BluetoothCodecConfig.md) Source codec type Opus. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CODEC_TYPE_SBC](../android/bluetooth/BluetoothCodecConfig.md) Source codec type SBC. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/bluetooth/BluetoothCodecConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBitsPerSample](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec bits per sample. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelMode](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec channel mode. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodecPriority](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec selection priority. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCodecSpecific1](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec specific value1. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCodecSpecific2](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec specific value2. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCodecSpecific3](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec specific value3. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCodecSpecific4](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec specific value4. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodecType](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the source codec type of this config. |
| --- | --- |
| [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md)? | [getExtendedCodecType](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the source codec type of this config. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleRate](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns the codec sample rate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns a hash representation of this BluetoothCodecConfig based on all the config values. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMandatoryCodec](../android/bluetooth/BluetoothCodecConfig.md))`()` Checks whether the codec is mandatory. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/bluetooth/BluetoothCodecConfig.md))`()` Returns a [String](../java/lang/String.md) that describes each BluetoothCodecConfig parameter current value. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothCodecConfig](../android/bluetooth/BluetoothCodecConfig.md)!\> | [CREATOR](../android/bluetooth/BluetoothCodecConfig.md) <br /> |

## Constants

### BITS_PER_SAMPLE_16

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BITS_PER_SAMPLE_16: Int
```

Codec bits per sample 16. 

 Value: 1

### BITS_PER_SAMPLE_24

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BITS_PER_SAMPLE_24: Int
```

Codec bits per sample 24. 

 Value: 2

### BITS_PER_SAMPLE_32

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BITS_PER_SAMPLE_32: Int
```

Codec bits per sample 32. 

 Value: 4

### BITS_PER_SAMPLE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BITS_PER_SAMPLE_NONE: Int
```

Codec bits per sample 0. Default value of the codec bits per sample. 

 Value: 0

### CHANNEL_MODE_MONO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_MODE_MONO: Int
```

Codec channel mode MONO. 

 Value: 1

### CHANNEL_MODE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_MODE_NONE: Int
```

Codec channel mode NONE. Default value of the codec channel mode. 

 Value: 0

### CHANNEL_MODE_STEREO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_MODE_STEREO: Int
```

Codec channel mode STEREO. 

 Value: 2

### CODEC_PRIORITY_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODEC_PRIORITY_DEFAULT: Int
```

Codec priority default. Default value used for codec priority. 

 Value: 0

### CODEC_PRIORITY_DISABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODEC_PRIORITY_DISABLED: Int
```

Codec priority disabled. Used to indicate that this codec is disabled and should not be used. 

 Value: -1

### CODEC_PRIORITY_HIGHEST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODEC_PRIORITY_HIGHEST: Int
```

Codec priority highest. Used to indicate the highest priority a codec can have. 

 Value: 1000000

### SAMPLE_RATE_176400

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_176400: Int
```

Codec sample rate 176400 Hz. 

 Value: 16

### SAMPLE_RATE_192000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_192000: Int
```

Codec sample rate 192000 Hz. 

 Value: 32

### SAMPLE_RATE_44100

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_44100: Int
```

Codec sample rate 44100 Hz. 

 Value: 1

### SAMPLE_RATE_48000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_48000: Int
```

Codec sample rate 48000 Hz. 

 Value: 2

### SAMPLE_RATE_88200

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_88200: Int
```

Codec sample rate 88200 Hz. 

 Value: 4

### SAMPLE_RATE_96000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_96000: Int
```

Codec sample rate 96000 Hz. 

 Value: 8

### SAMPLE_RATE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_RATE_NONE: Int
```

Codec sample rate 0 Hz. Default value used for codec sample rate. 

 Value: 0

### SOURCE_CODEC_TYPE_AAC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_AAC: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type AAC. 

 Value: 1

### SOURCE_CODEC_TYPE_APTX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_APTX: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type APTX. 

 Value: 2

### SOURCE_CODEC_TYPE_APTX_HD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_APTX_HD: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type APTX HD. 

 Value: 3

### SOURCE_CODEC_TYPE_INVALID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_INVALID: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type invalid. This is the default value used for codec type. 

 Value: 1000000

### SOURCE_CODEC_TYPE_LC3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_LC3: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type LC3. 

 Value: 5

### SOURCE_CODEC_TYPE_LDAC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_LDAC: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type LDAC. 

 Value: 4

### SOURCE_CODEC_TYPE_OPUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_OPUS: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type Opus. 

 Value: 6

### SOURCE_CODEC_TYPE_SBC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CODEC_TYPE_SBC: Int
```

**Deprecated:** *Use the [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md) values returned by [android.bluetooth.BluetoothA2dp#getSupportedCodecTypes](../android/bluetooth/BluetoothA2dp.md))instead.*

Source codec type SBC. This is the mandatory source codec type. 

 Value: 0

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getBitsPerSample

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBitsPerSample(): Int
```

Returns the codec bits per sample. The value can be a bitmask with all bits per sample supported.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothCodecConfig#BITS_PER_SAMPLE_NONE](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#BITS_PER_SAMPLE_16](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#BITS_PER_SAMPLE_24](../android/bluetooth/BluetoothCodecConfig.md), or [android.bluetooth.BluetoothCodecConfig#BITS_PER_SAMPLE_32](../android/bluetooth/BluetoothCodecConfig.md) |

### getChannelMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelMode(): Int
```

Returns the codec channel mode. The value can be a bitmask with all supported channel modes.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothCodecConfig#CHANNEL_MODE_NONE](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#CHANNEL_MODE_MONO](../android/bluetooth/BluetoothCodecConfig.md), or [android.bluetooth.BluetoothCodecConfig#CHANNEL_MODE_STEREO](../android/bluetooth/BluetoothCodecConfig.md) |

### getCodecPriority

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecPriority(): Int
```

Returns the codec selection priority.

The codec selection priority is relative to other codecs: larger value means higher priority.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothCodecConfig#CODEC_PRIORITY_DISABLED](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#CODEC_PRIORITY_DEFAULT](../android/bluetooth/BluetoothCodecConfig.md), or [android.bluetooth.BluetoothCodecConfig#CODEC_PRIORITY_HIGHEST](../android/bluetooth/BluetoothCodecConfig.md) |

### getCodecSpecific1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecSpecific1(): Long
```

Returns the codec specific value1. As the value and usage differ for each codec, please refer to the concerned codec specification to obtain the codec specific information.

See section 4.3.2 of the Bluetooth A2dp specification for SBC codec specific information elements.

See section 4.4.2 of the Bluetooth A2dp specification for MPEG-1,2 Audio codec specific information elements.

See section 4.5.2 of the Bluetooth A2dp specification for MPEG-2, 4 AAC codec specific information elements.

See section 4.6.2 of the Bluetooth A2dp specification for ATRAC family codec specific information elements.

See section 4.7.2 of the Bluetooth A2dp specification for Vendor Specific A2DP codec specific information elements. 

### getCodecSpecific2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecSpecific2(): Long
```

Returns the codec specific value2. As the value and usage differ for each codec, please refer to the concerned codec specification to obtain the codec specific information.

See section 4.3.2 of the Bluetooth A2dp specification for SBC codec specific information elements.

See section 4.4.2 of the Bluetooth A2dp specification for MPEG-1,2 Audio codec specific information elements.

See section 4.5.2 of the Bluetooth A2dp specification for MPEG-2, 4 AAC codec specific information elements.

See section 4.6.2 of the Bluetooth A2dp specification for ATRAC family codec specific information elements.

See section 4.7.2 of the Bluetooth A2dp specification for Vendor Specific A2DP codec specific information elements. 

### getCodecSpecific3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecSpecific3(): Long
```

Returns the codec specific value3. As the value and usage differ for each codec, please refer to the concerned codec specification to obtain the codec specific information.

See section 4.3.2 of the Bluetooth A2dp specification for SBC codec specific information elements.

See section 4.4.2 of the Bluetooth A2dp specification for MPEG-1,2 Audio codec specific information elements.

See section 4.5.2 of the Bluetooth A2dp specification for MPEG-2, 4 AAC codec specific information elements.

See section 4.6.2 of the Bluetooth A2dp specification for ATRAC family codec specific information elements.

See section 4.7.2 of the Bluetooth A2dp specification for Vendor Specific A2DP codec specific information elements. 

### getCodecSpecific4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecSpecific4(): Long
```

Returns the codec specific value4. As the value and usage differ for each codec, please refer to the concerned codec specification to obtain the codec specific information.

See section 4.3.2 of the Bluetooth A2dp specification for SBC codec specific information elements.

See section 4.4.2 of the Bluetooth A2dp specification for MPEG-1,2 Audio codec specific information elements.

See section 4.5.2 of the Bluetooth A2dp specification for MPEG-2, 4 AAC codec specific information elements.

See section 4.6.2 of the Bluetooth A2dp specification for ATRAC family codec specific information elements.

See section 4.7.2 of the Bluetooth A2dp specification for Vendor Specific A2DP codec specific information elements. 

### getCodecType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecType(): Int
```

**Deprecated:** *use [BluetoothCodecConfig.getExtendedCodecType](../android/bluetooth/BluetoothCodecConfig.md))instead.*

Returns the source codec type of this config.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_SBC](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_AAC](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_APTX](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_APTX_HD](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_LDAC](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_LC3](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_OPUS](../android/bluetooth/BluetoothCodecConfig.md), or [android.bluetooth.BluetoothCodecConfig#SOURCE_CODEC_TYPE_INVALID](../android/bluetooth/BluetoothCodecConfig.md) |

### getExtendedCodecType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtendedCodecType(): BluetoothCodecType?
```

Returns the source codec type of this config.

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------|
| [BluetoothCodecType](../android/bluetooth/BluetoothCodecType.md)? | This value may be`null`. |

### getSampleRate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleRate(): Int
```

Returns the codec sample rate. The value can be a bitmask with all supported sample rates.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_NONE](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_44100](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_48000](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_88200](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_96000](../android/bluetooth/BluetoothCodecConfig.md), [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_176400](../android/bluetooth/BluetoothCodecConfig.md), or [android.bluetooth.BluetoothCodecConfig#SAMPLE_RATE_192000](../android/bluetooth/BluetoothCodecConfig.md) |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash representation of this BluetoothCodecConfig based on all the config values.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isMandatoryCodec

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMandatoryCodec(): Boolean
```

Checks whether the codec is mandatory.

The actual mandatory codec type for Android Bluetooth audio is SBC. See [SOURCE_CODEC_TYPE_SBC](../android/bluetooth/BluetoothCodecConfig.md).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the codec is mandatory,`false`otherwise |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a [String](../java/lang/String.md) that describes each BluetoothCodecConfig parameter current value.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothCodecConfig!>
```
