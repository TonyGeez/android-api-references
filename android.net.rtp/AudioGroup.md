# AudioGroup

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioGroup

Kotlin| [Java](https://developer.android.com/reference/android/net/rtp/AudioGroup "View this page in Java") 
| --- | --- |

```
open class AudioGroup
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.rtp.AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager.html#) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

An AudioGroup is an audio hub for the speaker, the microphone, and [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) s. Each of these components can be logically turned on or off by calling [setMode(int)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#setMode(kotlin.Int))or [RtpStream.setMode(int)](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#setMode(kotlin.Int)). The AudioGroup will go through these components and process them one by one within its execution loop. The loop consists of four steps. First, for each AudioStream not in [RtpStream.MODE_SEND_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_SEND_ONLY:kotlin.Int), decodes its incoming packets and stores in its buffer. Then, if the microphone is enabled, processes the recorded audio and stores in its buffer. Third, if the speaker is enabled, mixes all AudioStream buffers and plays back. Finally, for each AudioStream not in [RtpStream.MODE_RECEIVE_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_RECEIVE_ONLY:kotlin.Int), mixes all other buffers and sends back the encoded packets. An AudioGroup does nothing if there is no AudioStream in it.

Few things must be noticed before using these classes. The performance is highly related to the system load and the network bandwidth. Usually a simpler [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec) costs fewer CPU cycles but requires more network bandwidth, and vise versa. Using two AudioStreams at the same time doubles not only the load but also the bandwidth. The condition varies from one device to another, and developers should choose the right combination in order to get the best result.

It is sometimes useful to keep multiple AudioGroups at the same time. For example, a Voice over IP (VoIP) application might want to put a conference call on hold in order to make a new call but still allow people in the conference call talking to each other. This can be done easily using two AudioGroups, but there are some limitations. Since the speaker and the microphone are globally shared resources, only one AudioGroup at a time is allowed to run in a mode other than [MODE_ON_HOLD](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_ON_HOLD:kotlin.Int). The others will be unable to acquire these resources and fail silently.

Using this class requires [android.Manifest.permission#RECORD_AUDIO](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#RECORD_AUDIO:kotlin.String) permission. Developers should set the audio mode to [AudioManager.MODE_IN_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#MODE_IN_COMMUNICATION:kotlin.Int) using [AudioManager.setMode(int)](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#setMode(kotlin.Int))and change it back when none of the AudioGroups is in use.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_ECHO_SUPPRESSION](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_ECHO_SUPPRESSION:kotlin.Int) This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the echo suppression is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_MUTED](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_MUTED:kotlin.Int) This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the microphone is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) This mode indicates that the speaker, the microphone, and all [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) s in the group are enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_ON_HOLD](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_ON_HOLD:kotlin.Int) This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the speaker and the microphone are both disabled. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#AudioGroup())`()` Creates an empty AudioGroup. |
| [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#AudioGroup(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Creates an empty AudioGroup. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#clear())`()` Removes every [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) in this group. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#getMode())`()` Returns the current mode. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream)!\>! | [getStreams](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#getStreams())`()` Returns the [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) s in this group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendDtmf](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#sendDtmf(kotlin.Int))`(`event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sends a DTMF digit to every [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) in this group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMode](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#setMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the current mode. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#finalize())`()` <br /> |

## Constants

### MODE_ECHO_SUPPRESSION

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_ECHO_SUPPRESSION: Int
```

**Deprecated:** *Deprecated in Java.*

This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the echo suppression is enabled. It should be only used when the speaker phone is on. 

 Value: 3

### MODE_MUTED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_MUTED: Int
```

**Deprecated:** *Deprecated in Java.*

This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the microphone is disabled. 

 Value: 1

### MODE_NORMAL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NORMAL: Int
```

**Deprecated:** *Deprecated in Java.*

This mode indicates that the speaker, the microphone, and all [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) s in the group are enabled. First, the packets received from the streams are decoded and mixed with the audio recorded from the microphone. Then, the results are played back to the speaker, encoded and sent back to each stream. 

 Value: 2

### MODE_ON_HOLD

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_ON_HOLD: Int
```

**Deprecated:** *Deprecated in Java.*

This mode is similar to [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int) except the speaker and the microphone are both disabled. 

 Value: 0

## Public constructors

### AudioGroup

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioGroup()
```

**Deprecated:** *Replaced by [AudioGroup(android.content.Context)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#AudioGroup(android.content.Context))*

Creates an empty AudioGroup. 

### AudioGroup

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioGroup(context: Context)
```

Creates an empty AudioGroup.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):Context the group belongs to This value cannot be`null`. |

## Public methods

### clear

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes every [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) in this group. 

### getMode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the current mode. 

### getStreams

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreams(): Array<AudioStream!>!
```

**Deprecated:** *Deprecated in Java.*

Returns the [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) s in this group. 

### sendDtmf

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendDtmf(event: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a DTMF digit to every [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) in this group. Currently only event`0`to`15`are supported.

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if the event is invalid. |

### setMode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMode(mode: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Changes the current mode. It must be one of [MODE_ON_HOLD](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_ON_HOLD:kotlin.Int), [MODE_MUTED](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_MUTED:kotlin.Int), [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_NORMAL:kotlin.Int), and [MODE_ECHO_SUPPRESSION](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#MODE_ECHO_SUPPRESSION:kotlin.Int).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mode to change to. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the mode is invalid. |

## Protected methods

### finalize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
