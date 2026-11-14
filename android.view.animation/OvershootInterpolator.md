# OvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OvershootInterpolator

Kotlin| [Java](OvershootInterpolator.md) 
| --- | --- |

```
open class OvershootInterpolator : BaseInterpolator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.BaseInterpolator](BaseInterpolator.md) ||
| | ↳ | [android.view.animation.OvershootInterpolator](OvershootInterpolator.md) |

An interpolator where the change flings forward and overshoots the last value then comes back.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OvershootInterpolator](OvershootInterpolator.md))`()` <br /> |
| [OvershootInterpolator](OvershootInterpolator.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |
| [OvershootInterpolator](OvershootInterpolator.md))`(`tension:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getInterpolation](OvershootInterpolator.md))`(`t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |

## Public constructors

### OvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OvershootInterpolator()
```  

### OvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OvershootInterpolator(
    context: Context!, 
    attrs: AttributeSet!)
```  

### OvershootInterpolator

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OvershootInterpolator(tension: Float)
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tension` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Amount of overshoot. When tension equals 0.0f, there is no overshoot and the interpolator becomes a simple deceleration interpolator. |

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
