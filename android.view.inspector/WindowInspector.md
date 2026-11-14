Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInspector

Kotlin | [Java](WindowInspector.md) 
| --- | --- |

```
class WindowInspector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inspector.WindowInspector](WindowInspector.md) |

Provides access to window inspection information.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGlobalWindowViewsListener](WindowInspector.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `consumer:` ` [Consumer](../java.util.function/Consumer.md)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android.view/View.md)!>!>`)` Adds a listener that is notified whenever the value of [getGlobalWindowViews()](WindowInspector.md)) changes. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android.view/View.md)!\> | [getGlobalWindowViews](WindowInspector.md))`()` <br /> |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGlobalWindowViewsListener](WindowInspector.md))`(`consumer:` ` [Consumer](../java.util.function/Consumer.md)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android.view/View.md)!>!>`)` Removes a listener from getting notifications of global window views changes. |
| --- | --- |

## Public methods

### addGlobalWindowViewsListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addGlobalWindowViewsListener(
    executor: Executor, 
    consumer: Consumer<MutableList<View!>!>
): Unit
```

Adds a listener that is notified whenever the value of [getGlobalWindowViews()](WindowInspector.md)) changes. The current value is provided immediately using the provided [Executor](../java.util.concurrent/Executor.md). The value is initially relayed using the main thread and then posted to the [Executor](../java.util.concurrent/Executor.md). Using a direct [Executor](../java.util.concurrent/Executor.md) and doing heavy calculations can cause performance issues. If this [Consumer](../java.util.function/Consumer.md) is already registered, then this method is a no op.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. |
| `consumer` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android.view/View.md)!\>!\>: This value cannot be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#getGlobalWindowViews()> 

### getGlobalWindowViews

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalWindowViews(): MutableList<View!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android.view/View.md)!> | the list of all window views attached to the current process This value cannot be `null`. |

### removeGlobalWindowViewsListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun removeGlobalWindowViewsListener(consumer: Consumer<MutableList<View!>!>): Unit
```

Removes a listener from getting notifications of global window views changes. If the [Consumer](../java.util.function/Consumer.md) is not registered this method is a no op.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `consumer` | [Consumer](../java.util.function/Consumer.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android.view/View.md)!\>!\>: This value cannot be `null`. |

**See Also**

- [#addGlobalWindowViewsListener(Executor, Consumer)](WindowInspector.md))
