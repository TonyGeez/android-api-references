# PatternPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PatternPathMotion

Kotlin| [Java](../android/transition/PatternPathMotion.md) 
| --- | --- |

```
open class PatternPathMotion : PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.transition.PathMotion](../android/transition/PathMotion.md) ||
| | ↳ | [android.transition.PatternPathMotion](../android/transition/PatternPathMotion.md) |

A PathMotion that takes a Path pattern and applies it to the separation between two points. The starting point of the Path will be moved to the origin and the end point will be scaled and rotated so that it matches with the target end point.

This may be used in XML as an element inside a transition. 

```kotlin
<code>&lt;changeBounds&gt;
      &lt;patternPathMotion android:patternPathData="M0 0 L0 100 L100 100"/&gt;
  &lt;/changeBounds&gt;</code>
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PatternPathMotion](../android/transition/PatternPathMotion.md))`()` Constructs a PatternPathMotion with a straight-line pattern. |
| [PatternPathMotion](../android/transition/PatternPathMotion.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` <br /> |
| [PatternPathMotion](../android/transition/PatternPathMotion.md))`(`patternPath:` ` [Path](../android/graphics/Path.md)!`)` Creates a PatternPathMotion with the Path defining a pattern of motion between two coordinates. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Path](../android/graphics/Path.md)! | [getPath](../android/transition/PatternPathMotion.md))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Path](../android/graphics/Path.md)! | [getPatternPath](../android/transition/PatternPathMotion.md))`()` Returns the Path defining a pattern of motion between two coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternPath](../android/transition/PatternPathMotion.md))`(`patternPath:` ` [Path](../android/graphics/Path.md)!`)` Sets the Path defining a pattern of motion between two coordinates. |
| --- | --- |

## Public constructors

### PatternPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PatternPathMotion()
```

Constructs a PatternPathMotion with a straight-line pattern. 

### PatternPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PatternPathMotion(
    context: Context!, 
    attrs: AttributeSet!)
```  

### PatternPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PatternPathMotion(patternPath: Path!)
```

Creates a PatternPathMotion with the Path defining a pattern of motion between two coordinates. The pattern will be translated, rotated, and scaled to fit between the start and end points. The pattern must not be empty and must have the end point differ from the start point.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `patternPath` | [Path](../android/graphics/Path.md)!:A Path to be used as a pattern for two-dimensional motion. |

## Public methods

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
| [Path](../android/graphics/Path.md)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](../android/graphics/Path.md))and end at`(endX, endY)`. |

### getPatternPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPatternPath(): Path!
```

Returns the Path defining a pattern of motion between two coordinates. The pattern will be translated, rotated, and scaled to fit between the start and end points. The pattern must not be empty and must have the end point differ from the start point.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Path](../android/graphics/Path.md)! | the Path defining a pattern of motion between two coordinates. |

### setPatternPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPatternPath(patternPath: Path!): Unit
```

Sets the Path defining a pattern of motion between two coordinates. The pattern will be translated, rotated, and scaled to fit between the start and end points. The pattern must not be empty and must have the end point differ from the start point.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `patternPath` | [Path](../android/graphics/Path.md)!:A Path to be used as a pattern for two-dimensional motion. |
