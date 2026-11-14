# AbstractCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractCursor

Kotlin| [Java](https://developer.android.com/reference/android/database/AbstractCursor "View this page in Java") 
| --- | --- |

```
abstract class AbstractCursor : CrossProcessCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#) |

| Known Direct Subclasses [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor), [MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor), [MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor) |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor) | A base class for Cursors that store their data in [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow) s. | | [MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor) | A mutable cursor implementation backed by an array of`Object`s. | | [MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor) | A convenience class that lets you present an array of Cursors as a single linear Cursor. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) |-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase). | |
| --- | --- | --- | --- | --- | --- | --- |

This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [SelfContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor.SelfContentObserver) Cursors use this class to track changes others make to their URI. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#AbstractCursor())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#close())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#deactivate())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillWindow](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#fillWindow(kotlin.Int,%20android.database.CursorWindow))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `window:` ` [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)!`)` <br /> |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getBlob(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnCount())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndex(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndexOrThrow(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnName(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getColumnNames](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnNames())`()` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getCount())`()` <br /> |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getDouble(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getExtras())`()` <br /> |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getFloat(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getInt(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getLong(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getNotificationUri](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUri())`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>? | [getNotificationUris](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUris())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getPosition())`()` <br /> |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getShort(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getString(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getType(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getWantsAllOnMoveCalls())`()` <br /> |
| open [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)! | [getWindow](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getWindow())`()` If the cursor is backed by a [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow), returns a pre-filled window with the contents of the cursor, otherwise null. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isAfterLast())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isBeforeFirst())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isClosed())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFirst())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isLast())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isNull(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#move(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToFirst())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToLast())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToNext())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPosition(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPrevious())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMove](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onMove(kotlin.Int,%20kotlin.Int))`(`oldPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#requery())`()` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [respond](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#respond(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!`, `notifyUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Specifies a content URI to watch for changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`, `notifyUris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)), except this version allows to watch multiple content URIs for changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPosition](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#checkPosition())`()` This function throws CursorIndexOutOfBoundsException if the cursor position is out of bounds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#finalize())`()` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getUpdatedField](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getUpdatedField(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFieldUpdated](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFieldUpdated(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChange](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onChange(kotlin.Boolean))`(`selfChange:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Subclasses must call this method when they finish committing updates to notify all observers. |

| Properties ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mClosed](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mClosed:kotlin.Boolean) <br /> |
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)! | [mContentResolver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mContentResolver:android.content.ContentResolver) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mPos](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mPos:kotlin.Int) <br /> |
| --- | --- |

## Public constructors

### AbstractCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AbstractCursor()
```

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### copyStringToBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun copyStringToBuffer(
    columnIndex: Int, 
    buffer: CharArrayBuffer!
): Unit
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. if the target column is null, return buffer Value is 0 or greater |
| `buffer` | [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!:the buffer to copy the text into. |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deactivate(): Unit
```  

### fillWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillWindow(
    position: Int, 
    window: CursorWindow!
): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based index of the first row to copy into the window. |
| `window` | [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)!:The window to fill. |

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlob(column: Int): ByteArray!
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the value of that column as a byte array. |

### getColumnCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of columns Value is 0 or greater |

### getColumnIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnIndex(columnName: String!): Int
```

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the target column. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the zero-based column index for the given column name, or -1 if the column name does not exist. Value is -1 or greater |

### getColumnIndexOrThrow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnIndexOrThrow(columnName: String!): Int
```

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the target column. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the zero-based column index for the given column name Value is 0 or greater |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the column does not exist |

### getColumnName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnName(columnIndex: Int): String!
```

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

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the names of the columns returned in this query. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows in the cursor. Value is 0 or greater |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDouble(column: Int): Double
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value of that column as a double. |

### getExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle!
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | cursor-defined values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle) if there are no values. Never`null`. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFloat(column: Int): Float
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the value of that column as a float. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInt(column: Int): Int
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of that column as an int. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLong(column: Int): Long
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of that column as a long. |

### getNotificationUri

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUri(): Uri!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | Returns a URI that can be used with [ContentResolver.registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUris(): MutableList<Uri!>?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>? | Returns URIs that can be used with [ContentResolver.registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current cursor position. Value is -1 or greater |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShort(column: Int): Short
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value of that column as a short. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getString(column: Int): String!
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of that column as a String. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(column: Int): Int
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), [android.database.Cursor#FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), [android.database.Cursor#FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), [android.database.Cursor#FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), or [android.database.Cursor#FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) |

### getWantsAllOnMoveCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWantsAllOnMoveCalls(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether all cursor movement should result in a call to onMove(). |

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): CursorWindow!
```

If the cursor is backed by a [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow), returns a pre-filled window with the contents of the cursor, otherwise null.

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)! | The pre-filled window that backs this cursor, or null if none. |

### isAfterLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAfterLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is after the last result. |

### isBeforeFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBeforeFirst(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is before the first result. |

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the cursor is closed. |

### isFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFirst(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the first entry. |

### isLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the last entry. |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNull(column: Int): Boolean
```

| Parameters ||
|---------------|------------------------------------------------------------------|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the column value is null. |

### move

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun move(offset: Int): Boolean
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to be applied from the current position. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the requested move fully succeeded. |

### moveToFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun moveToFirst(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun moveToLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun moveToNext(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun moveToPosition(position: Int): Boolean
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based position to move to. Value is -1 or greater |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the requested move fully succeeded. |

### moveToPrevious

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun moveToPrevious(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### onMove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMove(
    oldPosition: Int, 
    newPosition: Int
): Boolean
```

This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `oldPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position that we're moving from |
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position that we're moving to |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the move is successful, false otherwise |

### registerContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerContentObserver(observer: ContentObserver!): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!:the object that gets notified when the content backing the cursor changes. |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!:the object that gets notified when the cursors data set changes. |

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requery(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the requery succeeded, false if not, in which case the cursor becomes invalid. |

### respond

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun respond(extras: Bundle!): Bundle!
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:extra values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle). Never`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | extra values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle). Never`null`. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExtras(extras: Bundle!): Unit
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) to set, or null to set an empty bundle. |

### setNotificationUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationUri(
    cr: ContentResolver!, 
    notifyUri: Uri!
): Unit
```

Specifies a content URI to watch for changes.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!:The content resolver from the caller's context. |
| `uri` | The content URI to watch. |
| `notifyUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The URI to watch for changes. This can be a specific row URI, or a base URI for a whole class of content. |
| --- | --- |

### setNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationUris(
    cr: ContentResolver, 
    notifyUris: MutableList<Uri!>
): Unit
```

Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)), except this version allows to watch multiple content URIs for changes.

If this is not implemented, this is equivalent to calling [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))with the first URI in`uris`.

Calling this overrides any previous call to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#):This value cannot be`null`. |
| `uris` | The content URIs to watch. This value cannot be`null`. |
| `notifyUris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:This value cannot be`null`. |
| --- | --- |

### unregisterContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterContentObserver(observer: ContentObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!:the object to unregister. |

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!:the object to unregister. |

## Protected methods

### checkPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun checkPosition(): Unit
```

This function throws CursorIndexOutOfBoundsException if the cursor position is out of bounds. Subclass implementations of the get functions should call this before attempting to retrieve data.

| Exceptions ||
|----------------------------------------------------|---|
| `android.database.CursorIndexOutOfBoundsException` | |

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

### getUpdatedField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getUpdatedField(columnIndex: Int): Any!
```

**Deprecated:** *Always returns null since Cursors do not support updating rows* 

### isFieldUpdated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun isFieldUpdated(columnIndex: Int): Boolean
```

**Deprecated:** *Always returns false since Cursors do not support updating rows* 

### onChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onChange(selfChange: Boolean): Unit
```

Subclasses must call this method when they finish committing updates to notify all observers.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------|
| `selfChange` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): |

## Properties

### mClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mClosed: Boolean
```

**Deprecated:** *Use [isClosed()](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isClosed())instead.* 

### mContentResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mContentResolver: ContentResolver!
```

**Deprecated:** *Do not use.* 

### mPos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mPos: Int
```

**Deprecated:** *Use [getPosition()](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getPosition())instead.*
