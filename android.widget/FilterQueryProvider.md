# FilterQueryProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterQueryProvider

Kotlin | [Java](FilterQueryProvider.md) 
| --- | --- |

```
interface FilterQueryProvider
```

| [android.widget.FilterQueryProvider](FilterQueryProvider.md) |

This class can be used by external clients of CursorAdapter and CursorTreeAdapter to define how the content of the adapter should be filtered.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Cursor](../android.database/Cursor.md)! | [runQuery](FilterQueryProvider.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Runs a query with the specified constraint. |

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
| [Cursor](../android.database/Cursor.md)! | a Cursor representing the results of the new query |
