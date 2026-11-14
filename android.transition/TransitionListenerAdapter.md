# TransitionListenerAdapter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionListenerAdapter

Kotlin| [Java](TransitionListenerAdapter.md) 
| --- | --- |

```
abstract class TransitionListenerAdapter : Transition.TransitionListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.TransitionListenerAdapter](TransitionListenerAdapter.md) |

This adapter class provides empty implementations of the methods from . Any custom listener that cares only about a subset of the methods of this listener can simply subclass this adapter class instead of implementing the interface directly.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransitionListenerAdapter](TransitionListenerAdapter.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionCancel](TransitionListenerAdapter.md))`(`transition:` ` [Transition](Transition.md)!`)` Notification about the cancellation of the transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionEnd](TransitionListenerAdapter.md))`(`transition:` ` [Transition](Transition.md)!`)` Notification about the end of the transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionPause](TransitionListenerAdapter.md))`(`transition:` ` [Transition](Transition.md)!`)` Notification when a transition is paused. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionResume](TransitionListenerAdapter.md))`(`transition:` ` [Transition](Transition.md)!`)` Notification when a transition is resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionStart](TransitionListenerAdapter.md))`(`transition:` ` [Transition](Transition.md)!`)` Notification about the start of the transition. |

## Public constructors

### TransitionListenerAdapter

```
TransitionListenerAdapter()
```

## Public methods

### onTransitionCancel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTransitionCancel(transition: Transition!): Unit
```

Notification about the cancellation of the transition. Note that cancel may be called by a parent [TransitionSet](TransitionSet.md) on a child transition which has not yet started. This allows the child transition to restore state on target objects which was set at [createAnimator()](Transition.md))time.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](Transition.md)!:The transition which was canceled. |

### onTransitionEnd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTransitionEnd(transition: Transition!): Unit
```

Notification about the end of the transition. Canceled transitions will always notify listeners of both the cancellation and end events. That is, [onTransitionEnd(android.transition.Transition)](../android/transition/Transition.TransitionListener.md))is always called, regardless of whether the transition was canceled or played through to completion.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](Transition.md)!:The transition which reached its end. |

### onTransitionPause

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTransitionPause(transition: Transition!): Unit
```

Notification when a transition is paused. Note that createAnimator() may be called by a parent [TransitionSet](TransitionSet.md) on a child transition which has not yet started. This allows the child transition to restore state on target objects which was set at [createAnimator()](Transition.md))time.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](Transition.md)!:The transition which was paused. |

### onTransitionResume

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTransitionResume(transition: Transition!): Unit
```

Notification when a transition is resumed. Note that resume() may be called by a parent [TransitionSet](TransitionSet.md) on a child transition which has not yet started. This allows the child transition to restore state which may have changed in an earlier call to [onTransitionPause(android.transition.Transition)](../android/transition/Transition.TransitionListener.md)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](Transition.md)!:The transition which was resumed. |

### onTransitionStart

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTransitionStart(transition: Transition!): Unit
```

Notification about the start of the transition.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](Transition.md)!:The started transition. |
