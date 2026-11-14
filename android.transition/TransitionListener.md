# Transition.TransitionListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionListener

Kotlin| [Java](https://developer.android.com/reference/android/transition/Transition.TransitionListener "View this page in Java") 

```
interface TransitionListener
```

| [android.transition.Transition.TransitionListener](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#) |

| Known Direct Subclasses [TransitionListenerAdapter](https://developer.android.com/reference/kotlin/android/transition/TransitionListenerAdapter) |--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [TransitionListenerAdapter](https://developer.android.com/reference/kotlin/android/transition/TransitionListenerAdapter) | This adapter class provides empty implementations of the methods from . | |

A transition listener receives notifications from a transition. Notifications indicate transition lifecycle events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionCancel](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionCancel(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`)` Notification about the cancellation of the transition. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionEnd](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionEnd(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`)` Notification about the end of the transition. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionPause](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionPause(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`)` Notification when a transition is paused. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionResume](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionResume(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`)` Notification when a transition is resumed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransitionStart](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionStart(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!`)` Notification about the start of the transition. |

## Public methods

### onTransitionCancel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransitionCancel(transition: Transition!): Unit
```

Notification about the cancellation of the transition. Note that cancel may be called by a parent [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet) on a child transition which has not yet started. This allows the child transition to restore state on target objects which was set at [createAnimator()](https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues))time.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The transition which was canceled. |

### onTransitionEnd

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransitionEnd(transition: Transition!): Unit
```

Notification about the end of the transition. Canceled transitions will always notify listeners of both the cancellation and end events. That is, [onTransitionEnd(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionEnd(android.transition.Transition))is always called, regardless of whether the transition was canceled or played through to completion.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The transition which reached its end. |

### onTransitionPause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransitionPause(transition: Transition!): Unit
```

Notification when a transition is paused. Note that createAnimator() may be called by a parent [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet) on a child transition which has not yet started. This allows the child transition to restore state on target objects which was set at [createAnimator()](https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues))time.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The transition which was paused. |

### onTransitionResume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransitionResume(transition: Transition!): Unit
```

Notification when a transition is resumed. Note that resume() may be called by a parent [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet) on a child transition which has not yet started. This allows the child transition to restore state which may have changed in an earlier call to [onTransitionPause(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener#onTransitionPause(android.transition.Transition)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The transition which was resumed. |

### onTransitionStart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransitionStart(transition: Transition!): Unit
```

Notification about the start of the transition.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)!:The started transition. |
