Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioManager

```
open class AudioManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioManager](AudioManager.md) |

AudioManager provides access to volume and ringer mode control.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioPlaybackCallback` Interface for receiving update notifications about the playback activity on the system. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback` Interface for receiving update notifications about the recording configuration. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.OnAudioFocusChangeListener` Interface definition for a callback to be invoked when the audio focus of the system is updated. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.OnCommunicationDeviceChangedListener` Listener registered by client to be notified upon communication audio device change. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.OnModeChangedListener` Interface definition of a callback that is notified when the audio mode changes |
| abstract | `https://developer.android.com/reference/kotlin/android/media/AudioManager.OnPreferredMixerAttributesChangedListener` Interface to be notified of changes in the preferred mixer attributes. |
| --- | --- |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_AUDIO_BECOMING_NOISY:kotlin.String` Broadcast intent, a hint for applications that audio is about to become 'noisy' due to a change in audio outputs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` Broadcast Action: A sticky broadcast indicating an HDMI cable was plugged or unplugged. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HEADSET_PLUG:kotlin.String` Broadcast Action: Wired Headset plugged in or unplugged. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_MICROPHONE_MUTE_CHANGED:kotlin.String` Broadcast Action: microphone muting state changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_CHANGED:kotlin.String` Sticky broadcast intent action indicating that the Bluetooth SCO audio connection state has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` Sticky broadcast intent action indicating that the Bluetooth SCO audio connection state has been updated. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SPEAKERPHONE_STATE_CHANGED:kotlin.String` Broadcast Action: speakerphone state changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int` Decrease the ringer volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_MUTE:kotlin.Int` Mute the volume. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int` Increase the ringer volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int` Maintain the previous ringer volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_TOGGLE_MUTE:kotlin.Int` Toggle the mute state. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_UNMUTE:kotlin.Int` Unmute the volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN:kotlin.Int` Used to indicate a gain of audio focus, or a request of audio focus, of unknown duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT:kotlin.Int` Used to indicate a temporary gain or request of audio focus, anticipated to last a short amount of time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE:kotlin.Int` Used to indicate a temporary request of audio focus, anticipated to last a short amount of time, during which no other applications, or system components, should play anything. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK:kotlin.Int` Used to indicate a temporary request of audio focus, anticipated to last a short amount of time, and where it is acceptable for other audio applications to keep playing after having lowered their output level (also referred to as "ducking"). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS:kotlin.Int` Used to indicate a loss of audio focus of unknown duration. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS_TRANSIENT:kotlin.Int` Used to indicate a transient loss of audio focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK:kotlin.Int` Used to indicate a transient loss of audio focus where the loser of the audio focus can lower its output volume if it wants to continue playing (also referred to as "ducking"), as the new focus owner doesn't require others to be silent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_NONE:kotlin.Int` Used to indicate no audio focus has been gained or lost, or requested. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_DELAYED:kotlin.Int` A focus change request whose granting is delayed: the request was successful, but the requester will only be granted audio focus once the condition that prevented immediate granting has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int` A failed focus change request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_GRANTED:kotlin.Int` A successful focus change request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIO_SESSION_ID_GENERATE:kotlin.Int` A special audio session ID to indicate that the audio session ID isn't known and the framework should generate a new value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_BITSTREAM_SUPPORTED:kotlin.Int` Return value for getDirectPlaybackSupport: direct playback supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_NOT_SUPPORTED:kotlin.Int` Return value for getDirectPlaybackSupport: direct playback not supported. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` Return value for getDirectPlaybackSupport: direct offload playback supported with gapless transitions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` Return value for getDirectPlaybackSupport: direct offload playback supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_ALWAYS:kotlin.Int` The surround sound formats are ALWAYS available, even if they are not detected by the hardware. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_AUTO:kotlin.Int` The surround sound formats are available for use if they are detected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_MANUAL:kotlin.Int` Surround sound formats are available according to the choice of user, even if they are not detected by the hardware. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_NEVER:kotlin.Int` The surround sound formats are NEVER available, even if they are detected by the hardware. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_UNKNOWN:kotlin.Int` The mode for surround sound formats is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ERROR:kotlin.Int` A default error code. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ERROR_DEAD_OBJECT:kotlin.Int` An error code indicating that the object reporting it is no longer valid and needs to be recreated. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_AUDIO_PLUG_STATE:kotlin.String` Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to communicate whether HDMI is plugged in or unplugged. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_ENCODINGS:kotlin.String` Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to define the audio encodings supported by the connected HDMI device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_MAX_CHANNEL_COUNT:kotlin.String` Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to define the maximum number of channels supported by the HDMI device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_RINGER_MODE:kotlin.String` The new ringer mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_PREVIOUS_STATE:kotlin.String` Extra for intent `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` containing the previous bluetooth SCO connection state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_STATE:kotlin.String` Extra for intent `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_CHANGED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` containing the new bluetooth SCO connection state. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_VIBRATE_SETTING:kotlin.String` The new vibrate setting for a particular type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_VIBRATE_TYPE:kotlin.String` The vibrate type whose setting has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` Whether to include ringer modes as possible options when changing volume. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` Whether to play a sound when changing the volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` Removes any sounds/vibrate that may be in the queue, or are playing (related to changing volume). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` Show a toast containing the current volume. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` Whether to vibrate if going into the vibrate ringer mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_BACK:kotlin.Int` Back sound |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_DOWN:kotlin.Int` Focus has moved down |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_LEFT:kotlin.Int` Focus has moved left |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_RIGHT:kotlin.Int` Focus has moved right |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_UP:kotlin.Int` Focus has moved up |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_DELETE:kotlin.Int` IME delete keypress sound |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_INVALID:kotlin.Int` Invalid keypress sound |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_RETURN:kotlin.Int` IME return_keypress sound |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_SPACEBAR:kotlin.Int` IME spacebar keypress sound |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_STANDARD:kotlin.Int` IME standard keypress sound |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEY_CLICK:kotlin.Int` Keyboard and direction pad click sound |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_ALL:kotlin.Int` Specifies to the getDevices method to include both source and sink devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_INPUTS:kotlin.Int` Specifies to the getDevices method to include source (i.e. input) audio devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_OUTPUTS:kotlin.Int` Specifies to the getDevices method to include sink (i.e. output) audio devices. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int` Use this mode whenever an assistant conversation mode is started. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_REDIRECT:kotlin.Int` A telephony call is established and its audio is being redirected to another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_SCREENING:kotlin.Int` Call screening in progress. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_COMMUNICATION_REDIRECT:kotlin.Int` An audio/video chat or VoIP call is established and its audio is being redirected to another device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CURRENT:kotlin.Int` Current audio mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_INVALID:kotlin.Int` Invalid audio mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int` In call audio mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_COMMUNICATION:kotlin.Int` In communication audio mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_NORMAL:kotlin.Int` Normal audio mode: not ringing and no call established. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_RINGTONE:kotlin.Int` Ringing audio mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#NUM_STREAMS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` Return value for getPlaybackOffloadSupport: offload playback supported with gapless transitions |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_NOT_SUPPORTED:kotlin.Int` Return value for getPlaybackOffloadSupport: offload playback not supported |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` Return value for getPlaybackOffloadSupport: offload playback supported |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_FRAMES_PER_BUFFER:kotlin.String` Used as a key for getProperty to request the native or optimal output buffer size for this device's low latency output stream, in decimal PCM frames. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_SAMPLE_RATE:kotlin.String` Used as a key for getProperty to request the native or optimal output sample rate for this device's low latency output stream, in decimal Hz. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_AUDIO_SOURCE_UNPROCESSED:kotlin.String` Used as a key for getProperty to determine if the unprocessed audio source is available and supported with the expected frequency range and level response. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_MIC_NEAR_ULTRASOUND:kotlin.String` Used as a key for getProperty to determine if the default microphone audio source supports near-ultrasound frequencies (range of 18 - 21 kHz). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_SPEAKER_NEAR_ULTRASOUND:kotlin.String` Used as a key for getProperty to determine if the default speaker audio path supports near-ultrasound frequencies (range of 18 - 21 kHz). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_CHANGED_ACTION:kotlin.String` Sticky broadcast intent action indicating that the ringer mode has changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_NORMAL:kotlin.Int` Ringer mode that may be audible and may vibrate. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_SILENT:kotlin.Int` Ringer mode that will be silent and will not vibrate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_VIBRATE:kotlin.Int` Ringer mode that will be silent and will vibrate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_ALL:kotlin.Int` Used for mask parameter of setRouting. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_BLUETOOTH:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_BLUETOOTH_A2DP:kotlin.Int` Routing audio output to bluetooth A2DP |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_BLUETOOTH_SCO:kotlin.Int` Routing audio output to bluetooth SCO |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_EARPIECE:kotlin.Int` Routing audio output to earpiece |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_HEADSET:kotlin.Int` Routing audio output to headset |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#ROUTE_SPEAKER:kotlin.Int` Routing audio output to speaker |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTED:kotlin.Int` Value for extra `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_PREVIOUS_STATE:kotlin.String` indicating that the SCO audio channel is established |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTING:kotlin.Int` Value for extra EXTRA_SCO_AUDIO_STATE or EXTRA_SCO_AUDIO_PREVIOUS_STATE indicating that the SCO audio channel is being established |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_DISCONNECTED:kotlin.Int` Value for extra EXTRA_SCO_AUDIO_STATE or EXTRA_SCO_AUDIO_PREVIOUS_STATE indicating that the SCO audio channel is not established |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_ERROR:kotlin.Int` Value for extra EXTRA_SCO_AUDIO_STATE indicating that there was an error trying to obtain the state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ACCESSIBILITY:kotlin.Int` Used to identify the volume of audio streams for accessibility prompts |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int` Used to identify the volume of audio streams for alarms |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ASSISTANT:kotlin.Int` Used to identify the volume of audio streams for virtual assistant |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_DTMF:kotlin.Int` Used to identify the volume of audio streams for DTMF Tones |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int` Used to identify the volume of audio streams for music playback |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int` Used to identify the volume of audio streams for notifications |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int` Used to identify the volume of audio streams for the phone ring |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int` Used to identify the volume of audio streams for system sounds |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int` Used to identify the volume of audio streams for phone calls |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#USE_DEFAULT_STREAM_TYPE:kotlin.Int` Suggests using the default stream type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_CHANGED_ACTION:kotlin.String` Broadcast intent action indicating that the vibrate setting has changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_OFF:kotlin.Int` Vibrate setting that suggests to never vibrate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ON:kotlin.Int` Vibrate setting that suggests to vibrate when possible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ONLY_SILENT:kotlin.Int` Vibrate setting that suggests to only vibrate when in the vibrate ringer mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_NOTIFICATION:kotlin.Int` Vibrate type that corresponds to notifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_RINGER:kotlin.Int` Vibrate type that corresponds to the ringer. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | abandonAudioFocus Abandon audio focus. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | abandonAudioFocusRequest Abandon audio focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnCommunicationDeviceChangedListener Adds a listener for being notified of changes to the communication audio device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnModeChangedListener Adds a listener to be notified of changes to the audio mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addOnPreferredMixerAttributesChangedListener Adds a listener for being notified of changes to the preferred mixer attributes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | adjustStreamVolume Adjusts the volume of a particular stream by one step in a direction. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | adjustSuggestedStreamVolume Adjusts the volume of the most relevant stream, or the given fallback stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | adjustVolume Adjusts the volume of the most relevant stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | adjustVolumeGroupVolume Adjusts the volume of a particular group associated to given id by one step in a direction. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canManageAssistantAudio Checks if the calling app can manage assistant audio. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearCommunicationDevice Cancels previous communication device selection made with setCommunicationDevice. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | clearPreferredMixerAttributes Clears the current preferred mixer attributes that were previously set via setPreferredMixerAttributes Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String` |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dispatchMediaKeyEvent Sends a simulated key event for a media button. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | generateAudioSessionId Return a new audio session identifier not associated with any player or effect. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioPlaybackConfiguration](AudioPlaybackConfiguration.md)!\> | getActivePlaybackConfigurations Returns the current active audio playback configurations of the device |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioRecordingConfiguration](AudioRecordingConfiguration.md)!\> | getActiveRecordingConfigurations Returns the current active audio recording configurations of the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAllowedCapturePolicy Return the capture policy. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\> | getAudioDevicesForAttributes Get the audio devices that would be used for the routing of the given audio attributes. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAudioHwSyncForSession Retrieves the Hardware A/V synchronization ID corresponding to the given audio session ID. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\> | getAvailableCommunicationDevices Returns a list of audio devices that can be selected for communication use cases via setCommunicationDevice. |
| open [AudioDeviceInfo](AudioDeviceInfo.md)? | getCommunicationDevice Returns currently selected audio device for communication. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\>! | getDevices Returns an array of AudioDeviceInfo objects corresponding to the audio devices currently connected to the system and meeting the criteria specified in the `flags` parameter. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDirectPlaybackSupport Returns a bitfield representing the different forms of direct playback currently available for a given audio format. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioProfile](AudioProfile.md)!\> | getDirectProfilesForAttributes Returns a list of direct AudioProfile that are supported for the specified AudioAttributes. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioProfile](AudioProfile.md)!\> | getDirectProfilesForAttributes Returns a list of direct AudioProfile that are supported for the specified AudioAttributes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEncodedSurroundMode Gets the surround sound mode. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MicrophoneInfo](MicrophoneInfo.md)!\>! | getMicrophones Returns a list of MicrophoneInfo that corresponds to the characteristics of all available microphones. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMode Returns the current audio mode. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getParameters Gets a variable number of parameter values from audio hardware. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPlaybackOffloadSupport Returns whether offloaded playback of an audio format is supported on the device or not and when supported whether gapless transitions are possible or not. |
| --- | --- |
| open [AudioMixerAttributes](AudioMixerAttributes.md)? | getPreferredMixerAttributes Returns current preferred mixer attributes that is set via setPreferredMixerAttributes |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getProperty Returns the value of the property with the specified key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRingerMode Returns the current ringtone mode. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRouting Returns the current audio routing bit vector for a specified mode. |
| open [Spatializer](Spatializer.md) | getSpatializer Return a handle to the optional platform's Spatializer |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStreamMaxVolume Returns the maximum volume index for a particular stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStreamMinVolume Returns the minimum volume index for a particular stream. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStreamVolume Returns the current volume index for a particular stream. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getStreamVolumeDb Returns the volume in dB (decibel) for the given stream type at the given volume index, on the given type of audio output device. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | getSupportedDeviceTypes Returns a Set of unique Integers corresponding to audio device type identifiers that can *potentially* be connected to the system and meeting the criteria specified in the `direction` parameter. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioMixerAttributes](AudioMixerAttributes.md)!\> | getSupportedMixerAttributes Returns the AudioMixerAttributes that can be used to set as preferred mixer attributes via setPreferredMixerAttributes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVibrateSetting Returns whether the user's vibrate setting for a vibrate type. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVolumeGroupIdForAttributes Returns the volume group id associated to the given AudioAttributes. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isBluetoothA2dpOn Checks whether a Bluetooth A2DP audio peripheral is connected or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isBluetoothScoAvailableOffCall Indicates if current platform supports use of SCO for off call use cases. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isBluetoothScoOn Checks whether communications use Bluetooth SCO. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCallScreeningModeSupported Indicates if the platform supports a special call screening and call monitoring mode. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHapticPlaybackSupported Return if audio haptic coupled playback is supported or not. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isMicrophoneMute Checks whether the microphone mute is on or off. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isMusicActive Checks whether any music is active. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOffloadedPlaybackSupported Returns whether offloaded playback of an audio format is supported on the device. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRampingRingerEnabled Returns the current user setting for ramping ringer on incoming phone call ringtone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSpeakerphoneOn Checks whether the speakerphone is on or off. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isStreamMute Returns the current mute state for a particular stream. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSurroundFormatEnabled Gets whether a certain surround format is enabled or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVolumeFixed Indicates if the device implements a fixed volume policy. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVolumeGroupMuted Returns the current mute state for a particular volume group associated to the given id. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isWiredHeadsetOn Checks whether a wired headset is connected or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | loadSoundEffects Load Sound effects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | playSoundEffect Plays a sound effect (Key clicks, lid open/close...) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | playSoundEffect Plays a sound effect (Key clicks, lid open/close...) |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerAudioDeviceCallback Registers an AudioDeviceCallback object to receive notifications of changes to the set of connected audio devices. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerAudioPlaybackCallback Register a callback to be notified of audio playback changes through `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioPlaybackCallback` |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerAudioRecordingCallback Register a callback to be notified of audio recording changes through `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerMediaButtonEventReceiver Register a component to be the sole receiver of MEDIA_BUTTON intents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerMediaButtonEventReceiver Register a component to be the sole receiver of MEDIA_BUTTON intents. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerRemoteControlClient Registers the remote control client for providing information to display on the remote controls. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | registerRemoteController Registers a RemoteController instance for it to receive media metadata updates and playback state information from applications using RemoteControlClient, and control their playback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnCommunicationDeviceChangedListener Removes a previously added listener of changes to the communication audio device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnModeChangedListener Removes a previously added listener for changes to audio mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeOnPreferredMixerAttributesChangedListener Removes a previously added listener of changes to the preferred mixer attributes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | requestAudioFocus Request audio focus. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | requestAudioFocus Request audio focus. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAllowedCapturePolicy Specifies whether the audio played by this app may or may not be captured by other apps or the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBluetoothA2dpOn <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBluetoothScoOn Request use of Bluetooth SCO headset for communications. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setCommunicationDevice Selects the audio device that should be used for communication use cases, for instance voice or video calls. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setEncodedSurroundMode Sets the surround sound mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMicrophoneMute Sets the microphone mute on or off. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMode Sets the audio mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setParameters Sets a variable number of parameter values to audio hardware. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setPreferredMixerAttributes Configures the mixer attributes for a particular AudioAttributes over a given AudioDeviceInfo. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRingerMode Sets the ringer mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRouting Sets the audio routing for a specified mode |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSpeakerphoneOn Sets the speakerphone on or off. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStreamMute Mute or unmute an audio stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStreamSolo Solo or unsolo a particular stream. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStreamVolume Sets the volume index for a particular stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setSurroundFormatEnabled Sets and persists a certain surround format as enabled or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setVibrateSetting Sets the setting for when the vibrate type should vibrate. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWiredHeadsetOn Sets audio routing to the wired headset on or off. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | shouldVibrate Returns whether a particular type should vibrate according to user settings and the current ringer mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startBluetoothSco Start bluetooth SCO audio connection. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopBluetoothSco Stop bluetooth SCO audio connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unloadSoundEffects Unload Sound effects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterAudioDeviceCallback Unregisters an AudioDeviceCallback object which has been previously registered to receive notifications of changes to the set of connected audio devices. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterAudioPlaybackCallback Unregister an audio playback callback previously registered with registerAudioPlaybackCallback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterAudioRecordingCallback Unregister an audio recording callback previously registered with registerAudioRecordingCallback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterMediaButtonEventReceiver Unregister the receiver of MEDIA_BUTTON intents. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterMediaButtonEventReceiver Unregister the receiver of MEDIA_BUTTON intents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterRemoteControlClient Unregisters the remote control client that was providing information to display on the remote controls. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterRemoteController Unregisters a RemoteController, causing it to no longer receive media metadata and playback state information, and no longer be capable of controlling playback. |
| --- | --- |

## Constants

### ACTION_AUDIO_BECOMING_NOISY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_AUDIO_BECOMING_NOISY: String
```

Broadcast intent, a hint for applications that audio is about to become 'noisy' due to a change in audio outputs. For example, this intent may be sent when a wired headset is unplugged, or when an A2DP audio sink is disconnected, and the audio system is about to automatically switch audio route to the speaker. Applications that are controlling audio streams may consider pausing, reducing volume or some other action on receipt of this intent so as not to surprise the user with audio from the speaker.

 Value: "android.media.AUDIO_BECOMING_NOISY"

### ACTION_HDMI_AUDIO_PLUG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_HDMI_AUDIO_PLUG: String
```

Broadcast Action: A sticky broadcast indicating an HDMI cable was plugged or unplugged. The intent will have the following extra values: `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_AUDIO_PLUG_STATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_MAX_CHANNEL_COUNT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_ENCODINGS:kotlin.String`.

It can only be received by explicitly registering for it with android.content.Context#registerReceiver(BroadcastReceiver,IntentFilter).

 Value: "android.media.action.HDMI_AUDIO_PLUG"

### ACTION_HEADSET_PLUG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_HEADSET_PLUG: String
```

Broadcast Action: Wired Headset plugged in or unplugged. You *cannot* receive this through components declared in manifests, only by explicitly registering for it with android.content.Context#registerReceiver(BroadcastReceiver,IntentFilter).

The intent will have the following extra values:

- *state* - 0 for unplugged, 1 for plugged.
- *name* - Headset type, human readable string
- *microphone* - 1 if headset has a microphone, 0 otherwise

 Value: "android.intent.action.HEADSET_PLUG"

### ACTION_MICROPHONE_MUTE_CHANGED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MICROPHONE_MUTE_CHANGED: String
```

Broadcast Action: microphone muting state changed. You *cannot* receive this through components declared in manifests, only by explicitly registering for it with android.content.Context#registerReceiver(BroadcastReceiver,IntentFilter).

The intent has no extra values, use isMicrophoneMute to check whether the microphone is muted.

 Value: "android.media.action.MICROPHONE_MUTE_CHANGED"

### ACTION_SCO_AUDIO_STATE_CHANGED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCO_AUDIO_STATE_CHANGED: String
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` instead*

Sticky broadcast intent action indicating that the Bluetooth SCO audio connection state has changed. The intent contains on extra `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_STATE:kotlin.String` indicating the new state which is either `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_DISCONNECTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTED:kotlin.Int`

 Value: "android.media.SCO_AUDIO_STATE_CHANGED"

**See Also**

- startBluetoothSco

### ACTION_SCO_AUDIO_STATE_UPDATED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCO_AUDIO_STATE_UPDATED: String
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Sticky broadcast intent action indicating that the Bluetooth SCO audio connection state has been updated.

This intent has two extras:

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_STATE:kotlin.String` - The new SCO audio state.
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_PREVIOUS_STATE:kotlin.String`- The previous SCO audio state.

EXTRA_SCO_AUDIO_STATE or EXTRA_SCO_AUDIO_PREVIOUS_STATE can be any of:

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_DISCONNECTED:kotlin.Int`,
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTING:kotlin.Int` or
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTED:kotlin.Int`,

 Value: "android.media.ACTION_SCO_AUDIO_STATE_UPDATED"

**See Also**

- startBluetoothSco

### ACTION_SPEAKERPHONE_STATE_CHANGED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SPEAKERPHONE_STATE_CHANGED: String
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Broadcast Action: speakerphone state changed. You *cannot* receive this through components declared in manifests, only by explicitly registering for it with android.content.Context#registerReceiver(BroadcastReceiver,IntentFilter).

The intent has no extra values, use isSpeakerphoneOn to check whether the speakerphone functionality is enabled or not.

 Value: "android.media.action.SPEAKERPHONE_STATE_CHANGED"

### ADJUST_LOWER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_LOWER: Int
```

Decrease the ringer volume.

 Value: -1

**See Also**

- adjustVolume
- adjustStreamVolume

### ADJUST_MUTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_MUTE: Int
```

Mute the volume. Has no effect if the stream is already muted.

 Value: -100

**See Also**

- adjustVolume
- adjustStreamVolume

### ADJUST_RAISE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_RAISE: Int
```

Increase the ringer volume.

 Value: 1

**See Also**

- adjustVolume
- adjustStreamVolume

### ADJUST_SAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_SAME: Int
```

Maintain the previous ringer volume. This may be useful when needing to show the volume toast without actually modifying the volume.

 Value: 0

**See Also**

- adjustVolume
- adjustStreamVolume

### ADJUST_TOGGLE_MUTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_TOGGLE_MUTE: Int
```

Toggle the mute state. If muted the stream will be unmuted. If not muted the stream will be muted.

 Value: 101

**See Also**

- adjustVolume
- adjustStreamVolume

### ADJUST_UNMUTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADJUST_UNMUTE: Int
```

Unmute the volume. Has no effect if the stream is not muted.

 Value: 100

**See Also**

- adjustVolume
- adjustStreamVolume

### AUDIOFOCUS_GAIN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_GAIN: Int
```

Used to indicate a gain of audio focus, or a request of audio focus, of unknown duration.

 Value: 1

**See Also**

- onAudioFocusChange
- requestAudioFocus

### AUDIOFOCUS_GAIN_TRANSIENT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_GAIN_TRANSIENT: Int
```

Used to indicate a temporary gain or request of audio focus, anticipated to last a short amount of time. Examples of temporary changes are the playback of driving directions, or an event notification.

 Value: 2

**See Also**

- onAudioFocusChange
- requestAudioFocus

### AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE: Int
```

Used to indicate a temporary request of audio focus, anticipated to last a short amount of time, during which no other applications, or system components, should play anything. Examples of exclusive and transient audio focus requests are voice memo recording and speech recognition, during which the system shouldn't play any notifications, and media playback should have paused.

 Value: 4

**See Also**

- requestAudioFocus

### AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK: Int
```

Used to indicate a temporary request of audio focus, anticipated to last a short amount of time, and where it is acceptable for other audio applications to keep playing after having lowered their output level (also referred to as "ducking"). Examples of temporary changes are the playback of driving directions where playback of music in the background is acceptable.

 Value: 3

**See Also**

- onAudioFocusChange
- requestAudioFocus

### AUDIOFOCUS_LOSS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_LOSS: Int
```

Used to indicate a loss of audio focus of unknown duration.

 Value: -1

**See Also**

- onAudioFocusChange

### AUDIOFOCUS_LOSS_TRANSIENT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_LOSS_TRANSIENT: Int
```

Used to indicate a transient loss of audio focus.

 Value: -2

**See Also**

- onAudioFocusChange

### AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_LOSS_TRANSIENT_CAN_DUCK: Int
```

Used to indicate a transient loss of audio focus where the loser of the audio focus can lower its output volume if it wants to continue playing (also referred to as "ducking"), as the new focus owner doesn't require others to be silent.

 Value: -3

**See Also**

- onAudioFocusChange

### AUDIOFOCUS_NONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_NONE: Int
```

Used to indicate no audio focus has been gained or lost, or requested.

 Value: 0

### AUDIOFOCUS_REQUEST_DELAYED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_REQUEST_DELAYED: Int
```

A focus change request whose granting is delayed: the request was successful, but the requester will only be granted audio focus once the condition that prevented immediate granting has ended. See requestAudioFocus and setAcceptsDelayedFocusGain

 Value: 2

### AUDIOFOCUS_REQUEST_FAILED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_REQUEST_FAILED: Int
```

A failed focus change request.

 Value: 0

### AUDIOFOCUS_REQUEST_GRANTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIOFOCUS_REQUEST_GRANTED: Int
```

A successful focus change request.

 Value: 1

### AUDIO_SESSION_ID_GENERATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_SESSION_ID_GENERATE: Int
```

A special audio session ID to indicate that the audio session ID isn't known and the framework should generate a new value. This can be used when building a new AudioTrack instance with AudioTrack.

 Value: 0

### DIRECT_PLAYBACK_BITSTREAM_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECT_PLAYBACK_BITSTREAM_SUPPORTED: Int
```

Return value for getDirectPlaybackSupport: direct playback supported. This value covers direct playback that is bitstream pass-through such as compressed pass-through.

 Value: 4

### DIRECT_PLAYBACK_NOT_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECT_PLAYBACK_NOT_SUPPORTED: Int
```

Return value for getDirectPlaybackSupport: direct playback not supported.

 Value: 0

### DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED: Int
```

Return value for getDirectPlaybackSupport: direct offload playback supported with gapless transitions. Compressed offload is a variant of direct playback. It is the feature that allows audio processing tasks to be done on the Android device but not on the application processor, instead, it is handled by dedicated hardware such as audio DSPs. That will allow the application processor to be idle as much as possible, which is good for power saving. Compressed offload playback supports `https://developer.android.com/reference/kotlin/android/media/AudioTrack.StreamEventCallback` for event notifications. Gapless transitions indicates the ability to play consecutive audio tracks without an audio silence in between.

 Value: 3

### DIRECT_PLAYBACK_OFFLOAD_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECT_PLAYBACK_OFFLOAD_SUPPORTED: Int
```

Return value for getDirectPlaybackSupport: direct offload playback supported. Compressed offload is a variant of direct playback. It is the feature that allows audio processing tasks to be done on the Android device but not on the application processor, instead, it is handled by dedicated hardware such as audio DSPs. That will allow the application processor to be idle as much as possible, which is good for power saving. Compressed offload playback supports `https://developer.android.com/reference/kotlin/android/media/AudioTrack.StreamEventCallback` for event notifications.

 Value: 1

### ENCODED_SURROUND_OUTPUT_ALWAYS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODED_SURROUND_OUTPUT_ALWAYS: Int
```

The surround sound formats are ALWAYS available, even if they are not detected by the hardware. Those formats will be reported as part of the HDMI output capability. Applications are then free to use either PCM or encoded output.

 Value: 2

### ENCODED_SURROUND_OUTPUT_AUTO

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODED_SURROUND_OUTPUT_AUTO: Int
```

The surround sound formats are available for use if they are detected. This is the default mode.

 Value: 0

### ENCODED_SURROUND_OUTPUT_MANUAL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODED_SURROUND_OUTPUT_MANUAL: Int
```

Surround sound formats are available according to the choice of user, even if they are not detected by the hardware. Those formats will be reported as part of the HDMI output capability. Applications are then free to use either PCM or encoded output.

 Value: 3

### ENCODED_SURROUND_OUTPUT_NEVER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODED_SURROUND_OUTPUT_NEVER: Int
```

The surround sound formats are NEVER available, even if they are detected by the hardware. Those formats will not be reported.

 Value: 1

### ENCODED_SURROUND_OUTPUT_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCODED_SURROUND_OUTPUT_UNKNOWN: Int
```

The mode for surround sound formats is unknown.

 Value: -1

### ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR: Int
```

A default error code.

 Value: -1

### ERROR_DEAD_OBJECT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DEAD_OBJECT: Int
```

An error code indicating that the object reporting it is no longer valid and needs to be recreated.

 Value: -6

### EXTRA_AUDIO_PLUG_STATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_AUDIO_PLUG_STATE: String
```

Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to communicate whether HDMI is plugged in or unplugged. An integer value of 1 indicates a plugged-in state, 0 is unplugged.

 Value: "android.media.extra.AUDIO_PLUG_STATE"

### EXTRA_ENCODINGS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ENCODINGS: String
```

Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to define the audio encodings supported by the connected HDMI device. The corresponding array of encoding values is only available when the device is plugged in (as expressed by `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_AUDIO_PLUG_STATE:kotlin.String`). Encoding values are defined in AudioFormat (for instance see `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int`). Use getIntArrayExtra to retrieve the encoding values.

 Value: "android.media.extra.ENCODINGS"

### EXTRA_MAX_CHANNEL_COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_MAX_CHANNEL_COUNT: String
```

Extra used in `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_HDMI_AUDIO_PLUG:kotlin.String` to define the maximum number of channels supported by the HDMI device. The corresponding integer value is only available when the device is plugged in (as expressed by `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_AUDIO_PLUG_STATE:kotlin.String`).

 Value: "android.media.extra.MAX_CHANNEL_COUNT"

### EXTRA_RINGER_MODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RINGER_MODE: String
```

The new ringer mode.

 Value: "android.media.EXTRA_RINGER_MODE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_NORMAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_SILENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_VIBRATE:kotlin.Int`

### EXTRA_SCO_AUDIO_PREVIOUS_STATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SCO_AUDIO_PREVIOUS_STATE: String
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Extra for intent `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` containing the previous bluetooth SCO connection state.

 Value: "android.media.extra.SCO_AUDIO_PREVIOUS_STATE"

### EXTRA_SCO_AUDIO_STATE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SCO_AUDIO_STATE: String
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Extra for intent `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_CHANGED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` containing the new bluetooth SCO connection state.

 Value: "android.media.extra.SCO_AUDIO_STATE"

### EXTRA_VIBRATE_SETTING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VIBRATE_SETTING: String
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode and listen to `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_CHANGED_ACTION:kotlin.String` instead.*

The new vibrate setting for a particular type.

 Value: "android.media.EXTRA_VIBRATE_SETTING"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_VIBRATE_TYPE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_OFF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ONLY_SILENT:kotlin.Int`

### EXTRA_VIBRATE_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_VIBRATE_TYPE: String
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode and listen to `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_CHANGED_ACTION:kotlin.String` instead.*

The vibrate type whose setting has changed.

 Value: "android.media.EXTRA_VIBRATE_TYPE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_CHANGED_ACTION:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_NOTIFICATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_RINGER:kotlin.Int`

### FLAG_ALLOW_RINGER_MODES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ALLOW_RINGER_MODES: Int
```

Whether to include ringer modes as possible options when changing volume. For example, if true and volume level is 0 and the volume is adjusted with `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int`, then the ringer mode may switch the silent or vibrate mode.

By default this is on for the ring stream. If this flag is included, this behavior will be present regardless of the stream type being affected by the ringer mode.

 Value: 2

**See Also**

- adjustVolume
- adjustStreamVolume

### FLAG_PLAY_SOUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PLAY_SOUND: Int
```

Whether to play a sound when changing the volume.

If this is given to adjustVolume or adjustSuggestedStreamVolume, it may be ignored in some cases (for example, the decided stream type is not `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, or the volume is being adjusted downward).

 Value: 4

**See Also**

- adjustStreamVolume
- adjustVolume
- setStreamVolume

### FLAG_REMOVE_SOUND_AND_VIBRATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REMOVE_SOUND_AND_VIBRATE: Int
```

Removes any sounds/vibrate that may be in the queue, or are playing (related to changing volume).

 Value: 8

### FLAG_SHOW_UI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SHOW_UI: Int
```

Show a toast containing the current volume.

 Value: 1

**See Also**

- adjustStreamVolume
- adjustVolume
- setStreamVolume
- setRingerMode

### FLAG_VIBRATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_VIBRATE: Int
```

Whether to vibrate if going into the vibrate ringer mode.

 Value: 16

### FX_BACK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_BACK: Int
```

Back sound

 Value: 10

**See Also**

- playSoundEffect

### FX_FOCUS_NAVIGATION_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_FOCUS_NAVIGATION_DOWN: Int
```

Focus has moved down

 Value: 2

**See Also**

- playSoundEffect

### FX_FOCUS_NAVIGATION_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_FOCUS_NAVIGATION_LEFT: Int
```

Focus has moved left

 Value: 3

**See Also**

- playSoundEffect

### FX_FOCUS_NAVIGATION_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_FOCUS_NAVIGATION_RIGHT: Int
```

Focus has moved right

 Value: 4

**See Also**

- playSoundEffect

### FX_FOCUS_NAVIGATION_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_FOCUS_NAVIGATION_UP: Int
```

Focus has moved up

 Value: 1

**See Also**

- playSoundEffect

### FX_KEYPRESS_DELETE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEYPRESS_DELETE: Int
```

IME delete keypress sound

 Value: 7

**See Also**

- playSoundEffect

### FX_KEYPRESS_INVALID

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEYPRESS_INVALID: Int
```

Invalid keypress sound

 Value: 9

**See Also**

- playSoundEffect

### FX_KEYPRESS_RETURN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEYPRESS_RETURN: Int
```

IME return_keypress sound

 Value: 8

**See Also**

- playSoundEffect

### FX_KEYPRESS_SPACEBAR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEYPRESS_SPACEBAR: Int
```

IME spacebar keypress sound

 Value: 6

**See Also**

- playSoundEffect

### FX_KEYPRESS_STANDARD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEYPRESS_STANDARD: Int
```

IME standard keypress sound

 Value: 5

**See Also**

- playSoundEffect

### FX_KEY_CLICK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FX_KEY_CLICK: Int
```

Keyboard and direction pad click sound

 Value: 0

**See Also**

- playSoundEffect

### GET_DEVICES_ALL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_DEVICES_ALL: Int
```

Specifies to the getDevices method to include both source and sink devices.

 Value: 3

### GET_DEVICES_INPUTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_DEVICES_INPUTS: Int
```

Specifies to the getDevices method to include source (i.e. input) audio devices.

 Value: 1

### GET_DEVICES_OUTPUTS

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GET_DEVICES_OUTPUTS: Int
```

Specifies to the getDevices method to include sink (i.e. output) audio devices.

 Value: 2

### MODE_ASSISTANT_CONVERSATION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_ASSISTANT_CONVERSATION: Int
```

Use this mode whenever an assistant conversation mode is started.

To check if this mode is allowed to be used by an app, use canManageAssistantAudio.

 Value: 7

### MODE_CALL_REDIRECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_CALL_REDIRECT: Int
```

A telephony call is established and its audio is being redirected to another device.

 Value: 5

### MODE_CALL_SCREENING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_CALL_SCREENING: Int
```

Call screening in progress. Call is connected and audio is accessible to call screening applications but other audio use cases are still possible.

 Value: 4

### MODE_COMMUNICATION_REDIRECT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_COMMUNICATION_REDIRECT: Int
```

An audio/video chat or VoIP call is established and its audio is being redirected to another device.

 Value: 6

### MODE_CURRENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_CURRENT: Int
```

Current audio mode. Used to apply audio routing to current mode.

 Value: -1

### MODE_INVALID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_INVALID: Int
```

Invalid audio mode.

 Value: -2

### MODE_IN_CALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_IN_CALL: Int
```

In call audio mode. A telephony call is established.

 Value: 2

### MODE_IN_COMMUNICATION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_IN_COMMUNICATION: Int
```

In communication audio mode. An audio/video chat or VoIP call is established.

 Value: 3

### MODE_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_NORMAL: Int
```

Normal audio mode: not ringing and no call established.

 Value: 0

### MODE_RINGTONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODE_RINGTONE: Int
```

Ringing audio mode. An incoming is being signaled.

 Value: 1

### NUM_STREAMS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUM_STREAMS: Int
```

**Deprecated:** *Do not iterate on volume stream type values.*

 Value: 5

### PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED: Int
```

Return value for getPlaybackOffloadSupport: offload playback supported with gapless transitions

 Value: 2

### PLAYBACK_OFFLOAD_NOT_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYBACK_OFFLOAD_NOT_SUPPORTED: Int
```

Return value for getPlaybackOffloadSupport: offload playback not supported

 Value: 0

### PLAYBACK_OFFLOAD_SUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PLAYBACK_OFFLOAD_SUPPORTED: Int
```

Return value for getPlaybackOffloadSupport: offload playback supported

 Value: 1

### PROPERTY_OUTPUT_FRAMES_PER_BUFFER

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_OUTPUT_FRAMES_PER_BUFFER: String
```

Used as a key for getProperty to request the native or optimal output buffer size for this device's low latency output stream, in decimal PCM frames. Latency-sensitive apps should use this value as a minimum, and offer the user the option to override it. The low latency output stream is typically either the device's primary output stream, or another output stream with smaller buffers.

 Value: "android.media.property.OUTPUT_FRAMES_PER_BUFFER"

### PROPERTY_OUTPUT_SAMPLE_RATE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_OUTPUT_SAMPLE_RATE: String
```

Used as a key for getProperty to request the native or optimal output sample rate for this device's low latency output stream, in decimal Hz. Latency-sensitive apps should use this value as a default, and offer the user the option to override it. The low latency output stream is typically either the device's primary output stream, or another output stream with smaller buffers.

 Value: "android.media.property.OUTPUT_SAMPLE_RATE"

### PROPERTY_SUPPORT_AUDIO_SOURCE_UNPROCESSED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SUPPORT_AUDIO_SOURCE_UNPROCESSED: String
```

Used as a key for getProperty to determine if the unprocessed audio source is available and supported with the expected frequency range and level response.

 Value: "android.media.property.SUPPORT_AUDIO_SOURCE_UNPROCESSED"

### PROPERTY_SUPPORT_MIC_NEAR_ULTRASOUND

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SUPPORT_MIC_NEAR_ULTRASOUND: String
```

Used as a key for getProperty to determine if the default microphone audio source supports near-ultrasound frequencies (range of 18 - 21 kHz).

 Value: "android.media.property.SUPPORT_MIC_NEAR_ULTRASOUND"

### PROPERTY_SUPPORT_SPEAKER_NEAR_ULTRASOUND

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SUPPORT_SPEAKER_NEAR_ULTRASOUND: String
```

Used as a key for getProperty to determine if the default speaker audio path supports near-ultrasound frequencies (range of 18 - 21 kHz).

 Value: "android.media.property.SUPPORT_SPEAKER_NEAR_ULTRASOUND"

### RINGER_MODE_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RINGER_MODE_CHANGED_ACTION: String
```

Sticky broadcast intent action indicating that the ringer mode has changed. Includes the new ringer mode.

 Value: "android.media.RINGER_MODE_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_RINGER_MODE:kotlin.String`

### RINGER_MODE_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RINGER_MODE_NORMAL: Int
```

Ringer mode that may be audible and may vibrate. It will be audible if the volume before changing out of this mode was audible. It will vibrate if the vibrate setting is on.

 Value: 2

**See Also**

- setRingerMode
- getRingerMode

### RINGER_MODE_SILENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RINGER_MODE_SILENT: Int
```

Ringer mode that will be silent and will not vibrate. (This overrides the vibrate setting.)

 Value: 0

**See Also**

- setRingerMode
- getRingerMode

### RINGER_MODE_VIBRATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RINGER_MODE_VIBRATE: Int
```

Ringer mode that will be silent and will vibrate. (This will cause the phone ringer to always vibrate, but the notification vibrate to only vibrate if set.)

 Value: 1

**See Also**

- setRingerMode
- getRingerMode

### ROUTE_ALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_ALL: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Used for mask parameter of setRouting.

 Value: -1

### ROUTE_BLUETOOTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_BLUETOOTH: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

 Value: 4

### ROUTE_BLUETOOTH_A2DP

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_BLUETOOTH_A2DP: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Routing audio output to bluetooth A2DP

 Value: 16

### ROUTE_BLUETOOTH_SCO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_BLUETOOTH_SCO: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Routing audio output to bluetooth SCO

 Value: 4

### ROUTE_EARPIECE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_EARPIECE: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Routing audio output to earpiece

 Value: 1

### ROUTE_HEADSET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_HEADSET: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Routing audio output to headset

 Value: 8

### ROUTE_SPEAKER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROUTE_SPEAKER: Int
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Routing audio output to speaker

 Value: 2

### SCO_AUDIO_STATE_CONNECTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCO_AUDIO_STATE_CONNECTED: Int
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Value for extra `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_SCO_AUDIO_PREVIOUS_STATE:kotlin.String` indicating that the SCO audio channel is established

 Value: 1

### SCO_AUDIO_STATE_CONNECTING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCO_AUDIO_STATE_CONNECTING: Int
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Value for extra EXTRA_SCO_AUDIO_STATE or EXTRA_SCO_AUDIO_PREVIOUS_STATE indicating that the SCO audio channel is being established

 Value: 2

### SCO_AUDIO_STATE_DISCONNECTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCO_AUDIO_STATE_DISCONNECTED: Int
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Value for extra EXTRA_SCO_AUDIO_STATE or EXTRA_SCO_AUDIO_PREVIOUS_STATE indicating that the SCO audio channel is not established

 Value: 0

### SCO_AUDIO_STATE_ERROR

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCO_AUDIO_STATE_ERROR: Int
```

**Deprecated:** *Use addOnCommunicationDeviceChangedListener instead.*

Value for extra EXTRA_SCO_AUDIO_STATE indicating that there was an error trying to obtain the state

 Value: -1

### STREAM_ACCESSIBILITY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_ACCESSIBILITY: Int
```

Used to identify the volume of audio streams for accessibility prompts

 Value: 10

### STREAM_ALARM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_ALARM: Int
```

Used to identify the volume of audio streams for alarms

 Value: 4

### STREAM_ASSISTANT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_ASSISTANT: Int
```

Used to identify the volume of audio streams for virtual assistant

 Value: 11

### STREAM_DTMF

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_DTMF: Int
```

Used to identify the volume of audio streams for DTMF Tones

 Value: 8

### STREAM_MUSIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_MUSIC: Int
```

Used to identify the volume of audio streams for music playback

 Value: 3

### STREAM_NOTIFICATION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_NOTIFICATION: Int
```

Used to identify the volume of audio streams for notifications

 Value: 5

### STREAM_RING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_RING: Int
```

Used to identify the volume of audio streams for the phone ring

 Value: 2

### STREAM_SYSTEM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_SYSTEM: Int
```

Used to identify the volume of audio streams for system sounds

 Value: 1

### STREAM_VOICE_CALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREAM_VOICE_CALL: Int
```

Used to identify the volume of audio streams for phone calls

 Value: 0

### USE_DEFAULT_STREAM_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val USE_DEFAULT_STREAM_TYPE: Int
```

Suggests using the default stream type. This may not be used in all places a stream type is needed.

 Value: -2147483648

### VIBRATE_SETTING_CHANGED_ACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_SETTING_CHANGED_ACTION: String
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode and listen to `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_CHANGED_ACTION:kotlin.String` instead.*

Broadcast intent action indicating that the vibrate setting has changed. Includes the vibrate type and its new setting.

 Value: "android.media.VIBRATE_SETTING_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_VIBRATE_TYPE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#EXTRA_VIBRATE_SETTING:kotlin.String`

### VIBRATE_SETTING_OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_SETTING_OFF: Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Vibrate setting that suggests to never vibrate.

 Value: 0

**See Also**

- setVibrateSetting
- getVibrateSetting

### VIBRATE_SETTING_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_SETTING_ON: Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Vibrate setting that suggests to vibrate when possible.

 Value: 1

**See Also**

- setVibrateSetting
- getVibrateSetting

### VIBRATE_SETTING_ONLY_SILENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_SETTING_ONLY_SILENT: Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Vibrate setting that suggests to only vibrate when in the vibrate ringer mode.

 Value: 2

**See Also**

- setVibrateSetting
- getVibrateSetting

### VIBRATE_TYPE_NOTIFICATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_TYPE_NOTIFICATION: Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Vibrate type that corresponds to notifications.

 Value: 1

**See Also**

- setVibrateSetting
- getVibrateSetting
- shouldVibrate

### VIBRATE_TYPE_RINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIBRATE_TYPE_RINGER: Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Vibrate type that corresponds to the ringer.

 Value: 0

**See Also**

- setVibrateSetting
- getVibrateSetting
- shouldVibrate

## Public methods

### abandonAudioFocus

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun abandonAudioFocus(l: AudioManager.OnAudioFocusChangeListener!): Int
```

**Deprecated:** *use abandonAudioFocusRequest*

Abandon audio focus. Causes the previous focus owner, if any, to receive focus.

| Parameters ||
|---|---|
| `l` | [AudioManager.OnAudioFocusChangeListener](../android/media/AudioManager.OnAudioFocusChangeListener.md)!: the listener with which focus was requested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_GRANTED:kotlin.Int` |

### abandonAudioFocusRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun abandonAudioFocusRequest(focusRequest: AudioFocusRequest): Int
```

Abandon audio focus. Causes the previous focus owner, if any, to receive focus.

| Parameters ||
|---|---|
| `focusRequest` | [AudioFocusRequest](AudioFocusRequest.md): the AudioFocusRequest that was used when requesting focus with requestAudioFocus. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_GRANTED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if passed a null argument |

### addOnCommunicationDeviceChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnCommunicationDeviceChangedListener(
    executor: Executor, 
    listener: AudioManager.OnCommunicationDeviceChangedListener
): Unit
```

Adds a listener for being notified of changes to the communication audio device. See setCommunicationDevice.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [AudioManager.OnCommunicationDeviceChangedListener](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md): This value cannot be `null`. |

### addOnModeChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnModeChangedListener(
    executor: Executor, 
    listener: AudioManager.OnModeChangedListener
): Unit
```

Adds a listener to be notified of changes to the audio mode. See getMode

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [AudioManager.OnModeChangedListener](../android/media/AudioManager.OnModeChangedListener.md): This value cannot be `null`. |

### addOnPreferredMixerAttributesChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnPreferredMixerAttributesChangedListener(
    executor: Executor, 
    listener: AudioManager.OnPreferredMixerAttributesChangedListener
): Unit
```

Adds a listener for being notified of changes to the preferred mixer attributes.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to execute the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [AudioManager.OnPreferredMixerAttributesChangedListener](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md): the listener to be notified of changes in the preferred mixer attributes. This value cannot be `null`. |

### adjustStreamVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun adjustStreamVolume(
    streamType: Int, 
    direction: Int, 
    flags: Int
): Unit
```

Adjusts the volume of a particular stream by one step in a direction.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed.

From N onward, ringer mode adjustments that would toggle Do Not Disturb are not allowed unless the app has been granted Notification Policy Access. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream type to adjust. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ACCESSIBILITY:kotlin.Int`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction to adjust the volume. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the adjustment triggers a Do Not Disturb change and the caller is not granted notification policy access. |

**See Also**

- adjustVolume
- setStreamVolume

### adjustSuggestedStreamVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun adjustSuggestedStreamVolume(
    direction: Int, 
    suggestedStreamType: Int, 
    flags: Int
): Unit
```

Adjusts the volume of the most relevant stream, or the given fallback stream.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction to adjust the volume. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_MUTE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_UNMUTE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_TOGGLE_MUTE:kotlin.Int`. |
| `suggestedStreamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream type that will be used if there isn't a relevant stream. `https://developer.android.com/reference/kotlin/android/media/AudioManager#USE_DEFAULT_STREAM_TYPE:kotlin.Int` is valid here. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` |
| --- | --- |

**See Also**

- adjustVolume
- adjustStreamVolume
- setStreamVolume
- isVolumeFixed

### adjustVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun adjustVolume(
    direction: Int, 
    flags: Int
): Unit
```

Adjusts the volume of the most relevant stream. For example, if a call is active, it will have the highest priority regardless of if the in-call screen is showing. Another example, if music is playing in the background and a call is not active, the music stream will be adjusted.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction to adjust the volume. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_MUTE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_UNMUTE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_TOGGLE_MUTE:kotlin.Int`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` |

**See Also**

- adjustSuggestedStreamVolume
- adjustStreamVolume
- setStreamVolume
- isVolumeFixed

### adjustVolumeGroupVolume

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun adjustVolumeGroupVolume(
    groupId: Int, 
    direction: Int, 
    flags: Int
): Unit
```

Adjusts the volume of a particular group associated to given id by one step in a direction.

If the volume group is associated to a stream type, it fallbacks on adjustStreamVolume for compatibility reason.

Call first in prior getVolumeGroupIdForAttributes to retrieve the volume group id supporting the given AudioAttributes.

| Parameters ||
|---|---|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of the audio volume group to consider. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction to adjust the volume. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the adjustment triggers a Do Not Disturb change and the caller is not granted notification policy access. |

### canManageAssistantAudio

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canManageAssistantAudio(): Boolean
```

Checks if the calling app can manage assistant audio.

To request access, use `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_MANAGE_ASSISTANT_AUDIO:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the calling app can manage assistant audio, false otherwise. |

### clearCommunicationDevice

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearCommunicationDevice(): Unit
```

Cancels previous communication device selection made with setCommunicationDevice.

### clearPreferredMixerAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearPreferredMixerAttributes(
    attributes: AudioAttributes, 
    device: AudioDeviceInfo
): Boolean
```

Clears the current preferred mixer attributes that were previously set via setPreferredMixerAttributes 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes whose mixer attributes should be cleared. This value cannot be `null`. |
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md): the expected routing device. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true only if the preferred mixer attributes are removed successfully. |

**See Also**

- setPreferredMixerAttributes
- getPreferredMixerAttributes

### dispatchMediaKeyEvent

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dispatchMediaKeyEvent(keyEvent: KeyEvent!): Unit
```

Sends a simulated key event for a media button. To simulate a key press, you must first send a KeyEvent built with a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int` action, then another event with the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_UP:kotlin.Int` action.

The key event will be sent to the current media key event consumer which registered with registerMediaButtonEventReceiver.

| Parameters ||
|---|---|
| `keyEvent` | [KeyEvent](../android.view/KeyEvent.md)!: a media session `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`, as defined by isMediaSessionKey. |

### generateAudioSessionId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateAudioSessionId(): Int
```

Return a new audio session identifier not associated with any player or effect. An audio session identifier is a system wide unique identifier for a set of audio streams (one or more mixed together).

The primary use of the audio session ID is to associate audio effects to audio players, such as MediaPlayer or AudioTrack: all audio effects sharing the same audio session ID will be applied to the mixed audio content of the players that share the same audio session.

This method can for instance be used when creating one of the AudioEffect objects to define the audio session of the effect, or to specify a session for a speech synthesis utterance in `https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeech.Engine.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a new unclaimed and unused audio session identifier, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ERROR:kotlin.Int` when the system failed to generate a new session, a condition in which audio playback or recording will subsequently fail as well. |

### getActivePlaybackConfigurations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivePlaybackConfigurations(): MutableList<AudioPlaybackConfiguration!>
```

Returns the current active audio playback configurations of the device

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioPlaybackConfiguration!>` | a non-null list of playback configurations. An empty list indicates there is no playback active when queried. |

**See Also**

- AudioPlaybackConfiguration

### getActiveRecordingConfigurations

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActiveRecordingConfigurations(): MutableList<AudioRecordingConfiguration!>
```

Returns the current active audio recording configurations of the device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioRecordingConfiguration!>` | a non-null list of recording configurations. An empty list indicates there is no recording active when queried. |

**See Also**

- AudioRecordingConfiguration

### getAllowedCapturePolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllowedCapturePolicy(): Int
```

Return the capture policy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the capture policy set by setAllowedCapturePolicy or the default if it was not called. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_NONE:kotlin.Int` |

### getAudioDevicesForAttributes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioDevicesForAttributes(attributes: AudioAttributes): MutableList<AudioDeviceInfo!>
```

Get the audio devices that would be used for the routing of the given audio attributes. These are the devices anticipated to play sound from an AudioTrack created with the specified AudioAttributes. The audio routing can change if audio devices are physically connected or disconnected or concurrently through AudioRouting or MediaRouter.

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes for which the routing is being queried. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo!>` | an empty list if there was an issue with the request, a list of AudioDeviceInfo otherwise (typically one device, except for duplicated paths). This value cannot be `null`. |

### getAudioHwSyncForSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAudioHwSyncForSession(sessionId: Int): Int
```

Retrieves the Hardware A/V synchronization ID corresponding to the given audio session ID. For more details on Hardware A/V synchronization please refer to [media tunneling documentation](https://source.android.com/devices/tv/multimedia-tunneling/).

| Parameters ||
|---|---|
| `sessionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the audio session ID for which the HW A/V sync ID is retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the HW A/V sync ID for this audio session (an integer different from 0). |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if HW A/V synchronization is not supported. |

### getAvailableCommunicationDevices

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAvailableCommunicationDevices(): MutableList<AudioDeviceInfo!>
```

Returns a list of audio devices that can be selected for communication use cases via setCommunicationDevice.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo!>` | a list of AudioDeviceInfo suitable for use with setCommunicationDevice(). This value cannot be `null`. |

### getCommunicationDevice

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCommunicationDevice(): AudioDeviceInfo?
```

Returns currently selected audio device for communication.

This API replaces the following deprecated APIs:

- isBluetoothScoOn
- isSpeakerphoneOn

| Return ||
|---|---|
| AudioDeviceInfo | an AudioDeviceInfo indicating which audio device is currently selected for communication use cases. Can be null on platforms not supporting `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String`. is used. |

### getDevices

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDevices(flags: Int): Array<AudioDeviceInfo!>!
```

Returns an array of AudioDeviceInfo objects corresponding to the audio devices currently connected to the system and meeting the criteria specified in the `flags` parameter.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A set of bitflags specifying the criteria to test. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_INPUTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_OUTPUTS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo!>!` | A (possibly zero-length) array of AudioDeviceInfo objects. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_OUTPUTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_INPUTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_ALL:kotlin.Int`

### getDirectPlaybackSupport

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDirectPlaybackSupport(
    format: AudioFormat, 
    attributes: AudioAttributes
): Int
```

Returns a bitfield representing the different forms of direct playback currently available for a given audio format.

Direct playback means that the audio stream is not altered by the framework. The audio stream will not be resampled, volume scaled, downmixed or mixed with other content by the framework. But it may be wrapped in a higher level protocol such as IEC61937 for passthrough.

Checking for direct support can help the app select the representation of audio content that most closely matches the capabilities of the device and peripherals (e.g. A/V receiver) connected to it. Note that the provided stream can still be re-encoded or mixed with other streams, if needed.

| Parameters ||
|---|---|
| `format` | [AudioFormat](AudioFormat.md): the audio format (codec, sample rate, channels) being checked. This value cannot be `null`. |
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes to be used for playback. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the direct playback mode available with given format and attributes. The returned value will be `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_NOT_SUPPORTED:kotlin.Int` or a combination of `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_BITSTREAM_SUPPORTED:kotlin.Int`. Note that if `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` is present in the returned value, then `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` will be too. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#DIRECT_PLAYBACK_BITSTREAM_SUPPORTED:kotlin.Int` |

### getDirectProfilesForAttributes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDirectProfilesForAttributes(attributes: AudioAttributes): MutableList<AudioProfile!>
```

Returns a list of direct AudioProfile that are supported for the specified AudioAttributes. This can be empty in case of an error or if no direct playback is possible.

Direct playback means that the audio stream is not resampled or downmixed by the framework. Checking for direct support can help the app select the representation of audio content that most closely matches the capabilities of the device and peripherals (e.g. A/V receiver) connected to it. Note that the provided stream can still be re-encoded or mixed with other streams, if needed.

When using this information to inform your application which audio format to play, query again whenever audio output devices change (see AudioDeviceCallback).

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): a non-null AudioAttributes instance. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioProfile!>` | a list of AudioProfile This value cannot be `null`. |

### getDirectProfilesForAttributes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDirectProfilesForAttributes(
    attributes: AudioAttributes, 
    uid: Int
): MutableList<AudioProfile!>
```

Returns a list of direct AudioProfile that are supported for the specified AudioAttributes. This can be empty in case of an error or if no direct playback is possible.

Direct playback means that the audio stream is not resampled or downmixed by the framework. Checking for direct support can help the app select the representation of audio content that most closely matches the capabilities of the device and peripherals (e.g. A/V receiver) connected to it. Note that the provided stream can still be re-encoded or mixed with other streams, if needed.

When using this information to inform your application which audio format to play, query again whenever audio output devices change (see AudioDeviceCallback).

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): a non-null AudioAttributes instance. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Application/Service UID for the query |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioProfile!>` | a list of AudioProfile This value cannot be `null`. |

### getEncodedSurroundMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncodedSurroundMode(): Int
```

Gets the surround sound mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | true if successful, otherwise false. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_NEVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_MANUAL:kotlin.Int` |

### getMicrophones

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMicrophones(): MutableList<MicrophoneInfo!>!
```

Returns a list of MicrophoneInfo that corresponds to the characteristics of all available microphones. The list is empty when no microphones are available on the device. An error during the query will result in an IOException being thrown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/MicrophoneInfo!>!` | a list that contains all microphones' characteristics |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurs. |

### getMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMode(): Int
```

Returns the current audio mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current audio mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_RINGTONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_COMMUNICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_SCREENING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_REDIRECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_COMMUNICATION_REDIRECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int` |

### getParameters

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParameters(keys: String!): String!
```

Gets a variable number of parameter values from audio hardware.

| Parameters ||
|---|---|
| `keys` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: list of parameters |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | list of parameters key value pairs in the form: key1=value1;key2=value2;... |

### getPlaybackOffloadSupport

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getPlaybackOffloadSupport(
    format: AudioFormat, 
    attributes: AudioAttributes
): Int
```

**Deprecated:** *Use getDirectPlaybackSupport instead*

Returns whether offloaded playback of an audio format is supported on the device or not and when supported whether gapless transitions are possible or not.

Offloaded playback is the feature where the decoding and playback of an audio stream is not competing with other software resources. In general, it is supported by dedicated hardware, such as audio DSPs.

Note that this query only provides information about the support of an audio format, it does not indicate whether the resources necessary for the offloaded playback are available at that instant.

| Parameters ||
|---|---|
| `format` | [AudioFormat](AudioFormat.md): the audio format (codec, sample rate, channels) being checked. This value cannot be `null`. |
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes to be used for playback. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_NOT_SUPPORTED:kotlin.Int` if offload playback if not supported, `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` if offload playback is supported or `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` if gapless transitions are also supported. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#PLAYBACK_OFFLOAD_GAPLESS_SUPPORTED:kotlin.Int` |

### getPreferredMixerAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPreferredMixerAttributes(
    attributes: AudioAttributes, 
    device: AudioDeviceInfo
): AudioMixerAttributes?
```

Returns current preferred mixer attributes that is set via setPreferredMixerAttributes

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes whose mixer attributes should be set. This value cannot be `null`. |
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md): the expected routing device. This value cannot be `null`. |

| Return ||
|---|---|
| AudioMixerAttributes | the preferred mixer attributes, which will be null when no preferred mixer attributes have been set, or when they have been cleared. |

**See Also**

- setPreferredMixerAttributes
- clearPreferredMixerAttributes

### getProperty

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperty(key: String!): String!
```

Returns the value of the property with the specified key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: One of the strings corresponding to a property key: either `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_SAMPLE_RATE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_OUTPUT_FRAMES_PER_BUFFER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_MIC_NEAR_ULTRASOUND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_SPEAKER_NEAR_ULTRASOUND:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#PROPERTY_SUPPORT_AUDIO_SOURCE_UNPROCESSED:kotlin.String`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string representing the associated value for that property key, or null if there is no value for that key. |

### getRingerMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRingerMode(): Int
```

Returns the current ringtone mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current ringtone mode, one of `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_SILENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_VIBRATE:kotlin.Int`. |

**See Also**

- setRingerMode

### getRouting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRouting(mode: Int): Int
```

**Deprecated:** *Do not query audio routing directly, use isSpeakerphoneOn(), isBluetoothScoOn(), isBluetoothA2dpOn() and isWiredHeadsetOn() methods instead.*

Returns the current audio routing bit vector for a specified mode.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): audio mode to get route (e.g., MODE_RINGTONE) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an audio route bit vector that can be compared with ROUTE_xxx bits |

### getSpatializer

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpatializer(): Spatializer
```

Return a handle to the optional platform's Spatializer

| Return ||
|---|---|
| Spatializer | the `Spatializer` instance. This value cannot be `null`. |

**See Also**

- getImmersiveAudioLevel

### getStreamMaxVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamMaxVolume(streamType: Int): Int
```

Returns the maximum volume index for a particular stream.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream type whose maximum volume index is returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum valid volume index for the stream. |

**See Also**

- getStreamVolume

### getStreamMinVolume

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamMinVolume(streamType: Int): Int
```

Returns the minimum volume index for a particular stream.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream type whose minimum volume index is returned. Must be one of `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_DTMF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ACCESSIBILITY:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The minimum valid volume index for the stream. |

**See Also**

- getStreamVolume

### getStreamVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamVolume(streamType: Int): Int
```

Returns the current volume index for a particular stream.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream type whose volume index is returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The current volume index for the stream. |

**See Also**

- getStreamMaxVolume
- setStreamVolume

### getStreamVolumeDb

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStreamVolumeDb(
    streamType: Int, 
    index: Int, 
    deviceType: Int
): Float
```

Returns the volume in dB (decibel) for the given stream type at the given volume index, on the given type of audio output device.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): stream type for which the volume is queried. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_RING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_MUSIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ALARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_NOTIFICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_DTMF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ACCESSIBILITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_ASSISTANT:kotlin.Int` |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the volume index for which the volume is queried. The index value must be between the minimum and maximum index values for the given stream type (see getStreamMinVolume and getStreamMaxVolume). |
| `deviceType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type of audio output device for which volume is queried. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_EARPIECE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_WIRED_HEADPHONES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_SCO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLUETOOTH_A2DP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_ACCESSORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_USB_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_TELEPHONY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_ANALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_ARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HDMI_EARC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_LINE_DIGITAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_FM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_AUX_LINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_IP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_REMOTE_SUBMIX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_HEARING_AID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BUILTIN_SPEAKER_SAFE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_HEADSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_SPEAKER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_BROADCAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_DOCK_ANALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_MULTICHANNEL_GROUP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_HEARING_AID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo#TYPE_BLE_CENTRAL:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | a volume expressed in dB. A negative value indicates the audio signal is attenuated. A typical maximum value at the maximum volume index is 0 dB (no attenuation nor amplification). Muting is reflected by a value of `https://developer.android.com/reference/kotlin/java/lang/Float.html#NEGATIVE_INFINITY:kotlin.Float`. |

### getSupportedDeviceTypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedDeviceTypes(direction: Int): MutableSet<Int!>
```

Returns a Set of unique Integers corresponding to audio device type identifiers that can *potentially* be connected to the system and meeting the criteria specified in the `direction` parameter. Note that this set contains AudioDeviceInfo device type identifiers for both devices currently available *and* those that can be available if the user connects an audio peripheral. Examples include TYPE_WIRED_HEADSET if the Android device supports an analog headset jack or TYPE_USB_DEVICE if the Android device supports a USB host-mode port. These are generally a superset of device type identifiers associated with the AudioDeviceInfo objects returned from AudioManager.getDevices().

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The constant specifying whether input or output devices are queried. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_INPUTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_OUTPUTS:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | A (possibly zero-length) Set of Integer objects corresponding to the audio device types of devices supported by the implementation. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If an invalid direction constant is specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_OUTPUTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#GET_DEVICES_INPUTS:kotlin.Int`

### getSupportedMixerAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedMixerAttributes(device: AudioDeviceInfo): MutableList<AudioMixerAttributes!>
```

Returns the AudioMixerAttributes that can be used to set as preferred mixer attributes via setPreferredMixerAttributes.

Note that only USB devices are guaranteed to expose configurable mixer attributes. An empty list may be returned for all other types of devices as they may not allow dynamic configuration.

| Parameters ||
|---|---|
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md): the device to query. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/AudioMixerAttributes!>` | a list of AudioMixerAttributes that can be used as preferred mixer attributes for the given device. This value cannot be `null`. |

**See Also**

- setPreferredMixerAttributes

### getVibrateSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVibrateSetting(vibrateType: Int): Int
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Returns whether the user's vibrate setting for a vibrate type.

This shouldn't be needed by most clients that want to vibrate, instead see shouldVibrate.

| Parameters ||
|---|---|
| `vibrateType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of vibrate. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_NOTIFICATION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_RINGER:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The vibrate setting, one of `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_OFF:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ONLY_SILENT:kotlin.Int`. |

**See Also**

- setVibrateSetting
- shouldVibrate

### getVolumeGroupIdForAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVolumeGroupIdForAttributes(attributes: AudioAttributes): Int
```

Returns the volume group id associated to the given AudioAttributes.

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): The AudioAttributes to consider. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | audio volume group id supporting the given AudioAttributes if found, `android.media.audiopolicy.AudioVolumeGroup.DEFAULT_VOLUME_GROUP` otherwise. |

### isBluetoothA2dpOn

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBluetoothA2dpOn(): Boolean
```

**Deprecated:** *Use getDevices instead to list available audio devices.*

Checks whether a Bluetooth A2DP audio peripheral is connected or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a Bluetooth A2DP peripheral is connected false if otherwise |

### isBluetoothScoAvailableOffCall

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBluetoothScoAvailableOffCall(): Boolean
```

**Deprecated:** *This method is no longer necessary, the framework always supports SCO off call*

Indicates if current platform supports use of SCO for off call use cases. Application wanted to use bluetooth SCO audio when the phone is not in call must first call this method to make sure that the platform supports this feature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if bluetooth SCO can be used for audio when not in call false otherwise |

**See Also**

- startBluetoothSco

### isBluetoothScoOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isBluetoothScoOn(): Boolean
```

**Deprecated:** *Use getCommunicationDevice instead.*

Checks whether communications use Bluetooth SCO.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if SCO is used for communications; false if otherwise |

### isCallScreeningModeSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCallScreeningModeSupported(): Boolean
```

Indicates if the platform supports a special call screening and call monitoring mode.

When this mode is supported, it is possible to perform call screening and monitoring functions while other use cases like music or movie playback are active.

Use setMode with mode `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_SCREENING:kotlin.Int` to place the platform in call screening mode.

If call screening mode is not supported, setting mode to MODE_CALL_SCREENING will be ignored and will not change current mode reported by getMode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if call screening mode is supported, false otherwise. |

### isHapticPlaybackSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isHapticPlaybackSupported(): Boolean
```

Return if audio haptic coupled playback is supported or not.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether audio haptic playback supported. |

### isMicrophoneMute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMicrophoneMute(): Boolean
```

Checks whether the microphone mute is on or off.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if microphone is muted, false if it's not |

### isMusicActive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMusicActive(): Boolean
```

Checks whether any music is active.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if any music tracks are active. |

### isOffloadedPlaybackSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isOffloadedPlaybackSupported(
    format: AudioFormat, 
    attributes: AudioAttributes
): Boolean
```

Returns whether offloaded playback of an audio format is supported on the device.

Offloaded playback is the feature where the decoding and playback of an audio stream is not competing with other software resources. In general, it is supported by dedicated hardware, such as audio DSPs.

Note that this query only provides information about the support of an audio format, it does not indicate whether the resources necessary for the offloaded playback are available at that instant.

| Parameters ||
|---|---|
| `format` | [AudioFormat](AudioFormat.md): the audio format (codec, sample rate, channels) being checked. This value cannot be `null`. |
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes to be used for playback. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given audio format can be offloaded. |

### isRampingRingerEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRampingRingerEnabled(): Boolean
```

Returns the current user setting for ramping ringer on incoming phone call ringtone.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the incoming phone call ringtone is configured to gradually increase its volume, false otherwise. |

### isSpeakerphoneOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSpeakerphoneOn(): Boolean
```

**Deprecated:** *Use getCommunicationDevice instead.*

Checks whether the speakerphone is on or off.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if speakerphone is on, false if it's off |

### isStreamMute

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStreamMute(streamType: Int): Boolean
```

Returns the current mute state for a particular stream.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream to get mute state for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The mute state for the given stream. |

**See Also**

- adjustStreamVolume

### isSurroundFormatEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSurroundFormatEnabled(audioFormat: Int): Boolean
```

Gets whether a certain surround format is enabled or not.

| Parameters ||
|---|---|
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a surround format. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_LC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_TRUEHD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_MAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the required surround format is enabled |

### isVolumeFixed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVolumeFixed(): Boolean
```

Indicates if the device implements a fixed volume policy.

Some devices may not have volume control and may operate at a fixed volume, and may not enable muting or changing the volume of audio streams. This method will return true on such devices.

The following APIs have no effect when volume is fixed:

- adjustVolume
- adjustSuggestedStreamVolume
- adjustStreamVolume
- setStreamVolume
- setRingerMode
- setStreamSolo
- setStreamMute

### isVolumeGroupMuted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVolumeGroupMuted(groupId: Int): Boolean
```

Returns the current mute state for a particular volume group associated to the given id.

Call first in prior getVolumeGroupIdForAttributes to retrieve the volume group id supporting the given AudioAttributes.

| Parameters ||
|---|---|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): of the audio volume group to consider. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The mute state for the given audio volume group id. |

**See Also**

- adjustVolumeGroupVolume

### isWiredHeadsetOn

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWiredHeadsetOn(): Boolean
```

**Deprecated:** *Use getDevices instead to list available audio devices.*

Checks whether a wired headset is connected or not.

This is not a valid indication that audio playback is actually over the wired headset as audio routing depends on other conditions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a wired headset is connected. false if otherwise |

### loadSoundEffects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadSoundEffects(): Unit
```

Load Sound effects. This method must be called when sound effects are enabled.

### playSoundEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun playSoundEffect(effectType: Int): Unit
```

Plays a sound effect (Key clicks, lid open/close...)

| Parameters ||
|---|---|
| `effectType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of sound effect. NOTE: This version uses the UI settings to determine whether sounds are heard or not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEY_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_SPACEBAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_DELETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_RETURN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_BACK:kotlin.Int` |

### playSoundEffect

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun playSoundEffect(
    effectType: Int, 
    volume: Float
): Unit
```

Plays a sound effect (Key clicks, lid open/close...)

| Parameters ||
|---|---|
| `effectType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of sound effect. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEY_CLICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_FOCUS_NAVIGATION_RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_STANDARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_SPACEBAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_DELETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_RETURN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_KEYPRESS_INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FX_BACK:kotlin.Int` |
| `volume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Sound effect volume. The volume value is a raw scalar so UI controls should be scaled logarithmically. If a volume of -1 is specified, the AudioManager.STREAM_MUSIC stream volume minus 3dB will be used. NOTE: This version is for applications that have their own settings panel for enabling and controlling volume. |

### registerAudioDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerAudioDeviceCallback(
    callback: AudioDeviceCallback!, 
    handler: Handler?
): Unit
```

Registers an AudioDeviceCallback object to receive notifications of changes to the set of connected audio devices.

| Parameters ||
|---|---|
| `callback` | [AudioDeviceCallback](AudioDeviceCallback.md)!: The AudioDeviceCallback object to receive connect/disconnect notifications. |
| `handler` | [Handler](../android.os/Handler.md)?: Specifies the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` object for the thread on which to execute the callback. If `null`, the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` associated with the main `https://developer.android.com/reference/kotlin/android/os/Looper.html#` will be used. |

### registerAudioPlaybackCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerAudioPlaybackCallback(
    cb: AudioManager.AudioPlaybackCallback, 
    handler: Handler?
): Unit
```

Register a callback to be notified of audio playback changes through `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioPlaybackCallback`

| Parameters ||
|---|---|
| `cb` | [AudioManager.AudioPlaybackCallback](../android/media/AudioManager.AudioPlaybackCallback.md): non-null callback to register |
| `handler` | [Handler](../android.os/Handler.md)?: the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` object for the thread on which to execute the callback. If `null`, the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` associated with the main `https://developer.android.com/reference/kotlin/android/os/Looper.html#` will be used. |

### registerAudioRecordingCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerAudioRecordingCallback(
    cb: AudioManager.AudioRecordingCallback, 
    handler: Handler?
): Unit
```

Register a callback to be notified of audio recording changes through `https://developer.android.com/reference/kotlin/android/media/AudioManager.AudioRecordingCallback`

| Parameters ||
|---|---|
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md): non-null callback to register |
| `handler` | [Handler](../android.os/Handler.md)?: the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` object for the thread on which to execute the callback. If `null`, the `https://developer.android.com/reference/kotlin/android/os/Handler.html#` associated with the main `https://developer.android.com/reference/kotlin/android/os/Looper.html#` will be used. |

### registerMediaButtonEventReceiver

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerMediaButtonEventReceiver(eventReceiver: PendingIntent!): Unit
```

**Deprecated:** *Use setMediaButtonReceiver instead.*

Register a component to be the sole receiver of MEDIA_BUTTON intents. This is like registerMediaButtonEventReceiver, but allows the buttons to go to any PendingIntent. Note that you should only use this form if you know you will continue running for the full time until unregistering the PendingIntent.

| Parameters ||
|---|---|
| `eventReceiver` | [PendingIntent](../android.app/PendingIntent.md)!: target that will receive media button intents. The PendingIntent will be sent an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String` event when a media button action occurs, with `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_KEY_EVENT:kotlin.String` added and holding the key code of the media button that was pressed. |

### registerMediaButtonEventReceiver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerMediaButtonEventReceiver(eventReceiver: ComponentName!): Unit
```

**Deprecated:** *Use setMediaButtonReceiver instead.*

Register a component to be the sole receiver of MEDIA_BUTTON intents.

| Parameters ||
|---|---|
| `eventReceiver` | [ComponentName](../android.content/ComponentName.md)!: identifier of a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` that will receive the media button intent. This broadcast receiver must be declared in the application manifest. The package of the component must match that of the context you're registering from. |

### registerRemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerRemoteControlClient(rcClient: RemoteControlClient!): Unit
```

**Deprecated:** *Use MediaSession instead.*

Registers the remote control client for providing information to display on the remote controls.

| Parameters ||
|---|---|
| `rcClient` | [RemoteControlClient](RemoteControlClient.md)!: The remote control client from which remote controls will receive information to display. |

**See Also**

- RemoteControlClient

### registerRemoteController

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerRemoteController(rctlr: RemoteController!): Boolean
```

**Deprecated:** *Use addOnActiveSessionsChangedListener and MediaController instead.*

Registers a RemoteController instance for it to receive media metadata updates and playback state information from applications using RemoteControlClient, and control their playback.

Registration requires the `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener` listener to be one of the enabled notification listeners (see `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#`).

| Parameters ||
|---|---|
| `rctlr` | [RemoteController](RemoteController.md)!: the object to register. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the RemoteController was successfully registered, false if an error occurred, due to an internal system error, or insufficient permissions. |

### removeOnCommunicationDeviceChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnCommunicationDeviceChangedListener(listener: AudioManager.OnCommunicationDeviceChangedListener): Unit
```

Removes a previously added listener of changes to the communication audio device. See setCommunicationDevice.

| Parameters ||
|---|---|
| `listener` | [AudioManager.OnCommunicationDeviceChangedListener](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md): This value cannot be `null`. |

### removeOnModeChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnModeChangedListener(listener: AudioManager.OnModeChangedListener): Unit
```

Removes a previously added listener for changes to audio mode. See getMode

| Parameters ||
|---|---|
| `listener` | [AudioManager.OnModeChangedListener](../android/media/AudioManager.OnModeChangedListener.md): This value cannot be `null`. |

### removeOnPreferredMixerAttributesChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnPreferredMixerAttributesChangedListener(listener: AudioManager.OnPreferredMixerAttributesChangedListener): Unit
```

Removes a previously added listener of changes to the preferred mixer attributes.

| Parameters ||
|---|---|
| `listener` | [AudioManager.OnPreferredMixerAttributesChangedListener](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md): the listener to be notified of changes in the preferred mixer attributes, which were added via addOnPreferredMixerAttributesChangedListener. This value cannot be `null`. |

### requestAudioFocus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestAudioFocus(focusRequest: AudioFocusRequest): Int
```

Request audio focus. See the AudioFocusRequest for information about the options available to configure your request, and notification of focus gain and loss. **Note:** If an app targets Android 15 (API level 35) or higher, it cannot request audio focus unless it's the top app or running a foreground service. This requirement is similar to the [requirements for audio playback](../media/media3/session/background-playback.md). If an app requests audio focus when it does not meet these requirements, the method returns `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int`.

| Parameters ||
|---|---|
| `focusRequest` | [AudioFocusRequest](AudioFocusRequest.md): a AudioFocusRequest instance used to configure how focus is requested. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_GRANTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_DELAYED:kotlin.Int`. Note that the return value is never `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_DELAYED:kotlin.Int` when focus is requested without building the AudioFocusRequest with setAcceptsDelayedFocusGain set to `true`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if passed a null argument |

### requestAudioFocus

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestAudioFocus(
    l: AudioManager.OnAudioFocusChangeListener!, 
    streamType: Int, 
    durationHint: Int
): Int
```

**Deprecated:** *use requestAudioFocus*

Request audio focus. Send a request to obtain the audio focus. **Note:** If an app targets Android 15 (API level 35) or higher, it cannot request audio focus unless it's the top app or running a foreground service. This requirement is similar to the [requirements for audio playback](../media/media3/session/background-playback.md). If an app requests audio focus when it does not meet these requirements, the method returns `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int`.

| Parameters ||
|---|---|
| `l` | [AudioManager.OnAudioFocusChangeListener](../android/media/AudioManager.OnAudioFocusChangeListener.md)!: the listener to be notified of audio focus changes |
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the main audio stream type affected by the focus request |
| `durationHint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): use `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT:kotlin.Int` to indicate this focus request is temporary, and focus will be abandonned shortly. Examples of transient requests are for the playback of driving directions, or notifications sounds. Use `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT_MAY_DUCK:kotlin.Int` to indicate also that it's ok for the previous focus owner to keep playing if it ducks its audio output. Alternatively use `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN_TRANSIENT_EXCLUSIVE:kotlin.Int` for a temporary request that benefits from the system not playing disruptive sounds like notifications, for usecases such as voice memo recording, or speech recognition. Use `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_GAIN:kotlin.Int` for a focus request of unknown duration such as the playback of a song or a video. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_FAILED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#AUDIOFOCUS_REQUEST_GRANTED:kotlin.Int` |

### setAllowedCapturePolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAllowedCapturePolicy(capturePolicy: Int): Unit
```

Specifies whether the audio played by this app may or may not be captured by other apps or the system. The default is `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_ALL:kotlin.Int`. There are multiple ways to set this policy:

- for each track independently, see setAllowedCapturePolicy
- application-wide at runtime, with this method
- application-wide at build time, see `allowAudioPlaybackCapture` in the application manifest.

The most restrictive policy is always applied. See AudioPlaybackCaptureConfiguration for more details on which audio signals can be captured.

<br />

| Parameters ||
|---|---|
| `capturePolicy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_ALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_SYSTEM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_NONE:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_NONE:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | if the argument is not a valid value. |

### setBluetoothA2dpOn

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBluetoothA2dpOn(on: Boolean): Unit
```

**Deprecated:** *Use selectRoute instead.*

### setBluetoothScoOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBluetoothScoOn(on: Boolean): Unit
```

**Deprecated:** *Use #setCommunicationDevice() instead.*

Request use of Bluetooth SCO headset for communications.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application. This method has been a no-op for applications for several releases, and should not be used by any clients.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set true to use bluetooth SCO for communications; false to not use bluetooth SCO for communications |

### setCommunicationDevice

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCommunicationDevice(device: AudioDeviceInfo): Boolean
```

Selects the audio device that should be used for communication use cases, for instance voice or video calls. This method can be used by voice or video chat applications to select a different audio device than the one selected by default by the platform.

The device selection is expressed as an AudioDeviceInfo among devices returned by getAvailableCommunicationDevices. Note that only devices in a sink role (AKA output devices, see isSink) can be specified. The matching source device is selected automatically by the platform.

The selection is active as long as the requesting application process lives, until clearCommunicationDevice is called or until the device is disconnected. It is therefore important for applications to clear the request when a call ends or the the requesting activity or service is stopped or destroyed.

In case of simultaneous requests by multiple applications the priority is given to the application currently controlling the audio mode (see setMode). This is the latest application having selected mode `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_COMMUNICATION:kotlin.Int` or mode `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int`. Note that `MODE_IN_CALL` can only be selected by the main telephony application with permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_PHONE_STATE:kotlin.String`.

If the requested devices is not currently available, the request will be rejected and the method will return false.

This API replaces the following deprecated APIs:

- startBluetoothSco
- stopBluetoothSco
- setSpeakerphoneOn

#### Example

The example below shows how to enable and disable speakerphone mode.

```kotlin
// Get an AudioManager instance
  AudioManager audioManager = Context.getSystemService(AudioManager.class);
  AudioDeviceInfo speakerDevice = null;
  List<audiodeviceinfo>
  devices = audioManager.getAvailableCommunicationDevices();
  for (AudioDeviceInfo device : devices) {
      if (device.getType() == AudioDeviceInfo.TYPE_BUILTIN_SPEAKER) {
          speakerDevice = device;
          break;
      }
  }
  if (speakerDevice != null) {
      // Turn speakerphone ON.
      boolean result = audioManager.setCommunicationDevice(speakerDevice);
      if (!result) {
          // Handle error.
      }
      // Turn speakerphone OFF.
      audioManager.clearCommunicationDevice();
  }
  
</audiodeviceinfo>
```

| Parameters ||
|---|---|
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md): the requested audio device. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the request was accepted, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If an invalid device is specified. |

### setEncodedSurroundMode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEncodedSurroundMode(mode: Int): Boolean
```

Sets the surround sound mode. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_NEVER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_ALWAYS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#ENCODED_SURROUND_OUTPUT_MANUAL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if successful, otherwise false |

### setMicrophoneMute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMicrophoneMute(on: Boolean): Unit
```

Sets the microphone mute on or off.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set true to mute the microphone; false to turn mute off |

### setMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMode(mode: Int): Unit
```

Sets the audio mode.

The audio mode encompasses audio routing, volume management AND the behavior of the telephony layer. Therefore this method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application. In particular, the `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int` mode should only be used by the telephony application when it places a phone call, as it will cause signals from the radio layer to feed the platform mixer. The `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int` should only be used by applications that introduce an interactive assistant communication which would prioritize the audio management around streams with `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANT:kotlin.Int`. To use `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int`, the calling app must be allowed to manage assistant audio (see canManageAssistantAudio).

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the requested audio mode. (see android.media.AudioManager.AudioMode) Informs the HAL about the current audio state so that it can route the audio appropriately. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_NORMAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_RINGTONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_CALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_IN_COMMUNICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_SCREENING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_CALL_REDIRECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_COMMUNICATION_REDIRECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#MODE_ASSISTANT_CONVERSATION:kotlin.Int` |

### setParameters

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParameters(keyValuePairs: String!): Unit
```

Sets a variable number of parameter values to audio hardware.

| Parameters ||
|---|---|
| `keyValuePairs` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: list of parameters key value pairs in the form: key1=value1;key2=value2;... |

### setPreferredMixerAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPreferredMixerAttributes(
    attributes: AudioAttributes, 
    device: AudioDeviceInfo, 
    mixerAttributes: AudioMixerAttributes
): Boolean
```

Configures the mixer attributes for a particular AudioAttributes over a given AudioDeviceInfo.

Call getSupportedMixerAttributes to determine which mixer attributes can be used with the given device.

The ownership of preferred mixer attributes is recognized by uid. When a playback from the same uid is routed to the given audio device when calling this API, the output mixer/stream will be configured with the values previously set via this API.

Use clearPreferredMixerAttributes to cancel setting mixer attributes for this AudioAttributes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](AudioAttributes.md): the AudioAttributes whose mixer attributes should be set. Currently, only `https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_MEDIA:kotlin.Int` is supported. When playing audio targeted at the given device, use the same attributes for playback. This value cannot be `null`. |
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md): the device to be routed. Currently, only USB device will be allowed. This value cannot be `null`. |
| `mixerAttributes` | [AudioMixerAttributes](AudioMixerAttributes.md): the preferred mixer attributes. When playing audio targeted at the given device, use the same AudioFormat for both playback and the mixer attributes. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true only if the preferred mixer attributes are set successfully. |

**See Also**

- getPreferredMixerAttributes
- clearPreferredMixerAttributes

### setRingerMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRingerMode(ringerMode: Int): Unit
```

Sets the ringer mode.

Silent mode will mute the volume and will not vibrate. Vibrate mode will mute the volume and vibrate. Normal mode will be audible and may vibrate according to user settings.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed. \*

From N onward, ringer mode adjustments that would toggle Do Not Disturb are not allowed unless the app has been granted Notification Policy Access. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `ringerMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ringer mode, one of `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_SILENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#RINGER_MODE_VIBRATE:kotlin.Int`. |

**See Also**

- getRingerMode
- isVolumeFixed

### setRouting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRouting(
    mode: Int, 
    routes: Int, 
    mask: Int
): Unit
```

**Deprecated:** *Do not set audio routing directly, use setSpeakerphoneOn(), setBluetoothScoOn() methods instead.*

Sets the audio routing for a specified mode

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): audio mode to change route. E.g., MODE_RINGTONE. |
| `routes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit vector of routes requested, created from one or more of ROUTE_xxx types. Set bits indicate that route should be on |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bit vector of routes to change, created from one or more of ROUTE_xxx types. Unset bits indicate the route should be left unchanged |
| --- | --- |

### setSpeakerphoneOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSpeakerphoneOn(on: Boolean): Unit
```

**Deprecated:** *Use setCommunicationDevice or clearCommunicationDevice instead.*

Sets the speakerphone on or off.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set true to turn on speakerphone; false to turn it off |

### setStreamMute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStreamMute(
    streamType: Int, 
    state: Boolean
): Unit
```

**Deprecated:** *Use adjustStreamVolume with `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_MUTE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_UNMUTE:kotlin.Int` instead.*

Mute or unmute an audio stream.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed.

This method was deprecated in API level 22. Prior to API level 22 this method had significantly different behavior and should be used carefully. The following applies only to pre-22 platforms:

- The mute command is protected against client process death: if a process with an active mute request on a stream dies, this stream will be unmuted automatically.
- The mute requests for a given stream are cumulative: the AudioManager can receive several mute requests from one or more clients and the stream will be unmuted only when the same number of unmute requests are received.
- For a better user experience, applications MUST unmute a muted stream in onPause() and mute is again in onResume() if appropriate.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream to be muted/unmuted. |
| `state` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The required mute state: true for mute ON, false for mute OFF |

**See Also**

- isVolumeFixed

### setStreamSolo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStreamSolo(
    streamType: Int, 
    state: Boolean
): Unit
```

**Deprecated:** *Do not use. If you need exclusive audio playback use #requestAudioFocus.*

Solo or unsolo a particular stream.

Do not use. This method has been deprecated and is now a no-op. #requestAudioFocus should be used for exclusive audio playback.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream to be soloed/unsoloed. |
| `state` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The required solo state: true for solo ON, false for solo OFF |

**See Also**

- isVolumeFixed

### setStreamVolume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStreamVolume(
    streamType: Int, 
    index: Int, 
    flags: Int
): Unit
```

Sets the volume index for a particular stream.

This method has no effect if the device implements a fixed volume policy as indicated by isVolumeFixed.

From N onward, volume adjustments that would toggle Do Not Disturb are not allowed unless the app has been granted Notification Policy Access. See isNotificationPolicyAccessGranted.

| Parameters ||
|---|---|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The stream whose volume index should be set. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The volume index to set. See getStreamMaxVolume for the largest valid value. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_SHOW_UI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_ALLOW_RINGER_MODES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_PLAY_SOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_REMOVE_SOUND_AND_VIBRATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioManager#FLAG_VIBRATE:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the volume change triggers a Do Not Disturb change and the caller is not granted notification policy access. |

**See Also**

- getStreamMaxVolume
- getStreamVolume
- isVolumeFixed

### setSurroundFormatEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSurroundFormatEnabled(
    audioFormat: Int, 
    enabled: Boolean
): Boolean
```

Sets and persists a certain surround format as enabled or not.

This API is called by TvSettings surround sound menu when user enables or disables a surround sound format. This setting is persisted as global user setting. Applications should revert their changes to surround sound settings unless they intend to modify the global user settings across all apps. The framework does not auto-revert an application's settings after a lifecycle event. Audio focus is not required to apply these settings. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SETTINGS:kotlin.String`

| Parameters ||
|---|---|
| `audioFormat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_LC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_TRUEHD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_MAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the required surround format state, true for enabled, false for disabled |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if successful, otherwise false |

### setVibrateSetting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVibrateSetting(
    vibrateType: Int, 
    vibrateSetting: Int
): Unit
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Sets the setting for when the vibrate type should vibrate.

This method should only be used by applications that replace the platform-wide management of audio settings or the main telephony application.

| Parameters ||
|---|---|
| `vibrateType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of vibrate. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_NOTIFICATION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_RINGER:kotlin.Int`. |
| `vibrateSetting` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The vibrate setting, one of `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_OFF:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_SETTING_ONLY_SILENT:kotlin.Int`. |

**See Also**

- getVibrateSetting
- shouldVibrate

### setWiredHeadsetOn

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWiredHeadsetOn(on: Boolean): Unit
```

**Deprecated:** *Do not use.*

Sets audio routing to the wired headset on or off.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set true to route audio to/from wired headset; false disable wired headset audio |

### shouldVibrate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shouldVibrate(vibrateType: Int): Boolean
```

**Deprecated:** *Applications should maintain their own vibrate policy based on current ringer mode that can be queried via getRingerMode.*

Returns whether a particular type should vibrate according to user settings and the current ringer mode.

This shouldn't be needed by most clients that use notifications to vibrate. The notification manager will not vibrate if the policy doesn't allow it, so the client should always set a vibrate pattern and let the notification manager control whether or not to actually vibrate.

| Parameters ||
|---|---|
| `vibrateType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of vibrate. One of `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_NOTIFICATION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/AudioManager#VIBRATE_TYPE_RINGER:kotlin.Int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the type should vibrate at the instant this method is called. |

**See Also**

- setVibrateSetting
- getVibrateSetting

### startBluetoothSco

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startBluetoothSco(): Unit
```

**Deprecated:** *Use setCommunicationDevice instead.*

Start bluetooth SCO audio connection.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String`.

This method can be used by applications wanting to send and received audio to/from a bluetooth SCO headset while the phone is not in call.

As the SCO connection establishment can take several seconds, applications should not rely on the connection to be available when the method returns but instead register to receive the intent `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String` and wait for the state to be `https://developer.android.com/reference/kotlin/android/media/AudioManager#SCO_AUDIO_STATE_CONNECTED:kotlin.Int`.

As the ACTION_SCO_AUDIO_STATE_UPDATED intent is sticky, the application can check the SCO audio state before calling startBluetoothSco() by reading the intent returned by the receiver registration. If the state is already CONNECTED, no state change will be received via the intent after calling startBluetoothSco(). It is however useful to call startBluetoothSco() so that the connection stays active in case the current initiator stops the connection.

Unless the connection is already active as described above, the state will always transition from DISCONNECTED to CONNECTING and then either to CONNECTED if the connection succeeds or back to DISCONNECTED if the connection fails (e.g no headset is connected).

When finished with the SCO connection or if the establishment fails, the application must call stopBluetoothSco to clear the request and turn down the bluetooth connection.

Even if a SCO connection is established, the following restrictions apply on audio output streams so that they can be routed to SCO headset:

- the stream type must be `https://developer.android.com/reference/kotlin/android/media/AudioManager#STREAM_VOICE_CALL:kotlin.Int`
- the format must be mono
- the sampling must be 16kHz or 8kHz

The following restrictions apply on input streams:

- the format must be mono
- the sampling must be 8kHz

Note that the phone application always has the priority on the usage of the SCO connection for telephony. If this method is called while the phone is in call it will be ignored. Similarly, if a call is received or sent while an application is using the SCO connection, the connection will be lost for the application and NOT returned automatically when the call ends.

NOTE: up to and including API version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int`, this method initiates a virtual voice call to the bluetooth headset. After API version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int` only a raw SCO audio connection is established.
**See Also**

- stopBluetoothSco
- `https://developer.android.com/reference/kotlin/android/media/AudioManager#ACTION_SCO_AUDIO_STATE_UPDATED:kotlin.String`

### stopBluetoothSco

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopBluetoothSco(): Unit
```

**Deprecated:** *Use clearCommunicationDevice instead.*

Stop bluetooth SCO audio connection.

Requires Permission: `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String`.

This method must be called by applications having requested the use of bluetooth SCO audio with startBluetoothSco when finished with the SCO connection or if connection fails.
**See Also**

- startBluetoothSco

### unloadSoundEffects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unloadSoundEffects(): Unit
```

Unload Sound effects. This method can be called to free some memory when sound effects are disabled.

### unregisterAudioDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterAudioDeviceCallback(callback: AudioDeviceCallback!): Unit
```

Unregisters an AudioDeviceCallback object which has been previously registered to receive notifications of changes to the set of connected audio devices.

| Parameters ||
|---|---|
| `callback` | [AudioDeviceCallback](AudioDeviceCallback.md)!: The AudioDeviceCallback object that was previously registered with registerAudioDeviceCallback to be unregistered. |

### unregisterAudioPlaybackCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterAudioPlaybackCallback(cb: AudioManager.AudioPlaybackCallback): Unit
```

Unregister an audio playback callback previously registered with registerAudioPlaybackCallback.

| Parameters ||
|---|---|
| `cb` | [AudioManager.AudioPlaybackCallback](../android/media/AudioManager.AudioPlaybackCallback.md): non-null callback to unregister |

### unregisterAudioRecordingCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterAudioRecordingCallback(cb: AudioManager.AudioRecordingCallback): Unit
```

Unregister an audio recording callback previously registered with registerAudioRecordingCallback.

| Parameters ||
|---|---|
| `cb` | [AudioManager.AudioRecordingCallback](../android/media/AudioManager.AudioRecordingCallback.md): non-null callback to unregister |

### unregisterMediaButtonEventReceiver

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterMediaButtonEventReceiver(eventReceiver: PendingIntent!): Unit
```

**Deprecated:** *Use MediaSession instead.*

Unregister the receiver of MEDIA_BUTTON intents.

| Parameters ||
|---|---|
| `eventReceiver` | [PendingIntent](../android.app/PendingIntent.md)!: same PendingIntent that was registed with registerMediaButtonEventReceiver. |

### unregisterMediaButtonEventReceiver

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterMediaButtonEventReceiver(eventReceiver: ComponentName!): Unit
```

**Deprecated:** *Use MediaSession instead.*

Unregister the receiver of MEDIA_BUTTON intents.

| Parameters ||
|---|---|
| `eventReceiver` | [ComponentName](../android.content/ComponentName.md)!: identifier of a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` that was registered with registerMediaButtonEventReceiver. |

### unregisterRemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterRemoteControlClient(rcClient: RemoteControlClient!): Unit
```

**Deprecated:** *Use MediaSession instead.*

Unregisters the remote control client that was providing information to display on the remote controls.

| Parameters ||
|---|---|
| `rcClient` | [RemoteControlClient](RemoteControlClient.md)!: The remote control client to unregister. |

**See Also**

- registerRemoteControlClient

### unregisterRemoteController

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterRemoteController(rctlr: RemoteController!): Unit
```

**Deprecated:** *Use removeOnActiveSessionsChangedListener instead.*

Unregisters a RemoteController, causing it to no longer receive media metadata and playback state information, and no longer be capable of controlling playback.

| Parameters ||
|---|---|
| `rctlr` | [RemoteController](RemoteController.md)!: the object to unregister. |
