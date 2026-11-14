# FaceDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FaceDetector

Kotlin| [Java](../android/media/FaceDetector.md) 
| --- | --- |

```
open class FaceDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.FaceDetector](../android/media/FaceDetector.md) |

Identifies the faces of people in a [android.graphics.Bitmap](../android/graphics/Bitmap.md) graphic object.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Face](../android/media/FaceDetector.Face.md) A Face contains all the information identifying the location of a face in a bitmap. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FaceDetector](../android/media/FaceDetector.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxFaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a FaceDetector, configured with the size of the images to be analysed and the maximum number of faces that can be detected. |

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findFaces](../android/media/FaceDetector.md))`(`bitmap:` ` [Bitmap](../android/graphics/Bitmap.md)!`, `faces:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FaceDetector.Face](../android/media/FaceDetector.Face.md)!>!`)` Finds all the faces found in a given [android.graphics.Bitmap](../android/graphics/Bitmap.md). |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/FaceDetector.md))`()` <br /> |

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

Finds all the faces found in a given [android.graphics.Bitmap](../android/graphics/Bitmap.md). The supplied array is populated with [FaceDetector.Face](../android/media/FaceDetector.Face.md) s for each face found. The bitmap must be in 565 format (for now).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android/graphics/Bitmap.md)!:the [android.graphics.Bitmap](../android/graphics/Bitmap.md) graphic to be analyzed |
| `faces` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FaceDetector.Face](../android/media/FaceDetector.Face.md)!\>!:an array in which to place all found [FaceDetector.Face](../android/media/FaceDetector.Face.md) s. The array must be sized equal to the maxFaces value set at initialization |

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
