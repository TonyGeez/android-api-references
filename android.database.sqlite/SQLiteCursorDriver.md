# SQLiteCursorDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteCursorDriver

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteCursorDriver "View this page in Java") 
| --- | --- |

```
interface SQLiteCursorDriver
```

| [android.database.sqlite.SQLiteCursorDriver](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#) |

A driver for SQLiteCursors that is used to create them and gets notified by the cursors it creates on significant events in their lifetimes.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorClosed](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#cursorClosed())`()` Called by a SQLiteCursor when it it closed to destroy this object as well. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorDeactivated](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#cursorDeactivated())`()` Called by a SQLiteCursor when it is released. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorRequeried](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#cursorRequeried(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Called by a SQLiteCursor when it is requeried. |
| --- | --- |
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [query](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#query(android.database.sqlite.SQLiteDatabase.CursorFactory,%20kotlin.Array))`(`factory:` ` [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)!`, `bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Executes the query returning a Cursor over the result set. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBindArguments](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver#setBindArguments(kotlin.Array))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Set new bind arguments. |

## Public methods

### cursorClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cursorClosed(): Unit
```

Called by a SQLiteCursor when it it closed to destroy this object as well. 

### cursorDeactivated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cursorDeactivated(): Unit
```

Called by a SQLiteCursor when it is released. 

### cursorRequeried

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cursorRequeried(cursor: Cursor!): Unit
```

Called by a SQLiteCursor when it is requeried. 

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun query(
    factory: SQLiteDatabase.CursorFactory!, 
    bindArgs: Array<String!>!
): Cursor!
```

Executes the query returning a Cursor over the result set.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `factory` | [SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory)!:The CursorFactory to use when creating the Cursors, or null if standard SQLiteCursors should be returned. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | a Cursor over the result set |

### setBindArguments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBindArguments(bindArgs: Array<String!>!): Unit
```

Set new bind arguments. These will take effect in cursorRequeried().

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bindArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new arguments |
