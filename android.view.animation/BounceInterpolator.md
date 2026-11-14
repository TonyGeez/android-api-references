# BounceInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BounceInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/BounceInterpolator "View this page in Java") 
| --- | --- |

```
open class BounceInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator) ||
| | ↳ | [android.view.animation.BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator#) |

An interpolator where the change bounces at the end.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator#BounceInterpolator())`()` <br /> |
| [BounceInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator#BounceInterpolator(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/view/animation/BounceInterpolator#getInterpolation(kotlin.Float))`(`t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### BounceInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BounceInterpolator()
```  

### BounceInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BounceInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```

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
