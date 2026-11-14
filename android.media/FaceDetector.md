# FaceDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FaceDetector

Kotlin| [Java](https://developer.android.com/reference/android/media/FaceDetector "View this page in Java") 
| --- | --- |

```
open class FaceDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.FaceDetector](https://developer.android.com/reference/kotlin/android/media/FaceDetector#) |

Identifies the faces of people in a [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) graphic object.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Face](https://developer.android.com/reference/kotlin/android/media/FaceDetector.Face) A Face contains all the information identifying the location of a face in a bitmap. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FaceDetector](https://developer.android.com/reference/kotlin/android/media/FaceDetector#FaceDetector(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxFaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a FaceDetector, configured with the size of the images to be analysed and the maximum number of faces that can be detected. |

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findFaces](https://developer.android.com/reference/kotlin/android/media/FaceDetector#findFaces(android.graphics.Bitmap,%20kotlin.Array))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`, `faces:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FaceDetector.Face](https://developer.android.com/reference/kotlin/android/media/FaceDetector.Face)!>!`)` Finds all the faces found in a given [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/FaceDetector#finalize())`()` <br /> |

## Public constructors

### FaceDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FaceDetector(
    width: Int, 
    height: Int, 
    maxFaces: Int)
```

Creates a FaceDetector, configured with the size of the images to be analysed and the maximum number of faces that can be detected. These parameters cannot be changed once the object is constructed. Note that the width of the image must be even.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the width of the image |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the height of the image |
| `maxFaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of faces to identify |
| --- | --- |

## Public methods

### findFaces

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findFaces(
    bitmap: Bitmap!, 
    faces: Array<FaceDetector.Face!>!
): Int
```

Finds all the faces found in a given [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). The supplied array is populated with [FaceDetector.Face](https://developer.android.com/reference/kotlin/android/media/FaceDetector.Face) s for each face found. The bitmap must be in 565 format (for now).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:the [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) graphic to be analyzed |
| `faces` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FaceDetector.Face](https://developer.android.com/reference/kotlin/android/media/FaceDetector.Face)!\>!:an array in which to place all found [FaceDetector.Face](https://developer.android.com/reference/kotlin/android/media/FaceDetector.Face) s. The array must be sized equal to the maxFaces value set at initialization |

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of faces found |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the Bitmap dimensions don't match the dimensions defined at initialization or the given array is not sized equal to the maxFaces value defined at initialization |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
