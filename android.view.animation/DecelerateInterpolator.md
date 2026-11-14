# DecelerateInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecelerateInterpolator

Kotlin| [Java](DecelerateInterpolator.md) 
| --- | --- |

```
open class DecelerateInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](BaseInterpolator.md) ||
| | ↳ | [android.view.animation.DecelerateInterpolator](DecelerateInterpolator.md) |

An interpolator where the rate of change starts out quickly and and then decelerates.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DecelerateInterpolator](DecelerateInterpolator.md))`()` <br /> |
| [DecelerateInterpolator](DecelerateInterpolator.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |
| [DecelerateInterpolator](DecelerateInterpolator.md))`(`factor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](DecelerateInterpolator.md))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

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
