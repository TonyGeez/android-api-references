# TvView.OnUnhandledInputEventListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUnhandledInputEventListener

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvView.OnUnhandledInputEventListener "View this page in Java") 

```
interface OnUnhandledInputEventListener
```

| [android.media.tv.TvView.OnUnhandledInputEventListener](https://developer.android.com/reference/kotlin/android/media/tv/TvView.OnUnhandledInputEventListener#) |

Interface definition for a callback to be invoked when the unhandled input event is received.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onUnhandledInputEvent](https://developer.android.com/reference/kotlin/android/media/tv/TvView.OnUnhandledInputEventListener#onUnhandledInputEvent(android.view.InputEvent))`(`event:` ` [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent.html#)!`)` Called when an input event was not handled by the bound TV input. |

## Public methods

### onUnhandledInputEvent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnhandledInputEvent(event: InputEvent!): Boolean
```

Called when an input event was not handled by the bound TV input.

This is called asynchronously from where the event is dispatched. It gives the host application a chance to handle the unhandled input events.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `event` | [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent.html#)!:The input event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return`true`. If you want to allow the event to be handled by the next receiver, return`false`. |
