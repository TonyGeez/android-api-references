# TvAdView.OnUnhandledInputEventListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUnhandledInputEventListener

Kotlin| [Java](../android/media/tv/ad/TvAdView.OnUnhandledInputEventListener.md) 
| --- | --- |

```
interface OnUnhandledInputEventListener
```

| [android.media.tv.ad.TvAdView.OnUnhandledInputEventListener](../android/media/tv/ad/TvAdView.OnUnhandledInputEventListener.md) |

Interface definition for a callback to be invoked when the unhandled input event is received.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onUnhandledInputEvent](../android/media/tv/ad/TvAdView.OnUnhandledInputEventListener.md))`(`event:` ` [InputEvent](../android/view/InputEvent.md)`)` Called when an input event was not handled by the TV AD service. |

## Public methods

### onUnhandledInputEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnhandledInputEvent(event: InputEvent): Boolean
```

Called when an input event was not handled by the TV AD service.

This is called asynchronously from where the event is dispatched. It gives the host application a chance to handle the unhandled input events.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [InputEvent](../android/view/InputEvent.md):The input event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If you handled the event, return`true`. If you want to allow the event to be handled by the next receiver, return`false`. |
