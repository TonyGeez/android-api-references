# StateListAnimator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StateListAnimator

Kotlin| [Java](../android/animation/StateListAnimator.md) 
| --- | --- |

```
open class StateListAnimator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.StateListAnimator](../android/animation/StateListAnimator.md) |

Lets you define a number of Animators that will run on the attached View depending on the View's drawable state.

It can be defined in an XML file with the`<selector>`element. Each State Animator is defined in a nested`<item>`element.

## Summary

| XML attributes ||
|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:animation`](../android/animation/StateListAnimator.md) | Animation to use on each child. |
| [`android:state_activated`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. |
| [`android:state_active`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or drawable is considered "active" by its host. |
| --- | --- |
| [`android:state_checkable`](../android/animation/StateListAnimator.md) | State identifier indicating that the object may display a check mark. |
| [`android:state_checked`](../android/animation/StateListAnimator.md) | State identifier indicating that the object is currently checked. |
| [`android:state_enabled`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view is enabled. |
| --- | --- |
| [`android:state_first`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or drawable is in the first position in an ordered set. |
| [`android:state_focused`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view has input focus. |
| [`android:state_last`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or drawable is in the last position in an ordered set. |
| --- | --- |
| [`android:state_middle`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or drawable is in the middle position in an ordered set. |
| [`android:state_pressed`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when the user is pressing down in a view. |
| [`android:state_selected`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view (or one of its parents) is currently selected. |
| --- | --- |
| [`android:state_single`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view or drawable is considered "single" by its host. |
| [`android:state_window_focused`](../android/animation/StateListAnimator.md) | State value for StateListDrawable , set when a view's window has input focus. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [StateListAnimator](../android/animation/StateListAnimator.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addState](../android/animation/StateListAnimator.md))`(`specs:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `animator:` ` [Animator](../android/animation/Animator.md)!`)` Associates the given animator with the provided drawable state specs so that it will be run when the View's drawable state matches the specs. |
| open [StateListAnimator](../android/animation/StateListAnimator.md) | [clone](../android/animation/StateListAnimator.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [jumpToCurrentState](../android/animation/StateListAnimator.md))`()` If there is an animation running for a recent state change, ends it. |
| --- | --- |

## XML attributes

### android:animation

```
android:animation
```
Animation to use on each child.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:state_activated

```
android:state_activated
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or its parent has been "activated" meaning the user has currently marked it as being of interest. This is an alternative representation of state_checked for when the state should be propagated down the view hierarchy.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_active

```
android:state_active
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "active" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_checkable

```
android:state_checkable
```
State identifier indicating that the object may display a check mark. See [android.R.attr#state_checked](../android/R.attr.md) for the identifier that indicates whether it is actually checked.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_checked

```
android:state_checked
```
State identifier indicating that the object is currently checked. See [android.R.attr#state_checkable](../android/R.attr.md) for an additional identifier that can indicate if any object may ever display a check, regardless of whether state_checked is currently set.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_enabled

```
android:state_enabled
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view is enabled.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_first

```
android:state_first
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the first position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_focused

```
android:state_focused
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view has input focus.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_last

```
android:state_last
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the last position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_middle

```
android:state_middle
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is in the middle position in an ordered set. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_pressed

```
android:state_pressed
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when the user is pressing down in a view.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_selected

```
android:state_selected
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view (or one of its parents) is currently selected.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_single

```
android:state_single
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view or drawable is considered "single" by its host. Actual usage may vary between views. Consult the host view documentation for details.

May be a boolean value, such as "`true`" or "`false`". 

### android:state_window_focused

```
android:state_window_focused
```
State value for [StateListDrawable](../android/graphics/drawable/StateListDrawable.md), set when a view's window has input focus.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### StateListAnimator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StateListAnimator()
```

## Public methods

### addState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addState(
    specs: IntArray!, 
    animator: Animator!
): Unit
```

Associates the given animator with the provided drawable state specs so that it will be run when the View's drawable state matches the specs.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------|
| `specs` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The drawable state specs to match against |
| `animator` | [Animator](../android/animation/Animator.md)!:The animator to run when the specs match |

### clone

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): StateListAnimator
```

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------|
| [StateListAnimator](../android/animation/StateListAnimator.md) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### jumpToCurrentState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun jumpToCurrentState(): Unit
```

If there is an animation running for a recent state change, ends it.

This causes the animation to assign the end value(s) to the View.
