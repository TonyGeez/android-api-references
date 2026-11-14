Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SidePropagation

Kotlin | [Java](SidePropagation.md)
| --- | --- |

```
open class SidePropagation : VisibilityPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.transition.TransitionPropagation](TransitionPropagation.md) |||
| | ↳ | [android.transition.VisibilityPropagation](VisibilityPropagation.md) ||
| | | ↳ | [android.transition.SidePropagation](SidePropagation.md) |
| --- | --- | --- | --- |

A `TransitionPropagation` that propagates based on the distance to the side and, orthogonally, the distance to epicenter. If the transitioning View is visible in the start of the transition, then it will transition sooner when closer to the side and later when farther. If the view is not visible in the start of the transition, then it will transition later when closer to the side and sooner when farther from the edge. This is the default TransitionPropagation used with Slide.

## Summary

| Public constructors ||
|---|---|
| SidePropagation <br /> |

| Public methods ||
|---|---|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getStartDelay Called by Transition to alter the Animator start delay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPropagationSpeed Sets the speed at which transition propagation happens, relative to the duration of the Transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSide Sets the side that is used to calculate the transition propagation. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class VisibilityPropagation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | captureValues Captures the values in the start or end scene for the properties that this transition propagation monitors. These values are then passed as the startValues or endValues structure in a later call to getStartDelay. The main concern for an implementation is what the properties are that the transition cares about and what the values are for all of those properties. The start and end values will be compared later during the getStartDelay. method to determine the start delay. Subclasses must implement this method. The method should only be called by the transition system; it is not intended to be called from external classes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | getPropagationProperties Returns the set of property names stored in the TransitionValues object passed into captureValues that this transition propagation cares about for the purposes of preventing duplicate capturing of property values. A `TransitionPropagation` must override this method to prevent duplicate capturing of values and must contain at least one <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getViewVisibility Returns getVisibility for the View at the time the values were captured. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getViewX Returns the View's center x coordinate, relative to the screen, at the time the values were captured. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getViewY Returns the View's center y coordinate, relative to the screen, at the time the values were captured. <br /> | ||
| From class TransitionPropagation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getStartDelay Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero. <br /> | ||

## Public constructors

### SidePropagation

```
SidePropagation()
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

Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero.

| Parameters ||
|---|---|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!: The root of the View hierarchy running the transition. |
| `transition` | [Transition](Transition.md)!: The transition that created the Animator |
| `startValues` | [TransitionValues](TransitionValues.md)!: The values for a specific target in the start scene. |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!: The values for the target in the end scene. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | A start delay to use with the Animator created by `transition`. The delay will be offset by the minimum delay of all `TransitionPropagation`s used in the Transition so that the smallest delay will be 0. Returned values may be negative. |

### setPropagationSpeed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPropagationSpeed(propagationSpeed: Float): Unit
```

Sets the speed at which transition propagation happens, relative to the duration of the Transition. A `propagationSpeed` of 1 means that a View centered at the side set in setSide and View centered at the opposite edge will have a difference in start delay of approximately the duration of the Transition. A speed of 2 means the start delay difference will be approximately half of the duration of the transition. A value of 0 is illegal, but negative values will invert the propagation.

| Parameters ||
|---|---|
| `propagationSpeed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The speed at which propagation occurs, relative to the duration of the transition. A speed of 4 means it works 4 times as fast as the duration of the transition. May not be 0. |

### setSide

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSide(side: Int): Unit
```

Sets the side that is used to calculate the transition propagation. If the transitioning View is visible in the start of the transition, then it will transition sooner when closer to the side and later when farther. If the view is not visible in the start of the transition, then it will transition later when closer to the side and sooner when farther from the edge. The default is `https://developer.android.com/reference/kotlin/android/view/Gravity.html#BOTTOM:kotlin.Int`.

| Parameters ||
|---|---|
| `side` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The side that is used to calculate the transition propagation. Must be one of `https://developer.android.com/reference/kotlin/android/view/Gravity.html#LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Gravity.html#TOP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Gravity.html#RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Gravity.html#BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/Gravity.html#START:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/Gravity.html#END:kotlin.Int`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#LEFT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#RIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#START:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/Gravity.html#END:kotlin.Int` |
