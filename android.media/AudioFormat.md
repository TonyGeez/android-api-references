Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioFormat

```
class AudioFormat : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioFormat](AudioFormat.md) |

The AudioFormat class is used to access a number of audio format and channel configuration constants. They are for instance used in AudioTrackAudioRecord, as valid values in individual parameters of constructors like AudioTrack, where the fourth parameter is one of the `AudioFormat.ENCODING_*` constants. The `AudioFormat` constants are also used in MediaFormat to specify audio related values commonly used in media, such as for `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String`

The `https://developer.android.com/reference/kotlin/android/media/AudioFormat.Builder` class can be used to create instances of the `AudioFormat` format class. Refer to `https://developer.android.com/reference/kotlin/android/media/AudioFormat.Builder` for documentation on the mechanics of the configuration and building of such instances. Here we describe the main concepts that the `AudioFormat` class allow you to convey in each instance, they are:

1. [sample rate](AudioFormat.md)
2. [encoding](AudioFormat.md)
3. [channel masks](AudioFormat.md)

Closely associated with the `AudioFormat` is the notion of an [audio frame](AudioFormat.md), which is used throughout the documentation to represent the minimum size complete unit of audio data.

#### Sample rate

Expressed in Hz, the sample rate in an `AudioFormat` instance expresses the number of audio samples for each channel per second in the content you are playing or recording. It is not the sample rate at which content is rendered or produced. For instance a sound at a media sample rate of 8000Hz can be played on a device operating at a sample rate of 48000Hz; the sample rate conversion is automatically handled by the platform, it will not play at 6x speed.

As of API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, sample rates up to 192kHz are supported for `AudioRecord` and `AudioTrack`, with sample rate conversion performed as needed. To improve efficiency and avoid lossy conversions, it is recommended to match the sample rate for `AudioRecord` and `AudioTrack` to the endpoint device sample rate, and limit the sample rate to no more than 48kHz unless there are special device capabilities that warrant a higher rate.

#### Encoding

Audio encoding is used to describe the bit representation of audio data, which can be either linear PCM or compressed audio, such as AC3 or DTS.

For linear PCM, the audio encoding describes the sample size, 8 bits, 16 bits, or 32 bits, and the sample representation, integer or float.

- `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int`: The audio sample is a 8 bit unsigned integer in the range \[0, 255\], with a 128 offset for zero. This is typically stored as a Java byte in a byte array or ByteBuffer. Since the Java byte is *signed*, be careful with math operations and conversions as the most significant bit is inverted.
- `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`: The audio sample is a 16 bit signed integer typically stored as a Java short in a short array, but when the short is stored in a ByteBuffer, it is native endian (as compared to the default Java big endian). The short has full range from \[-32768, 32767\], and is sometimes interpreted as fixed point Q.15 data.
- `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`: Introduced in API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this encoding specifies that the audio sample is a 32 bit IEEE single precision float. The sample can be manipulated as a Java float in a float array, though within a ByteBuffer it is stored in native endian byte order. The nominal range of `ENCODING_PCM_FLOAT` audio data is \[-1.0, 1.0\]. It is implementation dependent whether the positive maximum of 1.0 is included in the interval. Values outside of the nominal range are clamped before sending to the endpoint device. Beware that the handling of NaN is undefined; subnormals may be treated as zero; and infinities are generally clamped just like other values for `AudioTrack` -- try to avoid infinities because they can easily generate a NaN. 
 To achieve higher audio bit depth than a signed 16 bit integer short, it is recommended to use `ENCODING_PCM_FLOAT` for audio capture, processing, and playback. Floats are efficiently manipulated by modern CPUs, have greater precision than 24 bit signed integers, and have greater dynamic range than 32 bit signed integers. `AudioRecord` as of API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` and `AudioTrack` as of API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int` support `ENCODING_PCM_FLOAT`.
- `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_24BIT_PACKED:kotlin.Int`: Introduced in API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, this encoding specifies the audio sample is an extended precision 24 bit signed integer stored as a 3 Java bytes in a `ByteBuffer` or byte array in native endian (see nativeOrder). Each sample has full range from \[-8388608, 8388607\], and can be interpreted as fixed point Q.23 data.
- `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_32BIT:kotlin.Int`: Introduced in API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, this encoding specifies the audio sample is an extended precision 32 bit signed integer stored as a 4 Java bytes in a `ByteBuffer` or byte array in native endian (see nativeOrder). Each sample has full range from \[-2147483648, 2147483647\], and can be interpreted as fixed point Q.31 data.

For compressed audio, the encoding specifies the method of compression, for example `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int`. The compressed audio data is typically stored as bytes in a byte array or ByteBuffer. When a compressed audio encoding is specified for an `AudioTrack`, it creates a direct (non-mixed) track for output to an endpoint (such as HDMI) capable of decoding the compressed audio. For (most) other endpoints, which are not capable of decoding such compressed audio, you will need to decode the data first, typically by creating a MediaCodec. Alternatively, one may use MediaPlayer for playback of compressed audio files or streams.

When compressed audio is sent out through a direct `AudioTrack`, it need not be written in exact multiples of the audio access unit; this differs from `MediaCodec` input buffers.

#### Channel mask

Channel masks are used in `AudioTrack` and `AudioRecord` to describe the samples and their arrangement in the audio frame. They are also used in the endpoint (e.g. a USB audio interface, a DAC connected to headphones) to specify allowable configurations of a particular device. 
As of API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, there are two types of channel masks: channel position masks and channel index masks.

##### Channel position masks

Channel position masks are the original Android channel masks, and are used since API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BASE:kotlin.Int`. For input and output, they imply a positional nature - the location of a speaker or a microphone for recording or playback. 
For a channel position mask, each allowed channel position corresponds to a bit in the channel mask. If that channel position is present in the audio frame, that bit is set, otherwise it is zero. The order of the bits (from lsb to msb) corresponds to the order of that position's sample in the audio frame. 
The canonical channel position masks by channel count are as follows: 

| channel count | channel position mask |
| --- | --- |
| 1 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` |
| 2 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` |
| 3 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_CENTER:kotlin.Int` |
| --- | --- | --- |
| 4 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_QUAD:kotlin.Int` |
| 5 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_QUAD:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_CENTER:kotlin.Int` |
| 6 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1:kotlin.Int` |
| --- | --- |
| 7 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_CENTER:kotlin.Int` |
| 8 | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1_SURROUND:kotlin.Int` |

<br />

These masks are an ORed composite of individual channel masks. For example `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` is composed of `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT:kotlin.Int`.

The following diagram represents the layout of the output channels, as seen from above the listener (in the center at the "lis" position, facing the front-center channel).

```kotlin
TFL --- TFC --- TFR     T is Top
        |  \       |       /  |
        |   FL --- FC --- FR  |     F is Front
        |   |\     |     /|   |
        |   | BFL-BFC-BFR |   |     BF is Bottom Front
        |   |             |   |
        |   FWL   lis   FWR   |     W is Wide
        |   |             |   |
       TSL  SL    TC     SR  TSR    S is Side
        |   |             |   |
        |   BL --- BC -- BR   |     B is Back
        |  /               \  |
        TBL --- TBC --- TBR     C is Center, L/R is Left/Right
  
```
All "T" (top) channels are above the listener, all "BF" (bottom-front) channels are below the listener, all others are in the listener's horizontal plane. When used in conjunction, LFE1 and LFE2 are below the listener, when used alone, LFE plane is undefined. See the channel definitions for the abbreviations

##### Channel index masks

Channel index masks are introduced in API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`. They allow the selection of a particular channel from the source or sink endpoint by number, i.e. the first channel, the second channel, and so forth. This avoids problems with artificially assigning positions to channels of an endpoint, or figuring what the ith position bit is within an endpoint's channel position mask etc. 
Here's an example where channel index masks address this confusion: dealing with a 4 channel USB device. Using a position mask, and based on the channel count, this would be a `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_QUAD:kotlin.Int` device, but really one is only interested in channel 0 through channel 3. The USB device would then have the following individual bit channel masks: `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_LEFT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_RIGHT:kotlin.Int`. But which is channel 0 and which is channel 3? 
For a channel index mask, each channel number is represented as a bit in the mask, from the lsb (channel 0) upwards to the msb, numerically this bit value is `1 << channelNumber`. A set bit indicates that channel is present in the audio frame, otherwise it is cleared. The order of the bits also correspond to that channel number's sample order in the audio frame. 
For the previous 4 channel USB device example, the device would have a channel index mask `0xF`. Suppose we wanted to select only the first and the third channels; this would correspond to a channel index mask `0x5` (the first and third bits set). If an `AudioTrack` uses this channel index mask, the audio frame would consist of two samples, the first sample of each frame routed to channel 0, and the second sample of each frame routed to channel 2. The canonical channel index masks by channel count are given by the formula `(1 << channelCount) - 1`.

##### Use cases

- *Channel position mask for an endpoint:* `CHANNEL_OUT_FRONT_LEFT`, `CHANNEL_OUT_FRONT_CENTER`, etc. for HDMI home theater purposes.
- *Channel position mask for an audio stream:* Creating an `AudioTrack` to output movie content, where 5.1 multichannel output is to be written.
- *Channel index mask for an endpoint:* USB devices for which input and output do not correspond to left or right speaker or microphone.
- *Channel index mask for an audio stream:* An `AudioRecord` may only want the third and fourth audio channels of the endpoint (i.e. the second channel pair), and not care the about position it corresponds to, in which case the channel index mask is `0xC`. Multichannel `AudioRecord` sessions should use channel index masks.

##### Ambisonics channel masks

<br />

As of API `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, another type of channel mask has been added: Ambisonics. This channel mask is used when dealing with audio scenes encoded using [the corresponding spatial format.](https://en.wikipedia.org/wiki/Ambisonics) The inherent requirement of the Ambisonics representation is that it uses certain channel counts that depend on the **order** used. The formula for calculating the channel count for **full sphere** Ambisonics representation is `(N + 1) ^ 2` where `N` is the order. The minimum order supported is `0` (`https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_0:kotlin.Int`) which uses 1 channel, and the maximum order is `14` (`https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_14:kotlin.Int`) which uses 225 channels. Since mobile devices may not possess enough power for dealing with such huge number of channels, the framework also allows using "horizontal-only" representation which significantly reduces the number of channels compared to full sphere. For the horizontal-only representation the number of channels is calculated using the formula `(2 * N + 1)`, thus the 14th horizontal-only representation `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_14_HRZ:kotlin.Int` uses only 29 channels. The Ambisonics channel mask actually only stores the number of channels used, and the flag `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_HORIZONTAL:kotlin.Int` for specifying whether it's a horizontal-only representation. Android assumes that the Ambisonics representation uses ACN channel order and SN3D normalization.

#### Audio Frame

For linear PCM, an audio frame consists of a set of samples captured at the same time, whose count and channel association are given by the [channel mask](AudioFormat.md), and whose sample contents are specified by the [encoding](AudioFormat.md). For example, a stereo 16 bit PCM frame consists of two 16 bit linear PCM samples, with a frame size of 4 bytes. For compressed audio, an audio frame may alternately refer to an access unit of compressed data bytes that is logically grouped together for decoding and bitstream access (e.g. MediaCodec), or a single byte of compressed data (e.g. getBufferSizeInFrames), or the linear PCM frame result from decoding the compressed data (e.g.getPlaybackHeadPosition), depending on the context where audio frame is used. For the purposes of getFrameSizeInBytes, a compressed data format returns a frame size of 1 byte.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/AudioFormat.Builder` Builder class for AudioFormat objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_HORIZONTAL:kotlin.Int` Ambisonics channel mask flag for the horizontal-only representation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_0:kotlin.Int` Ambisonics channel mask for order 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_0_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 0. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_1:kotlin.Int` Ambisonics channel mask for order 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_10:kotlin.Int` Ambisonics channel mask for order 10. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_10_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 10. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_11:kotlin.Int` Ambisonics channel mask for order 11. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_11_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 11. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_12:kotlin.Int` Ambisonics channel mask for order 12. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_12_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 12. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_13:kotlin.Int` Ambisonics channel mask for order 13. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_13_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 13. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_14:kotlin.Int` Ambisonics channel mask for order 14. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_14_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 14. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_1_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 1. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_2:kotlin.Int` Ambisonics channel mask for order 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_2_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_3:kotlin.Int` Ambisonics channel mask for order 3. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_3_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_4:kotlin.Int` Ambisonics channel mask for order 4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_4_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_5:kotlin.Int` Ambisonics channel mask for order 5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_5_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_6:kotlin.Int` Ambisonics channel mask for order 6. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_6_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_7:kotlin.Int` Ambisonics channel mask for order 7. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_7_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 7. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_8:kotlin.Int` Ambisonics channel mask for order 8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_8_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_9:kotlin.Int` Ambisonics channel mask for order 9. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_ACN_ORDER_9_HRZ:kotlin.Int` Ambisonics horizontal-only channel mask for order 9. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_CONFIGURATION_DEFAULT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_CONFIGURATION_INVALID:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_CONFIGURATION_MONO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_CONFIGURATION_STEREO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` Invalid audio channel mask |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_BACK:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_BACK_PROCESSED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_DEFAULT:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_FRONT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_FRONT_PROCESSED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_LEFT:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_LEFT_PROCESSED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_PRESSURE:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_RIGHT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_RIGHT_PROCESSED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_VOICE_DNLINK:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_VOICE_UPLINK:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_X_AXIS:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_Y_AXIS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_Z_AXIS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_13POINT0:kotlin.Int` Output channel mask for 13. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1:kotlin.Int` Output channel mask for 5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1POINT2:kotlin.Int` Output channel mask for 5. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1POINT4:kotlin.Int` Output channel mask for 5. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_6POINT1:kotlin.Int` Output channel mask for 6. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1POINT2:kotlin.Int` Output channel mask for 7. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1POINT4:kotlin.Int` Output channel mask for 7. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1_SURROUND:kotlin.Int` Output channel mask for 7. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_9POINT1POINT4:kotlin.Int` Output channel mask for 9. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_9POINT1POINT6:kotlin.Int` Output channel mask for 9. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_CENTER:kotlin.Int` Back center output channel (see BC in channel diagram) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_LEFT:kotlin.Int` Back left output channel (see BL in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_RIGHT:kotlin.Int` Back right output channel (see BR in channel diagram) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_CENTER:kotlin.Int` Bottom front center output channel (see BFC in channel diagram below FC) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_LEFT:kotlin.Int` Bottom front left output channel (see BFL in channel diagram below FL) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_RIGHT:kotlin.Int` Bottom front right output channel (see BFR in channel diagram below FR) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_DEFAULT:kotlin.Int` Default audio channel mask |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_CENTER:kotlin.Int` Front center output channel (see FC in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT:kotlin.Int` Front left output channel (see FL in channel diagram) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT_OF_CENTER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT:kotlin.Int` Front right output channel (see FR in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT_OF_CENTER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_WIDE_LEFT:kotlin.Int` Front wide left output channel (see FWL in channel diagram) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_WIDE_RIGHT:kotlin.Int` Front wide right output channel (see FWR in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY:kotlin.Int` LFE "low frequency effect" channel When used in conjunction with `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY_2:kotlin.Int`, it is intended to contain the left low-frequency effect signal, also referred to as "LFE1" in ITU-R BS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY_2:kotlin.Int` The second LFE channel When used in conjunction with `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY:kotlin.Int`, it is intended to contain the right low-frequency effect signal, also referred to as "LFE2" in ITU-R BS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_QUAD:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_SIDE_LEFT:kotlin.Int` Side left output channel (see SL in channel diagram) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_SIDE_RIGHT:kotlin.Int` Side right output channel (see SR in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_SURROUND:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_CENTER:kotlin.Int` Top back center output channel (see TBC in channel diagram above BC) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_LEFT:kotlin.Int` Top back left output channel (see TBL in channel diagram above BL) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_RIGHT:kotlin.Int` Top back right output channel (see TBR in channel diagram above BR) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_CENTER:kotlin.Int` Top center (above listener) output channel (see TC in channel diagram) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_CENTER:kotlin.Int` Top front center output channel (see TFC in channel diagram above FC) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_LEFT:kotlin.Int` Top front left output channel (see TFL in channel diagram above FL) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_RIGHT:kotlin.Int` Top front right output channel (see TFR in channel diagram above FR) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_SIDE_LEFT:kotlin.Int` Top side left output channel (see TSL in channel diagram above SL) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_SIDE_RIGHT:kotlin.Int` Top side right output channel (see TSR in channel diagram above SR) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_ELD:kotlin.Int` Audio data format: AAC ELD compressed |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V1:kotlin.Int` Audio data format: AAC HE V1 compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V2:kotlin.Int` Audio data format: AAC HE V2 compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_LC:kotlin.Int` Audio data format: AAC LC compressed |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_XHE:kotlin.Int` Audio data format: AAC xHE compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` Audio data format: AC-3 compressed, also known as Dolby Digital |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4:kotlin.Int` Audio data format: AC-4 (levels 0-3) sync frame transport format |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4_L4:kotlin.Int` Audio data format: AC-4 level 4 sync frame transport format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DEFAULT:kotlin.Int` Default audio data format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_MAT:kotlin.Int` Audio data format: Dolby MAT (Metadata-enhanced Audio Transmission) Dolby MAT bitstreams are used to transmit Dolby TrueHD, channel-based PCM, or PCM with metadata (object audio) over HDMI (e.g. Dolby Atmos content). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_TRUEHD:kotlin.Int` Audio data format: DOLBY TRUEHD compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DRA:kotlin.Int` Audio data format: DRA compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DSD:kotlin.Int` Audio data format: Direct Stream Digital |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int` Audio data format: DTS compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` Audio data format: DTS HD compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` Audio data format: DTS HD Master Audio compressed DTS HD Master Audio stream is variable bit rate and contains lossless audio. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD:kotlin.Int` Audio data format: DTS UHD Profile-1 compressed (aka DTS:X Profile 1) Has the same meaning and value as ENCODING_DTS_UHD_P1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` Audio data format: DTS UHD Profile-1 compressed (aka DTS:X Profile 1) Has the same meaning and value as the deprecated `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` Audio data format: DTS UHD Profile-2 compressed DTS-UHD Profile-2 supports delivery of Channel-Based Audio, Object-Based Audio and High Order Ambisonic presentations up to the fourth order. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` Audio data format: E-AC-3 compressed, also known as Dolby Digital Plus or DD+ |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int` Audio data format: E-AC-3-JOC compressed E-AC-3-JOC streams can be decoded by downstream devices supporting `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_AAC:kotlin.Int` Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_FLAC:kotlin.Int` Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_OPUS:kotlin.Int` Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_PCM:kotlin.Int` Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_AAC:kotlin.Int` Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_FLAC:kotlin.Int` Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_OPUS:kotlin.Int` Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_PCM:kotlin.Int` Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_AAC:kotlin.Int` Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_FLAC:kotlin.Int` Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_OPUS:kotlin.Int` Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_PCM:kotlin.Int` Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IEC61937:kotlin.Int` Audio data format: compressed audio wrapped in PCM for HDMI or S/PDIF passthrough. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_INVALID:kotlin.Int` Invalid audio data format |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MP3:kotlin.Int` Audio data format: MP3 compressed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L3:kotlin.Int` Audio data format: MPEG-H baseline profile, level 3 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L4:kotlin.Int` Audio data format: MPEG-H baseline profile, level 4 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L3:kotlin.Int` Audio data format: MPEG-H low complexity profile, level 3 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L4:kotlin.Int` Audio data format: MPEG-H low complexity profile, level 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_OPUS:kotlin.Int` Audio data format: OPUS compressed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` Audio data format: PCM 16 bit per sample. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_24BIT_PACKED:kotlin.Int` Audio data format: PCM 24 bit per sample packed as 3 bytes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_32BIT:kotlin.Int` Audio data format: PCM 32 bit per sample. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int` Audio data format: PCM 8 bit per sample. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int` Audio data format: single-precision floating-point per sample |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int` Sample rate will be a route-dependent value. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelAcnMask Return the Ambisonics channel mask. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelCount Return the channel count. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelIndexMask Return the channel index mask. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelMask Return the channel mask. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEncoding Return the encoding. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFrameSizeInBytes Return the frame size in bytes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSampleRate Return the sample rate. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AudioFormat](AudioFormat.md)!\> | `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CHANNEL_ACN_HORIZONTAL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_HORIZONTAL: Int
```

Ambisonics channel mask flag for the horizontal-only representation.

 Value: 512

### CHANNEL_ACN_ORDER_0

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_0: Int
```

Ambisonics channel mask for order 0.

 Value: 1

### CHANNEL_ACN_ORDER_0_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_0_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 0.

 Value: 513

### CHANNEL_ACN_ORDER_1

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_1: Int
```

Ambisonics channel mask for order 1.

 Value: 4

### CHANNEL_ACN_ORDER_10

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_10: Int
```

Ambisonics channel mask for order 10.

 Value: 121

### CHANNEL_ACN_ORDER_10_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_10_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 10.

 Value: 533

### CHANNEL_ACN_ORDER_11

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_11: Int
```

Ambisonics channel mask for order 11.

 Value: 144

### CHANNEL_ACN_ORDER_11_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_11_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 11.

 Value: 535

### CHANNEL_ACN_ORDER_12

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_12: Int
```

Ambisonics channel mask for order 12.

 Value: 169

### CHANNEL_ACN_ORDER_12_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_12_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 12.

 Value: 537

### CHANNEL_ACN_ORDER_13

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_13: Int
```

Ambisonics channel mask for order 13.

 Value: 196

### CHANNEL_ACN_ORDER_13_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_13_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 13.

 Value: 539

### CHANNEL_ACN_ORDER_14

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_14: Int
```

Ambisonics channel mask for order 14.

 Value: 225

### CHANNEL_ACN_ORDER_14_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_14_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 14.

 Value: 541

### CHANNEL_ACN_ORDER_1_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_1_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 1.

 Value: 515

### CHANNEL_ACN_ORDER_2

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_2: Int
```

Ambisonics channel mask for order 2.

 Value: 9

### CHANNEL_ACN_ORDER_2_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_2_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 2.

 Value: 517

### CHANNEL_ACN_ORDER_3

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_3: Int
```

Ambisonics channel mask for order 3.

 Value: 16

### CHANNEL_ACN_ORDER_3_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_3_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 3.

 Value: 519

### CHANNEL_ACN_ORDER_4

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_4: Int
```

Ambisonics channel mask for order 4.

 Value: 25

### CHANNEL_ACN_ORDER_4_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_4_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 4.

 Value: 521

### CHANNEL_ACN_ORDER_5

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_5: Int
```

Ambisonics channel mask for order 5.

 Value: 36

### CHANNEL_ACN_ORDER_5_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_5_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 5.

 Value: 523

### CHANNEL_ACN_ORDER_6

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_6: Int
```

Ambisonics channel mask for order 6.

 Value: 49

### CHANNEL_ACN_ORDER_6_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_6_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 6.

 Value: 525

### CHANNEL_ACN_ORDER_7

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_7: Int
```

Ambisonics channel mask for order 7.

 Value: 64

### CHANNEL_ACN_ORDER_7_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_7_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 7.

 Value: 527

### CHANNEL_ACN_ORDER_8

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_8: Int
```

Ambisonics channel mask for order 8.

 Value: 81

### CHANNEL_ACN_ORDER_8_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_8_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 8.

 Value: 529

### CHANNEL_ACN_ORDER_9

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_9: Int
```

Ambisonics channel mask for order 9.

 Value: 100

### CHANNEL_ACN_ORDER_9_HRZ

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_ACN_ORDER_9_HRZ: Int
```

Ambisonics horizontal-only channel mask for order 9.

 Value: 531

### CHANNEL_CONFIGURATION_DEFAULT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_CONFIGURATION_DEFAULT: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_DEFAULT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_DEFAULT:kotlin.Int` instead.*

 Value: 1

### CHANNEL_CONFIGURATION_INVALID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_CONFIGURATION_INVALID: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` instead.*

 Value: 0

### CHANNEL_CONFIGURATION_MONO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_CONFIGURATION_MONO: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_MONO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_MONO:kotlin.Int` instead.*

 Value: 2

### CHANNEL_CONFIGURATION_STEREO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_CONFIGURATION_STEREO: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int` instead.*

 Value: 3

### CHANNEL_INVALID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_INVALID: Int
```

Invalid audio channel mask

 Value: 0

### CHANNEL_IN_BACK

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_BACK: Int
```

 Value: 32

### CHANNEL_IN_BACK_PROCESSED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_BACK_PROCESSED: Int
```

 Value: 512

### CHANNEL_IN_DEFAULT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_DEFAULT: Int
```

 Value: 1

### CHANNEL_IN_FRONT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_FRONT: Int
```

 Value: 16

### CHANNEL_IN_FRONT_PROCESSED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_FRONT_PROCESSED: Int
```

 Value: 256

### CHANNEL_IN_LEFT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_LEFT: Int
```

 Value: 4

### CHANNEL_IN_LEFT_PROCESSED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_LEFT_PROCESSED: Int
```

 Value: 64

### CHANNEL_IN_MONO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_MONO: Int
```

 Value: 16

### CHANNEL_IN_PRESSURE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_PRESSURE: Int
```

 Value: 1024

### CHANNEL_IN_RIGHT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_RIGHT: Int
```

 Value: 8

### CHANNEL_IN_RIGHT_PROCESSED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_RIGHT_PROCESSED: Int
```

 Value: 128

### CHANNEL_IN_STEREO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_STEREO: Int
```

 Value: 12

### CHANNEL_IN_VOICE_DNLINK

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_VOICE_DNLINK: Int
```

 Value: 32768

### CHANNEL_IN_VOICE_UPLINK

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_VOICE_UPLINK: Int
```

 Value: 16384

### CHANNEL_IN_X_AXIS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_X_AXIS: Int
```

 Value: 2048

### CHANNEL_IN_Y_AXIS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_Y_AXIS: Int
```

 Value: 4096

### CHANNEL_IN_Z_AXIS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_IN_Z_AXIS: Int
```

 Value: 8192

### CHANNEL_OUT_13POINT0

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_13POINT0: Int
```

Output channel mask for 13.0

 Value: 30136348

### CHANNEL_OUT_5POINT1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_5POINT1: Int
```

Output channel mask for 5.1

 Value: 252

### CHANNEL_OUT_5POINT1POINT2

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_5POINT1POINT2: Int
```

Output channel mask for 5.1.2 Same as 5.1 with the addition of left and right top channels

 Value: 3145980

### CHANNEL_OUT_5POINT1POINT4

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_5POINT1POINT4: Int
```

Output channel mask for 5.1.4 Same as 5.1 with the addition of four top channels

 Value: 737532

### CHANNEL_OUT_6POINT1

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_6POINT1: Int
```

Output channel mask for 6.1 Same as 5.1 with the addition of the back center channel

 Value: 1276

### CHANNEL_OUT_7POINT1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_7POINT1: Int
```

**Deprecated:** *Not the typical 7.1 surround configuration. Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1_SURROUND:kotlin.Int` instead.*

 Value: 1020

### CHANNEL_OUT_7POINT1POINT2

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_7POINT1POINT2: Int
```

Output channel mask for 7.1.2 Same as 7.1 with the addition of left and right top channels

 Value: 3152124

### CHANNEL_OUT_7POINT1POINT4

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_7POINT1POINT4: Int
```

Output channel mask for 7.1.4 Same as 7.1 with the addition of four top channels

 Value: 743676

### CHANNEL_OUT_7POINT1_SURROUND

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_7POINT1_SURROUND: Int
```

Output channel mask for 7.1

 Value: 6396

### CHANNEL_OUT_9POINT1POINT4

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_9POINT1POINT4: Int
```

Output channel mask for 9.1.4 Same as 7.1.4 with the addition of left and right front wide channels

 Value: 202070268

### CHANNEL_OUT_9POINT1POINT6

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_9POINT1POINT6: Int
```

Output channel mask for 9.1.6 Same as 9.1.4 with the addition of left and right top side channels

 Value: 205215996

### CHANNEL_OUT_BACK_CENTER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BACK_CENTER: Int
```

Back center output channel (see BC in channel diagram)

 Value: 1024

### CHANNEL_OUT_BACK_LEFT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BACK_LEFT: Int
```

Back left output channel (see BL in channel diagram)

 Value: 64

### CHANNEL_OUT_BACK_RIGHT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BACK_RIGHT: Int
```

Back right output channel (see BR in channel diagram)

 Value: 128

### CHANNEL_OUT_BOTTOM_FRONT_CENTER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BOTTOM_FRONT_CENTER: Int
```

Bottom front center output channel (see BFC in channel diagram below FC)

 Value: 8388608

### CHANNEL_OUT_BOTTOM_FRONT_LEFT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BOTTOM_FRONT_LEFT: Int
```

Bottom front left output channel (see BFL in channel diagram below FL)

 Value: 4194304

### CHANNEL_OUT_BOTTOM_FRONT_RIGHT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_BOTTOM_FRONT_RIGHT: Int
```

Bottom front right output channel (see BFR in channel diagram below FR)

 Value: 16777216

### CHANNEL_OUT_DEFAULT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_DEFAULT: Int
```

Default audio channel mask

 Value: 1

### CHANNEL_OUT_FRONT_CENTER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_CENTER: Int
```

Front center output channel (see FC in channel diagram)

 Value: 16

### CHANNEL_OUT_FRONT_LEFT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_LEFT: Int
```

Front left output channel (see FL in channel diagram)

 Value: 4

### CHANNEL_OUT_FRONT_LEFT_OF_CENTER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_LEFT_OF_CENTER: Int
```

 Value: 256

### CHANNEL_OUT_FRONT_RIGHT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_RIGHT: Int
```

Front right output channel (see FR in channel diagram)

 Value: 8

### CHANNEL_OUT_FRONT_RIGHT_OF_CENTER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_RIGHT_OF_CENTER: Int
```

 Value: 512

### CHANNEL_OUT_FRONT_WIDE_LEFT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_WIDE_LEFT: Int
```

Front wide left output channel (see FWL in channel diagram)

 Value: 67108864

### CHANNEL_OUT_FRONT_WIDE_RIGHT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_FRONT_WIDE_RIGHT: Int
```

Front wide right output channel (see FWR in channel diagram)

 Value: 134217728

### CHANNEL_OUT_LOW_FREQUENCY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_LOW_FREQUENCY: Int
```

LFE "low frequency effect" channel When used in conjunction with `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY_2:kotlin.Int`, it is intended to contain the left low-frequency effect signal, also referred to as "LFE1" in ITU-R BS.2159-8

 Value: 32

### CHANNEL_OUT_LOW_FREQUENCY_2

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_LOW_FREQUENCY_2: Int
```

The second LFE channel When used in conjunction with `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY:kotlin.Int`, it is intended to contain the right low-frequency effect signal, also referred to as "LFE2" in ITU-R BS.2159-8

 Value: 33554432

### CHANNEL_OUT_MONO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_MONO: Int
```

 Value: 4

### CHANNEL_OUT_QUAD

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_QUAD: Int
```

 Value: 204

### CHANNEL_OUT_SIDE_LEFT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_SIDE_LEFT: Int
```

Side left output channel (see SL in channel diagram)

 Value: 2048

### CHANNEL_OUT_SIDE_RIGHT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_SIDE_RIGHT: Int
```

Side right output channel (see SR in channel diagram)

 Value: 4096

### CHANNEL_OUT_STEREO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_STEREO: Int
```

 Value: 12

### CHANNEL_OUT_SURROUND

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_SURROUND: Int
```

 Value: 1052

### CHANNEL_OUT_TOP_BACK_CENTER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_BACK_CENTER: Int
```

Top back center output channel (see TBC in channel diagram above BC)

 Value: 262144

### CHANNEL_OUT_TOP_BACK_LEFT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_BACK_LEFT: Int
```

Top back left output channel (see TBL in channel diagram above BL)

 Value: 131072

### CHANNEL_OUT_TOP_BACK_RIGHT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_BACK_RIGHT: Int
```

Top back right output channel (see TBR in channel diagram above BR)

 Value: 524288

### CHANNEL_OUT_TOP_CENTER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_CENTER: Int
```

Top center (above listener) output channel (see TC in channel diagram)

 Value: 8192

### CHANNEL_OUT_TOP_FRONT_CENTER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_FRONT_CENTER: Int
```

Top front center output channel (see TFC in channel diagram above FC)

 Value: 32768

### CHANNEL_OUT_TOP_FRONT_LEFT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_FRONT_LEFT: Int
```

Top front left output channel (see TFL in channel diagram above FL)

 Value: 16384

### CHANNEL_OUT_TOP_FRONT_RIGHT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_FRONT_RIGHT: Int
```

Top front right output channel (see TFR in channel diagram above FR)

 Value: 65536

### CHANNEL_OUT_TOP_SIDE_LEFT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_SIDE_LEFT: Int
```

Top side left output channel (see TSL in channel diagram above SL)

 Value: 1048576

### CHANNEL_OUT_TOP_SIDE_RIGHT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHANNEL_OUT_TOP_SIDE_RIGHT: Int
```

Top side right output channel (see TSR in channel diagram above SR)

 Value: 2097152

### ENCODING_AAC_ELD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AAC_ELD: Int
```

Audio data format: AAC ELD compressed

 Value: 15

### ENCODING_AAC_HE_V1

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AAC_HE_V1: Int
```

Audio data format: AAC HE V1 compressed

 Value: 11

### ENCODING_AAC_HE_V2

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AAC_HE_V2: Int
```

Audio data format: AAC HE V2 compressed

 Value: 12

### ENCODING_AAC_LC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AAC_LC: Int
```

Audio data format: AAC LC compressed

 Value: 10

### ENCODING_AAC_XHE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AAC_XHE: Int
```

Audio data format: AAC xHE compressed

 Value: 16

### ENCODING_AC3

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AC3: Int
```

Audio data format: AC-3 compressed, also known as Dolby Digital

 Value: 5

### ENCODING_AC4

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AC4: Int
```

Audio data format: AC-4 (levels 0-3) sync frame transport format

 Value: 17

### ENCODING_AC4_L4

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_AC4_L4: Int
```

Audio data format: AC-4 level 4 sync frame transport format

 Value: 32

### ENCODING_DEFAULT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DEFAULT: Int
```

Default audio data format

 Value: 1

### ENCODING_DOLBY_MAT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DOLBY_MAT: Int
```

Audio data format: Dolby MAT (Metadata-enhanced Audio Transmission) Dolby MAT bitstreams are used to transmit Dolby TrueHD, channel-based PCM, or PCM with metadata (object audio) over HDMI (e.g. Dolby Atmos content).

 Value: 19

### ENCODING_DOLBY_TRUEHD

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DOLBY_TRUEHD: Int
```

Audio data format: DOLBY TRUEHD compressed

 Value: 14

### ENCODING_DRA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DRA: Int
```

Audio data format: DRA compressed

 Value: 28

### ENCODING_DSD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DSD: Int
```

Audio data format: Direct Stream Digital

 Value: 31

### ENCODING_DTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS: Int
```

Audio data format: DTS compressed

 Value: 7

### ENCODING_DTS_HD

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS_HD: Int
```

Audio data format: DTS HD compressed

 Value: 8

### ENCODING_DTS_HD_MA

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS_HD_MA: Int
```

Audio data format: DTS HD Master Audio compressed DTS HD Master Audio stream is variable bit rate and contains lossless audio. Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` for lossless audio content (DTS-HD MA Lossless) and use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` for other DTS bitstreams with extension substream (DTS 8Ch Discrete, DTS Hi Res, DTS Express).

 Value: 29

### ENCODING_DTS_UHD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS_UHD: Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` instead.*

Audio data format: DTS UHD Profile-1 compressed (aka DTS:X Profile 1) Has the same meaning and value as ENCODING_DTS_UHD_P1.

 Value: 27

### ENCODING_DTS_UHD_P1

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS_UHD_P1: Int
```

Audio data format: DTS UHD Profile-1 compressed (aka DTS:X Profile 1) Has the same meaning and value as the deprecated `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD:kotlin.Int`.

 Value: 27

### ENCODING_DTS_UHD_P2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_DTS_UHD_P2: Int
```

Audio data format: DTS UHD Profile-2 compressed DTS-UHD Profile-2 supports delivery of Channel-Based Audio, Object-Based Audio and High Order Ambisonic presentations up to the fourth order. Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` to transmit DTS UHD Profile 1 (aka DTS:X Profile 1) bitstream. Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` to transmit DTS UHD Profile 2 (aka DTS:X Profile 2) bitstream.

 Value: 30

### ENCODING_E_AC3

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_E_AC3: Int
```

Audio data format: E-AC-3 compressed, also known as Dolby Digital Plus or DD+

 Value: 6

### ENCODING_E_AC3_JOC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_E_AC3_JOC: Int
```

Audio data format: E-AC-3-JOC compressed E-AC-3-JOC streams can be decoded by downstream devices supporting `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int`. Use `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` as the AudioTrack encoding when the downstream device supports `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` but not `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int`.

 Value: 18

### ENCODING_IAMF_BASE_ENHANCED_PROFILE_AAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_ENHANCED_PROFILE_AAC: Int
```

Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC.

 Value: 42

### ENCODING_IAMF_BASE_ENHANCED_PROFILE_FLAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_ENHANCED_PROFILE_FLAC: Int
```

Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC.

 Value: 43

### ENCODING_IAMF_BASE_ENHANCED_PROFILE_OPUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_ENHANCED_PROFILE_OPUS: Int
```

Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS.

 Value: 41

### ENCODING_IAMF_BASE_ENHANCED_PROFILE_PCM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_ENHANCED_PROFILE_PCM: Int
```

Audio data format: IAMF using the [base-enhanced profile](https://aomediacodec.github.io/iamf/#profiles-base-enhanced) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM.

 Value: 44

### ENCODING_IAMF_BASE_PROFILE_AAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_PROFILE_AAC: Int
```

Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC.

 Value: 38

### ENCODING_IAMF_BASE_PROFILE_FLAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_PROFILE_FLAC: Int
```

Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC.

 Value: 39

### ENCODING_IAMF_BASE_PROFILE_OPUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_PROFILE_OPUS: Int
```

Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS.

 Value: 37

### ENCODING_IAMF_BASE_PROFILE_PCM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_BASE_PROFILE_PCM: Int
```

Audio data format: IAMF using the [base profile](https://aomediacodec.github.io/iamf/#profiles-base) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM.

 Value: 40

### ENCODING_IAMF_SIMPLE_PROFILE_AAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_SIMPLE_PROFILE_AAC: Int
```

Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in AAC.

 Value: 34

### ENCODING_IAMF_SIMPLE_PROFILE_FLAC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_SIMPLE_PROFILE_FLAC: Int
```

Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in FLAC.

 Value: 35

### ENCODING_IAMF_SIMPLE_PROFILE_OPUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_SIMPLE_PROFILE_OPUS: Int
```

Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in OPUS.

 Value: 33

### ENCODING_IAMF_SIMPLE_PROFILE_PCM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IAMF_SIMPLE_PROFILE_PCM: Int
```

Audio data format: IAMF using the [simple profile](https://aomediacodec.github.io/iamf/#profiles-simple) with audio streams [encoded](https://aomediacodec.github.io/iamf/#codec_id) in PCM.

 Value: 36

### ENCODING_IEC61937

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_IEC61937: Int
```

Audio data format: compressed audio wrapped in PCM for HDMI or S/PDIF passthrough. For devices whose SDK version is less than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, the channel mask of IEC61937 track must be `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_STEREO:kotlin.Int`. Data should be written to the stream in a short\[\] array. If the data is written in a byte\[\] array then there may be endian problems on some platforms when converting to short internally.

 Value: 13

### ENCODING_INVALID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_INVALID: Int
```

Invalid audio data format

 Value: 0

### ENCODING_MP3

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_MP3: Int
```

Audio data format: MP3 compressed

 Value: 9

### ENCODING_MPEGH_BL_L3

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_MPEGH_BL_L3: Int
```

Audio data format: MPEG-H baseline profile, level 3

 Value: 23

### ENCODING_MPEGH_BL_L4

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_MPEGH_BL_L4: Int
```

Audio data format: MPEG-H baseline profile, level 4

 Value: 24

### ENCODING_MPEGH_LC_L3

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_MPEGH_LC_L3: Int
```

Audio data format: MPEG-H low complexity profile, level 3

 Value: 25

### ENCODING_MPEGH_LC_L4

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_MPEGH_LC_L4: Int
```

Audio data format: MPEG-H low complexity profile, level 4

 Value: 26

### ENCODING_OPUS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_OPUS: Int
```

Audio data format: OPUS compressed.

 Value: 20

### ENCODING_PCM_16BIT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_PCM_16BIT: Int
```

Audio data format: PCM 16 bit per sample. Guaranteed to be supported by devices.

 Value: 2

### ENCODING_PCM_24BIT_PACKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_PCM_24BIT_PACKED: Int
```

Audio data format: PCM 24 bit per sample packed as 3 bytes. The bytes are in little-endian order, so the least significant byte comes first in the byte array. Not guaranteed to be supported by devices, may be emulated if not supported.

 Value: 21

### ENCODING_PCM_32BIT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_PCM_32BIT: Int
```

Audio data format: PCM 32 bit per sample. Not guaranteed to be supported by devices, may be emulated if not supported.

 Value: 22

### ENCODING_PCM_8BIT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_PCM_8BIT: Int
```

Audio data format: PCM 8 bit per sample. Not guaranteed to be supported by devices.

 Value: 3

### ENCODING_PCM_FLOAT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODING_PCM_FLOAT: Int
```

Audio data format: single-precision floating-point per sample

 Value: 4

### SAMPLE_RATE_UNSPECIFIED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_RATE_UNSPECIFIED: Int
```

Sample rate will be a route-dependent value. For AudioTrack, it is usually the sink sample rate, and for AudioRecord it is usually the source sample rate.

 Value: 0

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getChannelAcnMask

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelAcnMask(): Int
```

Return the Ambisonics channel mask. See the section on [Ambisonics channel masks](AudioFormat.md) for more information.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values that can be set in setChannelAcnMask or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` if not set or an invalid mask was used. |

### getChannelCount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelCount(): Int
```

Return the channel count.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the channel count derived from the channel position mask or the channel index mask. Zero is returned if both the channel position mask and the channel index mask are not set. |

### getChannelIndexMask

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelIndexMask(): Int
```

Return the channel index mask. See the section on [channel masks](AudioFormat.md) for more information about the difference between index-based masks, and position-based masks (as returned by getChannelMask).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values that can be set in setChannelIndexMask or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` if not set or an invalid mask was used. |

### getChannelMask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelMask(): Int
```

Return the channel mask. See the section on [channel masks](AudioFormat.md) for more information about the difference between index-based masks(as returned by getChannelIndexMask) and the position-based mask returned by this function.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values that can be set in setChannelMask or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` if not set. |

### getEncoding

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncoding(): Int
```

Return the encoding. See the section on [encodings](AudioFormat.md) for more information about the different types of supported audio encoding.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values that can be set in setEncoding or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_INVALID:kotlin.Int` if not set. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MP3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_LC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IEC61937:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_TRUEHD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_ELD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_XHE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_MAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_24BIT_PACKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_32BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_PCM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_PCM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_PCM:kotlin.Int` |

### getFrameSizeInBytes

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFrameSizeInBytes(): Int
```

Return the frame size in bytes. For PCM or PCM packed compressed data this is the size of a sample multiplied by the channel count. For all other cases, including invalid/unset channel masks, this will return 1 byte. As an example, a stereo 16-bit PCM format would have a frame size of 4 bytes, an 8 channel float PCM format would have a frame size of 32 bytes, and a compressed data format (not packed in PCM) would have a frame size of 1 byte. Both AudioRecord or AudioTrack process data in multiples of this frame size.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The audio frame size in bytes corresponding to the encoding and the channel mask. Value is 1 or greater |

### getSampleRate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSampleRate(): Int
```

Return the sample rate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values that can be set in setSampleRate or `https://developer.android.com/reference/kotlin/android/media/AudioFormat#SAMPLE_RATE_UNSPECIFIED:kotlin.Int` if not set. |

### hashCode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AudioFormat!>
```
