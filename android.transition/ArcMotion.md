# ArcMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArcMotion

Kotlin| [Java](https://developer.android.com/reference/android/transition/ArcMotion "View this page in Java") 

```
open class ArcMotion : PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.transition.PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion) ||
| | ↳ | [android.transition.ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#) |

A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. If the horizontal distance between the points is less than the vertical distance, then the circle's center point will be horizontally aligned with the end point. If the vertical distance is less than the horizontal distance then the circle's center point will be vertically aligned with the end point.

When the two points are near horizontal or vertical, the curve of the motion will be small as the center of the circle will be far from both points. To force curvature of the path, [setMinimumHorizontalAngle(float)](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#setMinimumHorizontalAngle(kotlin.Float))and [setMinimumVerticalAngle(float)](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#setMinimumVerticalAngle(kotlin.Float))may be used to set the minimum angle of the arc between two points.

This may be used in XML as an element inside a transition. 

```kotlin
<code>&lt;changeBounds&gt;
    &lt;arcMotion android:minimumHorizontalAngle="15"
               android:minimumVerticalAngle="0"
               android:maximumAngle="90"/&gt;
  &lt;/changeBounds&gt;</code>
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#ArcMotion())`()` <br /> |
| [ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#ArcMotion(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaximumAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#getMaximumAngle())`()` Returns the maximum arc along the circle between two points. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinimumHorizontalAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#getMinimumHorizontalAngle())`()` Returns the minimum arc along the circle between two points aligned near horizontally. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinimumVerticalAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#getMinimumVerticalAngle())`()` Returns the minimum arc along the circle between two points aligned near vertically. |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [getPath](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#getPath(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#setMaximumAngle(kotlin.Float))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the maximum arc along the circle between two points. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumHorizontalAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#setMinimumHorizontalAngle(kotlin.Float))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the minimum arc along the circle between two points aligned near horizontally. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumVerticalAngle](https://developer.android.com/reference/kotlin/android/transition/ArcMotion#setMinimumVerticalAngle(kotlin.Float))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the minimum arc along the circle between two points aligned near vertically. |

## Public constructors

### ArcMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArcMotion()
```  

### ArcMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArcMotion(
    context: Context!, 
    attrs: AttributeSet!)
```

## Public methods

### getMaximumAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumAngle(): Float
```

Returns the maximum arc along the circle between two points. When start and end points have close to equal x and y differences, the curve between them is large. This forces the curved path to have an arc of at most the given angle.

The default value is 70 degrees.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The maximum angle of the arc on a circle describing the Path between the start and end points. |

### getMinimumHorizontalAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumHorizontalAngle(): Float
```

Returns the minimum arc along the circle between two points aligned near horizontally. When start and end points are close to horizontal, the calculated center point of the circle will be far from both points, giving a near straight path between the points. By setting a minimum angle, this forces the center point to be closer and give an exaggerated curve to the path.

The default value is 0.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The minimum arc along the circle between two points aligned near horizontally. |

### getMinimumVerticalAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumVerticalAngle(): Float
```

Returns the minimum arc along the circle between two points aligned near vertically. When start and end points are close to vertical, the calculated center point of the circle will be far from both points, giving a near straight path between the points. By setting a minimum angle, this forces the center point to be closer and give an exaggerated curve to the path.

The default value is 0.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The minimum angle of the arc on a circle describing the Path between two nearly vertically-separated points. |

### getPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPath(
    startX: Float, 
    startY: Float, 
    endX: Float, 
    endY: Float
): Path!
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the starting point. |
| `startY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the starting point. |
| `endX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the ending point. |
| `endY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the ending point. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](https://developer.android.com/reference/kotlin/android/graphics/Path.html#moveTo(kotlin.Float,%20kotlin.Float))and end at`(endX, endY)`. |

### setMaximumAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumAngle(angleInDegrees: Float): Unit
```

Sets the maximum arc along the circle between two points. When start and end points have close to equal x and y differences, the curve between them is large. This forces the curved path to have an arc of at most the given angle.

The default value is 70 degrees.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `angleInDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The maximum angle of the arc on a circle describing the Path between the start and end points. |

### setMinimumHorizontalAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumHorizontalAngle(angleInDegrees: Float): Unit
```

Sets the minimum arc along the circle between two points aligned near horizontally. When start and end points are close to horizontal, the calculated center point of the circle will be far from both points, giving a near straight path between the points. By setting a minimum angle, this forces the center point to be closer and give an exaggerated curve to the path.

The default value is 0.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `angleInDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The minimum angle of the arc on a circle describing the Path between two nearly horizontally-separated points. |

### setMinimumVerticalAngle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumVerticalAngle(angleInDegrees: Float): Unit
```

Sets the minimum arc along the circle between two points aligned near vertically. When start and end points are close to vertical, the calculated center point of the circle will be far from both points, giving a near straight path between the points. By setting a minimum angle, this forces the center point to be closer and give an exaggerated curve to the path.

The default value is 0.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `angleInDegrees` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The minimum angle of the arc on a circle describing the Path between two nearly vertically-separated points. |
