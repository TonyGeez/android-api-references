# PathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMotion

Kotlin| [Java](../android/transition/PathMotion.md) 
| --- | --- |

```
abstract class PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.PathMotion](../android/transition/PathMotion.md) |

| Known Direct Subclasses [ArcMotion](../android/transition/ArcMotion.md), [PatternPathMotion](../android/transition/PatternPathMotion.md) |----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------| | [ArcMotion](../android/transition/ArcMotion.md) | A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. | | [PatternPathMotion](../android/transition/PatternPathMotion.md) | A PathMotion that takes a Path pattern and applies it to the separation between two points. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This base class can be extended to provide motion along a Path to Transitions.

Transitions such as [android.transition.ChangeBounds](../android/transition/ChangeBounds.md) move Views, typically in a straight path between the start and end positions. Applications that desire to have these motions move in a curve can change how Views interpolate in two dimensions by extending PathMotion and implementing [getPath(float,float,float,float)](../android/transition/PathMotion.md)).

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
| [PathMotion](../android/transition/PathMotion.md))`()` <br /> |
| [PathMotion](../android/transition/PathMotion.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Path](../android/graphics/Path.md)! | [getPath](../android/transition/PathMotion.md))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Provide a Path to interpolate between two points`(startX, startY)`and`(endX, endY)`. |

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
| [Path](../android/graphics/Path.md)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](../android/graphics/Path.md))and end at`(endX, endY)`. |
