Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnOverBudgetListener

```
interface OnOverBudgetListener
```

| [android.app.MemoryBudgetManager.OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md) |

The callback that is notified when a budget is exceeded.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener#onOverBudget(kotlin.Long)(budget: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Invoked when the application or process exceeds it budget. |

## Public methods

### onOverBudget

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onOverBudget(budget: Long): Unit
```

Invoked when the application or process exceeds it budget.

| Parameters ||
|---|---|
| `budget` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): budget (in bytes) that was exceeded. |
