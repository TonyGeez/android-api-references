# MediaCodecList

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCodecList

Kotlin | [Java](MediaCodecList.md) 
| --- | --- |

```
class MediaCodecList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCodecList](MediaCodecList.md) |

Allows you to enumerate available codecs, each specified as a [MediaCodecInfo](MediaCodecInfo.md) object, find a codec supporting a given format and query the capabilities of a given codec.

See [MediaCodecInfo](MediaCodecInfo.md) for sample usage.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_CODECS](MediaCodecList.md) Use in [MediaCodecList](MediaCodecList.md)) to enumerate all codecs, even ones that are not suitable for regular (buffer-to-buffer) decoding or encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGULAR_CODECS](MediaCodecList.md) Use in [MediaCodecList](MediaCodecList.md)) to enumerate only codecs that are suitable for regular (buffer-to-buffer) decoding or encoding. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaCodecList](MediaCodecList.md))`(`kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a list of media-codecs of a specific kind. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findDecoderForFormat](MediaCodecList.md))`(`format:` ` [MediaFormat](MediaFormat.md)!`)` Find a decoder supporting a given [MediaFormat](MediaFormat.md) in the list of media-codecs. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findEncoderForFormat](MediaCodecList.md))`(`format:` ` [MediaFormat](MediaFormat.md)!`)` Find an encoder supporting a given [MediaFormat](MediaFormat.md) in the list of media-codecs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodecCount](MediaCodecList.md))`()` Count the number of available (regular) codecs. |
| --- | --- |
| static [MediaCodecInfo](MediaCodecInfo.md)! | [getCodecInfoAt](MediaCodecList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the [MediaCodecInfo](MediaCodecInfo.md) object for the codec at the given `index` in the regular list. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MediaCodecInfo](MediaCodecInfo.md)!\>! | [getCodecInfos](MediaCodecList.md))`()` Returns the list of [MediaCodecInfo](MediaCodecInfo.md) objects for the list of media-codecs. |

## Constants

### ALL_CODECS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_CODECS: Int
```

Use in [MediaCodecList](MediaCodecList.md)) to enumerate all codecs, even ones that are not suitable for regular (buffer-to-buffer) decoding or encoding. These include codecs, for example, that only work with special input or output surfaces, such as secure-only or tunneled-only codecs. 

 Value: 1

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported](../android/media/MediaCodecInfo.CodecCapabilities.md))
- [android.media.MediaCodecInfo.CodecCapabilities#FEATURE_SecurePlayback](../android/media/MediaCodecInfo.CodecCapabilities.md)
- [android.media.MediaCodecInfo.CodecCapabilities#FEATURE_TunneledPlayback](../android/media/MediaCodecInfo.CodecCapabilities.md) 

### REGULAR_CODECS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGULAR_CODECS: Int
```

Use in [MediaCodecList](MediaCodecList.md)) to enumerate only codecs that are suitable for regular (buffer-to-buffer) decoding or encoding. *NOTE:* These are the codecs that are returned prior to API 21, using the now deprecated static methods. 

 Value: 0

## Public constructors

### MediaCodecList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCodecList(kind: Int)
```

Create a list of media-codecs of a specific kind.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Either [MediaCodecList.REGULAR_CODECS](MediaCodecList.md) or [MediaCodecList.ALL_CODECS](MediaCodecList.md). |

## Public methods

### findDecoderForFormat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findDecoderForFormat(format: MediaFormat!): String!
```

Find a decoder supporting a given [MediaFormat](MediaFormat.md) in the list of media-codecs.

**Note:** On [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md), `format` must not contain a [frame rate](MediaFormat.md). Use `format.setString(MediaFormat.KEY_FRAME_RATE, null)` to clear any existing frame rate setting in the format.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [MediaFormat](MediaFormat.md)!: A decoder media format with optional feature directives. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of a decoder that supports the given format and feature requests, or `null` if no such codec has been found. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not a valid media format. |
| `java.lang.NullPointerException` | if format is null. |

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported(MediaFormat)](../android/media/MediaCodecInfo.CodecCapabilities.md)) 

### findEncoderForFormat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findEncoderForFormat(format: MediaFormat!): String!
```

Find an encoder supporting a given [MediaFormat](MediaFormat.md) in the list of media-codecs.

**Note:** On [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md), `format` must not contain a [frame rate](MediaFormat.md). Use `format.setString(MediaFormat.KEY_FRAME_RATE, null)` to clear any existing frame rate setting in the format.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [MediaFormat](MediaFormat.md)!: An encoder media format with optional feature directives. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of an encoder that supports the given format and feature requests, or `null` if no such codec has been found. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not a valid media format. |
| `java.lang.NullPointerException` | if format is null. |

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported(MediaFormat)](../android/media/MediaCodecInfo.CodecCapabilities.md)) 

### getCodecCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodecCount(): Int
```

**Deprecated:** *Use [getCodecInfos](MediaCodecList.md)) instead.*

Count the number of available (regular) codecs. 
**See Also**

- [#REGULAR_CODECS](MediaCodecList.md) 

### getCodecInfoAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodecInfoAt(index: Int): MediaCodecInfo!
```

**Deprecated:** *Use [getCodecInfos](MediaCodecList.md)) instead.*

Return the [MediaCodecInfo](MediaCodecInfo.md) object for the codec at the given `index` in the regular list. 
**See Also**

- [#REGULAR_CODECS](MediaCodecList.md) 

### getCodecInfos

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecInfos(): Array<MediaCodecInfo!>!
```

Returns the list of [MediaCodecInfo](MediaCodecInfo.md) objects for the list of media-codecs.
