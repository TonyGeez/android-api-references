# AccelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccelerateInterpolator

Kotlin| [Java](../android/view/animation/AccelerateInterpolator.md) 
| --- | --- |

```
open class AccelerateInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](../android/view/animation/BaseInterpolator.md) ||
| | ↳ | [android.view.animation.AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md) |

An interpolator where the rate of change starts out slowly and and then accelerates.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md))`()` <br /> |
| [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` <br /> |
| [AccelerateInterpolator](../android/view/animation/AccelerateInterpolator.md))`(`factor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](../android/view/animation/AccelerateInterpolator.md))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

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
