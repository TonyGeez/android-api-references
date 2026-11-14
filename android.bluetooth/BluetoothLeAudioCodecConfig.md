Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothLeAudioCodecConfig

```
class BluetoothLeAudioCodecConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothLeAudioCodecConfig](../android/bluetooth/BluetoothLeAudioCodecConfig.md) |

Represents the codec configuration for a Bluetooth LE Audio source device.

Contains the source codec type.

The source codec type values are the same as those supported by the device hardware.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig.Builder` Builder for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_16:kotlin.Int` Codec bits per sample 16. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_24:kotlin.Int` Codec bits per sample 24. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_32:kotlin.Int` Codec bits per sample 32. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_NONE:kotlin.Int` Codec bits per sample 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_1:kotlin.Int` Codec channel mode MONO. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_2:kotlin.Int` Codec channel mode STEREO. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_NONE:kotlin.Int` Codec channel mode NONE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_DEFAULT:kotlin.Int` Codec priority default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_DISABLED:kotlin.Int` Codec priority disabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_HIGHEST:kotlin.Int` Codec priority highest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_10000:kotlin.Int` Frame duration 10000 us. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_7500:kotlin.Int` Frame duration 7500 us. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_NONE:kotlin.Int` Frame duration 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_11025:kotlin.Int` Codec sample rate 11025 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_16000:kotlin.Int` Codec sample rate 16000 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_176400:kotlin.Int` Codec sample rate 176400 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_192000:kotlin.Int` Codec sample rate 192000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_22050:kotlin.Int` Codec sample rate 22050 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_24000:kotlin.Int` Codec sample rate 24000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_32000:kotlin.Int` Codec sample rate 32000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_384000:kotlin.Int` Codec sample rate 384000 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_44100:kotlin.Int` Codec sample rate 44100 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_48000:kotlin.Int` Codec sample rate 48000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_8000:kotlin.Int` Codec sample rate 8000 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_88200:kotlin.Int` Codec sample rate 88200 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_96000:kotlin.Int` Codec sample rate 96000 Hz. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_NONE:kotlin.Int` Codec sample rate 0 Hz. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_INVALID:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_LC3:kotlin.Int` Source codec type for LC3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_OPUS:kotlin.Int` Source codec type for Opus. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_OPUS_HI_RES:kotlin.Int` Source codec type for Opus High Resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_VENDOR_SPECIFIC:kotlin.Int` Source codec type used for Vendor Specific codecs. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getBitsPerSample()()` Returns the codec bits per sample. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getChannelCount()()` Returns the codec channel mode. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getCodecId()()` Returns the unique codec identifier. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getCodecName()()` Gets the codec name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getCodecPriority()()` Returns the codec selection priority. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getCodecType()()` Gets the codec type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getFrameDuration()()` Returns the frame duration. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getMaxOctetsPerFrame()()` Returns the maximum octets per frame |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getMinOctetsPerFrame()()` Returns the minimum octets per frame |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getOctetsPerFrame()()` Returns the octets per frame |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getSampleRate()()` Returns the codec sample rate. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#hashCode()()` Returns a hash representation of this BluetoothLeAudioCodecConfig based on all the config values. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothLeAudioCodecConfig](../android/bluetooth/BluetoothLeAudioCodecConfig.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CREATOR:android.os.Parcelable.Creator` `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#` interface implementation. |

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

 Value: 8

### BITS_PER_SAMPLE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BITS_PER_SAMPLE_NONE: Int
```

Codec bits per sample 0. Default value of the codec bits per sample.

 Value: 0

### CHANNEL_COUNT_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_COUNT_1: Int
```

Codec channel mode MONO.

 Value: 1

### CHANNEL_COUNT_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_COUNT_2: Int
```

Codec channel mode STEREO.

 Value: 2

### CHANNEL_COUNT_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_COUNT_NONE: Int
```

Codec channel mode NONE. Default value of the codec channel mode.

 Value: 0

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

### FRAME_DURATION_10000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRAME_DURATION_10000: Int
```

Frame duration 10000 us.

 Value: 2

### FRAME_DURATION_7500

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRAME_DURATION_7500: Int
```

Frame duration 7500 us.

 Value: 1

### FRAME_DURATION_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRAME_DURATION_NONE: Int
```

Frame duration 0. Default value of the frame duration.

 Value: 0

### SAMPLE_RATE_11025

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_11025: Int
```

Codec sample rate 11025 Hz.

 Value: 2

### SAMPLE_RATE_16000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_16000: Int
```

Codec sample rate 16000 Hz.

 Value: 4

### SAMPLE_RATE_176400

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_176400: Int
```

Codec sample rate 176400 Hz.

 Value: 1024

### SAMPLE_RATE_192000

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_192000: Int
```

Codec sample rate 192000 Hz.

 Value: 2048

### SAMPLE_RATE_22050

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_22050: Int
```

Codec sample rate 22050 Hz.

 Value: 8

### SAMPLE_RATE_24000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_24000: Int
```

Codec sample rate 24000 Hz.

 Value: 16

### SAMPLE_RATE_32000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_32000: Int
```

Codec sample rate 32000 Hz.

 Value: 32

### SAMPLE_RATE_384000

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_384000: Int
```

Codec sample rate 384000 Hz.

 Value: 4096

### SAMPLE_RATE_44100

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_44100: Int
```

Codec sample rate 44100 Hz.

 Value: 64

### SAMPLE_RATE_48000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_48000: Int
```

Codec sample rate 48000 Hz.

 Value: 128

### SAMPLE_RATE_8000

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_8000: Int
```

Codec sample rate 8000 Hz.

 Value: 1

### SAMPLE_RATE_88200

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_88200: Int
```

Codec sample rate 88200 Hz.

 Value: 256

### SAMPLE_RATE_96000

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_96000: Int
```

Codec sample rate 96000 Hz.

 Value: 512

### SAMPLE_RATE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_NONE: Int
```

Codec sample rate 0 Hz. Default value used for codec sample rate. Values are the bit mask as defined in the Bluetooth Assigned Numbers, Generic Audio, Supported_Sampling_Frequencies table.

 Value: 0

### SOURCE_CODEC_TYPE_INVALID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CODEC_TYPE_INVALID: Int
```

 Value: 1000000

### SOURCE_CODEC_TYPE_LC3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CODEC_TYPE_LC3: Int
```

Source codec type for LC3.

 Value: 0

### SOURCE_CODEC_TYPE_OPUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CODEC_TYPE_OPUS: Int
```

Source codec type for Opus.

 Value: 1

### SOURCE_CODEC_TYPE_OPUS_HI_RES

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CODEC_TYPE_OPUS_HI_RES: Int
```

Source codec type for Opus High Resolution.

 Value: 2

### SOURCE_CODEC_TYPE_VENDOR_SPECIFIC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CODEC_TYPE_VENDOR_SPECIFIC: Int
```

Source codec type used for Vendor Specific codecs. When this type is used, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#getCodecId()` should be used to get more information about the codec.

 Value: 255

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getBitsPerSample

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBitsPerSample(): Int
```

Returns the codec bits per sample.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_16:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_24:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#BITS_PER_SAMPLE_32:kotlin.Int` |

### getChannelCount

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelCount(): Int
```

Returns the codec channel mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CHANNEL_COUNT_2:kotlin.Int` |

### getCodecId

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodecId(): Long
```

Returns the unique codec identifier.

The codec identifier is 40 bits as defined by Bluetooth ASCS v1.0.1 in chapter 4.1. Audio Stream Endpoints

- Bits 0-7: Codec ID, as defined by Bluetooth Assigned numbers 2.11 Coding_Format and Codec_ID (HCI)
 - 0x06: LC3
 - 0xFF: Vendor
- Bits 8-23: Company ID, set to 0, if octet 0 is not 0xFF.
- Bits 24-39: Vendor-defined codec ID, set to 0, if octet 0 is not 0xFF.

### getCodecName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodecName(): String
```

Gets the codec name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the codec name. This value cannot be `null`. |

### getCodecPriority

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodecPriority(): Int
```

Returns the codec selection priority.

The codec selection priority is relative to other codecs: larger value means higher priority.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#CODEC_PRIORITY_HIGHEST:kotlin.Int` |

### getCodecType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodecType(): Int
```

Gets the codec type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the codec type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_LC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_OPUS_HI_RES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_VENDOR_SPECIFIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SOURCE_CODEC_TYPE_INVALID:kotlin.Int` |

### getFrameDuration

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFrameDuration(): Int
```

Returns the frame duration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_7500:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#FRAME_DURATION_10000:kotlin.Int` |

### getMaxOctetsPerFrame

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxOctetsPerFrame(): Int
```

Returns the maximum octets per frame

### getMinOctetsPerFrame

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinOctetsPerFrame(): Int
```

Returns the minimum octets per frame

### getOctetsPerFrame

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOctetsPerFrame(): Int
```

Returns the octets per frame

### getSampleRate

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSampleRate(): Int
```

Returns the codec sample rate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_8000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_11025:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_16000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_22050:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_24000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_32000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_44100:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_48000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_88200:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_96000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_176400:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_192000:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudioCodecConfig#SAMPLE_RATE_384000:kotlin.Int` |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash representation of this BluetoothLeAudioCodecConfig based on all the config values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `out` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<BluetoothLeAudioCodecConfig!>
```

`https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#` interface implementation.
