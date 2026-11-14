# ApplicationMediaCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationMediaCapabilities

Kotlin| [Java](https://developer.android.com/reference/android/media/ApplicationMediaCapabilities "View this page in Java") 

```
class ApplicationMediaCapabilities : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) |

ApplicationMediaCapabilities is an immutable class that encapsulates an application's capabilities for handling newer video codec format and media features.

Android 12 introduces Compatible media transcoding feature. See [Compatible media transcoding](https://developer.android.com/about/versions/12/features#compatible_media_transcoding). By default, Android assumes apps can support playback of all media formats. Apps that would like to request that media be transcoded into a more compatible format should declare their media capabilities in a media_capabilities.xml resource file and add it as a property tag in the AndroidManifest.xml file. Here is a example: 

```kotlin
<code>&lt;media-capabilities xmlns:android="http://schemas.android.com/apk/res/android"&gt;
   &lt;format android:name="HEVC" supported="true"/&gt;
   &lt;format android:name="HDR10" supported="false"/&gt;
   &lt;format android:name="HDR10Plus" supported="false"/&gt;
 &lt;/media-capabilities&gt;
 </code>
```
The ApplicationMediaCapabilities class is generated from this xml and used by the platform to represent an application's media capabilities in order to determine whether modern media files need to be transcoded for that application.

<br />

ApplicationMediaCapabilities objects can also be built by applications at runtime for use with [ContentResolver.openTypedAssetFileDescriptor(Uri, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle))to provide more control over the transcoding that is built into the platform. ApplicationMediaCapabilities provided by applications at runtime like this override the default manifest capabilities for that media access.The object could be build either through [createFromXml(org.xmlpull.v1.XmlPullParser)](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#createFromXml(org.xmlpull.v1.XmlPullParser))or through the builder class [ApplicationMediaCapabilities.Builder](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.Builder)

### Video Codec Support

Newer video codes include HEVC, VP9 and AV1. Application only needs to indicate their support for newer format with this class as they are assumed to support older format like h.264.

### Capability of handling HDR(high dynamic range) video

There are four types of HDR video(Dolby-Vision, HDR10, HDR10+, HLG) supported by the platform, application will only need to specify individual types they supported.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities.Builder) Builder class for [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) | [createFromXml](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#createFromXml(org.xmlpull.v1.XmlPullParser))`(`xmlParser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)`)` Creates [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) from an xml. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSupportedHdrTypes](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#getSupportedHdrTypes())`()` Query all hdr types that are supported by the application. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSupportedVideoMimeTypes](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#getSupportedVideoMimeTypes())`()` Query the video codec mime types supported by the application. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getUnsupportedHdrTypes](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#getUnsupportedHdrTypes())`()` Query all hdr types that are not supported by the application. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getUnsupportedVideoMimeTypes](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#getUnsupportedVideoMimeTypes())`()` Query the video codec mime types that are not supported by the application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFormatSpecified](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#isFormatSpecified(kotlin.String))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if a format is specified by the application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHdrTypeSupported](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#isHdrTypeSupported(kotlin.String))`(`hdrType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if a HDR type is supported by the application. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVideoMimeTypeSupported](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#isVideoMimeTypeSupported(kotlin.String))`(`videoMime:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if a video codec format is supported by the application. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### createFromXml

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createFromXml(xmlParser: XmlPullParser): ApplicationMediaCapabilities
```

Creates [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) from an xml. The xml's syntax is the same as the media_capabilities.xml used by the AndroidManifest.xml.

Here is an example: 

```kotlin
<code>&lt;media-capabilities xmlns:android="http://schemas.android.com/apk/res/android"&gt;
      &lt;format android:name="HEVC" supported="true"/&gt;
      &lt;format android:name="HDR10" supported="false"/&gt;
      &lt;format android:name="HDR10Plus" supported="false"/&gt;
  &lt;/media-capabilities&gt;
  </code>
```

<br />

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `xmlParser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#):The underlying [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#) that will read the xml. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [ApplicationMediaCapabilities](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#) | An ApplicationMediaCapabilities object. This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the capabilities in xml config are invalid or incompatible. |

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSupportedHdrTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedHdrTypes(): MutableList<String!>
```

Query all hdr types that are supported by the application.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | List of supported hdr types. The list will be empty if there are none. This value cannot be`null`. |

### getSupportedVideoMimeTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedVideoMimeTypes(): MutableList<String!>
```

Query the video codec mime types supported by the application.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | List of supported video codec mime types. The list will be empty if there are none. This value cannot be`null`. |

### getUnsupportedHdrTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnsupportedHdrTypes(): MutableList<String!>
```

Query all hdr types that are not supported by the application.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | List of unsupported hdr types. The list will be empty if there are none. This value cannot be`null`. |

### getUnsupportedVideoMimeTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnsupportedVideoMimeTypes(): MutableList<String!>
```

Query the video codec mime types that are not supported by the application.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | List of unsupported video codec mime types. The list will be empty if there are none. This value cannot be`null`. |

### isFormatSpecified

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFormatSpecified(format: String): Boolean
```

Query if a format is specified by the application.

The format could be either the video format or the hdr format.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the format. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if application specifies the format, false otherwise. |

### isHdrTypeSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHdrTypeSupported(hdrType: String): Boolean
```

Query if a HDR type is supported by the application.

If the application has not specified supporting the format or not, this will return false. Use [isFormatSpecified(java.lang.String)](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#isFormatSpecified(kotlin.String))to query if a format is specified or not.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hdrType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The type of the HDR format. This value cannot be`null`. Value is [android.media.MediaFeature.HdrType#DOLBY_VISION](https://developer.android.com/reference/kotlin/android/media/MediaFeature.HdrType#DOLBY_VISION:kotlin.String), [android.media.MediaFeature.HdrType#HDR10](https://developer.android.com/reference/kotlin/android/media/MediaFeature.HdrType#HDR10:kotlin.String), [android.media.MediaFeature.HdrType#HDR10_PLUS](https://developer.android.com/reference/kotlin/android/media/MediaFeature.HdrType#HDR10_PLUS:kotlin.String), or [android.media.MediaFeature.HdrType#HLG](https://developer.android.com/reference/kotlin/android/media/MediaFeature.HdrType#HLG:kotlin.String) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if application supports the HDR format, false otherwise. |

### isVideoMimeTypeSupported

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVideoMimeTypeSupported(videoMime: String): Boolean
```

Query if a video codec format is supported by the application.

If the application has not specified supporting the format or not, this will return false. Use [isFormatSpecified(java.lang.String)](https://developer.android.com/reference/kotlin/android/media/ApplicationMediaCapabilities#isFormatSpecified(kotlin.String))to query if a format is specified or not.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoMime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The mime type of the video codec format. Must be the one used in [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if application supports the video codec format, false otherwise. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ApplicationMediaCapabilities!>
```
