# AudioStream

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioStream

Kotlin| [Java](../android/net/rtp/AudioStream.md) 
| --- | --- |

```
open class AudioStream : RtpStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.rtp.RtpStream](../android/net/rtp/RtpStream.md) ||
| | ↳ | [android.net.rtp.AudioStream](../android/net/rtp/AudioStream.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](../android/net/sip/SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

An AudioStream is a [RtpStream](../android/net/rtp/RtpStream.md) which carrys audio payloads over Real-time Transport Protocol (RTP). Two different classes are developed in order to support various usages such as audio conferencing. An AudioStream represents a remote endpoint which consists of a network mapping and a configured [AudioCodec](../android/net/rtp/AudioCodec.md). On the other side, An [AudioGroup](../android/net/rtp/AudioGroup.md) represents a local endpoint which mixes all the AudioStreams and optionally interacts with the speaker and the microphone at the same time. The simplest usage includes one for each endpoints. For other combinations, developers should be aware of the limitations described in [AudioGroup](../android/net/rtp/AudioGroup.md).

An AudioStream becomes busy when it joins an AudioGroup. In this case most of the setter methods are disabled. This is designed to ease the task of managing native resources. One can always make an AudioStream leave its AudioGroup by calling [join(android.net.rtp.AudioGroup)](../android/net/rtp/AudioStream.md))with`null`and put it back after the modification is done.

Using this class requires [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission.

## Summary

| Inherited constants ||
|---|---|
| From class [RtpStream](../android/net/rtp/RtpStream.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NORMAL](../android/net/rtp/RtpStream.md) <br /> This mode indicates that the stream sends and receives packets at the same time. This is the initial mode for new streams. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_RECEIVE_ONLY](../android/net/rtp/RtpStream.md) <br /> This mode indicates that the stream only receives packets. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_SEND_ONLY](../android/net/rtp/RtpStream.md) <br /> This mode indicates that the stream only sends packets. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioStream](../android/net/rtp/AudioStream.md))`(`address:` ` [InetAddress](../java/net/InetAddress.md)!`)` Creates an AudioStream on the given local address. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioCodec](../android/net/rtp/AudioCodec.md)! | [getCodec](../android/net/rtp/AudioStream.md))`()` Returns the [AudioCodec](../android/net/rtp/AudioCodec.md), or`null`if it is not set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDtmfType](../android/net/rtp/AudioStream.md))`()` Returns the RTP payload type for dual-tone multi-frequency (DTMF) digits, or`-1`if it is not enabled. |
| open [AudioGroup](../android/net/rtp/AudioGroup.md)! | [getGroup](../android/net/rtp/AudioStream.md))`()` Returns the joined [AudioGroup](../android/net/rtp/AudioGroup.md). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBusy](../android/net/rtp/AudioStream.md))`()` Returns`true`if the stream has already joined an [AudioGroup](../android/net/rtp/AudioGroup.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [join](../android/net/rtp/AudioStream.md))`(`group:` ` [AudioGroup](../android/net/rtp/AudioGroup.md)!`)` Joins an [AudioGroup](../android/net/rtp/AudioGroup.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCodec](../android/net/rtp/AudioStream.md))`(`codec:` ` [AudioCodec](../android/net/rtp/AudioCodec.md)!`)` Sets the [AudioCodec](../android/net/rtp/AudioCodec.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDtmfType](../android/net/rtp/AudioStream.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the RTP payload type for dual-tone multi-frequency (DTMF) digits. |

| Inherited functions ||
|---|---|
| From class [RtpStream](../android/net/rtp/RtpStream.md) |-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [associate](../android/net/rtp/RtpStream.md))`(`address:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Associates with a remote host. This defines the destination of the outgoing packets. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/net/rtp/RtpStream.md))`()` <br /> | | [InetAddress](../java/net/InetAddress.md)! | [getLocalAddress](../android/net/rtp/RtpStream.md))`()` <br /> Returns the network address of the local host. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](../android/net/rtp/RtpStream.md))`()` <br /> Returns the network port of the local host. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](../android/net/rtp/RtpStream.md))`()` <br /> Returns the current mode. <br /> | | [InetAddress](../java/net/InetAddress.md)! | [getRemoteAddress](../android/net/rtp/RtpStream.md))`()` <br /> Returns the network address of the remote host or`null`if the stream is not associated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemotePort](../android/net/rtp/RtpStream.md))`()` <br /> Returns the network port of the remote host or`-1`if the stream is not associated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/net/rtp/RtpStream.md))`()` <br /> Releases allocated resources. The stream becomes inoperable after calling this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMode](../android/net/rtp/RtpStream.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Changes the current mode. It must be one of [MODE_NORMAL](../android/net/rtp/RtpStream.md), [MODE_SEND_ONLY](../android/net/rtp/RtpStream.md), and [MODE_RECEIVE_ONLY](../android/net/rtp/RtpStream.md). <br /> | ||

## Public constructors

### AudioStream

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AudioStream(address: InetAddress!)
```

Creates an AudioStream on the given local address. Note that the local port is assigned automatically to conform with RFC 3550.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](../java/net/InetAddress.md)!:The network address of the local host to bind to. |

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

Returns the [AudioCodec](../android/net/rtp/AudioCodec.md), or`null`if it is not set. 
**See Also**

- [#setCodec(AudioCodec)](../android/net/rtp/AudioStream.md)) 

### getDtmfType

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDtmfType(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the RTP payload type for dual-tone multi-frequency (DTMF) digits, or`-1`if it is not enabled. 
**See Also**

- [#setDtmfType(int)](../android/net/rtp/AudioStream.md)) 

### getGroup

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroup(): AudioGroup!
```

**Deprecated:** *Deprecated in Java.*

Returns the joined [AudioGroup](../android/net/rtp/AudioGroup.md). 

### isBusy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBusy(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns`true`if the stream has already joined an [AudioGroup](../android/net/rtp/AudioGroup.md). 

### join

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun join(group: AudioGroup!): Unit
```

**Deprecated:** *Deprecated in Java.*

Joins an [AudioGroup](../android/net/rtp/AudioGroup.md). Each stream can join only one group at a time. The group can be changed by passing a different one or removed by calling this method with`null`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `group` | [AudioGroup](../android/net/rtp/AudioGroup.md)!:The AudioGroup to join or`null`to leave. |

| Exceptions ||
|-----------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if the stream is not properly configured. |

**See Also**

- [android.net.rtp.AudioGroup](../android/net/rtp/AudioGroup.md) 

### setCodec

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCodec(codec: AudioCodec!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the [AudioCodec](../android/net/rtp/AudioCodec.md).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `codec` | [AudioCodec](../android/net/rtp/AudioCodec.md)!:The AudioCodec to be used. |

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

Sets the RTP payload type for dual-tone multi-frequency (DTMF) digits. The primary usage is to send digits to the remote gateway to perform certain tasks, such as second-stage dialing. According to RFC 2833, the RTP payload type for DTMF is assigned dynamically, so it must be in the range of 96 and 127. One can use`-1`to disable DTMF and free up the previous assigned type. This method cannot be called when the stream already joined an [AudioGroup](../android/net/rtp/AudioGroup.md).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The RTP payload type to be used or`-1`to disable it. |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if the type is invalid or used by codec. |
| `java.lang.IllegalStateException` | if the stream is busy. |

**See Also**

- [android.net.rtp.AudioGroup#sendDtmf(int)](../android/net/rtp/AudioGroup.md))
