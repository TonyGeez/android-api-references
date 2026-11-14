# MediaCodecList

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCodecList

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaCodecList "View this page in Java") 
| --- | --- |

```
class MediaCodecList
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#) |

Allows you to enumerate available codecs, each specified as a [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) object, find a codec supporting a given format and query the capabilities of a given codec.

See [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) for sample usage.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#ALL_CODECS:kotlin.Int) Use in [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#MediaCodecList(kotlin.Int)) to enumerate all codecs, even ones that are not suitable for regular (buffer-to-buffer) decoding or encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGULAR_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#REGULAR_CODECS:kotlin.Int) Use in [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#MediaCodecList(kotlin.Int)) to enumerate only codecs that are suitable for regular (buffer-to-buffer) decoding or encoding. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#MediaCodecList(kotlin.Int))`(`kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a list of media-codecs of a specific kind. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findDecoderForFormat](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findDecoderForFormat(android.media.MediaFormat))`(`format:` ` [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat)!`)` Find a decoder supporting a given [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) in the list of media-codecs. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [findEncoderForFormat](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findEncoderForFormat(android.media.MediaFormat))`(`format:` ` [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat)!`)` Find an encoder supporting a given [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) in the list of media-codecs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCodecCount](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#getCodecCount())`()` Count the number of available (regular) codecs. |
| --- | --- |
| static [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo)! | [getCodecInfoAt](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#getCodecInfoAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) object for the codec at the given `index` in the regular list. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo)!\>! | [getCodecInfos](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#getCodecInfos())`()` Returns the list of [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) objects for the list of media-codecs. |

## Constants

### ALL_CODECS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_CODECS: Int
```

Use in [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#MediaCodecList(kotlin.Int)) to enumerate all codecs, even ones that are not suitable for regular (buffer-to-buffer) decoding or encoding. These include codecs, for example, that only work with special input or output surfaces, such as secure-only or tunneled-only codecs. 

 Value: 1

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#isFormatSupported(android.media.MediaFormat))
- [android.media.MediaCodecInfo.CodecCapabilities#FEATURE_SecurePlayback](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_SecurePlayback:kotlin.String)
- [android.media.MediaCodecInfo.CodecCapabilities#FEATURE_TunneledPlayback](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_TunneledPlayback:kotlin.String) 

### REGULAR_CODECS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGULAR_CODECS: Int
```

Use in [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#MediaCodecList(kotlin.Int)) to enumerate only codecs that are suitable for regular (buffer-to-buffer) decoding or encoding. *NOTE:* These are the codecs that are returned prior to API 21, using the now deprecated static methods. 

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
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Either [MediaCodecList.REGULAR_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#REGULAR_CODECS:kotlin.Int) or [MediaCodecList.ALL_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#ALL_CODECS:kotlin.Int). |

## Public methods

### findDecoderForFormat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findDecoderForFormat(format: MediaFormat!): String!
```

Find a decoder supporting a given [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) in the list of media-codecs.

**Note:** On [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int), `format` must not contain a [frame rate](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String). Use `format.setString(MediaFormat.KEY_FRAME_RATE, null)` to clear any existing frame rate setting in the format.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat)!: A decoder media format with optional feature directives. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of a decoder that supports the given format and feature requests, or `null` if no such codec has been found. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not a valid media format. |
| `java.lang.NullPointerException` | if format is null. |

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported(MediaFormat)](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#isFormatSupported(android.media.MediaFormat)) 

### findEncoderForFormat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun findEncoderForFormat(format: MediaFormat!): String!
```

Find an encoder supporting a given [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) in the list of media-codecs.

**Note:** On [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int), `format` must not contain a [frame rate](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String). Use `format.setString(MediaFormat.KEY_FRAME_RATE, null)` to clear any existing frame rate setting in the format.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat)!: An encoder media format with optional feature directives. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of an encoder that supports the given format and feature requests, or `null` if no such codec has been found. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if format is not a valid media format. |
| `java.lang.NullPointerException` | if format is null. |

**See Also**

- [android.media.MediaCodecInfo.CodecCapabilities#isFormatSupported(MediaFormat)](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#isFormatSupported(android.media.MediaFormat)) 

### getCodecCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodecCount(): Int
```

**Deprecated:** *Use [getCodecInfos](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#getCodecInfos()) instead.*

Count the number of available (regular) codecs. 
**See Also**

- [#REGULAR_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#REGULAR_CODECS:kotlin.Int) 

### getCodecInfoAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCodecInfoAt(index: Int): MediaCodecInfo!
```

**Deprecated:** *Use [getCodecInfos](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#getCodecInfos()) instead.*

Return the [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) object for the codec at the given `index` in the regular list. 
**See Also**

- [#REGULAR_CODECS](https://developer.android.com/reference/kotlin/android/media/MediaCodecList#REGULAR_CODECS:kotlin.Int) 

### getCodecInfos

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecInfos(): Array<MediaCodecInfo!>!
```

Returns the list of [MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo) objects for the list of media-codecs.
