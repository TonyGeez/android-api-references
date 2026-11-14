# AnticipateInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnticipateInterpolator

Kotlin | [Java](https://developer.android.com/reference/android/view/animation/AnticipateInterpolator "View this page in Java") 
| --- | --- |

```
open class AnticipateInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator) ||
| | ↳ | [android.view.animation.AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator#) |

An interpolator where the change starts backward then flings forward.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator#AnticipateInterpolator())`()` <br /> |
| [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator#AnticipateInterpolator(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |
| [AnticipateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator#AnticipateInterpolator(kotlin.Float))`(`tension:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/view/animation/AnticipateInterpolator#getInterpolation(kotlin.Float))`(`t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### AnticipateInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnticipateInterpolator()
```  

### AnticipateInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnticipateInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### AnticipateInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AnticipateInterpolator(tension: Float)
```

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tension` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Amount of anticipation. When tension equals 0.0f, there is no anticipation and the interpolator becomes a simple acceleration interpolator. |

## Public methods

### getInterpolation

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolation(t: Float): Float
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `input` | A value between 0 and 1.0 indicating our current point in the animation where 0 represents the start and 1.0 represents the end |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The interpolation value. This value can be more than 1.0 for interpolators which overshoot their targets, or less than 0 for interpolators that undershoot their targets. |
