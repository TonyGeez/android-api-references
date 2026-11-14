Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteRawStatement

```
class SQLiteRawStatement : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.database.sqlite.SQLiteRawStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#) |

A represents a SQLite prepared statement. The methods correspond very closely to SQLite APIs that operate on a sqlite_stmt object. In general, each API in this class corresponds to a single SQLite API.

A `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#` must be created through a database, and there must be a transaction open at the time. Statements are implicitly closed when the outermost transaction ends, or if the current transaction is marked successful. Statements may be explicitly closed at any time with #close. The #close operation is idempotent and may be called multiple times without harm.

Multiple `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#`s may be open simultaneously. They are independent of each other. Closing one statement does not affect any other statement nor does it have any effect on the enclosing transaction.

Once a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#` has been closed, no further database operations are permitted on that statement. An `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown if a database operation is attempted on a closed statement.

All operations on a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#` must be invoked from the thread that created it. A `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` will be thrown if cross-thread use is detected.

A common pattern for statements is try-with-resources.

```kotlin
<code>
  // Begin a transaction.
  database.beginTransaction();
  try (SQLiteRawStatement statement = database.createRawStatement("SELECT * FROM ...")) {
      while (statement.step()) {
          // Fetch columns from the result rows.
      }
      database.setTransactionSuccessful();
  } finally {
      database.endTransaction();
  }
  </code>
```
Note that `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#` is unrelated to `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_BLOB:kotlin.Int` The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_BLOB. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_FLOAT:kotlin.Int` The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_FLOAT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_INTEGER:kotlin.Int` The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_INTEGER. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_NULL:kotlin.Int` The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_NULL. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_TEXT:kotlin.Int` The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_TEXT. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindBlob(kotlin.Int,%20kotlin.ByteArray)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Bind a blob to a parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindBlob(kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Bind a blob to a parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindDouble(kotlin.Int,%20kotlin.Double)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Bind a double to a parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindInt(kotlin.Int,%20kotlin.Int)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Bind an int to a parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindLong(kotlin.Int,%20kotlin.Long)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Bind a long to the parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindNull(kotlin.Int)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Bind a null to the parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#bindText(kotlin.Int,%20kotlin.String)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Bind a string to the parameter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#clearBindings()()` Clear all parameter bindings. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#close()()` Close the object and release any native resources. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnBlob(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the column value of the result row as a blob. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnDouble(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the column value as a double. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnInt(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the column value as a int. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnLength(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the length of the column value in the result row. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnLong(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the column value as a long. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnName(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the name of the column in the result row. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnText(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the column value as a text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the type of the column in the result row. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getParameterCount()()` Return the number of parameters in the statement. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getParameterIndex(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return the index of the parameter with specified name. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getParameterName(kotlin.Int)(parameterIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the name of the parameter at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getResultColumnCount()()` Return the number of columns in the result set for the statement. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#isOpen()()` Return true if the statement is still open and false otherwise. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#readColumnBlob(kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, buffer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy the column value of the result row, interpreted as a blob, into the buffer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#reset()()` Reset the statement. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#step()()` Step to the next result row. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#toString()()` Returns a string representation of the object. |

## Constants

### SQLITE_DATA_TYPE_BLOB

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_DATA_TYPE_BLOB: Int
```

The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_BLOB.

 Value: 4

### SQLITE_DATA_TYPE_FLOAT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_DATA_TYPE_FLOAT: Int
```

The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_FLOAT.

 Value: 2

### SQLITE_DATA_TYPE_INTEGER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_DATA_TYPE_INTEGER: Int
```

The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_INTEGER.

 Value: 1

### SQLITE_DATA_TYPE_NULL

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_DATA_TYPE_NULL: Int
```

The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_NULL.

 Value: 5

### SQLITE_DATA_TYPE_TEXT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SQLITE_DATA_TYPE_TEXT: Int
```

The constant returned by `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#getColumnType(kotlin.Int)` when the column value is SQLITE_TEXT.

 Value: 3

## Public methods

### bindBlob

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindBlob(
    parameterIndex: Int, 
    value: ByteArray
): Unit
```

Bind a blob to a parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The value to be bound to the parameter. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindBlob

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindBlob(
    parameterIndex: Int, 
    value: ByteArray, 
    offset: Int, 
    length: Int
): Unit
```

Bind a blob to a parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds. The sub-array value\[offset\] to value\[offset+length-1\] is bound.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): The value to be bound to the parameter. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An offset into the value array |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to bind from the value array. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalArgumentException` | if the sub-array exceeds the bounds of the value array. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindDouble

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindDouble(
    parameterIndex: Int, 
    value: Double
): Unit
```

Bind a double to a parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The value to be bound to the parameter. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindInt

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindInt(
    parameterIndex: Int, 
    value: Int
): Unit
```

Bind an int to a parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindLong

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindLong(
    parameterIndex: Int, 
    value: Long
): Unit
```

Bind a long to the parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds.

| Parameters ||
|---|---|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The value to be bound to the parameter. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindNull

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindNull(parameterIndex: Int): Unit
```

Bind a null to the parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### bindText

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun bindText(
    parameterIndex: Int, 
    value: String
): Unit
```

Bind a string to the parameter. Parameter indices start at 1. The function throws if the parameter index is out of bounds. The string may not be null.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter in the query. It is one-based. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The value to be bound to the parameter. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the parameter is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### clearBindings

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearBindings(): Unit
```

Clear all parameter bindings.

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### close

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Close the object and release any native resources. It is not an error to call this on an already-closed object.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### getColumnBlob

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnBlob(columnIndex: Int): ByteArray?
```

Return the column value of the result row as a blob. Column indices start at 0. This throws an exception if column is not in the result. This returns null if the column value is null. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_BLOB:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The value of the column as a blob, or null if the column is NULL. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnDouble

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnDouble(columnIndex: Int): Double
```

Return the column value as a double. Column indices start at 0. This throws an exception if column is not in the result. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_FLOAT:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | The value of a column as a double. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnInt

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnInt(columnIndex: Int): Int
```

Return the column value as a int. Column indices start at 0. This throws an exception if column is not in the result. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_INTEGER:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The value of the column as an int. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnLength(columnIndex: Int): Int
```

Return the length of the column value in the result row. Column indices start at 0. This returns 0 for a null and number of bytes for text or blob. Numeric values are converted to a string and the length of the string is returned. See the sqlite documentation for details. Note that this cannot be used to distinguish a null value from an empty text or blob. Note that this returns the number of bytes in the text value, not the number of characters.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The length, in bytes, of the value in the column. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnLong

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnLong(columnIndex: Int): Long
```

Return the column value as a long. Column indices start at 0. This throws an exception if column is not in the result. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_INTEGER:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The value of the column as an long. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnName(columnIndex: Int): String
```

Return the name of the column in the result row. Column indices start at 0. This throws an exception if column is not in the result.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the column in the result row. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `android.database.sqlite.SQLiteOutOfMemoryException` | if the database cannot allocate memory for the name. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnText

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnText(columnIndex: Int): String?
```

Return the column value as a text. Column indices start at 0. This throws an exception if column is not in the result. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_TEXT:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The value of the column as a string, or `null` when the column value is NULL. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getColumnType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getColumnType(columnIndex: Int): Int
```

Return the type of the column in the result row. Column indices start at 0.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The type of the value in the column of the result row. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_INTEGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_FLOAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_TEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_BLOB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_NULL:kotlin.Int` |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getParameterCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameterCount(): Int
```

Return the number of parameters in the statement.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of parameters in the statement. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getParameterIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameterIndex(name: String): Int
```

Return the index of the parameter with specified name. If the name does not match any parameter, 0 is returned.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of a parameter. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the parameter or 0 if the name does not identify a parameter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getParameterName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameterName(parameterIndex: Int): String?
```

Return the name of the parameter at the specified index. Null is returned if there is no such parameter or if the parameter does not have a name.

| Parameters ||
|---|---|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the parameter. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The name of the parameter. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### getResultColumnCount

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultColumnCount(): Int
```

Return the number of columns in the result set for the statement.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of columns in the result set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### isOpen

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOpen(): Boolean
```

Return true if the statement is still open and false otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the statement is open. |

### readColumnBlob

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readColumnBlob(
    columnIndex: Int, 
    buffer: ByteArray, 
    offset: Int, 
    length: Int, 
    srcOffset: Int
): Int
```

Copy the column value of the result row, interpreted as a blob, into the buffer. Column indices start at 0. This throws an exception if column is not in the result row. Bytes are copied into the buffer starting at the offset. Bytes are copied from the blob starting at srcOffset. Length bytes are copied unless the column value has fewer bytes available. The function returns the number of bytes copied. The column value will be converted if it is not of type `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteRawStatement#SQLITE_DATA_TYPE_BLOB:kotlin.Int`; see the sqlite documentation for details.

| Parameters ||
|---|---|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of a column in the result row. It is zero-based. |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): A pre-allocated array to be filled with the value of the column. This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An offset into the buffer: copying starts here. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to copy. |
| `srcOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset into the blob from which to start copying. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of bytes that were copied. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteBindOrColumnIndexOutOfRangeException` | if the column is out of range. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `android.database.sqlite.SQLiteMisuseException` | if the row has no data. See #getColumnType(). |
| `java.lang.IllegalArgumentException` | if the buffer is too small for offset+length. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### reset

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reset(): Unit
```

Reset the statement.

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### step

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun step(): Boolean
```

Step to the next result row. This returns true if the statement stepped to a new row, and false if the statement is done. The method throws on any other result, including a busy or locked database. If WAL is enabled then the database should never be locked or busy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if a row is available and false otherwise. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteDatabaseLockedException` | if the database is locked or busy. |
| `android.database.sqlite.SQLiteException` | if a native error occurs. |
| `java.lang.IllegalStateException` | if the statement is closed or this is a foreign thread. |

**See Also**

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
