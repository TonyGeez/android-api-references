Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatabaseUtils

Kotlin | [Java](../android/database/DatabaseUtils.md)
| --- | --- |

```
open class DatabaseUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.DatabaseUtils](../android/database/DatabaseUtils.md) |

Static utility methods for dealing with databases and `https://developer.android.com/reference/kotlin/android/database/Cursor`s.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils.InsertHelper` This class allows users to do multiple inserts into a table using the same statement. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ABORT:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ATTACH:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_BEGIN:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_COMMIT:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_DDL:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_OTHER:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_PRAGMA:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_SELECT:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UNPREPARED:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UPDATE:kotlin.Int` One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#DatabaseUtils()()` <br /> |

| Public methods ||
|---|---|
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#appendEscapedSQLString(java.lang.StringBuilder,%20kotlin.String)(sb: https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#!, sqlString: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Appends an SQL string to the given StringBuilder, including the opening and closing single quotes. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#appendSelectionArgs(kotlin.Array,%20kotlin.Array)(originalValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, newValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Appends one set of selection args to another. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#appendValueToSql(java.lang.StringBuilder,%20kotlin.Any)(sql: https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Appends an Object to an SQL string with the proper escaping, etc. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#bindObjectToProgram(android.database.sqlite.SQLiteProgram,%20kotlin.Int,%20kotlin.Any)(prog: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Binds the given Object to the given SQLiteProgram using the proper typing. |
| open static [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#blobFileDescriptorForQuery(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.Array)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the query on the db and return the blob value in the first column of the first row. |
| open static [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#blobFileDescriptorForQuery(android.database.sqlite.SQLiteStatement,%20kotlin.Array)(prog: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the pre-compiled query and return the blob value in the first column of the first row. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#concatenateWhere(kotlin.String,%20kotlin.String)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Concatenates two SQL WHERE clauses, handling empty or null values. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#createDbFromSqlStatements(android.content.Context,%20kotlin.String,%20kotlin.Int,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, dbName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dbVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sqlStatements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a db and populates it with the sql statements in sqlStatements. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorDoubleToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Double out of a field in a Cursor and writes it to a Map. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorDoubleToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Double out of a column in a Cursor and writes it to a ContentValues. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorDoubleToCursorValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Reads a Double out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorFloatToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Float out of a column in a Cursor and writes it to a ContentValues. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorIntToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Reads an Integer out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorIntToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Integer out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorIntToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Integer out of a column in a Cursor and writes it to a ContentValues. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorLongToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Reads a Long out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorLongToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Long out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorLongToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Long out of a column in a Cursor and writes it to a ContentValues. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorRowToContentValues(android.database.Cursor,%20android.content.ContentValues)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Read the entire contents of a cursor row and store them in a ContentValues. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorShortToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a Short out of a column in a Cursor and writes it to a ContentValues. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorStringToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!)` Reads a String out of a field in a Cursor and writes it to a Map. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorStringToContentValues(android.database.Cursor,%20kotlin.String,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a String out of a field in a Cursor and writes it to a Map. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorStringToContentValuesIfPresent(android.database.Cursor,%20android.content.ContentValues,%20kotlin.String)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, values: https://developer.android.com/reference/kotlin/android/content/ContentValues.html#!, column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Reads a String out of a column in a Cursor and writes it to a ContentValues. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#cursorStringToInsertHelper(android.database.Cursor,%20kotlin.String,%20android.database.DatabaseUtils.InsertHelper,%20kotlin.Int)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, inserter: https://developer.android.com/reference/kotlin/android/database/DatabaseUtils.InsertHelper!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reads a String out of a field in a Cursor and writes it to an InsertHelper. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCurrentRow(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!)` Prints the contents of a Cursor's current row to System. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCurrentRow(android.database.Cursor,%20java.io.PrintStream)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, stream: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#!)` Prints the contents of a Cursor's current row to a PrintSteam. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCurrentRow(android.database.Cursor,%20java.lang.StringBuilder)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, sb: https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#!)` Prints the contents of a Cursor's current row to a StringBuilder. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCurrentRowToString(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!)` Dump the contents of a Cursor's current row to a String. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCursor(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!)` Prints the contents of a Cursor to System. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCursor(android.database.Cursor,%20java.io.PrintStream)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, stream: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#!)` Prints the contents of a Cursor to a PrintSteam. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCursor(android.database.Cursor,%20java.lang.StringBuilder)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!, sb: https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#!)` Prints the contents of a Cursor to a StringBuilder. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#dumpCursorToString(android.database.Cursor)(cursor: https://developer.android.com/reference/kotlin/android/database/Cursor!)` Prints the contents of a Cursor to a String. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getCollationKey(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` return the collation key |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getHexCollationKey(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` return the collation key in hex format |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)(sql: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns one of the following which represent the type of the given SQL statement. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#longForQuery(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.Array)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the query on the db and return the value in the first column of the first row. |
| --- | --- |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#longForQuery(android.database.sqlite.SQLiteStatement,%20kotlin.Array)(prog: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the pre-compiled query and return the value in the first column of the first row. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#queryNumEntries(android.database.sqlite.SQLiteDatabase,%20kotlin.String)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Query the table for the number of rows in the table. |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#queryNumEntries(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.String)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Query the table for the number of rows in the table. |
| --- | --- |
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#queryNumEntries(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.String,%20kotlin.Array)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, table: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Query the table for the number of rows in the table. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#readExceptionFromParcel(android.os.Parcel)(reply: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` Special function for reading an exception result from the header of a parcel, to be used after receiving the result of a transaction. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#readExceptionWithFileNotFoundExceptionFromParcel(android.os.Parcel)(reply: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#readExceptionWithOperationApplicationExceptionFromParcel(android.os.Parcel)(reply: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#sqlEscapeString(kotlin.String)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` SQL-escape a string. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#stringForQuery(android.database.sqlite.SQLiteDatabase,%20kotlin.String,%20kotlin.Array)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, query: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the query on the db and return the value in the first column of the first row. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#stringForQuery(android.database.sqlite.SQLiteStatement,%20kotlin.Array)(prog: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement!, selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Utility method to run the pre-compiled query and return the value in the first column of the first row. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#writeExceptionToParcel(android.os.Parcel,%20java.lang.Exception)(reply: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!, e: https://developer.android.com/reference/kotlin/java/lang/Exception.html#!)` Special function for writing an exception result at the header of a parcel, to be used when returning an exception from a transaction. |

## Constants

### STATEMENT_ABORT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_ABORT: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 6

### STATEMENT_ATTACH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_ATTACH: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 3

### STATEMENT_BEGIN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_BEGIN: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 4

### STATEMENT_COMMIT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_COMMIT: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 5

### STATEMENT_DDL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_DDL: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 8

### STATEMENT_OTHER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_OTHER: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 99

### STATEMENT_PRAGMA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_PRAGMA: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 7

### STATEMENT_SELECT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_SELECT: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 1

### STATEMENT_UNPREPARED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_UNPREPARED: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 9

### STATEMENT_UPDATE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATEMENT_UPDATE: Int
```

One of the values returned by `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#getSqlStatementType(kotlin.String)`.

 Value: 2

## Public constructors

### DatabaseUtils

```
DatabaseUtils()
```

## Public methods

### appendEscapedSQLString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun appendEscapedSQLString(
    sb: StringBuilder!, 
    sqlString: String!
): Unit
```

Appends an SQL string to the given StringBuilder, including the opening and closing single quotes. Any single quotes internal to sqlString will be escaped. This method is deprecated because we want to encourage everyone to use the "?" binding form. However, when implementing a ContentProvider, one may want to add WHERE clauses that were not provided by the caller. Since "?" is a positional form, using it in this case could break the caller because the indexes would be shifted to accomodate the ContentProvider's internal bindings. In that case, it may be necessary to construct a WHERE clause manually. This method is useful for those cases.

| Parameters ||
|---|---|
| `sb` | [StringBuilder](../java/lang/StringBuilder.md)!: the StringBuilder that the SQL string will be appended to |
| `sqlString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the raw string to be appended, which may contain single quotes |

### appendSelectionArgs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun appendSelectionArgs(
    originalValues: Array<String!>!, 
    newValues: Array<String!>!
): Array<String!>!
```

Appends one set of selection args to another. This is useful when adding a selection argument to a user provided set.

### appendValueToSql

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun appendValueToSql(
    sql: StringBuilder!, 
    value: Any!
): Unit
```

Appends an Object to an SQL string with the proper escaping, etc.

### bindObjectToProgram

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun bindObjectToProgram(
    prog: SQLiteProgram!, 
    index: Int, 
    value: Any!
): Unit
```

Binds the given Object to the given SQLiteProgram using the proper typing. For example, bind numbers as longs/doubles, and everything else as a string by call toString() on it.

| Parameters ||
|---|---|
| `prog` | [SQLiteProgram](../android/database/sqlite/SQLiteProgram.md)!: the program to bind the object to |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the 1-based index to bind at |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the value to bind |
| --- | --- |

### blobFileDescriptorForQuery

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun blobFileDescriptorForQuery(
    db: SQLiteDatabase!, 
    query: String!, 
    selectionArgs: Array<String!>!
): ParcelFileDescriptor!
```

Utility method to run the query on the db and return the blob value in the first column of the first row.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#!` | A read-only file descriptor for a copy of the blob value. |

### blobFileDescriptorForQuery

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun blobFileDescriptorForQuery(
    prog: SQLiteStatement!, 
    selectionArgs: Array<String!>!
): ParcelFileDescriptor!
```

Utility method to run the pre-compiled query and return the blob value in the first column of the first row.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#!` | A read-only file descriptor for a copy of the blob value. |

### concatenateWhere

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun concatenateWhere(
    a: String!, 
    b: String!
): String!
```

Concatenates two SQL WHERE clauses, handling empty or null values.

### createDbFromSqlStatements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createDbFromSqlStatements(
    context: Context!, 
    dbName: String!, 
    dbVersion: Int, 
    sqlStatements: String!
): Unit
```

Creates a db and populates it with the sql statements in sqlStatements.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md)!: the context to use to create the db |
| `dbName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the db to create |
| `dbVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the version to set on the db |
| --- | --- |
| `sqlStatements` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the statements to use to populate the db. This should be a single string of the form returned by sqlite3's .dump command (statements separated by semicolons) |

### cursorDoubleToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorDoubleToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!, 
    key: String!
): Unit
```

Reads a Double out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The REAL field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| --- | --- |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key to store the value with in the map |

### cursorDoubleToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorDoubleToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a Double out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorDoubleToCursorValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorDoubleToCursorValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!
): Unit
```

Reads a Double out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The REAL field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| --- | --- |

### cursorFloatToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorFloatToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a Float out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorIntToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorIntToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!
): Unit
```

Reads an Integer out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The INTEGER field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into, with the field as the key |
| --- | --- |

### cursorIntToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorIntToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!, 
    key: String!
): Unit
```

Reads a Integer out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The INTEGER field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into, with the field as the key |
| --- | --- |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key to store the value with in the map |

### cursorIntToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorIntToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a Integer out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorLongToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorLongToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!
): Unit
```

Reads a Long out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The INTEGER field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into, with the field as the key |
| --- | --- |

### cursorLongToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorLongToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!, 
    key: String!
): Unit
```

Reads a Long out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The INTEGER field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| --- | --- |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key to store the value with in the map |

### cursorLongToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorLongToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a Long out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorRowToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorRowToContentValues(
    cursor: Cursor!, 
    values: ContentValues!
): Unit
```

Read the entire contents of a cursor row and store them in a ContentValues.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to read from. |
| `values` | [ContentValues](../android/content/ContentValues.md)!: the `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the row into. |

### cursorShortToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorShortToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a Short out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorStringToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorStringToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!
): Unit
```

Reads a String out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The TEXT field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into, with the field as the key |
| --- | --- |

### cursorStringToContentValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorStringToContentValues(
    cursor: Cursor!, 
    field: String!, 
    values: ContentValues!, 
    key: String!
): Unit
```

Reads a String out of a field in a Cursor and writes it to a Map.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The TEXT field to read |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into, with the field as the key |
| --- | --- |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The key to store the value with in the map |

### cursorStringToContentValuesIfPresent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorStringToContentValuesIfPresent(
    cursor: Cursor!, 
    values: ContentValues!, 
    column: String!
): Unit
```

Reads a String out of a column in a Cursor and writes it to a ContentValues. Adds nothing to the ContentValues if the column isn't present or if its value is null.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `values` | [ContentValues](../android/content/ContentValues.md)!: The `https://developer.android.com/reference/kotlin/android/content/ContentValues.html#` to put the value into |
| `column` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The column to read |
| --- | --- |

### cursorStringToInsertHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cursorStringToInsertHelper(
    cursor: Cursor!, 
    field: String!, 
    inserter: DatabaseUtils.InsertHelper!, 
    index: Int
): Unit
```

Reads a String out of a field in a Cursor and writes it to an InsertHelper.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: The cursor to read from |
| `field` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The TEXT field to read |
| `inserter` | [DatabaseUtils.InsertHelper](../android/database/DatabaseUtils.InsertHelper.md)!: The InsertHelper to bind into |
| --- | --- |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the bind entry in the InsertHelper |

### dumpCurrentRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCurrentRow(cursor: Cursor!): Unit
```

Prints the contents of a Cursor's current row to System.out.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print from |

### dumpCurrentRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCurrentRow(
    cursor: Cursor!, 
    stream: PrintStream!
): Unit
```

Prints the contents of a Cursor's current row to a PrintSteam.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |
| `stream` | [PrintStream](../java/io/PrintStream.md)!: the stream to print to |

### dumpCurrentRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCurrentRow(
    cursor: Cursor!, 
    sb: StringBuilder!
): Unit
```

Prints the contents of a Cursor's current row to a StringBuilder.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |
| `sb` | [StringBuilder](../java/lang/StringBuilder.md)!: the StringBuilder to print to |

### dumpCurrentRowToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCurrentRowToString(cursor: Cursor!): String!
```

Dump the contents of a Cursor's current row to a String.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a String that contains the dumped cursor row |

### dumpCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCursor(cursor: Cursor!): Unit
```

Prints the contents of a Cursor to System.out. The position is restored after printing.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |

### dumpCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCursor(
    cursor: Cursor!, 
    stream: PrintStream!
): Unit
```

Prints the contents of a Cursor to a PrintSteam. The position is restored after printing.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |
| `stream` | [PrintStream](../java/io/PrintStream.md)!: the stream to print to |

### dumpCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCursor(
    cursor: Cursor!, 
    sb: StringBuilder!
): Unit
```

Prints the contents of a Cursor to a StringBuilder. The position is restored after printing.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |
| `sb` | [StringBuilder](../java/lang/StringBuilder.md)!: the StringBuilder to print to |

### dumpCursorToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun dumpCursorToString(cursor: Cursor!): String!
```

Prints the contents of a Cursor to a String. The position is restored after printing.

| Parameters ||
|---|---|
| `cursor` | [Cursor](../android/database/Cursor.md)!: the cursor to print |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a String that contains the dumped cursor |

### getCollationKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getCollationKey(name: String!): String!
```

return the collation key

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the collation key |

### getHexCollationKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getHexCollationKey(name: String!): String!
```

return the collation key in hex format

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the collation key in hex format |

### getSqlStatementType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSqlStatementType(sql: String!): Int
```

Returns one of the following which represent the type of the given SQL statement.

1. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_SELECT:kotlin.Int`
2. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UPDATE:kotlin.Int`
3. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ATTACH:kotlin.Int`
4. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_BEGIN:kotlin.Int`
5. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_COMMIT:kotlin.Int`
6. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ABORT:kotlin.Int`
7. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_PRAGMA:kotlin.Int`
8. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_DDL:kotlin.Int`
9. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UNPREPARED:kotlin.Int`
10. `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_OTHER:kotlin.Int`

<br />

| Parameters ||
|---|---|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the SQL statement whose type is returned by this method |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | one of the values listed above. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_SELECT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UPDATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ATTACH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_BEGIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_COMMIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_ABORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_PRAGMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_DDL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_UNPREPARED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/DatabaseUtils#STATEMENT_OTHER:kotlin.Int` |

### longForQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun longForQuery(
    db: SQLiteDatabase!, 
    query: String!, 
    selectionArgs: Array<String!>!
): Long
```

Utility method to run the query on the db and return the value in the first column of the first row.

### longForQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun longForQuery(
    prog: SQLiteStatement!, 
    selectionArgs: Array<String!>!
): Long
```

Utility method to run the pre-compiled query and return the value in the first column of the first row.

### queryNumEntries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun queryNumEntries(
    db: SQLiteDatabase!, 
    table: String!
): Long
```

Query the table for the number of rows in the table.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!: the database the table is in |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table to query |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of rows in the table |

### queryNumEntries

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun queryNumEntries(
    db: SQLiteDatabase!, 
    table: String!, 
    selection: String!
): Long
```

Query the table for the number of rows in the table.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!: the database the table is in |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table to query |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will count all rows for the given table |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of rows in the table filtered by the selection |

### queryNumEntries

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun queryNumEntries(
    db: SQLiteDatabase!, 
    table: String!, 
    selection: String!, 
    selectionArgs: Array<String!>!
): Long
```

Query the table for the number of rows in the table.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!: the database the table is in |
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table to query |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will count all rows for the given table |
| --- | --- |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: You may include ?s in selection, which will be replaced by the values from selectionArgs, in order that they appear in the selection. The values will be bound as Strings. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of rows in the table filtered by the selection |

### readExceptionFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun readExceptionFromParcel(reply: Parcel!): Unit
```

Special function for reading an exception result from the header of a parcel, to be used after receiving the result of a transaction. This will throw the exception for you if it had been written to the Parcel, otherwise return and let you read the normal result data from the Parcel.

| Parameters ||
|---|---|
| `reply` | [Parcel](../android/os/Parcel.md)!: Parcel to read from |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcel.html#writeNoException()`

### readExceptionWithFileNotFoundExceptionFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun readExceptionWithFileNotFoundExceptionFromParcel(reply: Parcel!): Unit
```

### readExceptionWithOperationApplicationExceptionFromParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun readExceptionWithOperationApplicationExceptionFromParcel(reply: Parcel!): Unit
```

### sqlEscapeString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun sqlEscapeString(value: String!): String!
```

SQL-escape a string.

### stringForQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun stringForQuery(
    db: SQLiteDatabase!, 
    query: String!, 
    selectionArgs: Array<String!>!
): String!
```

Utility method to run the query on the db and return the value in the first column of the first row.

### stringForQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun stringForQuery(
    prog: SQLiteStatement!, 
    selectionArgs: Array<String!>!
): String!
```

Utility method to run the pre-compiled query and return the value in the first column of the first row.

### writeExceptionToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun writeExceptionToParcel(
    reply: Parcel!, 
    e: Exception!
): Unit
```

Special function for writing an exception result at the header of a parcel, to be used when returning an exception from a transaction. exception will be re-thrown by the function in another process

| Parameters ||
|---|---|
| `reply` | [Parcel](../android/os/Parcel.md)!: Parcel to write to |
| `e` | [Exception](../java/lang/Exception.md)!: The Exception to be written. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcel.html#writeNoException()`
- `https://developer.android.com/reference/kotlin/android/os/Parcel.html#writeException(java.lang.Exception)`
