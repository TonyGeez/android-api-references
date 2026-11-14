# CameraProfile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CameraProfile

Kotlin| [Java](../android/media/CameraProfile.md) 
| --- | --- |

```
open class CameraProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.CameraProfile](../android/media/CameraProfile.md) |

The CameraProfile class is used to retrieve the pre-defined still image capture (jpeg) quality levels (0-100) used for low, medium, and high quality settings in the Camera application.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH](../android/media/CameraProfile.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_LOW](../android/media/CameraProfile.md) Define three quality levels for JPEG image encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_MEDIUM](../android/media/CameraProfile.md) <br /> |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [CameraProfile](../android/media/CameraProfile.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJpegEncodingQualityParameter](../android/media/CameraProfile.md))`(`quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pre-defined still image capture (jpeg) quality level used for the given quality level in the Camera application for the first back-facing camera on the device. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getJpegEncodingQualityParameter](../android/media/CameraProfile.md))`(`cameraId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a pre-defined still image capture (jpeg) quality level used for the given quality level in the Camera application for the specified camera. |

## Constants

### QUALITY_HIGH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH: Int
```  

 Value: 2

### QUALITY_LOW

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_LOW: Int
```

Define three quality levels for JPEG image encoding. 

 Value: 0

### QUALITY_MEDIUM

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_MEDIUM: Int
```  

 Value: 1

## Public constructors

### CameraProfile

```
CameraProfile()
```

## Public methods

### getJpegEncodingQualityParameter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getJpegEncodingQualityParameter(quality: Int): Int
```

Returns a pre-defined still image capture (jpeg) quality level used for the given quality level in the Camera application for the first back-facing camera on the device. If the device has no back-facing camera, this returns 0.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target quality level |

### getJpegEncodingQualityParameter

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getJpegEncodingQualityParameter(
    cameraId: Int, 
    quality: Int
): Int
```

Returns a pre-defined still image capture (jpeg) quality level used for the given quality level in the Camera application for the specified camera.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------|
| `cameraId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the camera |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The target quality level |
