# PathInterpolator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/PathInterpolator "View this page in Java") 

```
open class PathInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator) ||
| | ↳ | [android.view.animation.PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#) |

An interpolator that can traverse a Path that extends from`Point``(0, 0)`to`(1, 1)`. The x coordinate along the`Path`is the input value and the output is the y coordinate of the line at that point. This means that the Path must conform to a function`y = f(x)`.

The`Path`must not have gaps in the x direction and must not loop back on itself such that there can be two points sharing the same x coordinate. It is alright to have a disjoint line in the vertical direction:

<br />

```kotlin
Path path = new Path();
      path.lineTo(0.25f, 0.25f);
      path.moveTo(0.25f, 0.5f);
      path.lineTo(1f, 1f);
  
```

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#PathInterpolator(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |
| [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#PathInterpolator(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)`)` Create an interpolator for an arbitrary`Path`. |
| [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#PathInterpolator(kotlin.Float,%20kotlin.Float))`(`controlX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `controlY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Create an interpolator for a quadratic Bezier curve. |
| [PathInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#PathInterpolator(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`controlX1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `controlY1:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `controlX2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `controlY2:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Create an interpolator for a cubic Bezier curve. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/view/animation/PathInterpolator#getInterpolation(kotlin.Float))`(`t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Using the line in the Path in this interpolator that can be described as`y = f(x)`, finds the y coordinate of the line given`t`as the x coordinate. |

## Public constructors

### PathInterpolator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### PathInterpolator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathInterpolator(path: Path)
```

Create an interpolator for an arbitrary`Path`. The`Path`must begin at`(0, 0)`and end at`(1, 1)`.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#):The`Path`to use to make the line representing the interpolator. This value cannot be`null`. |

### PathInterpolator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathInterpolator(
    controlX: Float, 
    controlY: Float)
```

Create an interpolator for a quadratic Bezier curve. The end points`(0, 0)`and`(1, 1)`are assumed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `controlX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the quadratic Bezier control point. |
| `controlY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the quadratic Bezier control point. |

### PathInterpolator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathInterpolator(
    controlX1: Float, 
    controlY1: Float, 
    controlX2: Float, 
    controlY2: Float)
```

Create an interpolator for a cubic Bezier curve. The end points`(0, 0)`and`(1, 1)`are assumed.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `controlX1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the first control point of the cubic Bezier. |
| `controlY1` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the first control point of the cubic Bezier. |
| `controlX2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the second control point of the cubic Bezier. |
| `controlY2` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the second control point of the cubic Bezier. |

## Public methods

### getInterpolation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolation(t: Float): Float
```

Using the line in the Path in this interpolator that can be described as`y = f(x)`, finds the y coordinate of the line given`t`as the x coordinate. Values less than 0 will always return 0 and values greater than 1 will always return 1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `input` | A value between 0 and 1.0 indicating our current point in the animation where 0 represents the start and 1.0 represents the end |
| `t` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Treated as the x coordinate along the line. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The y coordinate of the Path along the line where x =`t`. |

**See Also**

- [android.view.animation.Interpolator#getInterpolation(float)](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#getInterpolation(kotlin.Float))
