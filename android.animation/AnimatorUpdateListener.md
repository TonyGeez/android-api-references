Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorUpdateListener

Kotlin | [Java](../android/animation/ValueAnimator.AnimatorUpdateListener.md)
| --- | --- |

```
interface AnimatorUpdateListener
```

| [android.animation.ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md) |

Implementors of this interface can add themselves as update listeners to an `ValueAnimator` instance to receive callbacks on every animation frame, after the current frame's values have been calculated for that `ValueAnimator`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAnimationUpdate Notifies the occurrence of another frame of the animation. |

## Public methods

### onAnimationUpdate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAnimationUpdate(animation: ValueAnimator): Unit
```

Notifies the occurrence of another frame of the animation.

| Parameters ||
|---|---|
| `animation` | [ValueAnimator](ValueAnimator.md): The animation which was repeated. This value cannot be `null`. |
