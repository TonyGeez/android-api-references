# TimeAnimator.TimeListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeListener

Kotlin| [Java](https://developer.android.com/reference/android/animation/TimeAnimator.TimeListener "View this page in Java") 

```
interface TimeListener
```

| [android.animation.TimeAnimator.TimeListener](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator.TimeListener#) |

Implementors of this interface can set themselves as update listeners to a`TimeAnimator`instance to receive callbacks on every animation frame to receive the total time since the animator started and the delta time since the last frame. The first time the listener is called, deltaTime will be zero. The same is true for totalTime, unless the animator was set to a specific [currentPlayTime](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setCurrentPlayTime(kotlin.Long))prior to starting.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimeUpdate](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator.TimeListener#onTimeUpdate(android.animation.TimeAnimator,%20kotlin.Long,%20kotlin.Long))`(`animation:` ` [TimeAnimator](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator)!`, `totalTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `deltaTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Notifies listeners of the occurrence of another frame of the animation, along with information about the elapsed time. |

## Public methods

### onTimeUpdate

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTimeUpdate(
    animation: TimeAnimator!, 
    totalTime: Long, 
    deltaTime: Long
): Unit
```

Notifies listeners of the occurrence of another frame of the animation, along with information about the elapsed time.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [TimeAnimator](https://developer.android.com/reference/kotlin/android/animation/TimeAnimator)!:The animator sending out the notification. |
| `totalTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The total time elapsed since the animator started, in milliseconds. |
| `deltaTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time elapsed since the previous frame, in milliseconds. |
