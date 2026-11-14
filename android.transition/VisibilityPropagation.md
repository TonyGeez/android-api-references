# VisibilityPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibilityPropagation

Kotlin| [Java](https://developer.android.com/reference/android/transition/VisibilityPropagation "View this page in Java") 

```
abstract class VisibilityPropagation : TransitionPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.transition.TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation) ||
| | ↳ | [android.transition.VisibilityPropagation](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#) |

| Known Direct Subclasses [CircularPropagation](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation), [SidePropagation](https://developer.android.com/reference/kotlin/android/transition/SidePropagation) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [CircularPropagation](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. | | [SidePropagation](https://developer.android.com/reference/kotlin/android/transition/SidePropagation) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. | |

Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VisibilityPropagation](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#VisibilityPropagation())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureValues](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#captureValues(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPropagationProperties](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getPropagationProperties())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewVisibility](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewVisibility(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` Returns [android.view.View#getVisibility()](https://developer.android.com/reference/kotlin/android/view/View.html#getVisibility())for the View at the time the values were captured. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewX](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewX(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` Returns the View's center x coordinate, relative to the screen, at the time the values were captured. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewY](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation#getViewY(android.transition.TransitionValues))`(`values:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` Returns the View's center y coordinate, relative to the screen, at the time the values were captured. |

| Inherited functions ||
|---|---|
| From class [TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation#getStartDelay(android.view.ViewGroup,%20android.transition.Transition,%20android.transition.TransitionValues,%20android.transition.TransitionValues))`(`sceneRoot:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`, `startValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`, `endValues:` ` [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!`)` <br /> Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero. <br /> | ||

## Public constructors

### VisibilityPropagation

```
VisibilityPropagation()
```

## Public methods

### captureValues

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun captureValues(values: TransitionValues!): Unit
```

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionValues` | The holder for any values that the Transition wishes to store. Values are stored in the`values`field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call`transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

### getPropagationProperties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropagationProperties(): Array<String!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of property names as described in the class documentation for [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues). |

### getViewVisibility

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewVisibility(values: TransitionValues!): Int
```

Returns [android.view.View#getVisibility()](https://developer.android.com/reference/kotlin/android/view/View.html#getVisibility())for the View at the time the values were captured.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!:The TransitionValues captured at the start or end of the Transition. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [android.view.View#getVisibility()](https://developer.android.com/reference/kotlin/android/view/View.html#getVisibility())for the View at the time the values were captured. |

### getViewX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewX(values: TransitionValues!): Int
```

Returns the View's center x coordinate, relative to the screen, at the time the values were captured.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!:The TransitionValues captured at the start or end of the Transition. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the View's center x coordinate, relative to the screen, at the time the values were captured. |

### getViewY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewY(values: TransitionValues!): Int
```

Returns the View's center y coordinate, relative to the screen, at the time the values were captured.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!:The TransitionValues captured at the start or end of the Transition. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the View's center y coordinate, relative to the screen, at the time the values were captured. |
