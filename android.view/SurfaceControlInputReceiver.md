# SurfaceControlInputReceiver

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceControlInputReceiver

Kotlin| [Java](https://developer.android.com/reference/android/view/SurfaceControlInputReceiver "View this page in Java") 

```
interface SurfaceControlInputReceiver
```

| [android.view.SurfaceControlInputReceiver](https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver#) |

Provides a mechanism for a SurfaceControl to receive input events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onInputEvent](https://developer.android.com/reference/kotlin/android/view/SurfaceControlInputReceiver#onInputEvent(android.view.InputEvent))`(`event:` ` [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent)`)` When input events are batched, this is called at most once per frame. |

## Public methods

### onInputEvent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInputEvent(event: InputEvent): Boolean
```

When input events are batched, this is called at most once per frame. When non batched, this is called immediately for the input event.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent):The input event that was received. This input event object will become invalid and recycled after this method is invoked. If there is need to persist this object beyond the scope of this method, the overriding code should make a copy of this object. For example, using [MotionEvent.obtain(MotionEvent other)](https://developer.android.com/reference/kotlin/android/view/MotionEvent#obtain(android.view.MotionEvent))or [KeyEvent.KeyEvent(KeyEvent)](https://developer.android.com/reference/kotlin/android/view/KeyEvent#KeyEvent(android.view.KeyEvent))} This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, false otherwise. |
