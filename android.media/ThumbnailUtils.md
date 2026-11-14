# ThumbnailUtils

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThumbnailUtils

Kotlin| [Java](https://developer.android.com/reference/android/media/ThumbnailUtils "View this page in Java") 
| --- | --- |

```
open class ThumbnailUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ThumbnailUtils](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#) |

Utilities for generating visual thumbnails from files.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTIONS_RECYCLE_INPUT](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#OPTIONS_RECYCLE_INPUT:kotlin.Int) Constant used to indicate we should recycle the input in [extractThumbnail(android.graphics.Bitmap,int,int,int)](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#extractThumbnail(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))unless the output is the input. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [ThumbnailUtils](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#ThumbnailUtils())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [createAudioThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createAudioThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`, `size:` ` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Create a thumbnail for given audio file. |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [createAudioThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createAudioThumbnail(kotlin.String,%20kotlin.Int))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given audio file. |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [createImageThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createImageThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`, `size:` ` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Create a thumbnail for given image file. |
| --- | --- |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [createImageThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createImageThumbnail(kotlin.String,%20kotlin.Int))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given image file. |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [createVideoThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createVideoThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)`, `size:` ` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Create a thumbnail for given video file. |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [createVideoThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createVideoThumbnail(kotlin.String,%20kotlin.Int))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given video file. |
| --- | --- |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | [extractThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#extractThumbnail(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int))`(`source:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a centered bitmap of the desired size. |
| openstatic [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | [extractThumbnail](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#extractThumbnail(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`source:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a centered bitmap of the desired size. |

## Constants

### OPTIONS_RECYCLE_INPUT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTIONS_RECYCLE_INPUT: Int
```

Constant used to indicate we should recycle the input in [extractThumbnail(android.graphics.Bitmap,int,int,int)](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#extractThumbnail(android.graphics.Bitmap,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))unless the output is the input. 

 Value: 2

## Public constructors

### ThumbnailUtils

```
ThumbnailUtils()
```

## Public methods

### createAudioThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createAudioThumbnail(
    file: File, 
    size: Size, 
    signal: CancellationSignal?
): Bitmap
```

Create a thumbnail for given audio file.

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#loadThumbnail(android.net.Uri,%20android.util.Size,%20android.os.CancellationSignal))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):The audio file. This value cannot be`null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())was invoked. |

### createAudioThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createAudioThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createAudioThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createAudioThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given audio file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The audio file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Thumbnails.html#MINI_KIND:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | This value may be`null`. |

### createImageThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createImageThumbnail(
    file: File, 
    size: Size, 
    signal: CancellationSignal?
): Bitmap
```

Create a thumbnail for given image file.

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#loadThumbnail(android.net.Uri,%20android.util.Size,%20android.os.CancellationSignal))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):The image file. This value cannot be`null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())was invoked. |

### createImageThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createImageThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createImageThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createImageThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given image file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The image file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Thumbnails.html#MINI_KIND:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | This value may be`null`. |

### createVideoThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createVideoThumbnail(
    file: File, 
    size: Size, 
    signal: CancellationSignal?
): Bitmap
```

Create a thumbnail for given video file.

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#loadThumbnail(android.net.Uri,%20android.util.Size,%20android.os.CancellationSignal))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#):The video file. This value cannot be`null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())was invoked. |

### createVideoThumbnail

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createVideoThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createVideoThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](https://developer.android.com/reference/kotlin/android/media/ThumbnailUtils#createVideoThumbnail(java.io.File,%20android.util.Size,%20android.os.CancellationSignal)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given video file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The video file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](https://developer.android.com/reference/kotlin/android/provider/MediaStore.Images.Thumbnails.html#MINI_KIND:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | This value may be`null`. |

### extractThumbnail

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun extractThumbnail(
    source: Bitmap!, 
    width: Int, 
    height: Int
): Bitmap!
```

Creates a centered bitmap of the desired size.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `source` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:original bitmap source |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted height |
| --- | --- |

### extractThumbnail

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun extractThumbnail(
    source: Bitmap!, 
    width: Int, 
    height: Int, 
    options: Int
): Bitmap!
```

Creates a centered bitmap of the desired size.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------|
| `source` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:original bitmap source |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted height |
| --- | --- |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):options used during thumbnail extraction |
