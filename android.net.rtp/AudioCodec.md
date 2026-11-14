# AudioCodec

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioCodec

Kotlin | [Java](AudioCodec.md) 
| --- | --- |

```
open class AudioCodec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.rtp.AudioCodec](AudioCodec.md) |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](../android.net.sip/SipManager.md) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

This class defines a collection of audio codecs to be used with [AudioStream](AudioStream.md) s. Their parameters are designed to be exchanged using Session Description Protocol (SDP). Most of the values listed here can be found in RFC 3551, while others are described in separated standards.

Few simple configurations are defined as public static instances for the convenience of direct uses. More complicated ones could be obtained using [getCodec(int,java.lang.String,java.lang.String)](AudioCodec.md)). For example, one can use the following snippet to create a mode-1-only AMR codec. 

```kotlin
AudioCodec codec = AudioCodec.getCodec(100, "AMR/8000", "mode-set=1");
  
```

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [AudioCodec](AudioCodec.md)! | [getCodec](AudioCodec.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rtpmap:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fmtp:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an AudioCodec according to the given configuration. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioCodec](AudioCodec.md)!\>! | [getCodecs](AudioCodec.md))`()` Returns system supported audio codecs. |

| Properties ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AudioCodec](AudioCodec.md)! | [AMR](AudioCodec.md) Adaptive Multi-Rate narrowband audio codec, also known as AMR or AMR-NB. |
| static [AudioCodec](AudioCodec.md)! | [GSM](AudioCodec.md) GSM Full-Rate audio codec, also known as GSM-FR, GSM 06. |
| static [AudioCodec](AudioCodec.md)! | [GSM_EFR](AudioCodec.md) GSM Enhanced Full-Rate audio codec, also known as GSM-EFR, GSM 06. |
| --- | --- |
| static [AudioCodec](AudioCodec.md)! | [PCMA](AudioCodec.md) G. |
| static [AudioCodec](AudioCodec.md)! | [PCMU](AudioCodec.md) G. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [fmtp](AudioCodec.md) The format parameters to be used in the corresponding SDP attribute. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [rtpmap](AudioCodec.md) The encoding parameters to be used in the corresponding SDP attribute. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](AudioCodec.md) The RTP payload type of the encoding. |

## Public methods

### getCodec

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCodec(
    type: Int, 
    rtpmap: String!, 
    fmtp: String!
): AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

Creates an AudioCodec according to the given configuration.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The payload type of the encoding defined in RTP/AVP. |
| `rtpmap` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The encoding parameters specified in the corresponding SDP attribute, or null if it is not available. |
| `fmtp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The format parameters specified in the corresponding SDP attribute, or null if it is not available. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AudioCodec](AudioCodec.md)! | The configured AudioCodec or `null` if it is not supported. |

### getCodecs

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCodecs(): Array<AudioCodec!>!
```

**Deprecated:** *Deprecated in Java.*

Returns system supported audio codecs.

## Properties

### AMR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AMR: AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

Adaptive Multi-Rate narrowband audio codec, also known as AMR or AMR-NB. Currently CRC, robust sorting, and interleaving are not supported. See more details about these features in RFC 4867. 

### GSM

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GSM: AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

GSM Full-Rate audio codec, also known as GSM-FR, GSM 06.10, GSM, or simply FR. 

### GSM_EFR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GSM_EFR: AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

GSM Enhanced Full-Rate audio codec, also known as GSM-EFR, GSM 06.60, or simply EFR. 

### PCMA

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PCMA: AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

G.711 a-law audio codec. 

### PCMU

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PCMU: AudioCodec!
```

**Deprecated:** *Deprecated in Java.*

G.711 u-law audio codec. 

### fmtp

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val fmtp: String!
```

**Deprecated:** *Deprecated in Java.*

The format parameters to be used in the corresponding SDP attribute. 

### rtpmap

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val rtpmap: String!
```

**Deprecated:** *Deprecated in Java.*

The encoding parameters to be used in the corresponding SDP attribute. 

### type

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val type: Int
```

**Deprecated:** *Deprecated in Java.*

The RTP payload type of the encoding.
