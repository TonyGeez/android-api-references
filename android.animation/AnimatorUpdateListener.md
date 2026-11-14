Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorUpdateListener

Kotlin | [Java](https://developer.android.com/reference/android/animation/ValueAnimator.AnimatorUpdateListener "View this page in Java")
| --- | --- |

```
interface AnimatorUpdateListener
```

| [android.animation.ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener#) |

Implementors of this interface can add themselves as update listeners to an `ValueAnimator` instance to receive callbacks on every animation frame, after the current frame's values have been calculated for that `ValueAnimator`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener#onAnimationUpdate(android.animation.ValueAnimator)(animation: https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)` Notifies the occurrence of another frame of the animation. |

## Public methods

### onAnimationUpdate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAnimationUpdate(animation: ValueAnimator): Unit
```

Notifies the occurrence of another frame of the animation.

| Parameters ||
|---|---|
| `animation` | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator): The animation which was repeated. This value cannot be `null`. |
