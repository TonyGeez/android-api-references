# Animator.AnimatorListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorListener

Kotlin| [Java](../android/animation/Animator.AnimatorListener.md) 
| --- | --- |

```
interface AnimatorListener
```

| [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) |

| Known Direct Subclasses [AnimatorListenerAdapter](../android/animation/AnimatorListenerAdapter.md) |---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatorListenerAdapter](../android/animation/AnimatorListenerAdapter.md) | This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md). | |
| --- | --- | --- | --- | --- | --- | --- |

An animation listener receives notifications from an animation. Notifications indicate animation related events, such as the end or the repetition of the animation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationCancel](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies the cancellation of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies the end of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies the end of the animation. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationRepeat](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies the repetition of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`)` Notifies the start of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](../android/animation/Animator.md)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies the start of the animation as well as the animation's overall play direction. |
| --- | --- |

## Public methods

### onAnimationCancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationCancel(animation: Animator): Unit
```

Notifies the cancellation of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The animation which was canceled. This value cannot be`null`. |

### onAnimationEnd

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationEnd(animation: Animator): Unit
```

Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The animation which reached its end. This value cannot be`null`. |

### onAnimationEnd

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationEnd(
    animation: Animator, 
    isReverse: Boolean
): Unit
```

Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

This method's default behavior is to call [onAnimationEnd(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md)). This method can be overridden, though not required, to get the additional play direction info when an animation ends. Skipping calling super when overriding this method results in [onAnimationEnd(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md))not getting called.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The animation which reached its end. This value cannot be`null`. |
| `isReverse` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the animation is playing in reverse. |

### onAnimationRepeat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationRepeat(animation: Animator): Unit
```

Notifies the repetition of the animation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The animation which was repeated. This value cannot be`null`. |

### onAnimationStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationStart(animation: Animator): Unit
```

Notifies the start of the animation.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The started animation. This value cannot be`null`. |

### onAnimationStart

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationStart(
    animation: Animator, 
    isReverse: Boolean
): Unit
```

Notifies the start of the animation as well as the animation's overall play direction. This method's default behavior is to call [onAnimationStart(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md)). This method can be overridden, though not required, to get the additional play direction info when an animation starts. Skipping calling super when overriding this method results in [onAnimationStart(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md))not getting called.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](../android/animation/Animator.md):The started animation. This value cannot be`null`. |
| `isReverse` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the animation is playing in reverse. |
