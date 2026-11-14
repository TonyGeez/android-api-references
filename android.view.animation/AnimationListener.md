# Animation.AnimationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationListener

Kotlin| [Java](../android/view/animation/Animation.AnimationListener.md) 
| --- | --- |

```
interface AnimationListener
```

| [android.view.animation.Animation.AnimationListener](../android/view/animation/Animation.AnimationListener.md) |

An animation listener receives notifications from an animation. Notifications indicate animation related events, such as the end or the repetition of the animation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](../android/view/animation/Animation.AnimationListener.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`)` Notifies the end of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationRepeat](../android/view/animation/Animation.AnimationListener.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`)` Notifies the repetition of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](../android/view/animation/Animation.AnimationListener.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`)` Notifies the start of the animation. |
| --- | --- |

## Public methods

### onAnimationEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationEnd(animation: Animation!): Unit
```

Notifies the end of the animation. This callback is not invoked for animations with repeat count set to INFINITE.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](../android/view/animation/Animation.md)!:The animation which reached its end. |

### onAnimationRepeat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationRepeat(animation: Animation!): Unit
```

Notifies the repetition of the animation.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](../android/view/animation/Animation.md)!:The animation which was repeated. |

### onAnimationStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationStart(animation: Animation!): Unit
```

Notifies the start of the animation.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](../android/view/animation/Animation.md)!:The started animation. |
