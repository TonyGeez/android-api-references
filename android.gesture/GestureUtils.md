# GestureUtils

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureUtils

Kotlin| [Java](../android/gesture/GestureUtils.md) 
| --- | --- |

```
class GestureUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureUtils](../android/gesture/GestureUtils.md) |

Utility functions for gesture processing \& analysis, including methods for:

- feature extraction (e.g., samplers and those for calculating bounding boxes and gesture path lengths);
- geometric transformation (e.g., translation, rotation and scaling);
- gesture similarity comparison (e.g., calculating Euclidean or Cosine distances between two gestures).

<br />

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | [computeOrientedBoundingBox](../android/gesture/GestureUtils.md))`(`originalPoints:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Computes an oriented, minimum bounding box of a set of points. |
| static [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | [computeOrientedBoundingBox](../android/gesture/GestureUtils.md))`(`originalPoints:` ` [ArrayList](../java/util/ArrayList.md)< [GesturePoint](../android/gesture/GesturePoint.md)!>!`)` Computes an oriented, minimum bounding box of a set of points. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [spatialSampling](../android/gesture/GestureUtils.md))`(`gesture:` ` [Gesture](../android/gesture/Gesture.md)!`, `bitmapSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Samples the gesture spatially by rendering the gesture into a 2D grayscale bitmap. |
| --- | --- |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [spatialSampling](../android/gesture/GestureUtils.md))`(`gesture:` ` [Gesture](../android/gesture/Gesture.md)!`, `bitmapSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `keepAspectRatio:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Samples the gesture spatially by rendering the gesture into a 2D grayscale bitmap. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [temporalSampling](../android/gesture/GestureUtils.md))`(`stroke:` ` [GestureStroke](../android/gesture/GestureStroke.md)!`, `numPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Samples a stroke temporally into a given number of evenly-distributed points. |

## Public methods

### computeOrientedBoundingBox

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun computeOrientedBoundingBox(originalPoints: FloatArray!): OrientedBoundingBox!
```

Computes an oriented, minimum bounding box of a set of points.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------|
| `originalPoints` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!: |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------|
| [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | an oriented bounding box |

### computeOrientedBoundingBox

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun computeOrientedBoundingBox(originalPoints: ArrayList<GesturePoint!>!): OrientedBoundingBox!
```

Computes an oriented, minimum bounding box of a set of points.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalPoints` | [ArrayList](../java/util/ArrayList.md)\< [GesturePoint](../android/gesture/GesturePoint.md)!\>!: |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------|
| [OrientedBoundingBox](../android/gesture/OrientedBoundingBox.md)! | an oriented bounding box |

### spatialSampling

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spatialSampling(
    gesture: Gesture!, 
    bitmapSize: Int
): FloatArray!
```

Samples the gesture spatially by rendering the gesture into a 2D grayscale bitmap. Scales the gesture to fit the size of the bitmap. The scaling does not necessarily keep the aspect ratio of the gesture.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `gesture` | [Gesture](../android/gesture/Gesture.md)!:the gesture to be sampled |
| `bitmapSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the bitmap |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | a bitmapSize x bitmapSize grayscale bitmap that is represented as a 1D array. The float at index i represents the grayscale value at pixel \[i%bitmapSize, i/bitmapSize\] |

### spatialSampling

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun spatialSampling(
    gesture: Gesture!, 
    bitmapSize: Int, 
    keepAspectRatio: Boolean
): FloatArray!
```

Samples the gesture spatially by rendering the gesture into a 2D grayscale bitmap. Scales the gesture to fit the size of the bitmap.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `gesture` | [Gesture](../android/gesture/Gesture.md)!:the gesture to be sampled |
| `bitmapSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size of the bitmap |
| `keepAspectRatio` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if the scaling should keep the gesture's aspect ratio |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | a bitmapSize x bitmapSize grayscale bitmap that is represented as a 1D array. The float at index i represents the grayscale value at pixel \[i%bitmapSize, i/bitmapSize\] |

### temporalSampling

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun temporalSampling(
    stroke: GestureStroke!, 
    numPoints: Int
): FloatArray!
```

Samples a stroke temporally into a given number of evenly-distributed points.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| `stroke` | [GestureStroke](../android/gesture/GestureStroke.md)!:the gesture stroke to be sampled |
| `numPoints` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of points |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | the sampled points in the form of \[x1, y1, x2, y2, ..., xn, yn\] |
