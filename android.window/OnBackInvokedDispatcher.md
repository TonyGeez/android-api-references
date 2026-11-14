# OnBackInvokedDispatcher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackInvokedDispatcher

Kotlin| [Java](https://developer.android.com/reference/android/window/OnBackInvokedDispatcher "View this page in Java") 
| --- | --- |

```
interface OnBackInvokedDispatcher
```

| [android.window.OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#) |

Dispatcher to register [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) instances for handling back invocations. It also provides interfaces to update the attributes of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback). Attribute updates are proactively pushed to the window manager if they change the dispatch target (a.k.a. the callback to be invoked next), or its behavior.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_DEFAULT](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_DEFAULT:kotlin.Int) Default priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_OVERLAY](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_OVERLAY:kotlin.Int) Priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s for overlays such as menus and navigation drawers that should receive back dispatch before non-overlays. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_SYSTEM_NAVIGATION_OBSERVER](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_SYSTEM_NAVIGATION_OBSERVER:kotlin.Int) Priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s designed to observe system-level back handling. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#registerOnBackInvokedCallback(kotlin.Int,%20android.window.OnBackInvokedCallback))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback)`)` Registers a [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterOnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#unregisterOnBackInvokedCallback(android.window.OnBackInvokedCallback))`(`callback:` ` [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback)`)` Unregisters a [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback). |

## Constants

### PRIORITY_DEFAULT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_DEFAULT: Int
```

Default priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s. 

 Value: 0

### PRIORITY_OVERLAY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_OVERLAY: Int
```

Priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s for overlays such as menus and navigation drawers that should receive back dispatch before non-overlays. 

 Value: 1000000

### PRIORITY_SYSTEM_NAVIGATION_OBSERVER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_SYSTEM_NAVIGATION_OBSERVER: Int
```

Priority level of [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s designed to observe system-level back handling.

Callbacks registered with this priority are invoked only when a back event is not consumed by any other registered [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) with a priority of [PRIORITY_DEFAULT](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_DEFAULT:kotlin.Int) or higher. This means they are called when the system is about to perform its default back navigation action, such as finishing the current activity or executing a back-to-home animation.

These callbacks are purely observational. They do not consume the back event and cannot intercept it. Their invocation has no impact on the normal back navigation flow, making them suitable for logging, analytics, or triggering actions that should not prevent the system's own back handling.

The invocation order for multiple callbacks registered with this priority is undefined.

On API level 36 only, there is a restriction that only one callback with [PRIORITY_SYSTEM_NAVIGATION_OBSERVER](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_SYSTEM_NAVIGATION_OBSERVER:kotlin.Int) can be registered at a time. On API level 37 and higher, the number of registered observer callbacks is unrestricted. 

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

Registers a [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback). Within the same priority level, callbacks are invoked in the reverse order in which they are registered. Higher priority callbacks are invoked before lower priority ones.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The priority of the callback. Value is [android.window.OnBackInvokedDispatcher#PRIORITY_DEFAULT](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_DEFAULT:kotlin.Int), [android.window.OnBackInvokedDispatcher#PRIORITY_OVERLAY](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_OVERLAY:kotlin.Int), or [android.window.OnBackInvokedDispatcher#PRIORITY_SYSTEM_NAVIGATION_OBSERVER](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher#PRIORITY_SYSTEM_NAVIGATION_OBSERVER:kotlin.Int) Value is 0 or greater |
| `callback` | [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback):The callback to be registered. If the callback instance has been already registered, the existing instance (no matter its priority) will be unregistered and registered again. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the priority is negative. |

### unregisterOnBackInvokedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterOnBackInvokedCallback(callback: OnBackInvokedCallback): Unit
```

Unregisters a [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback):The callback to be unregistered. Does nothing if the callback has not been registered. This value cannot be`null`. |
