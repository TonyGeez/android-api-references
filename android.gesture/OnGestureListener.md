# GestureOverlayView.OnGestureListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGestureListener

Kotlin| [Java](https://developer.android.com/reference/android/gesture/GestureOverlayView.OnGestureListener "View this page in Java") 
| --- | --- |

```
interface OnGestureListener
```

| [android.gesture.GestureOverlayView.OnGestureListener](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.OnGestureListener#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGesture](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.OnGestureListener#onGesture(android.gesture.GestureOverlayView,%20android.view.MotionEvent))`(`overlay:` ` [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureCancelled](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.OnGestureListener#onGestureCancelled(android.gesture.GestureOverlayView,%20android.view.MotionEvent))`(`overlay:` ` [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureEnded](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.OnGestureListener#onGestureEnded(android.gesture.GestureOverlayView,%20android.view.MotionEvent))`(`overlay:` ` [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGestureStarted](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView.OnGestureListener#onGestureStarted(android.gesture.GestureOverlayView,%20android.view.MotionEvent))`(`overlay:` ` [GestureOverlayView](https://developer.android.com/reference/kotlin/android/gesture/GestureOverlayView)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |

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
