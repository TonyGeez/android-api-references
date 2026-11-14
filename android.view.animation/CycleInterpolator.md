# CycleInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CycleInterpolator

Kotlin| [Java](CycleInterpolator.md) 
| --- | --- |

```
open class CycleInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](BaseInterpolator.md) ||
| | ↳ | [android.view.animation.CycleInterpolator](CycleInterpolator.md) |

Repeats the animation for a specified number of cycles. The rate of change follows a sinusoidal pattern.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CycleInterpolator](CycleInterpolator.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |
| [CycleInterpolator](CycleInterpolator.md))`(`cycles:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](CycleInterpolator.md))`(`input:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### CycleInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CycleInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### CycleInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CycleInterpolator(cycles: Float)
```

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
