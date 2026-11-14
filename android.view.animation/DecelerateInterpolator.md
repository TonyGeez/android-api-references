# DecelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecelerateInterpolator

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/DecelerateInterpolator "View this page in Java") 
| --- | --- |

```
open class DecelerateInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/BaseInterpolator) ||
| | ↳ | [android.view.animation.DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator#) |

An interpolator where the rate of change starts out quickly and and then decelerates.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator#DecelerateInterpolator())`()` <br /> |
| [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator#DecelerateInterpolator(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` <br /> |
| [DecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator#DecelerateInterpolator(kotlin.Float))`(`factor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](https://developer.android.com/reference/kotlin/android/view/animation/DecelerateInterpolator#getInterpolation(kotlin.Float))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### DecelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecelerateInterpolator()
```  

### DecelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecelerateInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### DecelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecelerateInterpolator(factor: Float)
```

Constructor

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Degree to which the animation should be eased. Setting factor to 1.0f produces an upside-down y=x\^2 parabola. Increasing factor above 1.0f exaggerates the ease-out effect (i.e., it starts even faster and ends evens slower). |

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
