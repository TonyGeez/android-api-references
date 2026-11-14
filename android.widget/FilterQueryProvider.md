# FilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterQueryProvider

Kotlin | [Java](https://developer.android.com/reference/android/widget/FilterQueryProvider "View this page in Java") 

```
interface FilterQueryProvider
```

| [android.widget.FilterQueryProvider](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider#) |

This class can be used by external clients of CursorAdapter and CursorTreeAdapter to define how the content of the adapter should be filtered.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [runQuery](https://developer.android.com/reference/kotlin/android/widget/FilterQueryProvider#runQuery(kotlin.CharSequence))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. |

## Public methods

### runQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runQuery(constraint: CharSequence!): Cursor!
```

Runs a query with the specified constraint. This query is requested by the filter attached to this adapter. Contract: when constraint is null or empty, the original results, prior to any filtering, must be returned.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `constraint` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the constraint with which the query must be filtered |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a Cursor representing the results of the new query |
