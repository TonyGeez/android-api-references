# CircularPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CircularPropagation

Kotlin| [Java](../android/transition/CircularPropagation.md) 
| --- | --- |

```
open class CircularPropagation : VisibilityPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.transition.TransitionPropagation](../android/transition/TransitionPropagation.md) |||
| | ↳ | [android.transition.VisibilityPropagation](../android/transition/VisibilityPropagation.md) ||
| | | ↳ | [android.transition.CircularPropagation](../android/transition/CircularPropagation.md) |
| --- | --- | --- | --- |

A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. When a View is visible in the start of the transition, Views farther from the epicenter will transition sooner than Views closer to the epicenter. When a View is not in the start of the transition or is not visible at the start of the transition, it will transition sooner when closer to the epicenter and later when farther from the epicenter. This is the default TransitionPropagation used with [android.transition.Explode](../android/transition/Explode.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CircularPropagation](../android/transition/CircularPropagation.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](../android/transition/CircularPropagation.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `transition:` ` [Transition](../android/transition/Transition.md)!`, `startValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`, `endValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropagationSpeed](../android/transition/CircularPropagation.md))`(`propagationSpeed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speed at which transition propagation happens, relative to the duration of the Transition. |

| Inherited functions ||
|---|---|
| From class [VisibilityPropagation](../android/transition/VisibilityPropagation.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureValues](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPropagationProperties](../android/transition/VisibilityPropagation.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewVisibility](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> Returns [android.view.View#getVisibility()](../android/view/View.md))for the View at the time the values were captured. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewX](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> Returns the View's center x coordinate, relative to the screen, at the time the values were captured. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewY](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> Returns the View's center y coordinate, relative to the screen, at the time the values were captured. <br /> | ||
| From class [TransitionPropagation](../android/transition/TransitionPropagation.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](../android/transition/TransitionPropagation.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `transition:` ` [Transition](../android/transition/Transition.md)!`, `startValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`, `endValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero. <br /> | ||

## Public constructors

### CircularPropagation

```
CircularPropagation()
```

## Public methods

### getStartDelay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartDelay(
    sceneRoot: ViewGroup!, 
    transition: Transition!, 
    startValues: TransitionValues!, 
    endValues: TransitionValues!
): Long
```

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!:The root of the View hierarchy running the transition. |
| `transition` | [Transition](../android/transition/Transition.md)!:The transition that created the Animator |
| `startValues` | [TransitionValues](../android/transition/TransitionValues.md)!:The values for a specific target in the start scene. |
| --- | --- |
| `endValues` | [TransitionValues](../android/transition/TransitionValues.md)!:The values for the target in the end scene. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A start delay to use with the Animator created by`transition`. The delay will be offset by the minimum delay of all`TransitionPropagation`s used in the Transition so that the smallest delay will be 0. Returned values may be negative. |

### setPropagationSpeed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPropagationSpeed(propagationSpeed: Float): Unit
```

Sets the speed at which transition propagation happens, relative to the duration of the Transition. A`propagationSpeed`of 1 means that a View centered farthest from the epicenter and View centered at the epicenter will have a difference in start delay of approximately the duration of the Transition. A speed of 2 means the start delay difference will be approximately half of the duration of the transition. A value of 0 is illegal, but negative values will invert the propagation.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propagationSpeed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The speed at which propagation occurs, relative to the duration of the transition. A speed of 4 means it works 4 times as fast as the duration of the transition. May not be 0. |
