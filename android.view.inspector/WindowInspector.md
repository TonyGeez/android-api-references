Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInspector

Kotlin | [Java](https://developer.android.com/reference/android/view/inspector/WindowInspector "View this page in Java") 
| --- | --- |

```
class WindowInspector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inspector.WindowInspector](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#) |

Provides access to window inspection information.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGlobalWindowViewsListener](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#addGlobalWindowViewsListener(java.util.concurrent.Executor,%20java.util.function.Consumer))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `consumer:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!>!>`)` Adds a listener that is notified whenever the value of [getGlobalWindowViews()](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#getGlobalWindowViews()) changes. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!\> | [getGlobalWindowViews](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#getGlobalWindowViews())`()` <br /> |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGlobalWindowViewsListener](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#removeGlobalWindowViewsListener(java.util.function.Consumer))`(`consumer:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!>!>`)` Removes a listener from getting notifications of global window views changes. |
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

Adds a listener that is notified whenever the value of [getGlobalWindowViews()](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#getGlobalWindowViews()) changes. The current value is provided immediately using the provided [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#). The value is initially relayed using the main thread and then posted to the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#). Using a direct [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) and doing heavy calculations can cause performance issues. If this [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#) is already registered, then this method is a no op.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. |
| `consumer` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!\>!\>: This value cannot be `null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#getGlobalWindowViews()> 

### getGlobalWindowViews

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalWindowViews(): MutableList<View!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!> | the list of all window views attached to the current process This value cannot be `null`. |

### removeGlobalWindowViewsListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun removeGlobalWindowViewsListener(consumer: Consumer<MutableList<View!>!>): Unit
```

Removes a listener from getting notifications of global window views changes. If the [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#) is not registered this method is a no op.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `consumer` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!\>!\>: This value cannot be `null`. |

**See Also**

- [#addGlobalWindowViewsListener(Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/inspector/WindowInspector#addGlobalWindowViewsListener(java.util.concurrent.Executor,%20java.util.function.Consumer))
