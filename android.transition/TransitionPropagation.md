# TransitionPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionPropagation

Kotlin| [Java](TransitionPropagation.md) 
| --- | --- |

```
abstract class TransitionPropagation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.TransitionPropagation](TransitionPropagation.md) |

| Known Direct Subclasses [VisibilityPropagation](VisibilityPropagation.md) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------| | [VisibilityPropagation](VisibilityPropagation.md) | Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CircularPropagation](CircularPropagation.md), [SidePropagation](SidePropagation.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [CircularPropagation](CircularPropagation.md) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. | | [SidePropagation](SidePropagation.md) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Extend`TransitionPropagation`to customize start delays for Animators created in [android.transition.Transition#createAnimator(ViewGroup, * TransitionValues, TransitionValues)](Transition.md)). A Transition such as [android.transition.Explode](Explode.md) defaults to using [android.transition.CircularPropagation](CircularPropagation.md) and Views closer to the epicenter will move out of the scene later and into the scene sooner than Views farther from the epicenter, giving the appearance of inertia. With no TransitionPropagation, all Views will react simultaneously to the start of the transition.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransitionPropagation](TransitionPropagation.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [captureValues](TransitionPropagation.md))`(`transitionValues:` ` [TransitionValues](TransitionValues.md)!`)` Captures the values in the start or end scene for the properties that this transition propagation monitors. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPropagationProperties](TransitionPropagation.md))`()` Returns the set of property names stored in the [TransitionValues](TransitionValues.md) object passed into [captureValues(android.transition.TransitionValues)](TransitionPropagation.md))that this transition propagation cares about for the purposes of preventing duplicate capturing of property values. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](TransitionPropagation.md))`(`sceneRoot:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `transition:` ` [Transition](Transition.md)!`, `startValues:` ` [TransitionValues](TransitionValues.md)!`, `endValues:` ` [TransitionValues](TransitionValues.md)!`)` Called by Transition to alter the Animator start delay. |
| --- | --- |

## Public constructors

### TransitionPropagation

```
TransitionPropagation()
```

## Public methods

### captureValues

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun captureValues(transitionValues: TransitionValues!): Unit
```

Captures the values in the start or end scene for the properties that this transition propagation monitors. These values are then passed as the startValues or endValues structure in a later call to [getStartDelay(android.view.ViewGroup,android.transition.Transition,android.transition.TransitionValues,android.transition.TransitionValues)](TransitionPropagation.md)). The main concern for an implementation is what the properties are that the transition cares about and what the values are for all of those properties. The start and end values will be compared later during the [getStartDelay(android.view.ViewGroup,android.transition.Transition,android.transition.TransitionValues,android.transition.TransitionValues)](TransitionPropagation.md)). method to determine the start delay.

Subclasses must implement this method. The method should only be called by the transition system; it is not intended to be called from external classes.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionValues` | [TransitionValues](TransitionValues.md)!:The holder for any values that the Transition wishes to store. Values are stored in the`values`field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call`transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

### getPropagationProperties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPropagationProperties(): Array<String!>!
```

Returns the set of property names stored in the [TransitionValues](TransitionValues.md) object passed into [captureValues(android.transition.TransitionValues)](TransitionPropagation.md))that this transition propagation cares about for the purposes of preventing duplicate capturing of property values.

A`TransitionPropagation`must override this method to prevent duplicate capturing of values and must contain at least one

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of property names as described in the class documentation for [TransitionValues](TransitionValues.md). |

### getStartDelay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStartDelay(
    sceneRoot: ViewGroup!, 
    transition: Transition!, 
    startValues: TransitionValues!, 
    endValues: TransitionValues!
): Long
```

Called by Transition to alter the Animator start delay. All start delays will be adjusted such that the minimum becomes zero.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sceneRoot` | [ViewGroup](../android.view/ViewGroup.md)!:The root of the View hierarchy running the transition. |
| `transition` | [Transition](Transition.md)!:The transition that created the Animator |
| `startValues` | [TransitionValues](TransitionValues.md)!:The values for a specific target in the start scene. |
| --- | --- |
| `endValues` | [TransitionValues](TransitionValues.md)!:The values for the target in the end scene. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A start delay to use with the Animator created by`transition`. The delay will be offset by the minimum delay of all`TransitionPropagation`s used in the Transition so that the smallest delay will be 0. Returned values may be negative. |
