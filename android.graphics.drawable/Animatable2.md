# Animatable2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animatable2

Kotlin| [Java](../android/graphics/drawable/Animatable2.md) 
| --- | --- |

```
interface Animatable2 : Animatable
```

| [android.graphics.drawable.Animatable2](../android/graphics/drawable/Animatable2.md) |

| Known Direct Subclasses [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md), [AnimatedVectorDrawable](../android/graphics/drawable/AnimatedVectorDrawable.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md) | [Drawable](../android/graphics/drawable/Drawable.md) for drawing animated images (like GIF). | | [AnimatedVectorDrawable](../android/graphics/drawable/AnimatedVectorDrawable.md) | This class animates properties of a [android.graphics.drawable.VectorDrawable](../android/graphics/drawable/VectorDrawable.md) with animations defined using [android.animation.ObjectAnimator](../android/animation/ObjectAnimator.md) or [android.animation.AnimatorSet](../android/animation/AnimatorSet.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class that drawables supporting animations and callbacks should extend.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAnimationCallbacks](../android/graphics/drawable/Animatable2.md))`()` Removes all existing animation callbacks. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAnimationCallback](../android/graphics/drawable/Animatable2.md))`(`callback:` ` [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md)`)` Adds a callback to listen to the animation events. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAnimationCallback](../android/graphics/drawable/Animatable2.md))`(`callback:` ` [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md)`)` Removes the specified animation callback. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Animatable](../android/graphics/drawable/Animatable.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](../android/graphics/drawable/Animatable.md))`()` <br /> Indicates whether the animation is running. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/graphics/drawable/Animatable.md))`()` <br /> Starts the drawable's animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](../android/graphics/drawable/Animatable.md))`()` <br /> Stops the drawable's animation. <br /> | ||

## Public methods

### clearAnimationCallbacks

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearAnimationCallbacks(): Unit
```

Removes all existing animation callbacks. 

### registerAnimationCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerAnimationCallback(callback: Animatable2.AnimationCallback): Unit
```

Adds a callback to listen to the animation events.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md):Callback to add. This value cannot be`null`. |

### unregisterAnimationCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterAnimationCallback(callback: Animatable2.AnimationCallback): Boolean
```

Removes the specified animation callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Animatable2.AnimationCallback](../android/graphics/drawable/Animatable2.AnimationCallback.md):Callback to remove. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if callback didn't exist in the call back list, or`true`if callback has been removed successfully. |
