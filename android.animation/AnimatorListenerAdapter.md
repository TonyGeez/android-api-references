# AnimatorListenerAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorListenerAdapter

Kotlin| [Java](AnimatorListenerAdapter.md) 
| --- | --- |

```
abstract class AnimatorListenerAdapter : Animator.AnimatorListener, Animator.AnimatorPauseListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.AnimatorListenerAdapter](AnimatorListenerAdapter.md) |

This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md). Any custom listener that cares only about a subset of the methods of this listener can simply subclass this adapter class instead of implementing the interface directly.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatorListenerAdapter](AnimatorListenerAdapter.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationCancel](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies the cancellation of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies the end of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationPause](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies that the animation was paused. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationRepeat](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies the repetition of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationResume](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies that the animation was resumed, after being previously paused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](AnimatorListenerAdapter.md))`(`animation:` ` [Animator](Animator.md)`)` Notifies the start of the animation. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AnimatorListener](../android/animation/Animator.AnimatorListener.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](Animator.md)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE. This method's default behavior is to call [onAnimationEnd(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md)). This method can be overridden, though not required, to get the additional play direction info when an animation ends. Skipping calling super when overriding this method results in [onAnimationEnd(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md))not getting called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](../android/animation/Animator.AnimatorListener.md))`(`animation:` ` [Animator](Animator.md)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies the start of the animation as well as the animation's overall play direction. This method's default behavior is to call [onAnimationStart(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md)). This method can be overridden, though not required, to get the additional play direction info when an animation starts. Skipping calling super when overriding this method results in [onAnimationStart(android.animation.Animator)](../android/animation/Animator.AnimatorListener.md))not getting called. <br /> | ||

## Public constructors

### AnimatorListenerAdapter

```
AnimatorListenerAdapter()
```

## Public methods

### onAnimationCancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationCancel(animation: Animator): Unit
```

Notifies the cancellation of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The animation which was canceled. This value cannot be`null`. |

### onAnimationEnd

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationEnd(animation: Animator): Unit
```

Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The animation which reached its end. This value cannot be`null`. |

### onAnimationPause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationPause(animation: Animator): Unit
```

Notifies that the animation was paused.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The animaton being paused. This value cannot be`null`. |

### onAnimationRepeat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationRepeat(animation: Animator): Unit
```

Notifies the repetition of the animation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The animation which was repeated. This value cannot be`null`. |

### onAnimationResume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationResume(animation: Animator): Unit
```

Notifies that the animation was resumed, after being previously paused.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The animation being resumed. This value cannot be`null`. |

### onAnimationStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationStart(animation: Animator): Unit
```

Notifies the start of the animation.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](Animator.md):The started animation. This value cannot be`null`. |
