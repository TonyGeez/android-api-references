Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MemoryBudgetManager

```
class MemoryBudgetManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.MemoryBudgetManager](MemoryBudgetManager.md) |

This class is the client interface to memory budgets for applications and processes. A memory budget is a promise by the application or one of its processes that its memory requirements will not exceed some limit. The budget is not a hard limit: it can be exceeded but that will likely cause processes to slow down as they try to release memory and drop below the budget limit.

A budget declaration is not a request for memory from the system, nor does the declaration influence how the system allocates memory to a process. Budgets allow an application to monitor its own resource use.

The memory usage tracked against these budgets includes:

- Anonymous allocations, most commonly the Java heap and native heap.
- File-backed pages (such as files mapped into memory or cached by the process).

In the case of memory shared between processes (e.g., shared memory segments), the usage is charged to the first process that maps or allocates it.

The tracked memory usage does *not* include native graphics buffers or DMA-BUFs.

There are two sets of limits on memory, in addition to the budgets managed through this interface. There are system limits and manifest budgets (declared via `<memory-budget>` in the manifest). Budgets managed through this interface may not exceed the system or manifest limits. Any attempt to exceed the system or manifest limits will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. However, the budget set through this interface can be changed at any time, up or down, so long as the new value does not exceed the system or manifest limits.

A budget must be positive; attempting to set a budget that is zero or negative will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.

A package (application) budget applies to all processes in the application as a group (specifically, all processes running under the application's UID). If the application shares a UID with other applications, the budget applies to the aggregate usage of all processes running under that shared UID.

A process budget applies to a single process. It is possible to set a large budget on a process and a small budget on the package; the package budget dominates and the large process budget is irrelevant. This is not an error.

The primary interfaces provided by this class are:

- **Memory Budget Configuration:**
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setPackageBudgetBytes(kotlin.Long)` / `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#clearPackageBudget()` - Sets or clears the memory budget for the application.
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setProcessBudgetBytes(kotlin.Long)` / `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#clearProcessBudget()` - Sets or clears the memory budget for the calling process.
- **Memory Budget Queries:**
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageBudgetBytes()` - Returns the current budget for the application.
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessBudgetBytes()` - Returns the current budget for the calling process.
- **Memory Usage Queries:**
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageCurrentUsageBytes()` - Returns the aggregate memory usage across all processes in the application package.
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessCurrentUsageBytes()` - Returns the memory usage for the caller's specific process.
- **Over-Budget Event Monitoring:**
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener` - Callback interface notified when memory usage exceeds a budget threshold.
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#registerPackageOverBudgetListener(android.os.Looper,%20android.app.MemoryBudgetManager.OnOverBudgetListener)` / `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#unregisterPackageOverBudgetListener(android.app.MemoryBudgetManager.OnOverBudgetListener)` - Registers or unregisters listeners for package-level budget breaches.
 - `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#registerProcessOverBudgetListener(android.os.Looper,%20android.app.MemoryBudgetManager.OnOverBudgetListener)` / `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#unregisterProcessOverBudgetListener(android.app.MemoryBudgetManager.OnOverBudgetListener)` - Registers or unregisters listeners for process-level budget breaches.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener` The callback that is notified when a budget is exceeded. |

| Constants ||
|---|---|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#LIMIT_IS_DISABLED:kotlin.Long` This value is returned by `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageBudgetBytes()` and `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessBudgetBytes()` if there is no memory limit associated with the application or process, respectively. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#clearPackageBudget()()` Removes the package budget, if any, for the caller's application. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#clearProcessBudget()()` Removes the process budget, if any, for the caller's process. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageBudgetBytes()()` Returns the budget for the caller's application. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageCurrentUsageBytes()()` Returns the aggregate memory usage across all processes running under the caller's application UID. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessBudgetBytes()()` Returns the budget for the caller's process. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessCurrentUsageBytes()()` Returns the current memory usage for the caller's process. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#registerPackageOverBudgetListener(android.os.Looper,%20android.app.MemoryBudgetManager.OnOverBudgetListener)(looper: https://developer.android.com/reference/kotlin/android/os/Looper.html#?, listener: https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener)` Registers to be notified if the caller's application exceeds its package budget. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#registerProcessOverBudgetListener(android.os.Looper,%20android.app.MemoryBudgetManager.OnOverBudgetListener)(looper: https://developer.android.com/reference/kotlin/android/os/Looper.html#?, listener: https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener)` Registers to be notified if the caller's process exceeds its process budget. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setPackageBudgetBytes(kotlin.Long)(budgetBytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the memory budget for the caller's application. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setProcessBudgetBytes(kotlin.Long)(budgetBytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the memory budget for the caller's process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#unregisterPackageOverBudgetListener(android.app.MemoryBudgetManager.OnOverBudgetListener)(listener: https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener)` Unregisters a package budget listener. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#unregisterProcessOverBudgetListener(android.app.MemoryBudgetManager.OnOverBudgetListener)(listener: https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener)` Unregisters a process budget listener. |
| --- | --- |

## Constants

### LIMIT_IS_DISABLED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIMIT_IS_DISABLED: Long
```

This value is returned by `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getPackageBudgetBytes()` and `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#getProcessBudgetBytes()` if there is no memory limit associated with the application or process, respectively. This value may not be passed to a function that sets a budget: use the clear functions instead.

 Value: -1L

## Public methods

### clearPackageBudget

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearPackageBudget(): Unit
```

Removes the package budget, if any, for the caller's application. Any manifest budget or system limit that was masked by the package budget is resumed.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not allowed to set budgets, such as from an isolated process |

### clearProcessBudget

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearProcessBudget(): Unit
```

Removes the process budget, if any, for the caller's process. Any manifest budget or system limit that was masked by the process budget is resumed.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller is not allowed to set budgets, such as from an isolated process |

### getPackageBudgetBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageBudgetBytes(): Long
```

Returns the budget for the caller's application. The value returned will be the last value set via `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setPackageBudgetBytes(kotlin.Long)`, if any, or the existing system or manifest limit, if there is no package budget.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | memory limit for the caller's application in bytes; may return `LIMIT_IS_DISABLED` |

### getPackageCurrentUsageBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageCurrentUsageBytes(): Long
```

Returns the aggregate memory usage across all processes running under the caller's application UID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current memory usage in bytes. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if there is an error parsing the current usage value from the underlying memory tracking system. |
| `java.lang.SecurityException` | if the caller is an isolated process or access to the underlying memory tracking system is unavailable. |
| `java.lang.UnsupportedOperationException` | if memory budgets are not supported. |
| --- | --- |

### getProcessBudgetBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProcessBudgetBytes(): Long
```

Returns the budget for the caller's process. The value returned will be the last value set via `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager#setProcessBudgetBytes(kotlin.Long)`, if any, or the existing system or manifest limit, if there is no process budget.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | memory limit for the caller's process in bytes; may return `LIMIT_IS_DISABLED` |

### getProcessCurrentUsageBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProcessCurrentUsageBytes(): Long
```

Returns the current memory usage for the caller's process.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current memory usage in bytes. |

| Exceptions ||
|---|---|
| `java.lang.NumberFormatException` | if there is an error parsing the current usage value from the underlying memory tracking system. |
| `java.lang.SecurityException` | if access to the underlying memory tracking system is unavailable. |
| `java.lang.UnsupportedOperationException` | if memory budgets are not supported. |
| --- | --- |

### registerPackageOverBudgetListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerPackageOverBudgetListener(
    looper: Looper?, 
    listener: MemoryBudgetManager.OnOverBudgetListener
): Unit
```

Registers to be notified if the caller's application exceeds its package budget. The package budget is based on the aggregate memory usage of all processes running under the same UID. An over-budget event can be triggered by memory allocations in any of these processes.

An OnOverBudgetListener callback can only be registered once.

| Parameters ||
|---|---|
| `looper` | [Looper](../android.os/Looper.md)?: `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener` callbacks will be dispatched on this Looper's thread. If `null`, the looper from Looper.getMainLooper() will be used. |
| `listener` | [MemoryBudgetManager.OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md): callback to be notified of an over-budget event. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a looper is not provided and one can't be found on the current thread. |
| `java.lang.IllegalStateException` | if registration fails |
| `java.lang.SecurityException` | if the caller is an isolated process. |
| --- | --- |

### registerProcessOverBudgetListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerProcessOverBudgetListener(
    looper: Looper?, 
    listener: MemoryBudgetManager.OnOverBudgetListener
): Unit
```

Registers to be notified if the caller's process exceeds its process budget. This listener will only be notified of breaches due to memory allocations within the calling process.

An OnOverBudgetListener callback can only be registered once.

| Parameters ||
|---|---|
| `looper` | [Looper](../android.os/Looper.md)?: `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener` callbacks will be dispatched on this Looper's thread. If `null`, the looper from Looper.getMainLooper() will be used. |
| `listener` | [MemoryBudgetManager.OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md): callback to be notified of an over-budget event. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a looper is not provided and one can't be found on the current thread. |
| `java.lang.IllegalStateException` | if registration fails |

### setPackageBudgetBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPackageBudgetBytes(budgetBytes: Long): Unit
```

Sets the memory budget for the caller's application. The budget applies to the cumulative memory use by all processes within the application. This does not affect any budgets for processes within the application.

| Parameters ||
|---|---|
| `budgetBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): declared budget, in bytes. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the budget is invalid. |
| `java.lang.SecurityException` | if the caller is not allowed to set budgets, such as from an isolated process |

### setProcessBudgetBytes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setProcessBudgetBytes(budgetBytes: Long): Unit
```

Sets the memory budget for the caller's process.

| Parameters ||
|---|---|
| `budgetBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): declared budget, in bytes. Value is 0 or greater |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the budget is invalid. |
| `java.lang.SecurityException` | if the caller is not allowed to set budgets, such as from an isolated process |

### unregisterPackageOverBudgetListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterPackageOverBudgetListener(listener: MemoryBudgetManager.OnOverBudgetListener): Unit
```

Unregisters a package budget listener.

| Parameters ||
|---|---|
| `listener` | [MemoryBudgetManager.OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md): The callback to be notified of an over-budget event. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the listener was not registered. |

### unregisterProcessOverBudgetListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterProcessOverBudgetListener(listener: MemoryBudgetManager.OnOverBudgetListener): Unit
```

Unregisters a process budget listener.

| Parameters ||
|---|---|
| `listener` | [MemoryBudgetManager.OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md): The callback to be notified of an over-budget event. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the listener was not registered. |
