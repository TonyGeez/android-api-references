# GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureDetector

Kotlin| [Java](https://developer.android.com/reference/android/view/GestureDetector "View this page in Java") 

```
open class GestureDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#) |

Detects various gestures and events using the supplied [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) s. The [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) callback will notify users when a particular motion event has occurred. This class should only be used with [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) s reported via touch (don't use for trackball events). To use this class:

- Create an instance of the`GestureDetector`for your [View](https://developer.android.com/reference/kotlin/android/view/View)
- In the [View.onTouchEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onTouchEvent(android.view.MotionEvent))method ensure you call [onTouchEvent(android.view.MotionEvent)](https://developer.android.com/reference/kotlin/android/view/GestureDetector#onTouchEvent(android.view.MotionEvent)). The methods defined in your callback will be executed when the events occur.
- If listening for [OnContextClickListener.onContextClick(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener#onContextClick(android.view.MotionEvent))you must call [onGenericMotionEvent(android.view.MotionEvent)](https://developer.android.com/reference/kotlin/android/view/GestureDetector#onGenericMotionEvent(android.view.MotionEvent))in [View.onGenericMotionEvent(MotionEvent)](https://developer.android.com/reference/kotlin/android/view/View#onGenericMotionEvent(android.view.MotionEvent)).

<br />

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener) The listener that is used to notify when a context click occurs. |
| abstract | [OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener) The listener that is used to notify when a double-tap or a confirmed single-tap occur. |
| abstract | [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) The listener that is used to notify when gestures occur. |
| open | [SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener) A convenience class to extend when you only want to listen for a subset of all the gestures. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.content.Context,%20android.view.GestureDetector.OnGestureListener))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?`, `listener:` ` [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener)`)` Creates a GestureDetector with the supplied listener. |
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.content.Context,%20android.view.GestureDetector.OnGestureListener,%20android.os.Handler))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?`, `listener:` ` [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#). |
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.content.Context,%20android.view.GestureDetector.OnGestureListener,%20android.os.Handler,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?`, `listener:` ` [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`, `unused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#). |
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.view.GestureDetector.OnGestureListener))`(`listener:` ` [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener)`)` Creates a GestureDetector with the supplied listener. |
| [GestureDetector](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.view.GestureDetector.OnGestureListener,%20android.os.Handler))`(`listener:` ` [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Creates a GestureDetector with the supplied listener. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLongpressEnabled](https://developer.android.com/reference/kotlin/android/view/GestureDetector#isLongpressEnabled())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/view/GestureDetector#onGenericMotionEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Analyzes the given generic motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) supplied. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/view/GestureDetector#onTouchEvent(android.view.MotionEvent))`(`ev:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent)`)` Analyzes the given motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) supplied. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector#setContextClickListener(android.view.GestureDetector.OnContextClickListener))`(`onContextClickListener:` ` [GestureDetector.OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener)?`)` Sets the listener which will be called for context clicks. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIsLongpressEnabled](https://developer.android.com/reference/kotlin/android/view/GestureDetector#setIsLongpressEnabled(kotlin.Boolean))`(`isLongpressEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether longpress is enabled, if this is enabled when a user presses and holds down you get a longpress event and nothing further. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector#setOnDoubleTapListener(android.view.GestureDetector.OnDoubleTapListener))`(`onDoubleTapListener:` ` [GestureDetector.OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener)?`)` Sets the listener which will be called for double-tap and related gestures. |

## Public constructors

### GestureDetector

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener)
```

Creates a GestureDetector with the supplied listener. You may only use this constructor from a [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?:An [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) or a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) created from [Context.createWindowContext(int, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener):the listener invoked for all the callbacks, this must not be null. If the listener implements the [OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener) or [OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener) then it will also be set as the listener for these callbacks (for example when using the [SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener)). |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](https://developer.android.com/reference/kotlin/android/os/Handler.html#Handler()) 

### GestureDetector

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?)
```

Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?:An [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) or a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) created from [Context.createWindowContext(int, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener):the listener invoked for all the callbacks, this must not be null. If the listener implements the [OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener) or [OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener) then it will also be set as the listener for these callbacks (for example when using the [SimpleOnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.SimpleOnGestureListener)). |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler to use for running deferred listener events. This value may be`null`. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](https://developer.android.com/reference/kotlin/android/os/Handler.html#Handler()) 

### GestureDetector

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?, 
    unused: Boolean)
```

Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?:An [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) or a [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) created from [Context.createWindowContext(int, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#createWindowContext(kotlin.Int,%20android.os.Bundle))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener):the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler to use for running deferred listener events. This value may be`null`. |
| `unused` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):currently not used. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](https://developer.android.com/reference/kotlin/android/os/Handler.html#Handler()) 

### GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(listener: GestureDetector.OnGestureListener)
```

**Deprecated:** *Use [GestureDetector(android.content.Context,android.view.GestureDetector.OnGestureListener)](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.content.Context,%20android.view.GestureDetector.OnGestureListener))instead.*

Creates a GestureDetector with the supplied listener. You may only use this constructor from a UI thread (this is the usual situation).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener):the listener invoked for all the callbacks, this must not be null. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](https://developer.android.com/reference/kotlin/android/os/Handler.html#Handler()) 

### GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?)
```

**Deprecated:** *Use [GestureDetector(android.content.Context,android.view.GestureDetector.OnGestureListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/view/GestureDetector#GestureDetector(android.content.Context,%20android.view.GestureDetector.OnGestureListener,%20android.os.Handler))instead.*

Creates a GestureDetector with the supplied listener. This variant of the constructor should be used from a non-UI thread (as it allows specifying the Handler).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GestureDetector.OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener):the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler to use This value may be`null`. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

## Public methods

### isLongpressEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLongpressEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if longpress is enabled, else false. |

### onGenericMotionEvent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGenericMotionEvent(ev: MotionEvent): Boolean
```

Analyzes the given generic motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) supplied.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The current motion event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) consumed the event, else false. |

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(ev: MotionEvent): Boolean
```

Analyzes the given motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) supplied.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ev` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent):The current motion event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the [OnGestureListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnGestureListener) consumed the event, else false. |

### setContextClickListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContextClickListener(onContextClickListener: GestureDetector.OnContextClickListener?): Unit
```

Sets the listener which will be called for context clicks.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onContextClickListener` | [GestureDetector.OnContextClickListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnContextClickListener)?:the listener invoked for all the callbacks, or null to stop listening for context clicks. |

### setIsLongpressEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIsLongpressEnabled(isLongpressEnabled: Boolean): Unit
```

Set whether longpress is enabled, if this is enabled when a user presses and holds down you get a longpress event and nothing further. If it's disabled the user can press and hold down and then later moved their finger and you will get scroll events. By default longpress is enabled.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------|
| `isLongpressEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether longpress should be enabled. |

### setOnDoubleTapListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDoubleTapListener(onDoubleTapListener: GestureDetector.OnDoubleTapListener?): Unit
```

Sets the listener which will be called for double-tap and related gestures.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onDoubleTapListener` | [GestureDetector.OnDoubleTapListener](https://developer.android.com/reference/kotlin/android/view/GestureDetector.OnDoubleTapListener)?:the listener invoked for all the callbacks, or null to stop listening for double-tap gestures. |
