# AnimatorListenerAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorListenerAdapter

Kotlin| [Java](https://developer.android.com/reference/android/animation/AnimatorListenerAdapter "View this page in Java") 
| --- | --- |

```
abstract class AnimatorListenerAdapter : Animator.AnimatorListener, Animator.AnimatorPauseListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.AnimatorListenerAdapter](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#) |

This adapter class provides empty implementations of the methods from [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener). Any custom listener that cares only about a subset of the methods of this listener can simply subclass this adapter class instead of implementing the interface directly.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatorListenerAdapter](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#AnimatorListenerAdapter())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationCancel](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationCancel(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies the cancellation of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationEnd(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies the end of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationPause](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationPause(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies that the animation was paused. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationRepeat](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationRepeat(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies the repetition of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationResume](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationResume(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies that the animation was resumed, after being previously paused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](https://developer.android.com/reference/kotlin/android/animation/AnimatorListenerAdapter#onAnimationStart(android.animation.Animator))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`)` Notifies the start of the animation. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator,%20kotlin.Boolean))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE. This method's default behavior is to call [onAnimationEnd(android.animation.Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator)). This method can be overridden, though not required, to get the additional play direction info when an animation ends. Skipping calling super when overriding this method results in [onAnimationEnd(android.animation.Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator))not getting called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator,%20kotlin.Boolean))`(`animation:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)`, `isReverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies the start of the animation as well as the animation's overall play direction. This method's default behavior is to call [onAnimationStart(android.animation.Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator)). This method can be overridden, though not required, to get the additional play direction info when an animation starts. Skipping calling super when overriding this method results in [onAnimationStart(android.animation.Animator)](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator))not getting called. <br /> | ||

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
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The animation which was canceled. This value cannot be`null`. |

### onAnimationEnd

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationEnd(animation: Animator): Unit
```

Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The animation which reached its end. This value cannot be`null`. |

### onAnimationPause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationPause(animation: Animator): Unit
```

Notifies that the animation was paused.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The animaton being paused. This value cannot be`null`. |

### onAnimationRepeat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationRepeat(animation: Animator): Unit
```

Notifies the repetition of the animation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The animation which was repeated. This value cannot be`null`. |

### onAnimationResume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationResume(animation: Animator): Unit
```

Notifies that the animation was resumed, after being previously paused.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The animation being resumed. This value cannot be`null`. |

### onAnimationStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAnimationStart(animation: Animator): Unit
```

Notifies the start of the animation.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator):The started animation. This value cannot be`null`. |
