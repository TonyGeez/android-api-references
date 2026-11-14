Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackAnimationCallback

Kotlin | [Java](OnBackAnimationCallback.md)
| --- | --- |

```
interface OnBackAnimationCallback : OnBackInvokedCallback
```

| [android.window.OnBackAnimationCallback](OnBackAnimationCallback.md) |

Interface for applications to register back animation callbacks along their custom back handling.

This allows the client to customize various back behaviors by overriding the corresponding callback methods.

Callback instances can be added to and removed from OnBackInvokedDispatcher, which is held at window level and accessible through getOnBackInvokedDispatcher, getOnBackInvokedDispatcher, getOnBackInvokedDispatcher and findOnBackInvokedDispatcher.

When back is triggered, callbacks on the in-focus window are invoked in reverse order in which they are added within the same priority. Between different priorities, callbacks with higher priority are invoked first.

<br />

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBackCancelled Called when a back gesture or back button press has been cancelled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBackProgressed Called when a back gesture progresses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onBackStarted Called when a back gesture has been started, or back button has been pressed down. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class OnBackInvokedCallback |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBackInvoked Called when a back gesture has been completed and committed, or back button pressed has been released and committed. <br /> | ||

## Public methods

### onBackCancelled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackCancelled(): Unit
```

Called when a back gesture or back button press has been cancelled.

### onBackProgressed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackProgressed(backEvent: BackEvent): Unit
```

Called when a back gesture progresses.

| Parameters ||
|---|---|
| `backEvent` | [BackEvent](BackEvent.md): An BackEvent object describing the progress event. This value cannot be `null`. |

**See Also**

- BackEvent

### onBackStarted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackStarted(backEvent: BackEvent): Unit
```

Called when a back gesture has been started, or back button has been pressed down.

| Parameters ||
|---|---|
| `backEvent` | [BackEvent](BackEvent.md): The BackEvent containing information about the touch or button press. This value cannot be `null`. |

**See Also**

- BackEvent
