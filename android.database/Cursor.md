# Cursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Cursor

Kotlin| [Java](https://developer.android.com/reference/android/database/Cursor "View this page in Java") 

```
interface Cursor : Closeable
```

| [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor#) |

| Known Direct Subclasses [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor), [CursorWrapper](https://developer.android.com/reference/kotlin/android/database/CursorWrapper), [MockCursor](https://developer.android.com/reference/kotlin/android/test/mock/MockCursor.html#) |----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor) | A cross process cursor is an extension of a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor#) that also supports usage from remote processes. | | [CursorWrapper](https://developer.android.com/reference/kotlin/android/database/CursorWrapper) | Wrapper class for Cursor that delegates all calls to the actual cursor object. | | [MockCursor](https://developer.android.com/reference/kotlin/android/test/mock/MockCursor.html#) | A mock [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor#) class that isolates the test code from real Cursor implementation. | |

| Known Indirect Subclasses [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor), [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor), [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper), [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper), [MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor), [MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor), [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) |------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. | | [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor) | A base class for Cursors that store their data in [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow) s. | | [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper) | Cursor wrapper that implements [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor). | | [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper) | Cursor wrapper that implements [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor). | | [MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor) | A mutable cursor implementation backed by an array of`Object`s. | | [MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor) | A convenience class that lets you present an array of Cursors as a single linear Cursor. | | [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase). | |

This interface provides random read-write access to the result set returned by a database query.

Cursor implementations are not required to be synchronized so code using a Cursor from multiple threads should perform its own synchronization when using the Cursor.

Implementations should subclass [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is blob |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int) Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is float |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int) Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is integer |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int) Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column is null |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int) Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is string |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/Cursor#close())`()` Closes the Cursor, releasing all of its resources and making it completely invalid. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/Cursor#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!`)` Retrieves the requested column text and stores it in the buffer provided. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate())`()` Deactivates the Cursor, making all calls on it fail until [requery](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())is called. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](https://developer.android.com/reference/kotlin/android/database/Cursor#getBlob(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a byte array. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnCount())`()` Return total number of columns |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndex(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the zero-based index for the given column name, or -1 if the column doesn't exist. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndexOrThrow(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the zero-based index for the given column name, or throws [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) if the column doesn't exist. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnName(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the column name at the given zero-based column index. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getColumnNames](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnNames())`()` Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/database/Cursor#getCount())`()` Returns the numbers of rows in the cursor. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/database/Cursor#getDouble(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a double. |
| abstract [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/database/Cursor#getExtras())`()` Returns a bundle of extra values. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/database/Cursor#getFloat(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a float. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/database/Cursor#getInt(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as an int. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/database/Cursor#getLong(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a long. |
| abstract [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getNotificationUri](https://developer.android.com/reference/kotlin/android/database/Cursor#getNotificationUri())`()` Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>? | [getNotificationUris](https://developer.android.com/reference/kotlin/android/database/Cursor#getNotificationUris())`()` Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/database/Cursor#getPosition())`()` Returns the current position of the cursor in the row set. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/android/database/Cursor#getShort(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a short. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/database/Cursor#getString(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the requested column as a String. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns data type of the given column's value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](https://developer.android.com/reference/kotlin/android/database/Cursor#getWantsAllOnMoveCalls())`()` onMove() will only be called across processes if this method returns true. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](https://developer.android.com/reference/kotlin/android/database/Cursor#isAfterLast())`()` Returns whether the cursor is pointing to the position after the last row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](https://developer.android.com/reference/kotlin/android/database/Cursor#isBeforeFirst())`()` Returns whether the cursor is pointing to the position before the first row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/database/Cursor#isClosed())`()` return true if the cursor is closed |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](https://developer.android.com/reference/kotlin/android/database/Cursor#isFirst())`()` Returns whether the cursor is pointing to the first row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](https://developer.android.com/reference/kotlin/android/database/Cursor#isLast())`()` Returns whether the cursor is pointing to the last row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/android/database/Cursor#isNull(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns`true`if the value in the indicated column is null. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](https://developer.android.com/reference/kotlin/android/database/Cursor#move(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Move the cursor by a relative amount, forward or backward, from the current position. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](https://developer.android.com/reference/kotlin/android/database/Cursor#moveToFirst())`()` Move the cursor to the first row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](https://developer.android.com/reference/kotlin/android/database/Cursor#moveToLast())`()` Move the cursor to the last row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](https://developer.android.com/reference/kotlin/android/database/Cursor#moveToNext())`()` Move the cursor to the next row. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](https://developer.android.com/reference/kotlin/android/database/Cursor#moveToPosition(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Move the cursor to an absolute position. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](https://developer.android.com/reference/kotlin/android/database/Cursor#moveToPrevious())`()` Move the cursor to the previous row. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` Register an observer that is called when changes happen to the content backing this cursor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via [requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery()), [deactivate()](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()), or #close(). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())`()` Performs the query that created the cursor again, refreshing its contents. |
| abstract [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [respond](https://developer.android.com/reference/kotlin/android/database/Cursor#respond(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` This is an out-of-band way for the user of a cursor to communicate with the cursor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](https://developer.android.com/reference/kotlin/android/database/Cursor#setExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Sets a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) that will be returned by [getExtras()](https://developer.android.com/reference/kotlin/android/database/Cursor#getExtras()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Register to watch a content URI for changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)), except this version allows to watch multiple content URIs for changes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#unregisterContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` Unregister an observer that has previously been registered with this cursor via [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` Unregister an observer that has previously been registered with this cursor via [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)). |

## Constants

### FIELD_TYPE_BLOB

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_BLOB: Int
```

Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is blob 

 Value: 4

### FIELD_TYPE_FLOAT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_FLOAT: Int
```

Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is float 

 Value: 2

### FIELD_TYPE_INTEGER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_INTEGER: Int
```

Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is integer 

 Value: 1

### FIELD_TYPE_NULL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_NULL: Int
```

Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column is null 

 Value: 0

### FIELD_TYPE_STRING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIELD_TYPE_STRING: Int
```

Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is string 

 Value: 3

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike [deactivate()](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate())a call to [requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())will not make the Cursor valid again.

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
| `buffer` | [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!:the buffer to copy the text into. |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deactivate(): Unit
```

**Deprecated:** *Since [requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())is deprecated, so too is this.*

Deactivates the Cursor, making all calls on it fail until [requery](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())is called. Inactive Cursors use fewer resources than active Cursors. Calling [requery](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())will make the cursor active again. 

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

Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use [getColumnIndexOrThrow(java.lang.String)](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndexOrThrow(kotlin.String))instead, which will make the error more clear.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the target column. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the zero-based column index for the given column name, or -1 if the column name does not exist. Value is -1 or greater |

**See Also**

- [#getColumnIndexOrThrow(String)](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndexOrThrow(kotlin.String)) 

### getColumnIndexOrThrow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnIndexOrThrow(columnName: String!): Int
```

Returns the zero-based index for the given column name, or throws [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) if the column doesn't exist. If you're not sure if a column will exist or not use [getColumnIndex(java.lang.String)](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndex(kotlin.String))and check for -1, which is more efficient than catching the exceptions.

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

- [#getColumnIndex(String)](https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndex(kotlin.String)) 

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
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | cursor-defined values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle) if there are no values. Never`null`. |

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

Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)).

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | Returns a URI that can be used with [ContentResolver.registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUris(): MutableList<Uri!>?
```

Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)).

If this is not implemented, this is equivalent to calling [getNotificationUri()](https://developer.android.com/reference/kotlin/android/database/Cursor#getNotificationUri()).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>? | Returns URIs that can be used with [ContentResolver.registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

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

Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as [getInt(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getInt(kotlin.Int)), [getFloat(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getFloat(kotlin.Int))etc.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), [android.database.Cursor#FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), [android.database.Cursor#FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), [android.database.Cursor#FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), or [android.database.Cursor#FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) |

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

Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until [requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery())is called.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!:the object that gets notified when the content backing the cursor changes. |

**See Also**

- [#unregisterContentObserver(ContentObserver)](https://developer.android.com/reference/kotlin/android/database/Cursor#unregisterContentObserver(android.database.ContentObserver)) 

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via [requery()](https://developer.android.com/reference/kotlin/android/database/Cursor#requery()), [deactivate()](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()), or #close().

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!:the object that gets notified when the cursors data set changes. |

**See Also**

- [#unregisterDataSetObserver(DataSetObserver)](https://developer.android.com/reference/kotlin/android/database/Cursor#unregisterDataSetObserver(android.database.DataSetObserver)) 

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requery(): Boolean
```

**Deprecated:** *Don't use this. Just request a new cursor, so you can do this asynchronously and update your list view once the new cursor comes back.*

Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to [deactivate](https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()). Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread.

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
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:extra values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle). Never`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | extra values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle). Never`null`. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setExtras(extras: Bundle!): Unit
```

Sets a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) that will be returned by [getExtras()](https://developer.android.com/reference/kotlin/android/database/Cursor#getExtras()).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) to set, or null to set an empty bundle. |

### setNotificationUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNotificationUri(
    cr: ContentResolver!, 
    uri: Uri!
): Unit
```

Register to watch a content URI for changes. This can be the URI of a specific data row (for example, "content://my_provider_type/23"), or a a generic URI for a content type.

Calling this overrides any previous call to [setNotificationUris(android.content.ContentResolver,java.util.List)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!:The content resolver from the caller's context. The listener attached to this resolver will be notified. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The content URI to watch. |

### setNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationUris(
    cr: ContentResolver, 
    uris: MutableList<Uri!>
): Unit
```

Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)), except this version allows to watch multiple content URIs for changes.

If this is not implemented, this is equivalent to calling [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))with the first URI in`uris`.

Calling this overrides any previous call to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#):The content resolver from the caller's context. The listener attached to this resolver will be notified. This value cannot be`null`. |
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:The content URIs to watch. This value cannot be`null`. |

### unregisterContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterContentObserver(observer: ContentObserver!): Unit
```

Unregister an observer that has previously been registered with this cursor via [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!:the object to unregister. |

**See Also**

- [#registerContentObserver(ContentObserver)](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)) 

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

Unregister an observer that has previously been registered with this cursor via [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!:the object to unregister. |

**See Also**

- [#registerDataSetObserver(DataSetObserver)](https://developer.android.com/reference/kotlin/android/database/Cursor#registerDataSetObserver(android.database.DataSetObserver))
