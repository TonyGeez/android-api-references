# PatternPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PatternPathMotion

Kotlin| [Java](https://developer.android.com/reference/android/transition/PatternPathMotion "View this page in Java") 
| --- | --- |

```
open class PatternPathMotion : PathMotion
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.transition.PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion) ||
| | ↳ | [android.transition.PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#) |

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
| [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#PatternPathMotion())`()` Constructs a PatternPathMotion with a straight-line pattern. |
| [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#PatternPathMotion(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |
| [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#PatternPathMotion(android.graphics.Path))`(`patternPath:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Creates a PatternPathMotion with the Path defining a pattern of motion between two coordinates. |

| Public methods ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [getPath](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#getPath(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`startX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `startY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [getPatternPath](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#getPatternPath())`()` Returns the Path defining a pattern of motion between two coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternPath](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion#setPatternPath(android.graphics.Path))`(`patternPath:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Sets the Path defining a pattern of motion between two coordinates. |
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
| `patternPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:A Path to be used as a pattern for two-dimensional motion. |

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
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | A Path along which the points should be interpolated. The returned Path must start at point`(startX, startY)`, typically using [android.graphics.Path#moveTo(float, float)](https://developer.android.com/reference/kotlin/android/graphics/Path.html#moveTo(kotlin.Float,%20kotlin.Float))and end at`(endX, endY)`. |

### getPatternPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPatternPath(): Path!
```

Returns the Path defining a pattern of motion between two coordinates. The pattern will be translated, rotated, and scaled to fit between the start and end points. The pattern must not be empty and must have the end point differ from the start point.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | the Path defining a pattern of motion between two coordinates. |

### setPatternPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPatternPath(patternPath: Path!): Unit
```

Sets the Path defining a pattern of motion between two coordinates. The pattern will be translated, rotated, and scaled to fit between the start and end points. The pattern must not be empty and must have the end point differ from the start point.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `patternPath` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:A Path to be used as a pattern for two-dimensional motion. |
