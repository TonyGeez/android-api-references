# DynamicsProcessing

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DynamicsProcessing

Kotlin| [Java](https://developer.android.com/reference/android/media/audiofx/DynamicsProcessing "View this page in Java") 

```
class DynamicsProcessing : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.audiofx.AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) ||
| | ↳ | [android.media.audiofx.DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#) |

DynamicsProcessing is an audio effect for equalizing and changing dynamic range properties of the sound. It is composed of multiple stages including equalization, multi-band compression and limiter.

The number of bands and active stages is configurable, and most parameters can be controlled in realtime, such as gains, attack/release times, thresholds, etc.

The effect is instantiated and controlled by channels. Each channel has the same basic architecture, but all of their parameters are independent from other channels.

The basic channel configuration is: 

```kotlin
Channel 0          Channel 1       ....       Channel N-1
       Input              Input                       Input
         |                  |                           |
    +----v----+        +----v----+                 +----v----+
    |inputGain|        |inputGain|                 |inputGain|
    +---------+        +---------+                 +---------+
         |                  |                           |
   +-----v-----+      +-----v-----+               +-----v-----+
   |   PreEQ   |      |   PreEQ   |               |   PreEQ   |
   +-----------+      +-----------+               +-----------+
         |                  |                           |
   +-----v-----+      +-----v-----+               +-----v-----+
   |    MBC    |      |    MBC    |               |    MBC    |
   +-----------+      +-----------+               +-----------+
         |                  |                           |
   +-----v-----+      +-----v-----+               +-----v-----+
   |  PostEQ   |      |  PostEQ   |               |  PostEQ   |
   +-----------+      +-----------+               +-----------+
         |                  |                           |
   +-----v-----+      +-----v-----+               +-----v-----+
   |  Limiter  |      |  Limiter  |               |  Limiter  |
   +-----------+      +-----------+               +-----------+
         |                  |                           |
      Output             Output                      Output
  
```

Where the stages are: inputGain: input gain factor in decibels (dB). 0 dB means no change in level. PreEQ: Multi-band Equalizer. MBC: Multi-band Compressor PostEQ: Multi-band Equalizer Limiter: Single band compressor/limiter.

An application creates a DynamicsProcessing object to instantiate and control this audio effect in the audio framework. A DynamicsProcessor.Config and DynamicsProcessor.Config.Builder are available to help configure the multiple stages and each band parameters if desired.

See each stage documentation for further details.

If no Config is specified during creation, a default configuration is chosen.

To attach the DynamicsProcessing to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the effect (see [AudioTrack.getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/AudioTrack.html#getAudioSessionId())and [MediaPlayer.getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#getAudioSessionId())).

To attach the DynamicsProcessing to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the DynamicsProcessing.

See [android.media.MediaPlayer#getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#getAudioSessionId())for details on audio sessions.

See [android.media.audiofx.AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [BandBase](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.BandBase) Base class for bands |
| | [BandStage](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.BandStage) Base class for stages that hold bands |
| | [Channel](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Channel) Class for Channel configuration parameters. |
| | [Config](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config) Class for Config object, used by DynamicsProcessing to configure and update the audio effect. |
| | [Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq) Class for Equalizer stage |
| | [EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand) Class for Equalizer Bands Equalizer bands have three controllable parameters: enabled/disabled, cutoffFrequency and gain |
| | [Limiter](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Limiter) Class for Limiter Stage Limiter is a single band compressor at the end of the processing chain, commonly used to protect the signal from overloading and distortion. |
| | [Mbc](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Mbc) Class for Multi-Band Compressor (MBC) stage |
| | [MbcBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.MbcBand) Class for Multi-Band compressor bands MBC bands have multiple controllable parameters: enabled/disabled, cutoffFrequency, attackTime, releaseTime, ratio, threshold, kneeWidth, noiseGateThreshold, expanderRatio, preGain and postGain. |
| | [Stage](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Stage) base class for the different stages. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIANT_FAVOR_FREQUENCY_RESOLUTION](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#VARIANT_FAVOR_FREQUENCY_RESOLUTION:kotlin.Int) Index of variant that favors frequency resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIANT_FAVOR_TIME_RESOLUTION](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#VARIANT_FAVOR_TIME_RESOLUTION:kotlin.Int) Index of variant that favors time resolution resolution. |

| Inherited constants ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ALREADY_EXISTS:kotlin.Int) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_AUXILIARY:kotlin.String) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_INSERT:kotlin.String) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_POST_PROCESSING:kotlin.String) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_PRE_PROCESSING:kotlin.String) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR:kotlin.Int) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_BAD_VALUE:kotlin.Int) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_DEAD_OBJECT:kotlin.Int) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_INVALID_OPERATION:kotlin.Int) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_INIT:kotlin.Int) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_MEMORY:kotlin.Int) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int) - [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int) - [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int) - [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#SUCCESS:kotlin.Int) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#DynamicsProcessing(kotlin.Int))`(`audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |
| [DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#DynamicsProcessing(kotlin.Int,%20kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Config))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cfg:` ` [DynamicsProcessing.Config](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config)?`)` Class constructor for the DynamicsProcessing audio effect |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DynamicsProcessing.Channel](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Channel)! | [getChannelByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getChannelByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelCount](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getChannelCount())`()` Gets the number of channels in the effect engine |
| [DynamicsProcessing.Config](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config)! | [getConfig](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getConfig())`()` Returns the Config object used to setup this effect. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInputGainByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getInputGainByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Limiter](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Limiter)! | [getLimiterByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getLimiterByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.MbcBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.MbcBand)! | [getMbcBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getMbcBandByChannelIndex(kotlin.Int,%20kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Mbc](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Mbc)! | [getMbcByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getMbcByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)! | [getPostEqBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getPostEqBandByChannelIndex(kotlin.Int,%20kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)! | [getPostEqByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getPostEqByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)! | [getPreEqBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getPreEqBandByChannelIndex(kotlin.Int,%20kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)! | [getPreEqByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#getPreEqByChannelIndex(kotlin.Int))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setAllChannelsTo(android.media.audiofx.DynamicsProcessing.Channel))`(`channel:` ` [DynamicsProcessing.Channel](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Channel)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChannelTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setChannelTo(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Channel))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channel:` ` [DynamicsProcessing.Channel](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Channel)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputGainAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setInputGainAllChannelsTo(kotlin.Float))`(`inputGain:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputGainbyChannel](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setInputGainbyChannel(kotlin.Int,%20kotlin.Float))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputGain:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLimiterAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setLimiterAllChannelsTo(android.media.audiofx.DynamicsProcessing.Limiter))`(`limiter:` ` [DynamicsProcessing.Limiter](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Limiter)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLimiterByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setLimiterByChannelIndex(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Limiter))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limiter:` ` [DynamicsProcessing.Limiter](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Limiter)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setMbcAllChannelsTo(android.media.audiofx.DynamicsProcessing.Mbc))`(`mbc:` ` [DynamicsProcessing.Mbc](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Mbc)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcBandAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setMbcBandAllChannelsTo(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.MbcBand))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbcBand:` ` [DynamicsProcessing.MbcBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.MbcBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setMbcBandByChannelIndex(kotlin.Int,%20kotlin.Int,%20android.media.audiofx.DynamicsProcessing.MbcBand))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbcBand:` ` [DynamicsProcessing.MbcBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.MbcBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setMbcByChannelIndex(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Mbc))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbc:` ` [DynamicsProcessing.Mbc](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Mbc)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPostEqAllChannelsTo(android.media.audiofx.DynamicsProcessing.Eq))`(`postEq:` ` [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqBandAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPostEqBandAllChannelsTo(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.EqBand))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEqBand:` ` [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPostEqBandByChannelIndex(kotlin.Int,%20kotlin.Int,%20android.media.audiofx.DynamicsProcessing.EqBand))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEqBand:` ` [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPostEqByChannelIndex(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Eq))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEq:` ` [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPreEqAllChannelsTo(android.media.audiofx.DynamicsProcessing.Eq))`(`preEq:` ` [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqBandAllChannelsTo](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPreEqBandAllChannelsTo(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.EqBand))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEqBand:` ` [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqBandByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPreEqBandByChannelIndex(kotlin.Int,%20kotlin.Int,%20android.media.audiofx.DynamicsProcessing.EqBand))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEqBand:` ` [DynamicsProcessing.EqBand](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.EqBand)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqByChannelIndex](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing#setPreEqByChannelIndex(kotlin.Int,%20android.media.audiofx.DynamicsProcessing.Eq))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEq:` ` [DynamicsProcessing.Eq](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Eq)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#finalize())`()` <br /> | | [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)! | [getDescriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getDescriptor())`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getEnabled())`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#hasControl())`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!>! | [queryEffects](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#queryEffects())`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#release())`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setControlStatusListener(android.media.audiofx.AudioEffect.OnControlStatusChangeListener))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnableStatusListener(android.media.audiofx.AudioEffect.OnEnableStatusChangeListener))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AEC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AEC:java.util.UUID) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AGC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AGC:java.util.UUID) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_BASS_BOOST](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_BASS_BOOST:java.util.UUID) <br /> UUID for bass boost effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_DYNAMICS_PROCESSING:java.util.UUID) <br /> UUID for Dynamics Processing <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_ENV_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_ENV_REVERB:java.util.UUID) <br /> UUID for environmental reverberation effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_EQUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_EQUALIZER:java.util.UUID) <br /> UUID for equalizer effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) | [EFFECT_TYPE_HAPTIC_GENERATOR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_HAPTIC_GENERATOR:java.util.UUID) <br /> UUID for Haptic Generator. <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_LOUDNESS_ENHANCER:java.util.UUID) <br /> UUID for Loudness Enhancer <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_NS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_NS:java.util.UUID) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_PRESET_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_PRESET_REVERB:java.util.UUID) <br /> UUID for preset reverberation effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_VIRTUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_VIRTUALIZER:java.util.UUID) <br /> UUID for virtualizer effect <br /> | ||

## Constants

### VARIANT_FAVOR_FREQUENCY_RESOLUTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VARIANT_FAVOR_FREQUENCY_RESOLUTION: Int
```

Index of variant that favors frequency resolution. Frequency domain based implementation. 

 Value: 0

### VARIANT_FAVOR_TIME_RESOLUTION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VARIANT_FAVOR_TIME_RESOLUTION: Int
```

Index of variant that favors time resolution resolution. Time domain based implementation. 

 Value: 1

## Public constructors

### DynamicsProcessing

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicsProcessing(audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system-wide unique audio session identifier. The DynamicsProcessing will be attached to the MediaPlayer or AudioTrack in the same audio session. |

### DynamicsProcessing

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicsProcessing(
    priority: Int, 
    audioSession: Int, 
    cfg: DynamicsProcessing.Config?)
```

Class constructor for the DynamicsProcessing audio effect

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority level requested by the application for controlling the DynamicsProcessing engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system-wide unique audio session identifier. The DynamicsProcessing will be attached to the MediaPlayer or AudioTrack in the same audio session. |
| `cfg` | [DynamicsProcessing.Config](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config)?:Config object used to setup the audio effect, including bands per stage, and specific parameters for each stage/band. Use [android.media.audiofx.DynamicsProcessing.Config.Builder](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config.Builder) to create a Config object that suits your needs. A null cfg parameter will create and use a default configuration for the effect |

## Public methods

### getChannelByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelByChannelIndex(channelIndex: Int): DynamicsProcessing.Channel!
```  

### getChannelCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelCount(): Int
```

Gets the number of channels in the effect engine

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of channels currently in use by the effect engine |

### getConfig

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfig(): DynamicsProcessing.Config!
```

Returns the Config object used to setup this effect.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [DynamicsProcessing.Config](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing.Config)! | Config Current Config object used to setup this DynamicsProcessing effect. |

### getInputGainByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputGainByChannelIndex(channelIndex: Int): Float
```  

### getLimiterByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLimiterByChannelIndex(channelIndex: Int): DynamicsProcessing.Limiter!
```  

### getMbcBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMbcBandByChannelIndex(
    channelIndex: Int, 
    band: Int
): DynamicsProcessing.MbcBand!
```  

### getMbcByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMbcByChannelIndex(channelIndex: Int): DynamicsProcessing.Mbc!
```  

### getPostEqBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPostEqBandByChannelIndex(
    channelIndex: Int, 
    band: Int
): DynamicsProcessing.EqBand!
```  

### getPostEqByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPostEqByChannelIndex(channelIndex: Int): DynamicsProcessing.Eq!
```  

### getPreEqBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreEqBandByChannelIndex(
    channelIndex: Int, 
    band: Int
): DynamicsProcessing.EqBand!
```  

### getPreEqByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreEqByChannelIndex(channelIndex: Int): DynamicsProcessing.Eq!
```  

### setAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAllChannelsTo(channel: DynamicsProcessing.Channel!): Unit
```  

### setChannelTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setChannelTo(
    channelIndex: Int, 
    channel: DynamicsProcessing.Channel!
): Unit
```  

### setInputGainAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInputGainAllChannelsTo(inputGain: Float): Unit
```  

### setInputGainbyChannel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInputGainbyChannel(
    channelIndex: Int, 
    inputGain: Float
): Unit
```  

### setLimiterAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLimiterAllChannelsTo(limiter: DynamicsProcessing.Limiter!): Unit
```  

### setLimiterByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLimiterByChannelIndex(
    channelIndex: Int, 
    limiter: DynamicsProcessing.Limiter!
): Unit
```  

### setMbcAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMbcAllChannelsTo(mbc: DynamicsProcessing.Mbc!): Unit
```  

### setMbcBandAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMbcBandAllChannelsTo(
    band: Int, 
    mbcBand: DynamicsProcessing.MbcBand!
): Unit
```  

### setMbcBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMbcBandByChannelIndex(
    channelIndex: Int, 
    band: Int, 
    mbcBand: DynamicsProcessing.MbcBand!
): Unit
```  

### setMbcByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMbcByChannelIndex(
    channelIndex: Int, 
    mbc: DynamicsProcessing.Mbc!
): Unit
```  

### setPostEqAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPostEqAllChannelsTo(postEq: DynamicsProcessing.Eq!): Unit
```  

### setPostEqBandAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPostEqBandAllChannelsTo(
    band: Int, 
    postEqBand: DynamicsProcessing.EqBand!
): Unit
```  

### setPostEqBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPostEqBandByChannelIndex(
    channelIndex: Int, 
    band: Int, 
    postEqBand: DynamicsProcessing.EqBand!
): Unit
```  

### setPostEqByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPostEqByChannelIndex(
    channelIndex: Int, 
    postEq: DynamicsProcessing.Eq!
): Unit
```  

### setPreEqAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreEqAllChannelsTo(preEq: DynamicsProcessing.Eq!): Unit
```  

### setPreEqBandAllChannelsTo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreEqBandAllChannelsTo(
    band: Int, 
    preEqBand: DynamicsProcessing.EqBand!
): Unit
```  

### setPreEqBandByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreEqBandByChannelIndex(
    channelIndex: Int, 
    band: Int, 
    preEqBand: DynamicsProcessing.EqBand!
): Unit
```  

### setPreEqByChannelIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPreEqByChannelIndex(
    channelIndex: Int, 
    preEq: DynamicsProcessing.Eq!
): Unit
```
