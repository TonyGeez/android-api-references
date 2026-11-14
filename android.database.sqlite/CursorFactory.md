# SQLiteDatabase.CursorFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorFactory

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteDatabase.CursorFactory "View this page in Java") 
| --- | --- |

```
interface CursorFactory
```

| [android.database.sqlite.SQLiteDatabase.CursorFactory](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory#) |

Used to allow returning sub-classes of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) when calling query.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [newCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory#newCursor(android.database.sqlite.SQLiteDatabase,%20android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery))`(`db:` ` [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase)!`, `masterQuery:` ` [SQLiteCursorDriver](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver)!`, `editTable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `query:` ` [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery)!`)` See [SQLiteCursor.SQLiteCursor(SQLiteCursorDriver, String, SQLiteQuery)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#SQLiteCursor(android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery)). |

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

See [SQLiteCursor.SQLiteCursor(SQLiteCursorDriver, String, SQLiteQuery)](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#SQLiteCursor(android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery)).
