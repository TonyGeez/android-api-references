# MediaRoute2Info

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRoute2Info

Kotlin| [Java](../android/media/MediaRoute2Info.md) 
| --- | --- |

```
class MediaRoute2Info : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaRoute2Info](../android/media/MediaRoute2Info.md) |

Describes the properties of a route.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/MediaRoute2Info.Builder.md) Builder for [media route info](../android/media/MediaRoute2Info.md). |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_CONNECTED](../android/media/MediaRoute2Info.md) A connection state indicating the route is connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_CONNECTING](../android/media/MediaRoute2Info.md) A connection state indicating the route is in the process of connecting and is not yet ready for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_DISCONNECTED](../android/media/MediaRoute2Info.md) The default connection state indicating the route is disconnected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_LIVE_AUDIO](../android/media/MediaRoute2Info.md) Route feature: Live audio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_LIVE_VIDEO](../android/media/MediaRoute2Info.md) Route feature: Live video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_AUDIO_PLAYBACK](../android/media/MediaRoute2Info.md) Route feature: Remote audio playback. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_PLAYBACK](../android/media/MediaRoute2Info.md) Route feature: Remote playback. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_VIDEO_PLAYBACK](../android/media/MediaRoute2Info.md) Route feature: Remote video playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_FIXED](../android/media/MediaRoute2Info.md) Playback information indicating the playback volume is fixed, i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_VARIABLE](../android/media/MediaRoute2Info.md) Playback information indicating the playback volume is variable and can be controlled from this object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER](../android/media/MediaRoute2Info.md) Indicates that the route is never suitable for media playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER](../android/media/MediaRoute2Info.md) Indicates the route is always suitable for media playback. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER](../android/media/MediaRoute2Info.md) Indicates that the route is suitable for media playback only after explicit user selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_AUX_LINE](../android/media/MediaRoute2Info.md) Indicates the route is using the auxiliary line-level connectors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BLE_HEADSET](../android/media/MediaRoute2Info.md) Indicates the route is a Bluetooth Low Energy (BLE) HEADSET. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BLUETOOTH_A2DP](../android/media/MediaRoute2Info.md) Indicates the route is a bluetooth device, such as a bluetooth speaker or headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BUILTIN_SPEAKER](../android/media/MediaRoute2Info.md) Indicates the route is the speaker system (i.e. a mono speaker or stereo speakers) built into the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DOCK](../android/media/MediaRoute2Info.md) Indicates the route is the audio device associated with a dock. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GROUP](../android/media/MediaRoute2Info.md) Indicates the route is a group of devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI](../android/media/MediaRoute2Info.md) Indicates the route is an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI_ARC](../android/media/MediaRoute2Info.md) Indicates the route is an Audio Return Channel of an HDMI connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI_EARC](../android/media/MediaRoute2Info.md) Indicates the route is an Enhanced Audio Return Channel of an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HEARING_AID](../android/media/MediaRoute2Info.md) Indicates the route is a hearing aid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINE_ANALOG](../android/media/MediaRoute2Info.md) Indicates the route is an analog line-level connection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINE_DIGITAL](../android/media/MediaRoute2Info.md) Indicates the route is a digital line connection (for example S/PDIF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MULTICHANNEL_SPEAKER_GROUP](../android/media/MediaRoute2Info.md) Indicates the route is a speaker group supporting multichannel contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_AUDIO_VIDEO_RECEIVER](../android/media/MediaRoute2Info.md) Indicates the route is a remote Audio/Video Receiver (AVR). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_CAR](../android/media/MediaRoute2Info.md) Indicates the route is a remote car. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_COMPUTER](../android/media/MediaRoute2Info.md) Indicates the route is a remote computer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_GAME_CONSOLE](../android/media/MediaRoute2Info.md) Indicates the route is a remote gaming console. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SMARTPHONE](../android/media/MediaRoute2Info.md) Indicates the route is a remote smartphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SMARTWATCH](../android/media/MediaRoute2Info.md) Indicates the route is a remote smartwatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SPEAKER](../android/media/MediaRoute2Info.md) Indicates the route is a remote speaker. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TABLET](../android/media/MediaRoute2Info.md) Indicates the route is a remote tablet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TABLET_DOCKED](../android/media/MediaRoute2Info.md) Indicates the route is a remote docked tablet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TV](../android/media/MediaRoute2Info.md) Indicates the route is a remote TV. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](../android/media/MediaRoute2Info.md) Indicates the route's type is unknown or undefined. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_ACCESSORY](../android/media/MediaRoute2Info.md) Indicates the route is a USB audio device in accessory mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_DEVICE](../android/media/MediaRoute2Info.md) Indicates the route is a USB audio device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_HEADSET](../android/media/MediaRoute2Info.md) Indicates the route is a USB audio headset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WIRED_HEADPHONES](../android/media/MediaRoute2Info.md) Indicates the route is a pair of wired headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WIRED_HEADSET](../android/media/MediaRoute2Info.md) Indicates the route is a headset, which is the combination of a headphones and a microphone. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/MediaRoute2Info.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/media/MediaRoute2Info.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getClientPackageName](../android/media/MediaRoute2Info.md))`()` Gets the package name of the app using the route. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](../android/media/MediaRoute2Info.md))`()` Gets the connection state of the route. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDeduplicationIds](../android/media/MediaRoute2Info.md))`()` Gets the deduplication IDs associated to the route. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](../android/media/MediaRoute2Info.md))`()` Gets the user-visible description of the route. |
| --- | --- |
| [Bundle](../android/os/Bundle.md)? | [getExtras](../android/media/MediaRoute2Info.md))`()` Gets an optional bundle with extra data. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getFeatures](../android/media/MediaRoute2Info.md))`()` Gets the supported features of the route. |
| [Uri](../android/net/Uri.md)? | [getIconUri](../android/media/MediaRoute2Info.md))`()` Gets the URI of the icon representing this route. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](../android/media/MediaRoute2Info.md))`()` Gets the id of the route. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getName](../android/media/MediaRoute2Info.md))`()` Gets the user-visible name of the route. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getRequiredPermissions](../android/media/MediaRoute2Info.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSuitabilityStatus](../android/media/MediaRoute2Info.md))`()` Returns the route suitability status. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/media/MediaRoute2Info.md))`()` Returns the type of this route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolume](../android/media/MediaRoute2Info.md))`()` Gets the current volume of the route. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeHandling](../android/media/MediaRoute2Info.md))`()` Gets information about how volume is handled on the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeMax](../android/media/MediaRoute2Info.md))`()` Gets the maximum volume of the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/media/MediaRoute2Info.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemRoute](../android/media/MediaRoute2Info.md))`()` Returns whether the route is a system route or not. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/media/MediaRoute2Info.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/MediaRoute2Info.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MediaRoute2Info](../android/media/MediaRoute2Info.md)!\> | [CREATOR](../android/media/MediaRoute2Info.md) <br /> |

## Constants

### CONNECTION_STATE_CONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_CONNECTED: Int
```

A connection state indicating the route is connected. 

 Value: 2

**See Also**

- [#getConnectionState](../android/media/MediaRoute2Info.md)) 

### CONNECTION_STATE_CONNECTING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_CONNECTING: Int
```

A connection state indicating the route is in the process of connecting and is not yet ready for use. 

 Value: 1

**See Also**

- [#getConnectionState](../android/media/MediaRoute2Info.md)) 

### CONNECTION_STATE_DISCONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_DISCONNECTED: Int
```

The default connection state indicating the route is disconnected. 

 Value: 0

**See Also**

- [#getConnectionState](../android/media/MediaRoute2Info.md)) 

### FEATURE_LIVE_AUDIO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_LIVE_AUDIO: String
```

Route feature: Live audio.

A route that supports live audio routing will allow the media audio stream to be sent to supported destinations. This can include internal speakers or audio jacks on the device itself, A2DP devices, and more.

When a live audio route is selected, audio routing is transparent to the application. All audio played on the media stream will be routed to the selected destination.

Refer to the class documentation for details about live audio routes. 

 Value: "android.media.route.feature.LIVE_AUDIO"

### FEATURE_LIVE_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_LIVE_VIDEO: String
```

Route feature: Live video.

A route that supports live video routing will allow a mirrored version of the device's primary display or a customized [Presentation](../android/app/Presentation.md) to be sent to supported destinations.

When a live video route is selected, audio and video routing is transparent to the application. By default, audio and video is routed to the selected destination. For certain live video routes, the application may also use a [Presentation](../android/app/Presentation.md) to replace the mirrored view on the external display with different content.

Refer to the class documentation for details about live video routes. 

 Value: "android.media.route.feature.LIVE_VIDEO"

**See Also**

- [android.app.Presentation](../android/app/Presentation.md) 

### FEATURE_REMOTE_AUDIO_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_AUDIO_PLAYBACK: String
```

Route feature: Remote audio playback.

A route that supports remote audio playback routing will allow an application to send requests to play audio content remotely to supported destinations. 

 Value: "android.media.route.feature.REMOTE_AUDIO_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_PLAYBACK](../android/media/MediaRoute2Info.md)
- [#FEATURE_REMOTE_VIDEO_PLAYBACK](../android/media/MediaRoute2Info.md) 

### FEATURE_REMOTE_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_PLAYBACK: String
```

Route feature: Remote playback.

A route that supports remote playback routing will allow an application to send requests to play content remotely to supported destinations. A route may only support [audio playback](../android/media/MediaRoute2Info.md) or [video playback](../android/media/MediaRoute2Info.md).

Remote playback routes destinations operate independently of the local device. When a remote playback route is selected, the application can control the content playing on the destination using [MediaRouter2.RoutingController.getControlHints()](../android/media/MediaRouter2.RoutingController.md)). The application may also receive status updates from the route regarding remote playback.

Refer to the class documentation for details about remote playback routes. 

 Value: "android.media.route.feature.REMOTE_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_AUDIO_PLAYBACK](../android/media/MediaRoute2Info.md)
- [#FEATURE_REMOTE_VIDEO_PLAYBACK](../android/media/MediaRoute2Info.md) 

### FEATURE_REMOTE_VIDEO_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_VIDEO_PLAYBACK: String
```

Route feature: Remote video playback.

A route that supports remote video playback routing will allow an application to send requests to play video content remotely to supported destinations. 

 Value: "android.media.route.feature.REMOTE_VIDEO_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_PLAYBACK](../android/media/MediaRoute2Info.md)
- [#FEATURE_REMOTE_AUDIO_PLAYBACK](../android/media/MediaRoute2Info.md) 

### PLAYBACK_VOLUME_FIXED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_VOLUME_FIXED: Int
```

Playback information indicating the playback volume is fixed, i.e. it cannot be controlled from this object. An example of fixed playback volume is a remote player, playing over HDMI where the user prefers to control the volume on the HDMI sink, rather than attenuate at the source. 

 Value: 0

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolumeHandling()> 

### PLAYBACK_VOLUME_VARIABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_VOLUME_VARIABLE: Int
```

Playback information indicating the playback volume is variable and can be controlled from this object. 

 Value: 1

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolumeHandling()> 

### SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER: Int
```

Indicates that the route is never suitable for media playback. 

 Value: 2

### SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER: Int
```

Indicates the route is always suitable for media playback. 

 Value: 0

### SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER: Int
```

Indicates that the route is suitable for media playback only after explicit user selection. 

 Value: 1

### TYPE_AUX_LINE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_AUX_LINE: Int
```

Indicates the route is using the auxiliary line-level connectors. 

 Value: 19

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_AUX_LINE](../android/media/AudioDeviceInfo.md) 

### TYPE_BLE_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BLE_HEADSET: Int
```

Indicates the route is a Bluetooth Low Energy (BLE) HEADSET. 

 Value: 26

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_BLE_HEADSET](../android/media/AudioDeviceInfo.md) 

### TYPE_BLUETOOTH_A2DP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BLUETOOTH_A2DP: Int
```

Indicates the route is a bluetooth device, such as a bluetooth speaker or headphones. 

 Value: 8

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_BLUETOOTH_A2DP](../android/media/AudioDeviceInfo.md) 

### TYPE_BUILTIN_SPEAKER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BUILTIN_SPEAKER: Int
```

Indicates the route is the speaker system (i.e. a mono speaker or stereo speakers) built into the device. 

 Value: 2

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_BUILTIN_SPEAKER](../android/media/AudioDeviceInfo.md) 

### TYPE_DOCK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DOCK: Int
```

Indicates the route is the audio device associated with a dock. 

 Value: 13

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_DOCK](../android/media/AudioDeviceInfo.md) 

### TYPE_GROUP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GROUP: Int
```

Indicates the route is a group of devices. 

 Value: 2000

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_HDMI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI: Int
```

Indicates the route is an HDMI connection. 

 Value: 9

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_HDMI](../android/media/AudioDeviceInfo.md) 

### TYPE_HDMI_ARC

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI_ARC: Int
```

Indicates the route is an Audio Return Channel of an HDMI connection. 

 Value: 10

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_HDMI_ARC](../android/media/AudioDeviceInfo.md) 

### TYPE_HDMI_EARC

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI_EARC: Int
```

Indicates the route is an Enhanced Audio Return Channel of an HDMI connection. 

 Value: 29

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_HDMI_EARC](../android/media/AudioDeviceInfo.md) 

### TYPE_HEARING_AID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HEARING_AID: Int
```

Indicates the route is a hearing aid. 

 Value: 23

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_HEARING_AID](../android/media/AudioDeviceInfo.md) 

### TYPE_LINE_ANALOG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINE_ANALOG: Int
```

Indicates the route is an analog line-level connection. 

 Value: 5

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_LINE_ANALOG](../android/media/AudioDeviceInfo.md) 

### TYPE_LINE_DIGITAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINE_DIGITAL: Int
```

Indicates the route is a digital line connection (for example S/PDIF). 

 Value: 6

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_LINE_DIGITAL](../android/media/AudioDeviceInfo.md) 

### TYPE_MULTICHANNEL_SPEAKER_GROUP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MULTICHANNEL_SPEAKER_GROUP: Int
```

Indicates the route is a speaker group supporting multichannel contents.

The speakers in the group are connected together using local network based protocols. The speaker group requires additional input of the physical positions of each individual speaker to provide a better experience on multichannel contents. 

 Value: 32

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP](../android/media/AudioDeviceInfo.md) 

### TYPE_REMOTE_AUDIO_VIDEO_RECEIVER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_AUDIO_VIDEO_RECEIVER: Int
```

Indicates the route is a remote Audio/Video Receiver (AVR).

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1003

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_CAR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_CAR: Int
```

Indicates the route is a remote car.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1008

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_COMPUTER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_COMPUTER: Int
```

Indicates the route is a remote computer.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1006

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_GAME_CONSOLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_GAME_CONSOLE: Int
```

Indicates the route is a remote gaming console.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1007

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_SMARTPHONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SMARTPHONE: Int
```

Indicates the route is a remote smartphone.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1010

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_SMARTWATCH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SMARTWATCH: Int
```

Indicates the route is a remote smartwatch.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1009

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_SPEAKER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SPEAKER: Int
```

Indicates the route is a remote speaker.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1002

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_TABLET

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TABLET: Int
```

Indicates the route is a remote tablet.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1004

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_TABLET_DOCKED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TABLET_DOCKED: Int
```

Indicates the route is a remote docked tablet.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1005

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_REMOTE_TV

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TV: Int
```

Indicates the route is a remote TV.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1001

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```

Indicates the route's type is unknown or undefined. 

 Value: 0

**See Also**

- [#getType](../android/media/MediaRoute2Info.md)) 

### TYPE_USB_ACCESSORY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_ACCESSORY: Int
```

Indicates the route is a USB audio device in accessory mode. 

 Value: 12

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_USB_ACCESSORY](../android/media/AudioDeviceInfo.md) 

### TYPE_USB_DEVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_DEVICE: Int
```

Indicates the route is a USB audio device. 

 Value: 11

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_USB_DEVICE](../android/media/AudioDeviceInfo.md) 

### TYPE_USB_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_HEADSET: Int
```

Indicates the route is a USB audio headset. 

 Value: 22

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_USB_HEADSET](../android/media/AudioDeviceInfo.md) 

### TYPE_WIRED_HEADPHONES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WIRED_HEADPHONES: Int
```

Indicates the route is a pair of wired headphones. 

 Value: 4

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_WIRED_HEADPHONES](../android/media/AudioDeviceInfo.md) 

### TYPE_WIRED_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WIRED_HEADSET: Int
```

Indicates the route is a headset, which is the combination of a headphones and a microphone. 

 Value: 3

**See Also**

- [#getType](../android/media/MediaRoute2Info.md))
- [android.media.AudioDeviceInfo#TYPE_WIRED_HEADSET](../android/media/AudioDeviceInfo.md)

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getClientPackageName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientPackageName(): String?
```

Gets the package name of the app using the route. Returns null if no apps are using this route. 

### getConnectionState

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(): Int
```

Gets the connection state of the route.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The connection state of this route: [CONNECTION_STATE_DISCONNECTED](../android/media/MediaRoute2Info.md), [CONNECTION_STATE_CONNECTING](../android/media/MediaRoute2Info.md), or [CONNECTION_STATE_CONNECTED](../android/media/MediaRoute2Info.md). Value is [android.media.MediaRoute2Info#CONNECTION_STATE_DISCONNECTED](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#CONNECTION_STATE_CONNECTING](../android/media/MediaRoute2Info.md), or [android.media.MediaRoute2Info#CONNECTION_STATE_CONNECTED](../android/media/MediaRoute2Info.md) |

### getDeduplicationIds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeduplicationIds(): MutableSet<String!>
```

Gets the deduplication IDs associated to the route.

Two routes with a matching deduplication ID originate from the same receiver device.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): CharSequence?
```

Gets the user-visible description of the route.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getExtras

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Gets an optional bundle with extra data.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](../android/os/Bundle.md)? | This value may be`null`. |

### getFeatures

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFeatures(): MutableList<String!>
```

Gets the supported features of the route.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getIconUri

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIconUri(): Uri?
```

Gets the URI of the icon representing this route.

This icon will be used in picker UIs if available.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](../android/net/Uri.md)? | The URI of the icon representing this route, or null if none. |

### getId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Gets the id of the route. The routes which are given by [MediaRouter2](../android/media/MediaRouter2.md) will have unique IDs.

In order to ensure uniqueness in [MediaRouter2](../android/media/MediaRouter2.md) side, the value of this method can be different from what was set in [MediaRoute2ProviderService](../android/media/MediaRoute2ProviderService.md).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.media.MediaRoute2Info.Builder#Builder(String, CharSequence)](../android/media/MediaRoute2Info.Builder.md)) 

### getName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): CharSequence
```

Gets the user-visible name of the route.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getRequiredPermissions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequiredPermissions(): MutableList<MutableSet<String!>!>
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!> | a list of permission sets - all the permissions in at least one of these sets must be held to see this route. This value cannot be`null`. |

### getSuitabilityStatus

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuitabilityStatus(): Int
```

Returns the route suitability status.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER](../android/media/MediaRoute2Info.md), or [android.media.MediaRoute2Info#SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER](../android/media/MediaRoute2Info.md) |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of this route.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.MediaRoute2Info#TYPE_UNKNOWN](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_BUILTIN_SPEAKER](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_WIRED_HEADSET](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_WIRED_HEADPHONES](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_BLUETOOTH_A2DP](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_HDMI](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_HDMI_ARC](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_HDMI_EARC](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_LINE_DIGITAL](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_LINE_ANALOG](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_AUX_LINE](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_USB_DEVICE](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_USB_ACCESSORY](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_DOCK](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_USB_HEADSET](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_HEARING_AID](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_BLE_HEADSET](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_TV](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_SPEAKER](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_AUDIO_VIDEO_RECEIVER](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_TABLET](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_TABLET_DOCKED](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_COMPUTER](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_GAME_CONSOLE](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_CAR](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_SMARTWATCH](../android/media/MediaRoute2Info.md), [android.media.MediaRoute2Info#TYPE_REMOTE_SMARTPHONE](../android/media/MediaRoute2Info.md), or [android.media.MediaRoute2Info#TYPE_GROUP](../android/media/MediaRoute2Info.md) |

### getVolume

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolume(): Int
```

Gets the current volume of the route. This may be invalid if the route is not selected. 

### getVolumeHandling

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeHandling(): Int
```

Gets information about how volume is handled on the route.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_FIXED](../android/media/MediaRoute2Info.md) or [PLAYBACK_VOLUME_VARIABLE](../android/media/MediaRoute2Info.md) Value is [android.media.MediaRoute2Info#PLAYBACK_VOLUME_FIXED](../android/media/MediaRoute2Info.md), or [android.media.MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE](../android/media/MediaRoute2Info.md) |

### getVolumeMax

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeMax(): Int
```

Gets the maximum volume of the route. 

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isSystemRoute

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSystemRoute(): Boolean
```

Returns whether the route is a system route or not.

System routes are media routes directly controlled by the system such as phone speaker, wired headset, and Bluetooth devices. 

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<MediaRoute2Info!>
```
