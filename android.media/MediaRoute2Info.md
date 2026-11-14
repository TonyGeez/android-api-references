# MediaRoute2Info

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRoute2Info

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaRoute2Info "View this page in Java") 

```
class MediaRoute2Info : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaRoute2Info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#) |

Describes the properties of a route.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info.Builder) Builder for [media route info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#). |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTED:kotlin.Int) A connection state indicating the route is connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTING:kotlin.Int) A connection state indicating the route is in the process of connecting and is not yet ready for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTION_STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_DISCONNECTED:kotlin.Int) The default connection state indicating the route is disconnected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_LIVE_AUDIO](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_LIVE_AUDIO:kotlin.String) Route feature: Live audio. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_LIVE_VIDEO](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_LIVE_VIDEO:kotlin.String) Route feature: Live video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_AUDIO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_AUDIO_PLAYBACK:kotlin.String) Route feature: Remote audio playback. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_PLAYBACK:kotlin.String) Route feature: Remote playback. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REMOTE_VIDEO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_VIDEO_PLAYBACK:kotlin.String) Route feature: Remote video playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_FIXED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_FIXED:kotlin.Int) Playback information indicating the playback volume is fixed, i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_VARIABLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE:kotlin.Int) Playback information indicating the playback volume is variable and can be controlled from this object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER:kotlin.Int) Indicates that the route is never suitable for media playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER:kotlin.Int) Indicates the route is always suitable for media playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER:kotlin.Int) Indicates that the route is suitable for media playback only after explicit user selection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_AUX_LINE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_AUX_LINE:kotlin.Int) Indicates the route is using the auxiliary line-level connectors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BLE_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLE_HEADSET:kotlin.Int) Indicates the route is a Bluetooth Low Energy (BLE) HEADSET. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BLUETOOTH_A2DP](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLUETOOTH_A2DP:kotlin.Int) Indicates the route is a bluetooth device, such as a bluetooth speaker or headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BUILTIN_SPEAKER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BUILTIN_SPEAKER:kotlin.Int) Indicates the route is the speaker system (i.e. a mono speaker or stereo speakers) built into the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DOCK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_DOCK:kotlin.Int) Indicates the route is the audio device associated with a dock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GROUP](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_GROUP:kotlin.Int) Indicates the route is a group of devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI:kotlin.Int) Indicates the route is an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI_ARC](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_ARC:kotlin.Int) Indicates the route is an Audio Return Channel of an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HDMI_EARC](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_EARC:kotlin.Int) Indicates the route is an Enhanced Audio Return Channel of an HDMI connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HEARING_AID](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HEARING_AID:kotlin.Int) Indicates the route is a hearing aid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINE_ANALOG](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_ANALOG:kotlin.Int) Indicates the route is an analog line-level connection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LINE_DIGITAL](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_DIGITAL:kotlin.Int) Indicates the route is a digital line connection (for example S/PDIF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MULTICHANNEL_SPEAKER_GROUP](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_MULTICHANNEL_SPEAKER_GROUP:kotlin.Int) Indicates the route is a speaker group supporting multichannel contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_AUDIO_VIDEO_RECEIVER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_AUDIO_VIDEO_RECEIVER:kotlin.Int) Indicates the route is a remote Audio/Video Receiver (AVR). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_CAR](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_CAR:kotlin.Int) Indicates the route is a remote car. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_COMPUTER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_COMPUTER:kotlin.Int) Indicates the route is a remote computer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_GAME_CONSOLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_GAME_CONSOLE:kotlin.Int) Indicates the route is a remote gaming console. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SMARTPHONE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTPHONE:kotlin.Int) Indicates the route is a remote smartphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SMARTWATCH](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTWATCH:kotlin.Int) Indicates the route is a remote smartwatch. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_SPEAKER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SPEAKER:kotlin.Int) Indicates the route is a remote speaker. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TABLET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET:kotlin.Int) Indicates the route is a remote tablet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TABLET_DOCKED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET_DOCKED:kotlin.Int) Indicates the route is a remote docked tablet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REMOTE_TV](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TV:kotlin.Int) Indicates the route is a remote TV. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_UNKNOWN:kotlin.Int) Indicates the route's type is unknown or undefined. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_ACCESSORY:kotlin.Int) Indicates the route is a USB audio device in accessory mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_DEVICE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_DEVICE:kotlin.Int) Indicates the route is a USB audio device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_HEADSET:kotlin.Int) Indicates the route is a USB audio headset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WIRED_HEADPHONES](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADPHONES:kotlin.Int) Indicates the route is a pair of wired headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WIRED_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADSET:kotlin.Int) Indicates the route is a headset, which is the combination of a headphones and a microphone. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getClientPackageName](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getClientPackageName())`()` Gets the package name of the app using the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getConnectionState())`()` Gets the connection state of the route. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDeduplicationIds](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getDeduplicationIds())`()` Gets the deduplication IDs associated to the route. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getDescription())`()` Gets the user-visible description of the route. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getExtras())`()` Gets an optional bundle with extra data. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getFeatures](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getFeatures())`()` Gets the supported features of the route. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getIconUri](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getIconUri())`()` Gets the URI of the icon representing this route. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getId())`()` Gets the id of the route. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getName](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getName())`()` Gets the user-visible name of the route. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\> | [getRequiredPermissions](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getRequiredPermissions())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSuitabilityStatus](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getSuitabilityStatus())`()` Returns the route suitability status. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())`()` Returns the type of this route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolume](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolume())`()` Gets the current volume of the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeHandling](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolumeHandling())`()` Gets information about how volume is handled on the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeMax](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getVolumeMax())`()` Gets the maximum volume of the route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemRoute](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#isSystemRoute())`()` Returns whether the route is a system route or not. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MediaRoute2Info](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CONNECTION_STATE_CONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_CONNECTED: Int
```

A connection state indicating the route is connected. 

 Value: 2

**See Also**

- [#getConnectionState](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getConnectionState()) 

### CONNECTION_STATE_CONNECTING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_CONNECTING: Int
```

A connection state indicating the route is in the process of connecting and is not yet ready for use. 

 Value: 1

**See Also**

- [#getConnectionState](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getConnectionState()) 

### CONNECTION_STATE_DISCONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_STATE_DISCONNECTED: Int
```

The default connection state indicating the route is disconnected. 

 Value: 0

**See Also**

- [#getConnectionState](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getConnectionState()) 

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

A route that supports live video routing will allow a mirrored version of the device's primary display or a customized [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) to be sent to supported destinations.

When a live video route is selected, audio and video routing is transparent to the application. By default, audio and video is routed to the selected destination. For certain live video routes, the application may also use a [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) to replace the mirrored view on the external display with different content.

Refer to the class documentation for details about live video routes. 

 Value: "android.media.route.feature.LIVE_VIDEO"

**See Also**

- [android.app.Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) 

### FEATURE_REMOTE_AUDIO_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_AUDIO_PLAYBACK: String
```

Route feature: Remote audio playback.

A route that supports remote audio playback routing will allow an application to send requests to play audio content remotely to supported destinations. 

 Value: "android.media.route.feature.REMOTE_AUDIO_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_PLAYBACK:kotlin.String)
- [#FEATURE_REMOTE_VIDEO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_VIDEO_PLAYBACK:kotlin.String) 

### FEATURE_REMOTE_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_PLAYBACK: String
```

Route feature: Remote playback.

A route that supports remote playback routing will allow an application to send requests to play content remotely to supported destinations. A route may only support [audio playback](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_AUDIO_PLAYBACK:kotlin.String) or [video playback](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_VIDEO_PLAYBACK:kotlin.String).

Remote playback routes destinations operate independently of the local device. When a remote playback route is selected, the application can control the content playing on the destination using [MediaRouter2.RoutingController.getControlHints()](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#getControlHints()). The application may also receive status updates from the route regarding remote playback.

Refer to the class documentation for details about remote playback routes. 

 Value: "android.media.route.feature.REMOTE_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_AUDIO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_AUDIO_PLAYBACK:kotlin.String)
- [#FEATURE_REMOTE_VIDEO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_VIDEO_PLAYBACK:kotlin.String) 

### FEATURE_REMOTE_VIDEO_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REMOTE_VIDEO_PLAYBACK: String
```

Route feature: Remote video playback.

A route that supports remote video playback routing will allow an application to send requests to play video content remotely to supported destinations. 

 Value: "android.media.route.feature.REMOTE_VIDEO_PLAYBACK"

**See Also**

- [#FEATURE_REMOTE_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_PLAYBACK:kotlin.String)
- [#FEATURE_REMOTE_AUDIO_PLAYBACK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#FEATURE_REMOTE_AUDIO_PLAYBACK:kotlin.String) 

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

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_AUX_LINE](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_AUX_LINE:kotlin.Int) 

### TYPE_BLE_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BLE_HEADSET: Int
```

Indicates the route is a Bluetooth Low Energy (BLE) HEADSET. 

 Value: 26

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_BLE_HEADSET](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_HEADSET:kotlin.Int) 

### TYPE_BLUETOOTH_A2DP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BLUETOOTH_A2DP: Int
```

Indicates the route is a bluetooth device, such as a bluetooth speaker or headphones. 

 Value: 8

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_BLUETOOTH_A2DP](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_A2DP:kotlin.Int) 

### TYPE_BUILTIN_SPEAKER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BUILTIN_SPEAKER: Int
```

Indicates the route is the speaker system (i.e. a mono speaker or stereo speakers) built into the device. 

 Value: 2

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_BUILTIN_SPEAKER](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER:kotlin.Int) 

### TYPE_DOCK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DOCK: Int
```

Indicates the route is the audio device associated with a dock. 

 Value: 13

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_DOCK](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK:kotlin.Int) 

### TYPE_GROUP

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GROUP: Int
```

Indicates the route is a group of devices. 

 Value: 2000

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_HDMI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI: Int
```

Indicates the route is an HDMI connection. 

 Value: 9

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_HDMI](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI:kotlin.Int) 

### TYPE_HDMI_ARC

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI_ARC: Int
```

Indicates the route is an Audio Return Channel of an HDMI connection. 

 Value: 10

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_HDMI_ARC](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_ARC:kotlin.Int) 

### TYPE_HDMI_EARC

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HDMI_EARC: Int
```

Indicates the route is an Enhanced Audio Return Channel of an HDMI connection. 

 Value: 29

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_HDMI_EARC](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_EARC:kotlin.Int) 

### TYPE_HEARING_AID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HEARING_AID: Int
```

Indicates the route is a hearing aid. 

 Value: 23

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_HEARING_AID](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HEARING_AID:kotlin.Int) 

### TYPE_LINE_ANALOG

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINE_ANALOG: Int
```

Indicates the route is an analog line-level connection. 

 Value: 5

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_LINE_ANALOG](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_ANALOG:kotlin.Int) 

### TYPE_LINE_DIGITAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LINE_DIGITAL: Int
```

Indicates the route is a digital line connection (for example S/PDIF). 

 Value: 6

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_LINE_DIGITAL](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_DIGITAL:kotlin.Int) 

### TYPE_MULTICHANNEL_SPEAKER_GROUP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MULTICHANNEL_SPEAKER_GROUP: Int
```

Indicates the route is a speaker group supporting multichannel contents.

The speakers in the group are connected together using local network based protocols. The speaker group requires additional input of the physical positions of each individual speaker to provide a better experience on multichannel contents. 

 Value: 32

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP:kotlin.Int) 

### TYPE_REMOTE_AUDIO_VIDEO_RECEIVER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_AUDIO_VIDEO_RECEIVER: Int
```

Indicates the route is a remote Audio/Video Receiver (AVR).

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1003

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_CAR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_CAR: Int
```

Indicates the route is a remote car.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1008

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_COMPUTER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_COMPUTER: Int
```

Indicates the route is a remote computer.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1006

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_GAME_CONSOLE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_GAME_CONSOLE: Int
```

Indicates the route is a remote gaming console.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1007

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_SMARTPHONE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SMARTPHONE: Int
```

Indicates the route is a remote smartphone.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1010

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_SMARTWATCH

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SMARTWATCH: Int
```

Indicates the route is a remote smartwatch.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1009

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_SPEAKER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_SPEAKER: Int
```

Indicates the route is a remote speaker.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1002

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_TABLET

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TABLET: Int
```

Indicates the route is a remote tablet.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1004

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_TABLET_DOCKED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TABLET_DOCKED: Int
```

Indicates the route is a remote docked tablet.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1005

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_REMOTE_TV

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REMOTE_TV: Int
```

Indicates the route is a remote TV.

A remote device uses a routing protocol managed by the application, as opposed to the routing being done by the system. 

 Value: 1001

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: Int
```

Indicates the route's type is unknown or undefined. 

 Value: 0

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType()) 

### TYPE_USB_ACCESSORY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_ACCESSORY: Int
```

Indicates the route is a USB audio device in accessory mode. 

 Value: 12

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_ACCESSORY:kotlin.Int) 

### TYPE_USB_DEVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_DEVICE: Int
```

Indicates the route is a USB audio device. 

 Value: 11

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_USB_DEVICE](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_DEVICE:kotlin.Int) 

### TYPE_USB_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB_HEADSET: Int
```

Indicates the route is a USB audio headset. 

 Value: 22

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_USB_HEADSET](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_HEADSET:kotlin.Int) 

### TYPE_WIRED_HEADPHONES

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WIRED_HEADPHONES: Int
```

Indicates the route is a pair of wired headphones. 

 Value: 4

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_WIRED_HEADPHONES](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADPHONES:kotlin.Int) 

### TYPE_WIRED_HEADSET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WIRED_HEADSET: Int
```

Indicates the route is a headset, which is the combination of a headphones and a microphone. 

 Value: 3

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#getType())
- [android.media.AudioDeviceInfo#TYPE_WIRED_HEADSET](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADSET:kotlin.Int)

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The connection state of this route: [CONNECTION_STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_DISCONNECTED:kotlin.Int), [CONNECTION_STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTING:kotlin.Int), or [CONNECTION_STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTED:kotlin.Int). Value is [android.media.MediaRoute2Info#CONNECTION_STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_DISCONNECTED:kotlin.Int), [android.media.MediaRoute2Info#CONNECTION_STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTING:kotlin.Int), or [android.media.MediaRoute2Info#CONNECTION_STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#CONNECTION_STATE_CONNECTED:kotlin.Int) |

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
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

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
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI of the icon representing this route, or null if none. |

### getId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Gets the id of the route. The routes which are given by [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2) will have unique IDs.

In order to ensure uniqueness in [MediaRouter2](https://developer.android.com/reference/kotlin/android/media/MediaRouter2) side, the value of this method can be different from what was set in [MediaRoute2ProviderService](https://developer.android.com/reference/kotlin/android/media/MediaRoute2ProviderService).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

**See Also**

- [android.media.MediaRoute2Info.Builder#Builder(String, CharSequence)](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info.Builder#Builder(kotlin.String,%20kotlin.CharSequence)) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_DEFAULT_TRANSFER:kotlin.Int), [android.media.MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_SUITABLE_FOR_MANUAL_TRANSFER:kotlin.Int), or [android.media.MediaRoute2Info#SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#SUITABILITY_STATUS_NOT_SUITABLE_FOR_TRANSFER:kotlin.Int) |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of this route.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.MediaRoute2Info#TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_UNKNOWN:kotlin.Int), [android.media.MediaRoute2Info#TYPE_BUILTIN_SPEAKER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BUILTIN_SPEAKER:kotlin.Int), [android.media.MediaRoute2Info#TYPE_WIRED_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADSET:kotlin.Int), [android.media.MediaRoute2Info#TYPE_WIRED_HEADPHONES](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_WIRED_HEADPHONES:kotlin.Int), [android.media.MediaRoute2Info#TYPE_BLUETOOTH_A2DP](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLUETOOTH_A2DP:kotlin.Int), [android.media.MediaRoute2Info#TYPE_HDMI](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI:kotlin.Int), [android.media.MediaRoute2Info#TYPE_HDMI_ARC](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_ARC:kotlin.Int), [android.media.MediaRoute2Info#TYPE_HDMI_EARC](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HDMI_EARC:kotlin.Int), [android.media.MediaRoute2Info#TYPE_LINE_DIGITAL](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_DIGITAL:kotlin.Int), [android.media.MediaRoute2Info#TYPE_LINE_ANALOG](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_LINE_ANALOG:kotlin.Int), [android.media.MediaRoute2Info#TYPE_AUX_LINE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_AUX_LINE:kotlin.Int), [android.media.MediaRoute2Info#TYPE_USB_DEVICE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_DEVICE:kotlin.Int), [android.media.MediaRoute2Info#TYPE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_ACCESSORY:kotlin.Int), [android.media.MediaRoute2Info#TYPE_DOCK](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_DOCK:kotlin.Int), [android.media.MediaRoute2Info#TYPE_USB_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_USB_HEADSET:kotlin.Int), [android.media.MediaRoute2Info#TYPE_HEARING_AID](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_HEARING_AID:kotlin.Int), [android.media.MediaRoute2Info#TYPE_BLE_HEADSET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_BLE_HEADSET:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_TV](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TV:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_SPEAKER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SPEAKER:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_AUDIO_VIDEO_RECEIVER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_AUDIO_VIDEO_RECEIVER:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_TABLET](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_TABLET_DOCKED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_TABLET_DOCKED:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_COMPUTER](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_COMPUTER:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_GAME_CONSOLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_GAME_CONSOLE:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_CAR](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_CAR:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_SMARTWATCH](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTWATCH:kotlin.Int), [android.media.MediaRoute2Info#TYPE_REMOTE_SMARTPHONE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_REMOTE_SMARTPHONE:kotlin.Int), or [android.media.MediaRoute2Info#TYPE_GROUP](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#TYPE_GROUP:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYBACK_VOLUME_FIXED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_FIXED:kotlin.Int) or [PLAYBACK_VOLUME_VARIABLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE:kotlin.Int) Value is [android.media.MediaRoute2Info#PLAYBACK_VOLUME_FIXED](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_FIXED:kotlin.Int), or [android.media.MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE](https://developer.android.com/reference/kotlin/android/media/MediaRoute2Info#PLAYBACK_VOLUME_VARIABLE:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MediaRoute2Info!>
```
