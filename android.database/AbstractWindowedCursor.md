# AbstractWindowedCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractWindowedCursor

Kotlin| [Java](AbstractWindowedCursor.md) 
| --- | --- |

```
abstract class AbstractWindowedCursor : AbstractCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.AbstractCursor](AbstractCursor.md) ||
| | ↳ | [android.database.AbstractWindowedCursor](AbstractWindowedCursor.md) |

| Known Direct Subclasses [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) |-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) | A Cursor implementation that exposes results from a query on a [SQLiteDatabase](../android.database.sqlite/SQLiteDatabase.md). | |
| --- | --- | --- | --- | --- | --- | --- |

A base class for Cursors that store their data in [CursorWindow](CursorWindow.md) s.

The cursor owns the cursor window it uses. When the cursor is closed, its window is also closed. Likewise, when the window used by the cursor is changed, its old window is closed. This policy of strict ownership ensures that cursor windows are not leaked.

Subclasses are responsible for filling the cursor window with data during [onMove(int,int)](AbstractCursor.md)), allocating a new cursor window if necessary. During [requery()](AbstractCursor.md)), the existing cursor window should be cleared and filled with new data.

If the contents of the cursor change or become invalid, the old window must be closed (because it is owned by the cursor) and set to null.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractWindowedCursor](AbstractWindowedCursor.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](CharArrayBuffer.md)!`)` <br /> |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [CursorWindow](CursorWindow.md)! | [getWindow](AbstractWindowedCursor.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWindow](AbstractWindowedCursor.md))`()` Returns true if the cursor has an associated cursor window. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlob](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFloat](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLong](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isString](AbstractWindowedCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWindow](AbstractWindowedCursor.md))`(`window:` ` [CursorWindow](CursorWindow.md)!`)` Sets a new cursor window for the cursor to use. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkPosition](AbstractWindowedCursor.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractCursor](AbstractCursor.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](AbstractCursor.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](AbstractCursor.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillWindow](AbstractCursor.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `window:` ` [CursorWindow](CursorWindow.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AbstractCursor.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](AbstractCursor.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](AbstractCursor.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](AbstractCursor.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](AbstractCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getColumnNames](AbstractCursor.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](AbstractCursor.md))`()` <br /> | | [Bundle](../android.os/Bundle.md)! | [getExtras](AbstractCursor.md))`()` <br /> | | [Uri](../android.net/Uri.md)! | [getNotificationUri](AbstractCursor.md))`()` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>? | [getNotificationUris](AbstractCursor.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](AbstractCursor.md))`()` <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getUpdatedField](AbstractCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFieldUpdated](AbstractCursor.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](AbstractCursor.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](AbstractCursor.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](AbstractCursor.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](AbstractCursor.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChange](AbstractCursor.md))`(`selfChange:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Subclasses must call this method when they finish committing updates to notify all observers. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMove](AbstractCursor.md))`(`oldPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](AbstractCursor.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](AbstractCursor.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](AbstractCursor.md))`()` <br /> | | [Bundle](../android.os/Bundle.md)! | [respond](AbstractCursor.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](AbstractCursor.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](AbstractCursor.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)!`, `notifyUri:` ` [Uri](../android.net/Uri.md)!`)` <br /> Specifies a content URI to watch for changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](AbstractCursor.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)`, `notifyUris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>`)` <br /> Similar to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md)), except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md))with the first URI in`uris`. Calling this overrides any previous call to [setNotificationUri(android.content.ContentResolver,android.net.Uri)](Cursor.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](AbstractCursor.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](AbstractCursor.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CursorWindow](CursorWindow.md)! | [mWindow](AbstractWindowedCursor.md) The cursor window owned by this cursor. |

| Inherited properties ||
|---|---|
| From class [AbstractCursor](AbstractCursor.md) |----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mClosed](AbstractCursor.md) <br /> | | [ContentResolver](../android.content/ContentResolver.md)! | [mContentResolver](AbstractCursor.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mPos](AbstractCursor.md) <br /> | ||

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
| `buffer` | [CharArrayBuffer](CharArrayBuffer.md)!:the buffer to copy the text into. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](Cursor.md), [android.database.Cursor#FIELD_TYPE_INTEGER](Cursor.md), [android.database.Cursor#FIELD_TYPE_FLOAT](Cursor.md), [android.database.Cursor#FIELD_TYPE_STRING](Cursor.md), or [android.database.Cursor#FIELD_TYPE_BLOB](Cursor.md) |

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): CursorWindow!
```

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [CursorWindow](CursorWindow.md)! | The pre-filled window that backs this cursor, or null if none. |

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
| `window` | [CursorWindow](CursorWindow.md)!:The new cursor window, typically a remote cursor window. |

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
