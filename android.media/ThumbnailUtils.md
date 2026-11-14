# ThumbnailUtils

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThumbnailUtils

Kotlin| [Java](ThumbnailUtils.md) 
| --- | --- |

```
open class ThumbnailUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.ThumbnailUtils](ThumbnailUtils.md) |

Utilities for generating visual thumbnails from files.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTIONS_RECYCLE_INPUT](ThumbnailUtils.md) Constant used to indicate we should recycle the input in [extractThumbnail(android.graphics.Bitmap,int,int,int)](ThumbnailUtils.md))unless the output is the input. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [ThumbnailUtils](ThumbnailUtils.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Bitmap](../android.graphics/Bitmap.md) | [createAudioThumbnail](ThumbnailUtils.md))`(`file:` ` [File](../java.io/File.md)`, `size:` ` [Size](../android.util/Size.md)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` Create a thumbnail for given audio file. |
| openstatic [Bitmap](../android.graphics/Bitmap.md)? | [createAudioThumbnail](ThumbnailUtils.md))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given audio file. |
| openstatic [Bitmap](../android.graphics/Bitmap.md) | [createImageThumbnail](ThumbnailUtils.md))`(`file:` ` [File](../java.io/File.md)`, `size:` ` [Size](../android.util/Size.md)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` Create a thumbnail for given image file. |
| --- | --- |
| openstatic [Bitmap](../android.graphics/Bitmap.md)? | [createImageThumbnail](ThumbnailUtils.md))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given image file. |
| openstatic [Bitmap](../android.graphics/Bitmap.md) | [createVideoThumbnail](ThumbnailUtils.md))`(`file:` ` [File](../java.io/File.md)`, `size:` ` [Size](../android.util/Size.md)`, `signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` Create a thumbnail for given video file. |
| openstatic [Bitmap](../android.graphics/Bitmap.md)? | [createVideoThumbnail](ThumbnailUtils.md))`(`filePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a thumbnail for given video file. |
| --- | --- |
| openstatic [Bitmap](../android.graphics/Bitmap.md)! | [extractThumbnail](ThumbnailUtils.md))`(`source:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a centered bitmap of the desired size. |
| openstatic [Bitmap](../android.graphics/Bitmap.md)! | [extractThumbnail](ThumbnailUtils.md))`(`source:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a centered bitmap of the desired size. |

## Constants

### OPTIONS_RECYCLE_INPUT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTIONS_RECYCLE_INPUT: Int
```

Constant used to indicate we should recycle the input in [extractThumbnail(android.graphics.Bitmap,int,int,int)](ThumbnailUtils.md))unless the output is the input. 

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

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](../android.content/ContentResolver.md))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):The audio file. This value cannot be`null`. |
| `size` | [Size](../android.util/Size.md):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](../android.graphics/Bitmap.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](../android.os/CancellationSignal.md))was invoked. |

### createAudioThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createAudioThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createAudioThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](ThumbnailUtils.md)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given audio file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The audio file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](../android/provider/MediaStore.Images.Thumbnails.md). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](../android.graphics/Bitmap.md)? | This value may be`null`. |

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

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](../android.content/ContentResolver.md))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):The image file. This value cannot be`null`. |
| `size` | [Size](../android.util/Size.md):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](../android.graphics/Bitmap.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](../android.os/CancellationSignal.md))was invoked. |

### createImageThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createImageThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createImageThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](ThumbnailUtils.md)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given image file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The image file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](../android/provider/MediaStore.Images.Thumbnails.md). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](../android.graphics/Bitmap.md)? | This value may be`null`. |

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

This method should only be used for files that you have direct access to; if you'd like to work with media hosted outside your app, consider using [ContentResolver.loadThumbnail(Uri, Size, CancellationSignal)](../android.content/ContentResolver.md))which enables remote providers to efficiently cache and invalidate thumbnails.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):The video file. This value cannot be`null`. |
| `size` | [Size](../android.util/Size.md):The desired thumbnail size. This value cannot be`null`. |
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?:This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Bitmap](../android.graphics/Bitmap.md) | This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](../android.os/CancellationSignal.md))was invoked. |

### createVideoThumbnail

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createVideoThumbnail(
    filePath: String, 
    kind: Int
): Bitmap?
```

**Deprecated:** *Callers should migrate to using [createVideoThumbnail(java.io.File,android.util.Size,android.os.CancellationSignal)](ThumbnailUtils.md)), as it offers more control over resizing and cancellation.*

Create a thumbnail for given video file.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The video file. This value cannot be`null`. |
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired thumbnail kind, such as [android.provider.MediaStore.Images.Thumbnails#MINI_KIND](../android/provider/MediaStore.Images.Thumbnails.md). |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](../android.graphics/Bitmap.md)? | This value may be`null`. |

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
| `source` | [Bitmap](../android.graphics/Bitmap.md)!:original bitmap source |
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
| `source` | [Bitmap](../android.graphics/Bitmap.md)!:original bitmap source |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted width |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):targeted height |
| --- | --- |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):options used during thumbnail extraction |
