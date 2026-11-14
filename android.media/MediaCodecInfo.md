# MediaCodecInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCodecInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCodecInfo "View this page in Java") 
| --- | --- |

```
class MediaCodecInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCodecInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#) |

Provides information about a given media codec available on the device. You can iterate through all codecs available by querying [MediaCodecList](https://developer.android.com/reference/kotlin/android/media/MediaCodecList). For example, here's how to find an encoder that supports a given MIME type: 

```kotlin
private static MediaCodecInfo selectCodec(String mimeType) {
      int numCodecs = MediaCodecList.getCodecCount();
      for (int i = 0; i < numCodecs; i++) {
          MediaCodecInfo codecInfo = MediaCodecList.getCodecInfoAt(i);
 
          if (!codecInfo.isEncoder()) {
              continue;
          }
 
          String[] types = codecInfo.getSupportedTypes();
          for (int j = 0; j < types.length; j++) {
              if (types[j].equalsIgnoreCase(mimeType)) {
                  return codecInfo;
              }
          }
      }
      return null;
  }
```

<br />

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AudioCapabilities](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.AudioCapabilities) A class that supports querying the audio capabilities of a codec. |
| | [CodecCapabilities](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities) Encapsulates the capabilities of a given codec component. |
| | [CodecProfileLevel](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel) Encapsulates the profiles available for a codec component. |
| --- | --- |
| | [EncoderCapabilities](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.EncoderCapabilities) A class that supports querying the encoding capabilities of a codec. |
| | [VideoCapabilities](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.VideoCapabilities) A class that supports querying the video capabilities of a codec. |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_MODEL_MEMORY_SAFE](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_MEMORY_SAFE:kotlin.Int) In this model the codec is not running in a sandboxed process, but written in a memory-safe way. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_MODEL_SANDBOXED](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_SANDBOXED:kotlin.Int) In this model the codec is running in a sandboxed process. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCanonicalName](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getCanonicalName())`()` Retrieve the underlying codec name. |
| [MediaCodecInfo.CodecCapabilities](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities)! | [getCapabilitiesForType](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getCapabilitiesForType(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Enumerates the capabilities of the codec component. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getName())`()` Retrieve the codec name. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityModel](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getSecurityModel())`()` Query the security model of the codec. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedTypes](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getSupportedTypes())`()` Query the media types supported by the codec. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAlias](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#isAlias())`()` Query if the codec is an alias for another underlying codec. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEncoder](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#isEncoder())`()` Query if the codec is an encoder. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHardwareAccelerated](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#isHardwareAccelerated())`()` Query if the codec is hardware accelerated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSoftwareOnly](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#isSoftwareOnly())`()` Query if the codec is software only. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVendor](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#isVendor())`()` Query if the codec is provided by the Android platform (false) or the device manufacturer (true). |

## Constants

### SECURITY_MODEL_MEMORY_SAFE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_MODEL_MEMORY_SAFE: Int
```

In this model the codec is not running in a sandboxed process, but written in a memory-safe way. It typically means that the software implementation of the codec is written in a memory-safe language such as Rust. 

 Value: 1

### SECURITY_MODEL_SANDBOXED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_MODEL_SANDBOXED: Int
```

In this model the codec is running in a sandboxed process. Even if a malicious content was fed to the codecs in this model, the impact will be contained in the sandboxed process. 

 Value: 0

## Public methods

### getCanonicalName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCanonicalName(): String
```

Retrieve the underlying codec name. Device implementations may provide multiple aliases (codec names) for the same underlying codec to maintain backward app compatibility. This method returns the name of the underlying codec name, which must not be another alias. For non-aliases this is always the name of the codec.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getCapabilitiesForType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapabilitiesForType(type: String!): MediaCodecInfo.CodecCapabilities!
```

Enumerates the capabilities of the codec component. Since a single component can support data of a variety of types, the type has to be specified to yield a meaningful result.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type to query |

### getName

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Retrieve the codec name.**Note:** Implementations may provide multiple aliases (codec names) for the same underlying codec, any of which can be used to instantiate the same underlying codec in [MediaCodec.createByCodecName](https://developer.android.com/reference/kotlin/android/media/MediaCodec#createByCodecName(kotlin.String)). Applications targeting SDK \< [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), cannot determine if the multiple codec names listed in MediaCodecList are in-fact for the same codec.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getSecurityModel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityModel(): Int
```

Query the security model of the codec.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.MediaCodecInfo#SECURITY_MODEL_SANDBOXED](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_SANDBOXED:kotlin.Int), [android.media.MediaCodecInfo#SECURITY_MODEL_MEMORY_SAFE](https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_MEMORY_SAFE:kotlin.Int), or android.media.MediaCodecInfo.SECURITY_MODEL_TRUSTED_CONTENT_ONLY |

### getSupportedTypes

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedTypes(): Array<String!>!
```

Query the media types supported by the codec. 

### isAlias

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAlias(): Boolean
```

Query if the codec is an alias for another underlying codec. 

### isEncoder

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEncoder(): Boolean
```

Query if the codec is an encoder. 

### isHardwareAccelerated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHardwareAccelerated(): Boolean
```

Query if the codec is hardware accelerated. This attribute is provided by the device manufacturer. Note that it cannot be tested for correctness. 

### isSoftwareOnly

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSoftwareOnly(): Boolean
```

Query if the codec is software only. Software-only codecs are more secure as they run in a tighter security sandbox. On the other hand, software-only codecs do not provide any performance guarantees. 

### isVendor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVendor(): Boolean
```

Query if the codec is provided by the Android platform (false) or the device manufacturer (true).
