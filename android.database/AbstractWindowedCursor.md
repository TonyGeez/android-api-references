# AbstractWindowedCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractWindowedCursor

Kotlin| [Java](https://developer.android.com/reference/android/database/AbstractWindowedCursor "View this page in Java") 
| --- | --- |

```
abstract class AbstractWindowedCursor : AbstractCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) ||
| | ↳ | [android.database.AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#) |

| Known Direct Subclasses [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) |-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteCursor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase). | |
| --- | --- | --- | --- | --- | --- | --- |

A base class for Cursors that store their data in [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow) s.

The cursor owns the cursor window it uses. When the cursor is closed, its window is also closed. Likewise, when the window used by the cursor is changed, its old window is closed. This policy of strict ownership ensures that cursor windows are not leaked.

Subclasses are responsible for filling the cursor window with data during [onMove(int,int)](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onMove(kotlin.Int,%20kotlin.Int)), allocating a new cursor window if necessary. During [requery()](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#requery()), the existing cursor window should be cleared and filled with new data.

If the contents of the cursor change or become invalid, the old window must be closed (because it is owned by the cursor) and set to null.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#AbstractWindowedCursor())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!`)` <br /> |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getBlob(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getDouble(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getFloat(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getInt(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getLong(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getShort(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getString(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getType(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)! | [getWindow](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#getWindow())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWindow](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#hasWindow())`()` Returns true if the cursor has an associated cursor window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlob](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#isBlob(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFloat](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#isFloat(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLong](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#isLong(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#isNull(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isString](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#isString(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWindow](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#setWindow(android.database.CursorWindow))`(`window:` ` [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)!`)` Sets a new cursor window for the cursor to use. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPosition](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#checkPosition())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#close())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#deactivate())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillWindow](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#fillWindow(kotlin.Int,%20android.database.CursorWindow))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `window:` ` [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#finalize())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnCount())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndex(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndexOrThrow(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnName(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getColumnNames](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnNames())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getCount())`()` <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getExtras())`()` <br /> | | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getNotificationUri](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUri())`()` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>? | [getNotificationUris](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUris())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getPosition())`()` <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getUpdatedField](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getUpdatedField(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getWantsAllOnMoveCalls())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isAfterLast())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isBeforeFirst())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isClosed())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFieldUpdated](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFieldUpdated(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFirst())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isLast())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#move(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToFirst())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToLast())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToNext())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPosition(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPrevious())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChange](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onChange(kotlin.Boolean))`(`selfChange:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Subclasses must call this method when they finish committing updates to notify all observers. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMove](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onMove(kotlin.Int,%20kotlin.Int))`(`oldPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#requery())`()` <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [respond](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#respond(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!`, `notifyUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` <br /> Specifies a content URI to watch for changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`, `notifyUris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` <br /> Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)), except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))with the first URI in`uris`. Calling this overrides any previous call to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)! | [mWindow](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor#mWindow:android.database.CursorWindow) The cursor window owned by this cursor. |

| Inherited properties ||
|---|---|
| From class [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) |----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mClosed](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mClosed:kotlin.Boolean) <br /> | | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)! | [mContentResolver](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mContentResolver:android.content.ContentResolver) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mPos](https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mPos:kotlin.Int) <br /> | ||

## Public constructors

### AbstractWindowedCursor

```
AbstractWindowedCursor()
```

## Public methods

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

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlob(columnIndex: Int): ByteArray!
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the value of that column as a byte array. |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(columnIndex: Int): Double
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value of that column as a double. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFloat(columnIndex: Int): Float
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the value of that column as a float. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(columnIndex: Int): Int
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of that column as an int. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(columnIndex: Int): Long
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of that column as a long. |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShort(columnIndex: Int): Short
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value of that column as a short. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(columnIndex: Int): String!
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of that column as a String. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(columnIndex: Int): Int
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), [android.database.Cursor#FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), [android.database.Cursor#FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), [android.database.Cursor#FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), or [android.database.Cursor#FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) |

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): CursorWindow!
```

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)! | The pre-filled window that backs this cursor, or null if none. |

### hasWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasWindow(): Boolean
```

Returns true if the cursor has an associated cursor window.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the cursor has an associated cursor window. |

### isBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBlob(columnIndex: Int): Boolean
```

**Deprecated:** *Use #getType* 

### isFloat

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFloat(columnIndex: Int): Boolean
```

**Deprecated:** *Use #getType* 

### isLong

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLong(columnIndex: Int): Boolean
```

**Deprecated:** *Use #getType* 

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(columnIndex: Int): Boolean
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based index of the target column. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the column value is null. |

### isString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isString(columnIndex: Int): Boolean
```

**Deprecated:** *Use #getType* 

### setWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWindow(window: CursorWindow!): Unit
```

Sets a new cursor window for the cursor to use.

The cursor takes ownership of the provided cursor window; the cursor window will be closed when the cursor is closed or when the cursor adopts a new cursor window.

If the cursor previously had a cursor window, then it is closed when the new cursor window is assigned.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `window` | [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow)!:The new cursor window, typically a remote cursor window. |

## Protected methods

### checkPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun checkPosition(): Unit
```

| Exceptions ||
|----------------------------------------------------|---|
| `android.database.CursorIndexOutOfBoundsException` | |

## Properties

### mWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mWindow: CursorWindow!
```

The cursor window owned by this cursor.
