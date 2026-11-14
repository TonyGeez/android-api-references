# AccelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccelerateInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/AccelerateInterpolator "View this page in Java") 

```
open class AccelerateInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator) ||
| | ↳ | [android.view.animation.AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator#) |

An interpolator where the rate of change starts out slowly and and then accelerates.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator#AccelerateInterpolator())`()` <br /> |
| [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator#AccelerateInterpolator(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |
| [AccelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator#AccelerateInterpolator(kotlin.Float))`(`factor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateInterpolator#getInterpolation(kotlin.Float))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### AccelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccelerateInterpolator()
```  

### AccelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccelerateInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### AccelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccelerateInterpolator(factor: Float)
```

Constructor

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Degree to which the animation should be eased. Seting factor to 1.0f produces a y=x\^2 parabola. Increasing factor above 1.0f exaggerates the ease-in effect (i.e., it starts even slower and ends evens faster) |

## Public methods

### getInterpolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolation(input: Float): Float
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A value between 0 and 1.0 indicating our current point in the animation where 0 represents the start and 1.0 represents the end |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The interpolation value. This value can be more than 1.0 for interpolators which overshoot their targets, or less than 0 for interpolators that undershoot their targets. |
