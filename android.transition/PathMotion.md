# PathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMotion

Kotlin| [Java](https://developer.android.com/reference/android/transition/PathMotion "View this page in Java") 
| --- | --- |

```
abstract class PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion#) |

| Known Direct Subclasses [ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion), [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion) |----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------| | [ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion) | A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. | | [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion) | A PathMotion that takes a Path pattern and applies it to the separation between two points. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This base class can be extended to provide motion along a Path to Transitions.

Transitions such as [android.transition.ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds) move Views, typically in a straight path between the start and end positions. Applications that desire to have these motions move in a curve can change how Views interpolate in two dimensions by extending PathMotion and implementing [getPath(float,float,float,float)](https://developer.android.com/reference/kotlin/android/transition/PathMotion#getPath(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)).

This may be used in XML as an element inside a transition. 

```kotlin
<code>&lt;changeBounds&gt;
      &lt;pathMotion class="my.app.transition.MyPathMotion"/&gt;
  &lt;/changeBounds&gt;
  </code>
```

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion#PathMotion())`()` <br /> |
| [PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion#PathMotion(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [getPath](https://developer.android.com/reference/kotlin/android/transition/PathMotion#getPath(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Provide a Path to interpolate between two points`(startX, startY)`and`(endX, endY)`. |

## Public constructors

### PathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathMotion()
```  

### PathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathMotion(
    context: Context!, 
    attrs: AttributeSet!)
```

## Public methods

### getPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPath(
    startX: Float, 
    startY: Float, 
    endX: Float, 
    endY: Float
): Path!
```

Provide a Path to interpolate between two points`(startX, startY)`and`(endX, endY)`. This allows controlled curved motion along two dimensions.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `startX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the starting point. |
| `startY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the starting point. |
| `endX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the ending point. |
| --- | --- |
| `endY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the ending point. |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](https://developer.android.com/reference/kotlin/android/graphics/Path.html#moveTo(kotlin.Float,%20kotlin.Float))and end at`(endX, endY)`. |
