# GestureOverlayView.OnGestureListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGestureListener

Kotlin| [Java](../android/gesture/GestureOverlayView.OnGestureListener.md) 
| --- | --- |

```
interface OnGestureListener
```

| [android.gesture.GestureOverlayView.OnGestureListener](../android/gesture/GestureOverlayView.OnGestureListener.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGesture](../android/gesture/GestureOverlayView.OnGestureListener.md))`(`overlay:` ` [GestureOverlayView](GestureOverlayView.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureCancelled](../android/gesture/GestureOverlayView.OnGestureListener.md))`(`overlay:` ` [GestureOverlayView](GestureOverlayView.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureEnded](../android/gesture/GestureOverlayView.OnGestureListener.md))`(`overlay:` ` [GestureOverlayView](GestureOverlayView.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureStarted](../android/gesture/GestureOverlayView.OnGestureListener.md))`(`overlay:` ` [GestureOverlayView](GestureOverlayView.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |

## Public methods

### onGesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGesture(
    overlay: GestureOverlayView!, 
    event: MotionEvent!
): Unit
```  

### onGestureCancelled

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGestureCancelled(
    overlay: GestureOverlayView!, 
    event: MotionEvent!
): Unit
```  

### onGestureEnded

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGestureEnded(
    overlay: GestureOverlayView!, 
    event: MotionEvent!
): Unit
```  

### onGestureStarted

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGestureStarted(
    overlay: GestureOverlayView!, 
    event: MotionEvent!
): Unit
```
