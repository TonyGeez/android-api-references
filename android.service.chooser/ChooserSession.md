# ChooserSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChooserSession

Kotlin| [Java](ChooserSession.md) 
| --- | --- |

```
class ChooserSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.chooser.ChooserSession](ChooserSession.md) |

A class that represents an interactive Chooser session.

A [StateListener](../android/service/chooser/ChooserSession.StateListener.md) callback can be used to receive updates about the session and communication from Chooser.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [StateListener](../android/service/chooser/ChooserSession.StateListener.md) A callback interface for Chooser session state updates. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CLOSED](ChooserSession.md) The session is closed by either side. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INITIALIZED](ChooserSession.md) The initial state: the session is initialized but the Chooser has not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STARTED](ChooserSession.md) The chooser is connected and can be updated. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addStateListener](ChooserSession.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [ChooserSession.StateListener](../android/service/chooser/ChooserSession.StateListener.md)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endSession](ChooserSession.md))`()` Terminates the session and closes Chooser. |
| [Rect](../android.graphics/Rect.md)? | [getBounds](ChooserSession.md))`()` Gets the last bounds reported by the Chooser. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](ChooserSession.md))`()` <br /> |
| [ChooserSessionToken](ChooserSessionToken.md) | [getToken](ChooserSession.md))`()` Returns this session's token. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeStateListener](ChooserSession.md))`(`listener:` ` [ChooserSession.StateListener](../android/service/chooser/ChooserSession.StateListener.md)`)` Removes a previously added UpdateListener callback. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetsEnabled](ChooserSession.md))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the targets in the chooser UI are enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateIntent](ChooserSession.md))`(`intent:` ` [Intent](../android.content/Intent.md)`)` Updates the chooser intent in an active Chooser session, causing Chooser to refresh its state and targets. |

## Constants

### STATE_CLOSED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CLOSED: Int
```

The session is closed by either side. 

 Value: 2

### STATE_INITIALIZED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_INITIALIZED: Int
```

The initial state: the session is initialized but the Chooser has not yet connected. 

 Value: 0

### STATE_STARTED

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STARTED: Int
```

The chooser is connected and can be updated. 

 Value: 1

## Public methods

### addStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addStateListener(
    executor: Executor, 
    listener: ChooserSession.StateListener
): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ChooserSession.StateListener](../android/service/chooser/ChooserSession.StateListener.md):make sure that the callback is cleared at the end of a component's lifecycle (e.g. Activity) or provide a properly maintained WeakReference wrapper to avoid memory leaks. This value cannot be`null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):This value cannot be`null`. |

### endSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun endSession(): Unit
```

Terminates the session and closes Chooser. 

### getBounds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBounds(): Rect?
```

Gets the last bounds reported by the Chooser.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rect](../android.graphics/Rect.md)? | the most recently reported Chooser bounds, or`null`if bounds have not yet been received via [ChooserSession.StateListener.onBoundsChanged(Rect)](../android/service/chooser/ChooserSession.StateListener.md)). |

### getState

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current session state. Value is [android.service.chooser.ChooserSession#STATE_INITIALIZED](ChooserSession.md), [android.service.chooser.ChooserSession#STATE_STARTED](ChooserSession.md), or [android.service.chooser.ChooserSession#STATE_CLOSED](ChooserSession.md) |

**See Also**

- [android.service.chooser.ChooserSession#STATE_INITIALIZED](ChooserSession.md)
- [android.service.chooser.ChooserSession#STATE_STARTED](ChooserSession.md)
- [android.service.chooser.ChooserSession#STATE_CLOSED](ChooserSession.md) 

### getToken

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToken(): ChooserSessionToken
```

Returns this session's token. A token serves as a session identifier and can be used to retrieve an active session from the [ChooserManager](ChooserManager.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ChooserSessionToken](ChooserSessionToken.md) | This value cannot be`null`. |

### removeStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeStateListener(listener: ChooserSession.StateListener): Unit
```

Removes a previously added UpdateListener callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ChooserSession.StateListener](../android/service/chooser/ChooserSession.StateListener.md):This value cannot be`null`. |

### setTargetsEnabled

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTargetsEnabled(isEnabled: Boolean): Unit
```

Sets whether the targets in the chooser UI are enabled. By default targets are enabled.

This method is primarily intended to allow for managing a transient state, particularly useful during long-running operations. By disabling targets, launching application can prevent unintended interactions.

A no-op when the session is not in the [STATE_STARTED](ChooserSession.md). 

### updateIntent

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateIntent(intent: Intent): Unit
```

Updates the chooser intent in an active Chooser session, causing Chooser to refresh its state and targets.

Only updates to the following extras in the provided intent are respected:

- [Intent.EXTRA_INTENT](../android.content/Intent.md)
- [Intent.EXTRA_EXCLUDE_COMPONENTS](../android.content/Intent.md)
- [Intent.EXTRA_CHOOSER_TARGETS](../android.content/Intent.md)
- [Intent.EXTRA_ALTERNATE_INTENTS](../android.content/Intent.md)
- [Intent.EXTRA_REPLACEMENT_EXTRAS](../android.content/Intent.md)
- [Intent.EXTRA_INITIAL_INTENTS](../android.content/Intent.md)
- [Intent.EXTRA_CHOOSER_RESULT_INTENT_SENDER](../android.content/Intent.md)
- [Intent.EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER](../android.content/Intent.md)

This method is a no-op if the session is not in the [STATE_STARTED](ChooserSession.md) state.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md):The new intent to apply to the session. This value cannot be`null`. |
