# SQLiteTransactionListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteTransactionListener

Kotlin | [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteTransactionListener "View this page in Java") 

```
interface SQLiteTransactionListener
```

| [android.database.sqlite.SQLiteTransactionListener](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener#) |

A listener for transaction events.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBegin](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener#onBegin())`()` Called immediately after the transaction begins. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCommit](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener#onCommit())`()` Called immediately before commiting the transaction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRollback](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTransactionListener#onRollback())`()` Called if the transaction is about to be rolled back. |

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
