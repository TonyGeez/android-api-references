# SQLiteDatabase.CursorFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorFactory

Kotlin| [Java](../android/database/sqlite/SQLiteDatabase.CursorFactory.md) 
| --- | --- |

```
interface CursorFactory
```

| [android.database.sqlite.SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md) |

Used to allow returning sub-classes of [Cursor](../android/database/Cursor.md) when calling query.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Cursor](../android/database/Cursor.md)! | [newCursor](../android/database/sqlite/SQLiteDatabase.CursorFactory.md))`(`db:` ` [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!`, `masterQuery:` ` [SQLiteCursorDriver](../android/database/sqlite/SQLiteCursorDriver.md)!`, `editTable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `query:` ` [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md)!`)` See [SQLiteCursor.SQLiteCursor(SQLiteCursorDriver, String, SQLiteQuery)](../android/database/sqlite/SQLiteCursor.md)). |

## Public methods

### newCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newCursor(
    db: SQLiteDatabase!, 
    masterQuery: SQLiteCursorDriver!, 
    editTable: String!, 
    query: SQLiteQuery!
): Cursor!
```

See [SQLiteCursor.SQLiteCursor(SQLiteCursorDriver, String, SQLiteQuery)](../android/database/sqlite/SQLiteCursor.md)).
