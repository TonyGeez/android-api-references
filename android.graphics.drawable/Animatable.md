# Animatable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animatable

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/Animatable "View this page in Java") 

```
interface Animatable
```

| [android.graphics.drawable.Animatable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#) |

| Known Direct Subclasses [Animatable2](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2), [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable) |-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------| | [Animatable2](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2) | Abstract class that drawables supporting animations and callbacks should extend. | | [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. | |

| Known Indirect Subclasses [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable), [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable) | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) for drawing animated images (like GIF). | | [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) | This class animates properties of a [android.graphics.drawable.VectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable) with animations defined using [android.animation.ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#) or [android.animation.AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.html#). | |

Interface that drawables supporting animations should implement.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#isRunning())`()` Indicates whether the animation is running. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#start())`()` Starts the drawable's animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#stop())`()` Stops the drawable's animation. |

## Public methods

### isRunning

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRunning(): Boolean
```

Indicates whether the animation is running.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the animation is running, false otherwise. |

### start

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(): Unit
```

Starts the drawable's animation. 

### stop

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun stop(): Unit
```

Stops the drawable's animation.
