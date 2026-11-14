# CircularPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CircularPropagation

Kotlin| [Java](https://developer.android.com/reference/android/transition/CircularPropagation "View this page in Java") 
| --- | --- |

```
open class CircularPropagation : VisibilityPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.transition.TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation) |||
| | ↳ | [android.transition.VisibilityPropagation](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation) ||
| | | ↳ | [android.transition.CircularPropagation](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation#) |
| --- | --- | --- | --- |

A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. When a View is visible in the start of the transition, Views farther from the epicenter will transition sooner than Views closer to the epicenter. When a View is not in the start of the transition or is not visible at the start of the transition, it will transition sooner when closer to the epicenter and later when farther from the epicenter. This is the default TransitionPropagation used with [android.transition.Explode](https://developer.android.com/reference/kotlin/android/transition/Explode).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CircularPropagation](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation#CircularPropagation())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation#getStartDelay(android.view.ViewGroup,%20android.transition.Transition,%20android.transition.TransitionValues,%20android.transition.TransitionValues))`(`sceneRoot:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`, `startValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`, `endValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropagationSpeed](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation#setPropagationSpeed(kotlin.Float))`(`propagationSpeed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the speed at which transition propagation happens, relative to the duration of the Transition. |

| Inherited functions ||
|---|---|
| From class [VisibilityPropagation](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureValues](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#captureValues(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPropagationProperties](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getPropagationProperties())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewVisibility](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewVisibility(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> Returns [android.view.View#getVisibility()](https://developer.android.com/reference/kotlin/android/view/View.html#getVisibility())for the View at the time the values were captured. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewX](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewX(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> Returns the View's center x coordinate, relative to the screen, at the time the values were captured. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewY](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewY(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> Returns the View's center y coordinate, relative to the screen, at the time the values were captured. <br /> | ||
| From class [TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation#getStartDelay(android.view.ViewGroup,%20android.transition.Transition,%20android.transition.TransitionValues,%20android.transition.TransitionValues))`(`sceneRoot:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`, `startValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`, `endValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero. <br /> | ||

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
| `sceneRoot` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The root of the View hierarchy running the transition. |
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The transition that created the Animator |
| `startValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!:The values for a specific target in the start scene. |
| --- | --- |
| `endValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!:The values for the target in the end scene. |

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
