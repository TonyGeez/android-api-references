# AudioStream

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioStream

Kotlin| [Java](https://developer.android.com/reference/android/net/rtp/AudioStream "View this page in Java") 
| --- | --- |

```
open class AudioStream : RtpStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.rtp.RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream) ||
| | ↳ | [android.net.rtp.AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager.html#) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

An AudioStream is a [RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream) which carrys audio payloads over Real-time Transport Protocol (RTP). Two different classes are developed in order to support various usages such as audio conferencing. An AudioStream represents a remote endpoint which consists of a network mapping and a configured [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec). On the other side, An [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup) represents a local endpoint which mixes all the AudioStreams and optionally interacts with the speaker and the microphone at the same time. The simplest usage includes one for each endpoints. For other combinations, developers should be aware of the limitations described in [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup).

An AudioStream becomes busy when it joins an AudioGroup. In this case most of the setter methods are disabled. This is designed to ease the task of managing native resources. One can always make an AudioStream leave its AudioGroup by calling [join(android.net.rtp.AudioGroup)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#join(android.net.rtp.AudioGroup))with`null`and put it back after the modification is done.

Using this class requires [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission.

## Summary

| Inherited constants ||
|---|---|
| From class [RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_NORMAL:kotlin.Int) <br /> This mode indicates that the stream sends and receives packets at the same time. This is the initial mode for new streams. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_RECEIVE_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_RECEIVE_ONLY:kotlin.Int) <br /> This mode indicates that the stream only receives packets. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_SEND_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_SEND_ONLY:kotlin.Int) <br /> This mode indicates that the stream only sends packets. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#AudioStream(java.net.InetAddress))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Creates an AudioStream on the given local address. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec)! | [getCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#getCodec())`()` Returns the [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec), or`null`if it is not set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDtmfType](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#getDtmfType())`()` Returns the RTP payload type for dual-tone multi-frequency (DTMF) digits, or`-1`if it is not enabled. |
| open [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup)! | [getGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#getGroup())`()` Returns the joined [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBusy](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#isBusy())`()` Returns`true`if the stream has already joined an [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [join](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#join(android.net.rtp.AudioGroup))`(`group:` ` [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup)!`)` Joins an [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#setCodec(android.net.rtp.AudioCodec))`(`codec:` ` [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec)!`)` Sets the [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDtmfType](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#setDtmfType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the RTP payload type for dual-tone multi-frequency (DTMF) digits. |

| Inherited functions ||
|---|---|
| From class [RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream) |-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [associate](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#associate(java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Associates with a remote host. This defines the destination of the outgoing packets. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#finalize())`()` <br /> | | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getLocalAddress())`()` <br /> Returns the network address of the local host. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getLocalPort())`()` <br /> Returns the network port of the local host. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getMode())`()` <br /> Returns the current mode. <br /> | | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getRemoteAddress](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getRemoteAddress())`()` <br /> Returns the network address of the remote host or`null`if the stream is not associated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemotePort](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getRemotePort())`()` <br /> Returns the network port of the remote host or`-1`if the stream is not associated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#release())`()` <br /> Releases allocated resources. The stream becomes inoperable after calling this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMode](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#setMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Changes the current mode. It must be one of [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_NORMAL:kotlin.Int), [MODE_SEND_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_SEND_ONLY:kotlin.Int), and [MODE_RECEIVE_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_RECEIVE_ONLY:kotlin.Int). <br /> | ||

## Public constructors

### AudioStream

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioStream(address: InetAddress!)
```

Creates an AudioStream on the given local address. Note that the local port is assigned automatically to conform with RFC 3550.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The network address of the local host to bind to. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------|
| `java.net.SocketException` | if the address cannot be bound or a problem occurs during binding. |

## Public methods

### getCodec

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCodec(): AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

Returns the [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec), or`null`if it is not set. 
**See Also**

- [#setCodec(AudioCodec)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#setCodec(android.net.rtp.AudioCodec)) 

### getDtmfType

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDtmfType(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the RTP payload type for dual-tone multi-frequency (DTMF) digits, or`-1`if it is not enabled. 
**See Also**

- [#setDtmfType(int)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream#setDtmfType(kotlin.Int)) 

### getGroup

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroup(): AudioGroup!
```

**Deprecated:** *Deprecated in Java.*

Returns the joined [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). 

### isBusy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBusy(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns`true`if the stream has already joined an [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). 

### join

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun join(group: AudioGroup!): Unit
```

**Deprecated:** *Deprecated in Java.*

Joins an [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup). Each stream can join only one group at a time. The group can be changed by passing a different one or removed by calling this method with`null`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `group` | [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup)!:The AudioGroup to join or`null`to leave. |

| Exceptions ||
|-----------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if the stream is not properly configured. |

**See Also**

- [android.net.rtp.AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup) 

### setCodec

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCodec(codec: AudioCodec!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `codec` | [AudioCodec](https://developer.android.com/reference/kotlin/android/net/rtp/AudioCodec)!:The AudioCodec to be used. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if its type is used by DTMF. |
| `java.lang.IllegalStateException` | if the stream is busy. |

### setDtmfType

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDtmfType(type: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the RTP payload type for dual-tone multi-frequency (DTMF) digits. The primary usage is to send digits to the remote gateway to perform certain tasks, such as second-stage dialing. According to RFC 2833, the RTP payload type for DTMF is assigned dynamically, so it must be in the range of 96 and 127. One can use`-1`to disable DTMF and free up the previous assigned type. This method cannot be called when the stream already joined an [AudioGroup](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The RTP payload type to be used or`-1`to disable it. |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if the type is invalid or used by codec. |
| `java.lang.IllegalStateException` | if the stream is busy. |

**See Also**

- [android.net.rtp.AudioGroup#sendDtmf(int)](https://developer.android.com/reference/kotlin/android/net/rtp/AudioGroup#sendDtmf(kotlin.Int))
