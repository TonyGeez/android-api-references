# CrossProcessCursorWrapper

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossProcessCursorWrapper

Kotlin| [Java](../android/database/CrossProcessCursorWrapper.md) 
| --- | --- |

```
open class CrossProcessCursorWrapper : CursorWrapper, CrossProcessCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.CursorWrapper](../android/database/CursorWrapper.md) ||
| | ↳ | [android.database.CrossProcessCursorWrapper](../android/database/CrossProcessCursorWrapper.md) |

Cursor wrapper that implements [CrossProcessCursor](../android/database/CrossProcessCursor.md).

If the wrapped cursor implements [CrossProcessCursor](../android/database/CrossProcessCursor.md), then the wrapper delegates [fillWindow](../android/database/CrossProcessCursorWrapper.md)), [getWindow()](../android/database/CrossProcessCursorWrapper.md))and [onMove](../android/database/CrossProcessCursorWrapper.md))to it. Otherwise, the wrapper provides default implementations of these methods that traverse the contents of the cursor similar to [AbstractCursor.fillWindow](../android/database/AbstractCursor.md)).

This wrapper can be used to adapt an ordinary [Cursor](../android/database/Cursor.md) into a [CrossProcessCursor](../android/database/CrossProcessCursor.md).

## Summary

| Inherited constants ||
|---|---|
| From class [Cursor](../android/database/Cursor.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](../android/database/Cursor.md) <br /> Value returned by [getType(int)](../android/database/Cursor.md))if the specified column type is blob <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](../android/database/Cursor.md) <br /> Value returned by [getType(int)](../android/database/Cursor.md))if the specified column type is float <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](../android/database/Cursor.md) <br /> Value returned by [getType(int)](../android/database/Cursor.md))if the specified column type is integer <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](../android/database/Cursor.md) <br /> Value returned by [getType(int)](../android/database/Cursor.md))if the specified column is null <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](../android/database/Cursor.md) <br /> Value returned by [getType(int)](../android/database/Cursor.md))if the specified column type is string <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CrossProcessCursorWrapper](../android/database/CrossProcessCursorWrapper.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Creates a cross process cursor wrapper. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillWindow](../android/database/CrossProcessCursorWrapper.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `window:` ` [CursorWindow](../android/database/CursorWindow.md)!`)` <br /> |
| open [CursorWindow](../android/database/CursorWindow.md)! | [getWindow](../android/database/CrossProcessCursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMove](../android/database/CrossProcessCursorWrapper.md))`(`oldPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CursorWrapper](../android/database/CursorWrapper.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/database/CursorWrapper.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](../android/database/CharArrayBuffer.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](../android/database/CursorWrapper.md))`()` <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](../android/database/CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](../android/database/CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](../android/database/CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getColumnNames](../android/database/CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](../android/database/CursorWrapper.md))`()` <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Bundle](../android/os/Bundle.md)! | [getExtras](../android/database/CursorWrapper.md))`()` <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Uri](../android/net/Uri.md)! | [getNotificationUri](../android/database/CursorWrapper.md))`()` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android/net/Uri.md)!>? | [getNotificationUris](../android/database/CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](../android/database/CursorWrapper.md))`()` <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](../android/database/CursorWrapper.md))`()` <br /> | | [Cursor](../android/database/Cursor.md)! | [getWrappedCursor](../android/database/CursorWrapper.md))`()` <br /> Gets the underlying cursor that is wrapped by this instance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](../android/database/CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](../android/database/CursorWrapper.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](../android/database/CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](../android/database/CursorWrapper.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](../android/database/CursorWrapper.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](../android/database/CursorWrapper.md))`(`observer:` ` [ContentObserver](../android/database/ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](../android/database/CursorWrapper.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](../android/database/CursorWrapper.md))`()` <br /> | | [Bundle](../android/os/Bundle.md)! | [respond](../android/database/CursorWrapper.md))`(`extras:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](../android/database/CursorWrapper.md))`(`extras:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](../android/database/CursorWrapper.md))`(`cr:` ` [ContentResolver](../android/content/ContentResolver.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](../android/database/CursorWrapper.md))`(`cr:` ` [ContentResolver](../android/content/ContentResolver.md)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android/net/Uri.md)!>`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](../android/database/CursorWrapper.md))`(`observer:` ` [ContentObserver](../android/database/ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](../android/database/CursorWrapper.md))`(`observer:` ` [DataSetObserver](../android/database/DataSetObserver.md)!`)` <br /> | ||

## Public constructors

### CrossProcessCursorWrapper

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CrossProcessCursorWrapper(cursor: Cursor!)
```

Creates a cross process cursor wrapper.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](../android/database/Cursor.md)!:The underlying cursor to wrap. |

## Public methods

### fillWindow

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillWindow(
    position: Int, 
    window: CursorWindow!
): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based index of the first row to copy into the window. |
| `window` | [CursorWindow](../android/database/CursorWindow.md)!:The window to fill. |

### getWindow

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): CursorWindow!
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------|
| [CursorWindow](../android/database/CursorWindow.md)! | The pre-filled window, or null if none. |

### onMove

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMove(
    oldPosition: Int, 
    newPosition: Int
): Boolean
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------|
| `oldPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position that we're moving from. |
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position that we're moving to. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the move is successful, false otherwise. |
