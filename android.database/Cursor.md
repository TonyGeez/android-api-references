# Cursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cursor

Kotlin| [Java](Cursor.md) 
| --- | --- |

```
interface Cursor : Closeable
```

| [android.database.Cursor](Cursor.md) |

| Known Direct Subclasses [CrossProcessCursor](CrossProcessCursor.md), [CursorWrapper](CursorWrapper.md), [MockCursor](../android.test.mock/MockCursor.md) |----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CrossProcessCursor](CrossProcessCursor.md) | A cross process cursor is an extension of a [Cursor](Cursor.md) that also supports usage from remote processes. | | [CursorWrapper](CursorWrapper.md) | Wrapper class for Cursor that delegates all calls to the actual cursor object. | | [MockCursor](../android.test.mock/MockCursor.md) | A mock [android.database.Cursor](Cursor.md) class that isolates the test code from real Cursor implementation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractCursor](AbstractCursor.md), [AbstractWindowedCursor](AbstractWindowedCursor.md), [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md), [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md), [MatrixCursor](MatrixCursor.md), [MergeCursor](MergeCursor.md), [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) |------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractCursor](AbstractCursor.md) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. | | [AbstractWindowedCursor](AbstractWindowedCursor.md) | A base class for Cursors that store their data in [CursorWindow](CursorWindow.md) s. | | [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) | Cursor wrapper that implements [CrossProcessCursor](CrossProcessCursor.md). | | [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) | Cursor wrapper that implements [CrossProcessCursor](CrossProcessCursor.md). | | [MatrixCursor](MatrixCursor.md) | A mutable cursor implementation backed by an array of`Object`s. | | [MergeCursor](MergeCursor.md) | A convenience class that lets you present an array of Cursors as a single linear Cursor. | | [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](../android.database.sqlite/SQLiteDatabase.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface provides random read-write access to the result set returned by a database query.

Cursor implementations are not required to be synchronized so code using a Cursor from multiple threads should perform its own synchronization when using the Cursor.

Implementations should subclass [AbstractCursor](AbstractCursor.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](Cursor.md) Value returned by [getType(int)](Cursor.md))if the specified column type is blob |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](Cursor.md) Value returned by [getType(int)](Cursor.md))if the specified column type is float |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](Cursor.md) Value returned by [getType(int)](Cursor.md))if the specified column type is integer |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](Cursor.md) Value returned by [getType(int)](Cursor.md))if the specified column is null |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](Cursor.md) Value returned by [getType(int)](Cursor.md))if the specified column type is string |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Cursor.md))`()` Closes the Cursor, releasing all of its resources and making it completely invalid. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](CharArrayBuffer.md)!`)` Retrieves the requested column text and stores it in the buffer provided. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](Cursor.md))`()` Deactivates the Cursor, making all calls on it fail until [requery](Cursor.md))is called. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a byte array. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](Cursor.md))`()` Return total number of columns |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](Cursor.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the zero-based index for the given column name, or -1 if the column doesn't exist. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](Cursor.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the zero-based index for the given column name, or throws [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if the column doesn't exist. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the column name at the given zero-based column index. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getColumnNames](Cursor.md))`()` Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](Cursor.md))`()` Returns the numbers of rows in the cursor. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a double. |
| abstract [Bundle](../android.os/Bundle.md)! | [getExtras](Cursor.md))`()` Returns a bundle of extra values. |
| --- | --- |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a float. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as an int. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a long. |
| --- | --- |
| abstract [Uri](../android.net/Uri.md)! | [getNotificationUri](Cursor.md))`()` Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUri](Cursor.md)). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>? | [getNotificationUris](Cursor.md))`()` Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUris](Cursor.md)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](Cursor.md))`()` Returns the current position of the cursor in the row set. |
| --- | --- |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a short. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a String. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns data type of the given column's value. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](Cursor.md))`()` onMove() will only be called across processes if this method returns true. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](Cursor.md))`()` Returns whether the cursor is pointing to the position after the last row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](Cursor.md))`()` Returns whether the cursor is pointing to the position before the first row. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](Cursor.md))`()` return true if the cursor is closed |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](Cursor.md))`()` Returns whether the cursor is pointing to the first row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](Cursor.md))`()` Returns whether the cursor is pointing to the last row. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](Cursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if the value in the indicated column is null. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](Cursor.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Move the cursor by a relative amount, forward or backward, from the current position. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](Cursor.md))`()` Move the cursor to the first row. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](Cursor.md))`()` Move the cursor to the last row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](Cursor.md))`()` Move the cursor to the next row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](Cursor.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Move the cursor to an absolute position. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](Cursor.md))`()` Move the cursor to the previous row. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](Cursor.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` Register an observer that is called when changes happen to the content backing this cursor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](Cursor.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via [requery()](Cursor.md)), [deactivate()](Cursor.md)), or #close(). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](Cursor.md))`()` Performs the query that created the cursor again, refreshing its contents. |
| abstract [Bundle](../android.os/Bundle.md)! | [respond](Cursor.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` This is an out-of-band way for the user of a cursor to communicate with the cursor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](Cursor.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` Sets a [Bundle](../android.os/Bundle.md) that will be returned by [getExtras()](Cursor.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](Cursor.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` Register to watch a content URI for changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](Cursor.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>`)` Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md)), except this version allows to watch multiple content URIs for changes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](Cursor.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` Unregister an observer that has previously been registered with this cursor via [registerContentObserver](Cursor.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](Cursor.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` Unregister an observer that has previously been registered with this cursor via [registerContentObserver](Cursor.md)). |

## Constants

### FIELD_TYPE_BLOB

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_BLOB: Int
```

Value returned by [getType(int)](Cursor.md))if the specified column type is blob 

 Value: 4

### FIELD_TYPE_FLOAT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_FLOAT: Int
```

Value returned by [getType(int)](Cursor.md))if the specified column type is float 

 Value: 2

### FIELD_TYPE_INTEGER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_INTEGER: Int
```

Value returned by [getType(int)](Cursor.md))if the specified column type is integer 

 Value: 1

### FIELD_TYPE_NULL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_NULL: Int
```

Value returned by [getType(int)](Cursor.md))if the specified column is null 

 Value: 0

### FIELD_TYPE_STRING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_STRING: Int
```

Value returned by [getType(int)](Cursor.md))if the specified column type is string 

 Value: 3

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike [deactivate()](Cursor.md))a call to [requery()](Cursor.md))will not make the Cursor valid again.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### copyStringToBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun copyStringToBuffer(
    columnIndex: Int, 
    buffer: CharArrayBuffer!
): Unit
```

Retrieves the requested column text and stores it in the buffer provided. If the buffer size is not sufficient, a new char buffer will be allocated and assigned to CharArrayBuffer.data

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. if the target column is null, return buffer Value is 0 or greater |
| `buffer` | [CharArrayBuffer](CharArrayBuffer.md)!:the buffer to copy the text into. |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deactivate(): Unit
```

**Deprecated:** *Since [requery()](Cursor.md))is deprecated, so too is this.*

Deactivates the Cursor, making all calls on it fail until [requery](Cursor.md))is called. Inactive Cursors use fewer resources than active Cursors. Calling [requery](Cursor.md))will make the cursor active again. 

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlob(columnIndex: Int): ByteArray!
```

Returns the value of the requested column as a byte array.

The result and whether this method throws an exception when the column value is null or the column type is not a blob type is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the value of that column as a byte array. |

### getColumnCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnCount(): Int
```

Return total number of columns

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of columns Value is 0 or greater |

### getColumnIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnIndex(columnName: String!): Int
```

Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use [getColumnIndexOrThrow(java.lang.String)](Cursor.md))instead, which will make the error more clear.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the target column. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the zero-based column index for the given column name, or -1 if the column name does not exist. Value is -1 or greater |

**See Also**

- [#getColumnIndexOrThrow(String)](Cursor.md)) 

### getColumnIndexOrThrow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnIndexOrThrow(columnName: String!): Int
```

Returns the zero-based index for the given column name, or throws [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if the column doesn't exist. If you're not sure if a column will exist or not use [getColumnIndex(java.lang.String)](Cursor.md))and check for -1, which is more efficient than catching the exceptions.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the target column. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the zero-based column index for the given column name Value is 0 or greater |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the column does not exist |

**See Also**

- [#getColumnIndex(String)](Cursor.md)) 

### getColumnName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnName(columnIndex: Int): String!
```

Returns the column name at the given zero-based column index.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the column name for the given column index. |

### getColumnNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnNames(): Array<String!>!
```

Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the names of the columns returned in this query. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCount(): Int
```

Returns the numbers of rows in the cursor.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows in the cursor. Value is 0 or greater |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDouble(columnIndex: Int): Double
```

Returns the value of the requested column as a double.

The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a`double`value is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value of that column as a double. |

### getExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getExtras(): Bundle!
```

Returns a bundle of extra values. This is an optional way for cursors to provide out-of-band metadata to their users. One use of this is for reporting on the progress of network requests that are required to fetch data for the cursor.

These values may only change when requery is called.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md)! | cursor-defined values, or [Bundle.EMPTY](../android.os/Bundle.md) if there are no values. Never`null`. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFloat(columnIndex: Int): Float
```

Returns the value of the requested column as a float.

The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a`float`value is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the value of that column as a float. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInt(columnIndex: Int): Int
```

Returns the value of the requested column as an int.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Integer.MIN_VALUE`,`Integer.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of that column as an int. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLong(columnIndex: Int): Long
```

Returns the value of the requested column as a long.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Long.MIN_VALUE`,`Long.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of that column as a long. |

### getNotificationUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNotificationUri(): Uri!
```

Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUri](Cursor.md)).

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md)! | Returns a URI that can be used with [ContentResolver.registerContentObserver](../android.content/ContentResolver.md))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUris(): MutableList<Uri!>?
```

Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUris](Cursor.md)).

If this is not implemented, this is equivalent to calling [getNotificationUri()](Cursor.md)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>? | Returns URIs that can be used with [ContentResolver.registerContentObserver](../android.content/ContentResolver.md))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPosition(): Int
```

Returns the current position of the cursor in the row set. The value is zero-based. When the row set is first returned the cursor will be at positon -1, which is before the first row. After the last row is returned another call to next() will leave the cursor past the last entry, at a position of count().

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current cursor position. Value is -1 or greater |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShort(columnIndex: Int): Short
```

Returns the value of the requested column as a short.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Short.MIN_VALUE`,`Short.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value of that column as a short. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getString(columnIndex: Int): String!
```

Returns the value of the requested column as a String.

The result and whether this method throws an exception when the column value is null or the column type is not a string type is implementation-defined.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of that column as a String. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getType(columnIndex: Int): Int
```

Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as [getInt(int)](Cursor.md)), [getFloat(int)](Cursor.md))etc.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](Cursor.md), [android.database.Cursor#FIELD_TYPE_INTEGER](Cursor.md), [android.database.Cursor#FIELD_TYPE_FLOAT](Cursor.md), [android.database.Cursor#FIELD_TYPE_STRING](Cursor.md), or [android.database.Cursor#FIELD_TYPE_BLOB](Cursor.md) |

### getWantsAllOnMoveCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWantsAllOnMoveCalls(): Boolean
```

onMove() will only be called across processes if this method returns true.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether all cursor movement should result in a call to onMove(). |

### isAfterLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAfterLast(): Boolean
```

Returns whether the cursor is pointing to the position after the last row.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is after the last result. |

### isBeforeFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isBeforeFirst(): Boolean
```

Returns whether the cursor is pointing to the position before the first row.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is before the first result. |

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isClosed(): Boolean
```

return true if the cursor is closed

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the cursor is closed. |

### isFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isFirst(): Boolean
```

Returns whether the cursor is pointing to the first row.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the first entry. |

### isLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isLast(): Boolean
```

Returns whether the cursor is pointing to the last row.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the last entry. |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNull(columnIndex: Int): Boolean
```

Returns`true`if the value in the indicated column is null.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the column value is null. |

### move

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun move(offset: Int): Boolean
```

Move the cursor by a relative amount, forward or backward, from the current position. Positive offsets move forwards, negative offsets move backwards. If the final position is outside of the bounds of the result set then the resultant position will be pinned to -1 or count() depending on whether the value is off the front or end of the set, respectively.

This method will return true if the requested destination was reachable, otherwise, it returns false. For example, if the cursor is at currently on the second entry in the result set and move(-5) is called, the position will be pinned at -1, and false will be returned.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to be applied from the current position. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the requested move fully succeeded. |

### moveToFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun moveToFirst(): Boolean
```

Move the cursor to the first row.

This method will return false if the cursor is empty.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun moveToLast(): Boolean
```

Move the cursor to the last row.

This method will return false if the cursor is empty.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun moveToNext(): Boolean
```

Move the cursor to the next row.

This method will return false if the cursor is already past the last entry in the result set.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun moveToPosition(position: Int): Boolean
```

Move the cursor to an absolute position. The valid range of values is -1 \<= position \<= count.

This method will return true if the request destination was reachable, otherwise, it returns false.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based position to move to. Value is -1 or greater |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the requested move fully succeeded. |

### moveToPrevious

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun moveToPrevious(): Boolean
```

Move the cursor to the previous row.

This method will return false if the cursor is already before the first entry in the result set.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### registerContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerContentObserver(observer: ContentObserver!): Unit
```

Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until [requery()](Cursor.md))is called.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](ContentObserver.md)!:the object that gets notified when the content backing the cursor changes. |

**See Also**

- [#unregisterContentObserver(ContentObserver)](Cursor.md)) 

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via [requery()](Cursor.md)), [deactivate()](Cursor.md)), or #close().

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](DataSetObserver.md)!:the object that gets notified when the cursors data set changes. |

**See Also**

- [#unregisterDataSetObserver(DataSetObserver)](Cursor.md)) 

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requery(): Boolean
```

**Deprecated:** *Don't use this. Just request a new cursor, so you can do this asynchronously and update your list view once the new cursor comes back.*

Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to [deactivate](Cursor.md)). Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the requery succeeded, false if not, in which case the cursor becomes invalid. |

### respond

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun respond(extras: Bundle!): Bundle!
```

This is an out-of-band way for the user of a cursor to communicate with the cursor. The structure of each bundle is entirely defined by the cursor.

One use of this is to tell a cursor that it should retry its network request after it reported an error.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android.os/Bundle.md)!:extra values, or [Bundle.EMPTY](../android.os/Bundle.md). Never`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md)! | extra values, or [Bundle.EMPTY](../android.os/Bundle.md). Never`null`. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setExtras(extras: Bundle!): Unit
```

Sets a [Bundle](../android.os/Bundle.md) that will be returned by [getExtras()](Cursor.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android.os/Bundle.md)!: [Bundle](../android.os/Bundle.md) to set, or null to set an empty bundle. |

### setNotificationUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNotificationUri(
    cr: ContentResolver!, 
    uri: Uri!
): Unit
```

Register to watch a content URI for changes. This can be the URI of a specific data row (for example, "content://my_provider_type/23"), or a a generic URI for a content type.

Calling this overrides any previous call to [setNotificationUris(android.content.ContentResolver,java.util.List)](Cursor.md)).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](../android.content/ContentResolver.md)!:The content resolver from the caller's context. The listener attached to this resolver will be notified. |
| `uri` | [Uri](../android.net/Uri.md)!:The content URI to watch. |

### setNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationUris(
    cr: ContentResolver, 
    uris: MutableList<Uri!>
): Unit
```

Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md)), except this version allows to watch multiple content URIs for changes.

If this is not implemented, this is equivalent to calling [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md))with the first URI in`uris`.

Calling this overrides any previous call to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](../android.content/ContentResolver.md):The content resolver from the caller's context. The listener attached to this resolver will be notified. This value cannot be`null`. |
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>:The content URIs to watch. This value cannot be`null`. |

### unregisterContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterContentObserver(observer: ContentObserver!): Unit
```

Unregister an observer that has previously been registered with this cursor via [registerContentObserver](Cursor.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](ContentObserver.md)!:the object to unregister. |

**See Also**

- [#registerContentObserver(ContentObserver)](Cursor.md)) 

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

Unregister an observer that has previously been registered with this cursor via [registerContentObserver](Cursor.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](DataSetObserver.md)!:the object to unregister. |

**See Also**

- [#registerDataSetObserver(DataSetObserver)](Cursor.md))
