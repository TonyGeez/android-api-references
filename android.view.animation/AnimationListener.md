# Animation.AnimationListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationListener

Kotlin| [Java](https://developer.android.com/reference/android/view/animation/Animation.AnimationListener "View this page in Java") 
| --- | --- |

```
interface AnimationListener
```

| [android.view.animation.Animation.AnimationListener](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#) |

An animation listener receives notifications from an animation. Notifications indicate animation related events, such as the end or the repetition of the animation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationEnd](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#onAnimationEnd(android.view.animation.Animation))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Notifies the end of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationRepeat](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#onAnimationRepeat(android.view.animation.Animation))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Notifies the repetition of the animation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAnimationStart](https://developer.android.com/reference/kotlin/android/view/animation/Animation.AnimationListener#onAnimationStart(android.view.animation.Animation))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Notifies the start of the animation. |
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
| `animation` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!:The animation which reached its end. |

### onAnimationRepeat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationRepeat(animation: Animation!): Unit
```

Notifies the repetition of the animation.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!:The animation which was repeated. |

### onAnimationStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAnimationStart(animation: Animation!): Unit
```

Notifies the start of the animation.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!:The started animation. |
