# Animator.AnimatorPauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorPauseListener

Kotlin | [Java](https://developer.android.com/reference/android/animation/Animator.AnimatorPauseListener "View this page in Java") 

```
interface AnimatorPauseListener
```

| [android.animation.Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener#) |

| Known Direct Subclasses [AnimatorListenerAdapter](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter) |---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatorListenerAdapter](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter) | This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener). | |

A pause listener receives notifications from an animation when the animation is [paused](https://developer.android.com/reference/kotlin/android/animation/Animator#pause()) or [resumed](https://developer.android.com/reference/kotlin/android/animation/Animator#resume()).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationPause](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener#onAnimationPause(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies that the animation was paused. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationResume](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener#onAnimationResume(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies that the animation was resumed, after being previously paused. |

## Public methods

### onAnimationPause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationPause(animation: Animator): Unit
```

Notifies that the animation was paused.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator): The animaton being paused. This value cannot be `null`. |

**See Also**

- [#pause()](https://developer.android.com/reference/kotlin/android/animation/Animator#pause()) 

### onAnimationResume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationResume(animation: Animator): Unit
```

Notifies that the animation was resumed, after being previously paused.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator): The animation being resumed. This value cannot be `null`. |

**See Also**

- [#resume()](https://developer.android.com/reference/kotlin/android/animation/Animator#resume())
