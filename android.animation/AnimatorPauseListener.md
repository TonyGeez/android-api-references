# Animator.AnimatorPauseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorPauseListener

Kotlin | [Java](../android/animation/Animator.AnimatorPauseListener.md) 
| --- | --- |

```
interface AnimatorPauseListener
```

| [android.animation.Animator.AnimatorPauseListener](../android/animation/Animator.AnimatorPauseListener.md) |

| Known Direct Subclasses [AnimatorListenerAdapter](../android/animation/AnimatorListenerAdapter.md) |---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatorListenerAdapter](../android/animation/AnimatorListenerAdapter.md) | This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md). | |
| --- | --- | --- | --- | --- | --- | --- |

A pause listener receives notifications from an animation when the animation is [paused](../android/animation/Animator.md)) or [resumed](../android/animation/Animator.md)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationPause](../android/animation/Animator.AnimatorPauseListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies that the animation was paused. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationResume](../android/animation/Animator.AnimatorPauseListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies that the animation was resumed, after being previously paused. |

## Public methods

### onAnimationPause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationPause(animation: Animator): Unit
```

Notifies that the animation was paused.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md): The animaton being paused. This value cannot be `null`. |

**See Also**

- [#pause()](../android/animation/Animator.md)) 

### onAnimationResume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationResume(animation: Animator): Unit
```

Notifies that the animation was resumed, after being previously paused.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md): The animation being resumed. This value cannot be `null`. |

**See Also**

- [#resume()](../android/animation/Animator.md))
