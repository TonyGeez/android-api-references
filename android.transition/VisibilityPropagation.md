# VisibilityPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibilityPropagation

Kotlin| [Java](../android/transition/VisibilityPropagation.md) 
| --- | --- |

```
abstract class VisibilityPropagation : TransitionPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.transition.TransitionPropagation](../android/transition/TransitionPropagation.md) ||
| | ↳ | [android.transition.VisibilityPropagation](../android/transition/VisibilityPropagation.md) |

| Known Direct Subclasses [CircularPropagation](../android/transition/CircularPropagation.md), [SidePropagation](../android/transition/SidePropagation.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [CircularPropagation](../android/transition/CircularPropagation.md) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. | | [SidePropagation](../android/transition/SidePropagation.md) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VisibilityPropagation](../android/transition/VisibilityPropagation.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureValues](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPropagationProperties](../android/transition/VisibilityPropagation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewVisibility](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` Returns [android.view.View#getVisibility()](../android/view/View.md))for the View at the time the values were captured. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewX](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` Returns the View's center x coordinate, relative to the screen, at the time the values were captured. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getViewY](../android/transition/VisibilityPropagation.md))`(`values:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` Returns the View's center y coordinate, relative to the screen, at the time the values were captured. |

| Inherited functions ||
|---|---|
| From class [TransitionPropagation](../android/transition/TransitionPropagation.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](../android/transition/TransitionPropagation.md))`(`sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`, `transition:` ` [Transition](../android/transition/Transition.md)!`, `startValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`, `endValues:` ` [TransitionValues](../android/transition/TransitionValues.md)!`)` <br /> Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero. <br /> | ||

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of property names as described in the class documentation for [TransitionValues](../android/transition/TransitionValues.md). |

### getViewVisibility

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewVisibility(values: TransitionValues!): Int
```

Returns [android.view.View#getVisibility()](../android/view/View.md))for the View at the time the values were captured.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](../android/transition/TransitionValues.md)!:The TransitionValues captured at the start or end of the Transition. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [android.view.View#getVisibility()](../android/view/View.md))for the View at the time the values were captured. |

### getViewX

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewX(values: TransitionValues!): Int
```

Returns the View's center x coordinate, relative to the screen, at the time the values were captured.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [TransitionValues](../android/transition/TransitionValues.md)!:The TransitionValues captured at the start or end of the Transition. |

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
| `values` | [TransitionValues](../android/transition/TransitionValues.md)!:The TransitionValues captured at the start or end of the Transition. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the View's center y coordinate, relative to the screen, at the time the values were captured. |
