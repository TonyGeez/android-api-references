# OnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackInvokedDispatcher

Kotlin| [Java](../android/window/OnBackInvokedDispatcher.md) 
| --- | --- |

```
interface OnBackInvokedDispatcher
```

| [android.window.OnBackInvokedDispatcher](../android/window/OnBackInvokedDispatcher.md) |

Dispatcher to register [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) instances for handling back invocations. It also provides interfaces to update the attributes of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md). Attribute updates are proactively pushed to the window manager if they change the dispatch target (a.k.a. the callback to be invoked next), or its behavior.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_DEFAULT](../android/window/OnBackInvokedDispatcher.md) Default priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_OVERLAY](../android/window/OnBackInvokedDispatcher.md) Priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s for overlays such as menus and navigation drawers that should receive back dispatch before non-overlays. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_SYSTEM_NAVIGATION_OBSERVER](../android/window/OnBackInvokedDispatcher.md) Priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s designed to observe system-level back handling. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnBackInvokedCallback](../android/window/OnBackInvokedDispatcher.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md)`)` Registers a [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnBackInvokedCallback](../android/window/OnBackInvokedDispatcher.md))`(`callback:` ` [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md)`)` Unregisters a [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md). |

## Constants

### PRIORITY_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_DEFAULT: Int
```

Default priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s. 

 Value: 0

### PRIORITY_OVERLAY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_OVERLAY: Int
```

Priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s for overlays such as menus and navigation drawers that should receive back dispatch before non-overlays. 

 Value: 1000000

### PRIORITY_SYSTEM_NAVIGATION_OBSERVER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_SYSTEM_NAVIGATION_OBSERVER: Int
```

Priority level of [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) s designed to observe system-level back handling.

Callbacks registered with this priority are invoked only when a back event is not consumed by any other registered [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md) with a priority of [PRIORITY_DEFAULT](../android/window/OnBackInvokedDispatcher.md) or higher. This means they are called when the system is about to perform its default back navigation action, such as finishing the current activity or executing a back-to-home animation.

These callbacks are purely observational. They do not consume the back event and cannot intercept it. Their invocation has no impact on the normal back navigation flow, making them suitable for logging, analytics, or triggering actions that should not prevent the system's own back handling.

The invocation order for multiple callbacks registered with this priority is undefined.

On API level 36 only, there is a restriction that only one callback with [PRIORITY_SYSTEM_NAVIGATION_OBSERVER](../android/window/OnBackInvokedDispatcher.md) can be registered at a time. On API level 37 and higher, the number of registered observer callbacks is unrestricted. 

 Value: -2

## Public methods

### registerOnBackInvokedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOnBackInvokedCallback(
    priority: Int, 
    callback: OnBackInvokedCallback
): Unit
```

Registers a [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md). Within the same priority level, callbacks are invoked in the reverse order in which they are registered. Higher priority callbacks are invoked before lower priority ones.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The priority of the callback. Value is [android.window.OnBackInvokedDispatcher#PRIORITY_DEFAULT](../android/window/OnBackInvokedDispatcher.md), [android.window.OnBackInvokedDispatcher#PRIORITY_OVERLAY](../android/window/OnBackInvokedDispatcher.md), or [android.window.OnBackInvokedDispatcher#PRIORITY_SYSTEM_NAVIGATION_OBSERVER](../android/window/OnBackInvokedDispatcher.md) Value is 0 or greater |
| `callback` | [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md):The callback to be registered. If the callback instance has been already registered, the existing instance (no matter its priority) will be unregistered and registered again. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the priority is negative. |

### unregisterOnBackInvokedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterOnBackInvokedCallback(callback: OnBackInvokedCallback): Unit
```

Unregisters a [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [OnBackInvokedCallback](../android/window/OnBackInvokedCallback.md):The callback to be unregistered. Does nothing if the callback has not been registered. This value cannot be`null`. |
