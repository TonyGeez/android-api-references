# DynamicsProcessing

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DynamicsProcessing

Kotlin| [Java](DynamicsProcessing.md) 
| --- | --- |

```
class DynamicsProcessing : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.DynamicsProcessing](DynamicsProcessing.md) |

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

To attach the DynamicsProcessing to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the effect (see [AudioTrack.getAudioSessionId()](../android.media/AudioTrack.md))and [MediaPlayer.getAudioSessionId()](../android.media/MediaPlayer.md))).

To attach the DynamicsProcessing to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the DynamicsProcessing.

See [android.media.MediaPlayer#getAudioSessionId()](../android.media/MediaPlayer.md))for details on audio sessions.

See [android.media.audiofx.AudioEffect](AudioEffect.md) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [BandBase](../android/media/audiofx/DynamicsProcessing.BandBase.md) Base class for bands |
| | [BandStage](../android/media/audiofx/DynamicsProcessing.BandStage.md) Base class for stages that hold bands |
| | [Channel](../android/media/audiofx/DynamicsProcessing.Channel.md) Class for Channel configuration parameters. |
| --- | --- |
| | [Config](../android/media/audiofx/DynamicsProcessing.Config.md) Class for Config object, used by DynamicsProcessing to configure and update the audio effect. |
| | [Eq](../android/media/audiofx/DynamicsProcessing.Eq.md) Class for Equalizer stage |
| | [EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md) Class for Equalizer Bands Equalizer bands have three controllable parameters: enabled/disabled, cutoffFrequency and gain |
| --- | --- |
| | [Limiter](../android/media/audiofx/DynamicsProcessing.Limiter.md) Class for Limiter Stage Limiter is a single band compressor at the end of the processing chain, commonly used to protect the signal from overloading and distortion. |
| | [Mbc](../android/media/audiofx/DynamicsProcessing.Mbc.md) Class for Multi-Band Compressor (MBC) stage |
| | [MbcBand](../android/media/audiofx/DynamicsProcessing.MbcBand.md) Class for Multi-Band compressor bands MBC bands have multiple controllable parameters: enabled/disabled, cutoffFrequency, attackTime, releaseTime, ratio, threshold, kneeWidth, noiseGateThreshold, expanderRatio, preGain and postGain. |
| --- | --- |
| | [Stage](../android/media/audiofx/DynamicsProcessing.Stage.md) base class for the different stages. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIANT_FAVOR_FREQUENCY_RESOLUTION](DynamicsProcessing.md) Index of variant that favors frequency resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIANT_FAVOR_TIME_RESOLUTION](DynamicsProcessing.md) Index of variant that favors time resolution resolution. |

| Inherited constants ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](AudioEffect.md) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](AudioEffect.md) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](AudioEffect.md) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](AudioEffect.md) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](AudioEffect.md) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](AudioEffect.md) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioEffect.md) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioEffect.md) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioEffect.md) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioEffect.md) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](AudioEffect.md) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](AudioEffect.md) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](AudioEffect.md) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](AudioEffect.md) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](AudioEffect.md) - [CONTENT_TYPE_MOVIE](AudioEffect.md) - [CONTENT_TYPE_GAME](AudioEffect.md) - [CONTENT_TYPE_VOICE](AudioEffect.md) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](AudioEffect.md). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](AudioEffect.md) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioEffect.md) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DynamicsProcessing](DynamicsProcessing.md))`(`audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |
| [DynamicsProcessing](DynamicsProcessing.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cfg:` ` [DynamicsProcessing.Config](../android/media/audiofx/DynamicsProcessing.Config.md)?`)` Class constructor for the DynamicsProcessing audio effect |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DynamicsProcessing.Channel](../android/media/audiofx/DynamicsProcessing.Channel.md)! | [getChannelByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChannelCount](DynamicsProcessing.md))`()` Gets the number of channels in the effect engine |
| [DynamicsProcessing.Config](../android/media/audiofx/DynamicsProcessing.Config.md)! | [getConfig](DynamicsProcessing.md))`()` Returns the Config object used to setup this effect. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInputGainByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Limiter](../android/media/audiofx/DynamicsProcessing.Limiter.md)! | [getLimiterByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.MbcBand](../android/media/audiofx/DynamicsProcessing.MbcBand.md)! | [getMbcBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| [DynamicsProcessing.Mbc](../android/media/audiofx/DynamicsProcessing.Mbc.md)! | [getMbcByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)! | [getPostEqBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)! | [getPostEqByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)! | [getPreEqBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)! | [getPreEqByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllChannelsTo](DynamicsProcessing.md))`(`channel:` ` [DynamicsProcessing.Channel](../android/media/audiofx/DynamicsProcessing.Channel.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChannelTo](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `channel:` ` [DynamicsProcessing.Channel](../android/media/audiofx/DynamicsProcessing.Channel.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputGainAllChannelsTo](DynamicsProcessing.md))`(`inputGain:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputGainbyChannel](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputGain:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLimiterAllChannelsTo](DynamicsProcessing.md))`(`limiter:` ` [DynamicsProcessing.Limiter](../android/media/audiofx/DynamicsProcessing.Limiter.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLimiterByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limiter:` ` [DynamicsProcessing.Limiter](../android/media/audiofx/DynamicsProcessing.Limiter.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcAllChannelsTo](DynamicsProcessing.md))`(`mbc:` ` [DynamicsProcessing.Mbc](../android/media/audiofx/DynamicsProcessing.Mbc.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcBandAllChannelsTo](DynamicsProcessing.md))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbcBand:` ` [DynamicsProcessing.MbcBand](../android/media/audiofx/DynamicsProcessing.MbcBand.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbcBand:` ` [DynamicsProcessing.MbcBand](../android/media/audiofx/DynamicsProcessing.MbcBand.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMbcByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mbc:` ` [DynamicsProcessing.Mbc](../android/media/audiofx/DynamicsProcessing.Mbc.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqAllChannelsTo](DynamicsProcessing.md))`(`postEq:` ` [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqBandAllChannelsTo](DynamicsProcessing.md))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEqBand:` ` [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEqBand:` ` [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPostEqByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `postEq:` ` [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqAllChannelsTo](DynamicsProcessing.md))`(`preEq:` ` [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqBandAllChannelsTo](DynamicsProcessing.md))`(`band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEqBand:` ` [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqBandByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `band:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEqBand:` ` [DynamicsProcessing.EqBand](../android/media/audiofx/DynamicsProcessing.EqBand.md)!`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreEqByChannelIndex](DynamicsProcessing.md))`(`channelIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preEq:` ` [DynamicsProcessing.Eq](../android/media/audiofx/DynamicsProcessing.Eq.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AudioEffect.md))`()` <br /> | | [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)! | [getDescriptor](AudioEffect.md))`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](AudioEffect.md))`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](AudioEffect.md))`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](AudioEffect.md))`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!>! | [queryEffects](AudioEffect.md))`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](AudioEffect.md))`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](AudioEffect.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AEC](AudioEffect.md) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AGC](AudioEffect.md) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_BASS_BOOST](AudioEffect.md) <br /> UUID for bass boost effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](AudioEffect.md) <br /> UUID for Dynamics Processing <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_ENV_REVERB](AudioEffect.md) <br /> UUID for environmental reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_EQUALIZER](AudioEffect.md) <br /> UUID for equalizer effect <br /> | | [UUID](../java.util/UUID.md) | [EFFECT_TYPE_HAPTIC_GENERATOR](AudioEffect.md) <br /> UUID for Haptic Generator. <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](AudioEffect.md) <br /> UUID for Loudness Enhancer <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_NS](AudioEffect.md) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_PRESET_REVERB](AudioEffect.md) <br /> UUID for preset reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_VIRTUALIZER](AudioEffect.md) <br /> UUID for virtualizer effect <br /> | ||

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
| `cfg` | [DynamicsProcessing.Config](../android/media/audiofx/DynamicsProcessing.Config.md)?:Config object used to setup the audio effect, including bands per stage, and specific parameters for each stage/band. Use [android.media.audiofx.DynamicsProcessing.Config.Builder](../android/media/audiofx/DynamicsProcessing.Config.Builder.md) to create a Config object that suits your needs. A null cfg parameter will create and use a default configuration for the effect |
| --- | --- |

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
| [DynamicsProcessing.Config](../android/media/audiofx/DynamicsProcessing.Config.md)! | Config Current Config object used to setup this DynamicsProcessing effect. |

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
