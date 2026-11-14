# ArcMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArcMotion

Kotlin| [Java](ArcMotion.md) 
| --- | --- |

```
open class ArcMotion : PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.transition.PathMotion](PathMotion.md) ||
| | ↳ | [android.transition.ArcMotion](ArcMotion.md) |

A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. If the horizontal distance between the points is less than the vertical distance, then the circle's center point will be horizontally aligned with the end point. If the vertical distance is less than the horizontal distance then the circle's center point will be vertically aligned with the end point.

When the two points are near horizontal or vertical, the curve of the motion will be small as the center of the circle will be far from both points. To force curvature of the path, [setMinimumHorizontalAngle(float)](ArcMotion.md))and [setMinimumVerticalAngle(float)](ArcMotion.md))may be used to set the minimum angle of the arc between two points.

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
| [ArcMotion](ArcMotion.md))`()` <br /> |
| [ArcMotion](ArcMotion.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMaximumAngle](ArcMotion.md))`()` Returns the maximum arc along the circle between two points. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinimumHorizontalAngle](ArcMotion.md))`()` Returns the minimum arc along the circle between two points aligned near horizontally. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getMinimumVerticalAngle](ArcMotion.md))`()` Returns the minimum arc along the circle between two points aligned near vertically. |
| --- | --- |
| open [Path](../android.graphics/Path.md)! | [getPath](ArcMotion.md))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumAngle](ArcMotion.md))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the maximum arc along the circle between two points. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumHorizontalAngle](ArcMotion.md))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the minimum arc along the circle between two points aligned near horizontally. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumVerticalAngle](ArcMotion.md))`(`angleInDegrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the minimum arc along the circle between two points aligned near vertically. |

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
| --- | --- |
| `endY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the ending point. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](../android.graphics/Path.md)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](../android.graphics/Path.md))and end at`(endX, endY)`. |

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
