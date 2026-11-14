Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioDeviceInfo

Kotlin | [Java](../android/media/AudioDeviceInfo.md)
| --- | --- |

```
class AudioDeviceInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioDeviceInfo](../android/media/AudioDeviceInfo.md) |

Provides information about an audio device.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_AUX_LINE:kotlin.Int` A device type describing the auxiliary line-level connectors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_BROADCAST:kotlin.Int` A device type describing a Bluetooth Low Energy (BLE) broadcast group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_HEADSET:kotlin.Int` A device type describing a Bluetooth Low Energy (BLE) audio headset or headphones. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_SPEAKER:kotlin.Int` A device type describing a Bluetooth Low Energy (BLE) audio speaker. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_A2DP:kotlin.Int` A device type describing a Bluetooth device supporting the A2DP profile. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_SCO:kotlin.Int` A device type describing a Bluetooth device typically used for telephony. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_EARPIECE:kotlin.Int` A device type describing the attached earphone speaker. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_MIC:kotlin.Int` A device type describing the microphone(s) built in a device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER:kotlin.Int` A device type describing the speaker system (i.e. a mono speaker or stereo speakers) built in a device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER_SAFE:kotlin.Int` A device type describing the speaker system (i.e. a mono speaker or stereo speakers) built in a device, that is specifically tuned for outputting sounds like notifications and alarms (i.e. sounds the user couldn't necessarily anticipate). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUS:kotlin.Int` A type-agnostic device used for communication with external audio systems |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK:kotlin.Int` A device type describing the audio device associated with a dock. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK_ANALOG:kotlin.Int` A device type describing the audio device associated with a dock using an analog connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_FM:kotlin.Int` A device type associated with the transmission of audio signals over FM. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_FM_TUNER:kotlin.Int` A device type for accessing the audio content transmitted over FM. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI:kotlin.Int` A device type describing an HDMI connection . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_ARC:kotlin.Int` A device type describing the Audio Return Channel of an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_EARC:kotlin.Int` A device type describing the Enhanced Audio Return Channel of an HDMI connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HEARING_AID:kotlin.Int` A device type describing a Hearing Aid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_IP:kotlin.Int` A device type connected over IP. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_ANALOG:kotlin.Int` A device type describing an analog line-level connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_DIGITAL:kotlin.Int` A device type describing a digital line connection (e.g. SPDIF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP:kotlin.Int` A device type describing a speaker group that supports multichannel contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_REMOTE_SUBMIX:kotlin.Int` A device type for rerouting audio within the Android framework between mixes and system applications. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_TELEPHONY:kotlin.Int` A device type describing the transmission of audio signals over the telephony network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_TV_TUNER:kotlin.Int` A device type for accessing the audio content transmitted over the TV tuner system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_UNKNOWN:kotlin.Int` A device type associated with an unknown or uninitialized device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_ACCESSORY:kotlin.Int` A device type describing a USB audio device in accessory mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_DEVICE:kotlin.Int` A device type describing a USB audio device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_HEADSET:kotlin.Int` A device type describing a USB audio headset. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADPHONES:kotlin.Int` A device type describing a pair of wired headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADSET:kotlin.Int` A device type describing a headset, which is the combination of a headphones and microphone. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getAddress()()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDescriptor](../android/media/AudioDescriptor.md)!\> | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getAudioDescriptors()()` <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioProfile](../android/media/AudioProfile.md)!\> | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getAudioProfiles()()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getChannelCounts()()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getChannelIndexMasks()()` <br /> |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getChannelMasks()()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getEncapsulationMetadataTypes()()` Returns an array of supported encapsulation metadata types for the device. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getEncapsulationModes()()` Returns an array of supported encapsulation modes for the device. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getEncodings()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getId()()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getProductName()()` <br /> |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getSampleRates()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getSpeakerLayoutChannelMask()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#getType()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#isSink()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#isSource()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#toString()()` Returns a string representation of the object. |

## Constants

### TYPE_AUX_LINE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_AUX_LINE: Int
```

A device type describing the auxiliary line-level connectors.

 Value: 19

### TYPE_BLE_BROADCAST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLE_BROADCAST: Int
```

A device type describing a Bluetooth Low Energy (BLE) broadcast group.

 Value: 30

### TYPE_BLE_HEADSET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLE_HEADSET: Int
```

A device type describing a Bluetooth Low Energy (BLE) audio headset or headphones. Headphones are grouped with headsets when the device is a sink: the features of headsets and headphones with regard to playback are the same.

 Value: 26

### TYPE_BLE_SPEAKER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLE_SPEAKER: Int
```

A device type describing a Bluetooth Low Energy (BLE) audio speaker.

 Value: 27

### TYPE_BLUETOOTH_A2DP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLUETOOTH_A2DP: Int
```

A device type describing a Bluetooth device supporting the A2DP profile.

 Value: 8

### TYPE_BLUETOOTH_SCO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BLUETOOTH_SCO: Int
```

A device type describing a Bluetooth device typically used for telephony.

 Value: 7

### TYPE_BUILTIN_EARPIECE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUILTIN_EARPIECE: Int
```

A device type describing the attached earphone speaker.

 Value: 1

### TYPE_BUILTIN_MIC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUILTIN_MIC: Int
```

A device type describing the microphone(s) built in a device.

 Value: 15

### TYPE_BUILTIN_SPEAKER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUILTIN_SPEAKER: Int
```

A device type describing the speaker system (i.e. a mono speaker or stereo speakers) built in a device.

 Value: 2

### TYPE_BUILTIN_SPEAKER_SAFE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUILTIN_SPEAKER_SAFE: Int
```

A device type describing the speaker system (i.e. a mono speaker or stereo speakers) built in a device, that is specifically tuned for outputting sounds like notifications and alarms (i.e. sounds the user couldn't necessarily anticipate).

Note that this physical audio device may be the same as `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER:kotlin.Int` but is driven differently to safely accommodate the different use case.

 Value: 24

### TYPE_BUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUS: Int
```

A type-agnostic device used for communication with external audio systems

 Value: 21

### TYPE_DOCK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DOCK: Int
```

A device type describing the audio device associated with a dock. Starting at API 34, this device type only represents digital docks, while docks with an analog connection are represented with `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK_ANALOG:kotlin.Int`.

 Value: 13

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK_ANALOG:kotlin.Int`

### TYPE_DOCK_ANALOG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DOCK_ANALOG: Int
```

A device type describing the audio device associated with a dock using an analog connection.

 Value: 31

### TYPE_FM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FM: Int
```

A device type associated with the transmission of audio signals over FM.

 Value: 14

### TYPE_FM_TUNER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FM_TUNER: Int
```

A device type for accessing the audio content transmitted over FM.

 Value: 16

### TYPE_HDMI

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HDMI: Int
```

A device type describing an HDMI connection .

 Value: 9

### TYPE_HDMI_ARC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HDMI_ARC: Int
```

A device type describing the Audio Return Channel of an HDMI connection.

 Value: 10

### TYPE_HDMI_EARC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HDMI_EARC: Int
```

A device type describing the Enhanced Audio Return Channel of an HDMI connection.

 Value: 29

### TYPE_HEARING_AID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_HEARING_AID: Int
```

A device type describing a Hearing Aid.

 Value: 23

### TYPE_IP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_IP: Int
```

A device type connected over IP.

 Value: 20

### TYPE_LINE_ANALOG

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LINE_ANALOG: Int
```

A device type describing an analog line-level connection.

 Value: 5

### TYPE_LINE_DIGITAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LINE_DIGITAL: Int
```

A device type describing a digital line connection (e.g. SPDIF).

 Value: 6

### TYPE_MULTICHANNEL_GROUP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MULTICHANNEL_GROUP: Int
```

A device type describing a speaker group that supports multichannel contents. The speakers in the group are connected together using local network based protocols. The speaker group requires additional input of the physical positions of each individual speaker to provide a better experience on multichannel contents.

 Value: 32

### TYPE_REMOTE_SUBMIX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_REMOTE_SUBMIX: Int
```

A device type for rerouting audio within the Android framework between mixes and system applications. This type is for instance encountered when querying the output device of a track (with `https://developer.android.com/reference/kotlin/android/media/AudioTrack#getRoutedDevice()` playing from a device in screen mirroring mode, where the audio is not heard on the device, but on the remote device.

 Value: 25

### TYPE_TELEPHONY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TELEPHONY: Int
```

A device type describing the transmission of audio signals over the telephony network.

 Value: 18

### TYPE_TV_TUNER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TV_TUNER: Int
```

A device type for accessing the audio content transmitted over the TV tuner system.

 Value: 17

### TYPE_UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_UNKNOWN: Int
```

A device type associated with an unknown or uninitialized device.

 Value: 0

### TYPE_USB_ACCESSORY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_USB_ACCESSORY: Int
```

A device type describing a USB audio device in accessory mode.

 Value: 12

### TYPE_USB_DEVICE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_USB_DEVICE: Int
```

A device type describing a USB audio device.

 Value: 11

### TYPE_USB_HEADSET

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_USB_HEADSET: Int
```

A device type describing a USB audio headset.

 Value: 22

### TYPE_WIRED_HEADPHONES

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WIRED_HEADPHONES: Int
```

A device type describing a pair of wired headphones.

 Value: 4

### TYPE_WIRED_HEADSET

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_WIRED_HEADSET: Int
```

A device type describing a headset, which is the combination of a headphones and microphone.

 Value: 3

## Public methods

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getAddress

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): String
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The "address" string of the device. This generally contains device-specific parameters. This value cannot be `null`. |

### getAudioDescriptors

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioDescriptors(): MutableList<AudioDescriptor!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioDescriptor!>` | A list of `https://developer.android.com/reference/kotlin/android/media/AudioDescriptor` supported by the audio devices. This value cannot be `null`. |

### getAudioProfiles

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioProfiles(): MutableList<AudioProfile!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioProfile!>` | A list of `https://developer.android.com/reference/kotlin/android/media/AudioProfile` supported by the audio devices. This value cannot be `null`. |

### getChannelCounts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelCounts(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of channel counts (1, 2, 4, ...) for which this audio device can be configured. Note: an empty array indicates that the device supports arbitrary channel counts. This value cannot be `null`. |

### getChannelIndexMasks

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelIndexMasks(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of channel index masks for which this audio device can be configured. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioFormat`

### getChannelMasks

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChannelMasks(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of channel position masks (e.g. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_IN_STEREO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1:kotlin.Int`) for which this audio device can be configured. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioFormat`

### getEncapsulationMetadataTypes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncapsulationMetadataTypes(): IntArray
```

Returns an array of supported encapsulation metadata types for the device. The metadata type returned should be allowed for all encapsulation modes supported by the device. Some metadata types may apply only to certain compressed stream formats, the returned list is the union of subsets. The array can include any of `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_FRAMEWORK_TUNER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_DVB_AD_DESCRIPTOR:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of supported encapsulation metadata types for the device. This may be an empty array if no metadata types are supported. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_FRAMEWORK_TUNER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_DVB_AD_DESCRIPTOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_METADATA_TYPE_SUPPLEMENTARY_AUDIO_PLACEMENT:kotlin.Int` |

### getEncapsulationModes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncapsulationModes(): IntArray
```

Returns an array of supported encapsulation modes for the device. The array can include any of the `AudioTrack` encapsulation modes, e.g. `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_ELEMENTARY_STREAM:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of supported encapsulation modes for the device. This may be an empty array if no encapsulation modes are supported. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioTrack#ENCAPSULATION_MODE_ELEMENTARY_STREAM:kotlin.Int` |

### getEncodings

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncodings(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of audio encodings (e.g. `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int`) supported by the audio device. `ENCODING_PCM_FLOAT` indicates the device supports more than 16 bits of integer precision. As there is no AudioFormat constant specifically defined for 24-bit PCM, the value `ENCODING_PCM_FLOAT` indicates that `https://developer.android.com/reference/kotlin/android/media/AudioTrack` or `https://developer.android.com/reference/kotlin/android/media/AudioRecord` can preserve at least 24 bits of integer precision to that device. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioFormat`

### getId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The internal device ID. |

### getProductName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProductName(): CharSequence!
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The human-readable name of the audio device. |

### getSampleRates

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSampleRates(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | An array of sample rates supported by the audio device. Note: an empty array indicates that the device supports arbitrary rates. This value cannot be `null`. |

### getSpeakerLayoutChannelMask

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSpeakerLayoutChannelMask(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A ChannelMask representing the speaker layout of a TYPE_BUILTIN_SPEAKER device. Valid only for speakers built-in to the device. The layout channel mask only indicates which speaker channels are present, the physical layout of the speakers should be informed by a standard for multi-channel sound playback systems, such as ITU-R BS.2051. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_LEFT_OF_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_RIGHT_OF_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BACK_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_SIDE_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_SIDE_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_FRONT_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_BACK_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_SIDE_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_TOP_SIDE_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_CENTER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_BOTTOM_FRONT_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_LOW_FREQUENCY_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_WIDE_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_FRONT_WIDE_RIGHT:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioFormat`

### getType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The device type identifier of the audio device (i.e. TYPE_BUILTIN_SPEAKER). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADPHONES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_SCO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_A2DP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_ACCESSORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_TELEPHONY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_ANALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_ARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_EARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_DIGITAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_FM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_AUX_LINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HEARING_AID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_MIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_FM_TUNER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_TV_TUNER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER_SAFE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_REMOTE_SUBMIX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_BROADCAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK_ANALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP:kotlin.Int` |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isSink

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSink(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the audio device is a sink for audio data (i.e. an output). |

### isSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSource(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the audio device is a source for audio data (e.e an input). |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
