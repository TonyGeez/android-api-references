# SQLiteTransactionListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteTransactionListener

Kotlin | [Java](../android/database/sqlite/SQLiteTransactionListener.md) 
| --- | --- |

```
interface SQLiteTransactionListener
```

| [android.database.sqlite.SQLiteTransactionListener](../android/database/sqlite/SQLiteTransactionListener.md) |

A listener for transaction events.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBegin](../android/database/sqlite/SQLiteTransactionListener.md))`()` Called immediately after the transaction begins. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCommit](../android/database/sqlite/SQLiteTransactionListener.md))`()` Called immediately before commiting the transaction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRollback](../android/database/sqlite/SQLiteTransactionListener.md))`()` Called if the transaction is about to be rolled back. |
| --- | --- |

## Public methods

### onBegin

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBegin(): Unit
```

Called immediately after the transaction begins. 

### onCommit

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCommit(): Unit
```

Called immediately before commiting the transaction. 

### onRollback

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRollback(): Unit
```

Called if the transaction is about to be rolled back.
