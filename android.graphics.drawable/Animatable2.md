# Animatable2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Animatable2

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/Animatable2 "View this page in Java") 
| --- | --- |

```
interface Animatable2 : Animatable
```

| [android.graphics.drawable.Animatable2](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2#) |

| Known Direct Subclasses [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable), [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable) | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) for drawing animated images (like GIF). | | [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) | This class animates properties of a [android.graphics.drawable.VectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable) with animations defined using [android.animation.ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#) or [android.animation.AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.html#). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class that drawables supporting animations and callbacks should extend.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAnimationCallbacks](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2#clearAnimationCallbacks())`()` Removes all existing animation callbacks. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2#registerAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback))`(`callback:` ` [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)`)` Adds a callback to listen to the animation events. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2#unregisterAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback))`(`callback:` ` [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)`)` Removes the specified animation callback. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Animatable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#isRunning())`()` <br /> Indicates whether the animation is running. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#start())`()` <br /> Starts the drawable's animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable#stop())`()` <br /> Stops the drawable's animation. <br /> | ||

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
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback):Callback to add. This value cannot be`null`. |

### unregisterAnimationCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterAnimationCallback(callback: Animatable2.AnimationCallback): Boolean
```

Removes the specified animation callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback):Callback to remove. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if callback didn't exist in the call back list, or`true`if callback has been removed successfully. |
