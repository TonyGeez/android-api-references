# ChooserSession

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChooserSession

Kotlin| [Java](https://developer.android.com/reference/android/service/chooser/ChooserSession "View this page in Java") 
| --- | --- |

```
class ChooserSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.chooser.ChooserSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#) |

A class that represents an interactive Chooser session.

A [StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener) callback can be used to receive updates about the session and communication from Chooser.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener) A callback interface for Chooser session state updates. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CLOSED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_CLOSED:kotlin.Int) The session is closed by either side. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_INITIALIZED:kotlin.Int) The initial state: the session is initialized but the Chooser has not yet connected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int) The chooser is connected and can be updated. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addStateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#addStateListener(java.util.concurrent.Executor,%20android.service.chooser.ChooserSession.StateListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [ChooserSession.StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endSession](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#endSession())`()` Terminates the session and closes Chooser. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | [getBounds](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#getBounds())`()` Gets the last bounds reported by the Chooser. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#getState())`()` <br /> |
| [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken) | [getToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#getToken())`()` Returns this session's token. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeStateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#removeStateListener(android.service.chooser.ChooserSession.StateListener))`(`listener:` ` [ChooserSession.StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener)`)` Removes a previously added UpdateListener callback. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetsEnabled](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#setTargetsEnabled(kotlin.Boolean))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the targets in the chooser UI are enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateIntent](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#updateIntent(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`)` Updates the chooser intent in an active Chooser session, causing Chooser to refresh its state and targets. |

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
| `listener` | [ChooserSession.StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener):make sure that the callback is cleared at the end of a component's lifecycle (e.g. Activity) or provide a properly maintained WeakReference wrapper to avoid memory leaks. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):This value cannot be`null`. |

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
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)? | the most recently reported Chooser bounds, or`null`if bounds have not yet been received via [ChooserSession.StateListener.onBoundsChanged(Rect)](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener#onBoundsChanged(android.graphics.Rect)). |

### getState

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current session state. Value is [android.service.chooser.ChooserSession#STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_INITIALIZED:kotlin.Int), [android.service.chooser.ChooserSession#STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int), or [android.service.chooser.ChooserSession#STATE_CLOSED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_CLOSED:kotlin.Int) |

**See Also**

- [android.service.chooser.ChooserSession#STATE_INITIALIZED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_INITIALIZED:kotlin.Int)
- [android.service.chooser.ChooserSession#STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int)
- [android.service.chooser.ChooserSession#STATE_CLOSED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_CLOSED:kotlin.Int) 

### getToken

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getToken(): ChooserSessionToken
```

Returns this session's token. A token serves as a session identifier and can be used to retrieve an active session from the [ChooserManager](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager).

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ChooserSessionToken](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSessionToken) | This value cannot be`null`. |

### removeStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeStateListener(listener: ChooserSession.StateListener): Unit
```

Removes a previously added UpdateListener callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ChooserSession.StateListener](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession.StateListener):This value cannot be`null`. |

### setTargetsEnabled

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTargetsEnabled(isEnabled: Boolean): Unit
```

Sets whether the targets in the chooser UI are enabled. By default targets are enabled.

This method is primarily intended to allow for managing a transient state, particularly useful during long-running operations. By disabling targets, launching application can prevent unintended interactions.

A no-op when the session is not in the [STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int). 

### updateIntent

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateIntent(intent: Intent): Unit
```

Updates the chooser intent in an active Chooser session, causing Chooser to refresh its state and targets.

Only updates to the following extras in the provided intent are respected:

- [Intent.EXTRA_INTENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INTENT:kotlin.String)
- [Intent.EXTRA_EXCLUDE_COMPONENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_EXCLUDE_COMPONENTS:kotlin.String)
- [Intent.EXTRA_CHOOSER_TARGETS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_TARGETS:kotlin.String)
- [Intent.EXTRA_ALTERNATE_INTENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ALTERNATE_INTENTS:kotlin.String)
- [Intent.EXTRA_REPLACEMENT_EXTRAS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_REPLACEMENT_EXTRAS:kotlin.String)
- [Intent.EXTRA_INITIAL_INTENTS](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_INITIAL_INTENTS:kotlin.String)
- [Intent.EXTRA_CHOOSER_RESULT_INTENT_SENDER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_RESULT_INTENT_SENDER:kotlin.String)
- [Intent.EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_CHOOSER_REFINEMENT_INTENT_SENDER:kotlin.String)

This method is a no-op if the session is not in the [STATE_STARTED](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserSession#STATE_STARTED:kotlin.Int) state.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):The new intent to apply to the session. This value cannot be`null`. |
