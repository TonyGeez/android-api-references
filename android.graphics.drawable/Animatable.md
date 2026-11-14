# Animatable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animatable

Kotlin| [Java](Animatable.md) 
| --- | --- |

```
interface Animatable
```

| [android.graphics.drawable.Animatable](Animatable.md) |

| Known Direct Subclasses [Animatable2](Animatable2.md), [AnimationDrawable](AnimationDrawable.md) |-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------| | [Animatable2](Animatable2.md) | Abstract class that drawables supporting animations and callbacks should extend. | | [AnimationDrawable](AnimationDrawable.md) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AnimatedImageDrawable](AnimatedImageDrawable.md), [AnimatedVectorDrawable](AnimatedVectorDrawable.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatedImageDrawable](AnimatedImageDrawable.md) | [Drawable](Drawable.md) for drawing animated images (like GIF). | | [AnimatedVectorDrawable](AnimatedVectorDrawable.md) | This class animates properties of a [android.graphics.drawable.VectorDrawable](VectorDrawable.md) with animations defined using [android.animation.ObjectAnimator](../android.animation/ObjectAnimator.md) or [android.animation.AnimatorSet](../android.animation/AnimatorSet.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface that drawables supporting animations should implement.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](Animatable.md))`()` Indicates whether the animation is running. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](Animatable.md))`()` Starts the drawable's animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](Animatable.md))`()` Stops the drawable's animation. |
| --- | --- |

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
