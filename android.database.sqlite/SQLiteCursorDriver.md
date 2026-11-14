# SQLiteCursorDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteCursorDriver

Kotlin| [Java](SQLiteCursorDriver.md) 
| --- | --- |

```
interface SQLiteCursorDriver
```

| [android.database.sqlite.SQLiteCursorDriver](SQLiteCursorDriver.md) |

A driver for SQLiteCursors that is used to create them and gets notified by the cursors it creates on significant events in their lifetimes.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorClosed](SQLiteCursorDriver.md))`()` Called by a SQLiteCursor when it it closed to destroy this object as well. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorDeactivated](SQLiteCursorDriver.md))`()` Called by a SQLiteCursor when it is released. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorRequeried](SQLiteCursorDriver.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` Called by a SQLiteCursor when it is requeried. |
| --- | --- |
| abstract [Cursor](../android.database/Cursor.md)! | [query](SQLiteCursorDriver.md))`(`factory:` ` [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)!`, `bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Executes the query returning a Cursor over the result set. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBindArguments](SQLiteCursorDriver.md))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Set new bind arguments. |

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
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)!:The CursorFactory to use when creating the Cursors, or null if standard SQLiteCursors should be returned. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------|
| [Cursor](../android.database/Cursor.md)! | a Cursor over the result set |

### setBindArguments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBindArguments(bindArgs: Array<String!>!): Unit
```

Set new bind arguments. These will take effect in cursorRequeried().

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bindArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new arguments |
