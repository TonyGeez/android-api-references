# GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureDetector

Kotlin| [Java](GestureDetector.md) 
| --- | --- |

```
open class GestureDetector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.GestureDetector](GestureDetector.md) |

Detects various gestures and events using the supplied [MotionEvent](MotionEvent.md) s. The [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) callback will notify users when a particular motion event has occurred. This class should only be used with [MotionEvent](MotionEvent.md) s reported via touch (don't use for trackball events). To use this class:

- Create an instance of the`GestureDetector`for your [View](View.md)
- In the [View.onTouchEvent(MotionEvent)](View.md))method ensure you call [onTouchEvent(android.view.MotionEvent)](GestureDetector.md)). The methods defined in your callback will be executed when the events occur.
- If listening for [OnContextClickListener.onContextClick(MotionEvent)](../android/view/GestureDetector.OnContextClickListener.md))you must call [onGenericMotionEvent(android.view.MotionEvent)](GestureDetector.md))in [View.onGenericMotionEvent(MotionEvent)](View.md)).

<br />

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md) The listener that is used to notify when a context click occurs. |
| abstract | [OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md) The listener that is used to notify when a double-tap or a confirmed single-tap occur. |
| abstract | [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) The listener that is used to notify when gestures occur. |
| --- | --- |
| open | [SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md) A convenience class to extend when you only want to listen for a subset of all the gestures. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GestureDetector](GestureDetector.md))`(`context:` ` [Context](../android.content/Context.md)?`, `listener:` ` [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md)`)` Creates a GestureDetector with the supplied listener. |
| [GestureDetector](GestureDetector.md))`(`context:` ` [Context](../android.content/Context.md)?`, `listener:` ` [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](../android.os/Handler.md). |
| [GestureDetector](GestureDetector.md))`(`context:` ` [Context](../android.content/Context.md)?`, `listener:` ` [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`, `unused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](../android.os/Handler.md). |
| [GestureDetector](GestureDetector.md))`(`listener:` ` [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md)`)` Creates a GestureDetector with the supplied listener. |
| [GestureDetector](GestureDetector.md))`(`listener:` ` [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Creates a GestureDetector with the supplied listener. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLongpressEnabled](GestureDetector.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](GestureDetector.md))`(`ev:` ` [MotionEvent](MotionEvent.md)`)` Analyzes the given generic motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) supplied. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](GestureDetector.md))`(`ev:` ` [MotionEvent](MotionEvent.md)`)` Analyzes the given motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) supplied. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContextClickListener](GestureDetector.md))`(`onContextClickListener:` ` [GestureDetector.OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md)?`)` Sets the listener which will be called for context clicks. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIsLongpressEnabled](GestureDetector.md))`(`isLongpressEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether longpress is enabled, if this is enabled when a user presses and holds down you get a longpress event and nothing further. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDoubleTapListener](GestureDetector.md))`(`onDoubleTapListener:` ` [GestureDetector.OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md)?`)` Sets the listener which will be called for double-tap and related gestures. |
| --- | --- |

## Public constructors

### GestureDetector

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener)
```

Creates a GestureDetector with the supplied listener. You may only use this constructor from a [Looper](../android.os/Looper.md) thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)?:An [Activity](../android.app/Activity.md) or a [Context](../android.content/Context.md) created from [Context.createWindowContext(int, Bundle)](../android.content/Context.md))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md):the listener invoked for all the callbacks, this must not be null. If the listener implements the [OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md) or [OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md) then it will also be set as the listener for these callbacks (for example when using the [SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md)). |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](../android.os/Handler.md)) 

### GestureDetector

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?)
```

Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](../android.os/Handler.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)?:An [Activity](../android.app/Activity.md) or a [Context](../android.content/Context.md) created from [Context.createWindowContext(int, Bundle)](../android.content/Context.md))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md):the listener invoked for all the callbacks, this must not be null. If the listener implements the [OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md) or [OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md) then it will also be set as the listener for these callbacks (for example when using the [SimpleOnGestureListener](../android/view/GestureDetector.SimpleOnGestureListener.md)). |
| `handler` | [Handler](../android.os/Handler.md)?:the handler to use for running deferred listener events. This value may be`null`. |
| --- | --- |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](../android.os/Handler.md)) 

### GestureDetector

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    context: Context?, 
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?, 
    unused: Boolean)
```

Creates a GestureDetector with the supplied listener that runs deferred events on the thread associated with the supplied [Handler](../android.os/Handler.md).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)?:An [Activity](../android.app/Activity.md) or a [Context](../android.content/Context.md) created from [Context.createWindowContext(int, Bundle)](../android.content/Context.md))This value may be`null`. |
| `listener` | [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md):the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](../android.os/Handler.md)?:the handler to use for running deferred listener events. This value may be`null`. |
| --- | --- |
| `unused` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):currently not used. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](../android.os/Handler.md)) 

### GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(listener: GestureDetector.OnGestureListener)
```

**Deprecated:** *Use [GestureDetector(android.content.Context,android.view.GestureDetector.OnGestureListener)](GestureDetector.md))instead.*

Creates a GestureDetector with the supplied listener. You may only use this constructor from a UI thread (this is the usual situation).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md):the listener invoked for all the callbacks, this must not be null. |

| Exceptions ||
|----------------------------------|----------------------|
| `java.lang.NullPointerException` | if`listener`is null. |

**See Also**

- [android.os.Handler#Handler()](../android.os/Handler.md)) 

### GestureDetector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureDetector(
    listener: GestureDetector.OnGestureListener, 
    handler: Handler?)
```

**Deprecated:** *Use [GestureDetector(android.content.Context,android.view.GestureDetector.OnGestureListener,android.os.Handler)](GestureDetector.md))instead.*

Creates a GestureDetector with the supplied listener. This variant of the constructor should be used from a non-UI thread (as it allows specifying the Handler).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GestureDetector.OnGestureListener](../android/view/GestureDetector.OnGestureListener.md):the listener invoked for all the callbacks, this must not be null. |
| `handler` | [Handler](../android.os/Handler.md)?:the handler to use This value may be`null`. |

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

Analyzes the given generic motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) supplied.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ev` | [MotionEvent](MotionEvent.md):The current motion event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) consumed the event, else false. |

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(ev: MotionEvent): Boolean
```

Analyzes the given motion event and if applicable triggers the appropriate callbacks on the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) supplied.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `ev` | [MotionEvent](MotionEvent.md):The current motion event. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the [OnGestureListener](../android/view/GestureDetector.OnGestureListener.md) consumed the event, else false. |

### setContextClickListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContextClickListener(onContextClickListener: GestureDetector.OnContextClickListener?): Unit
```

Sets the listener which will be called for context clicks.

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onContextClickListener` | [GestureDetector.OnContextClickListener](../android/view/GestureDetector.OnContextClickListener.md)?:the listener invoked for all the callbacks, or null to stop listening for context clicks. |

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
| `onDoubleTapListener` | [GestureDetector.OnDoubleTapListener](../android/view/GestureDetector.OnDoubleTapListener.md)?:the listener invoked for all the callbacks, or null to stop listening for double-tap gestures. |
