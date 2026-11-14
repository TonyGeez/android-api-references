# CrossProcessCursorWrapper

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossProcessCursorWrapper

Kotlin| [Java](CrossProcessCursorWrapper.md) 
| --- | --- |

```
open class CrossProcessCursorWrapper : CursorWrapper, CrossProcessCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.CursorWrapper](CursorWrapper.md) ||
| | ↳ | [android.database.CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) |

Cursor wrapper that implements [CrossProcessCursor](CrossProcessCursor.md).

If the wrapped cursor implements [CrossProcessCursor](CrossProcessCursor.md), then the wrapper delegates [fillWindow](CrossProcessCursorWrapper.md)), [getWindow()](CrossProcessCursorWrapper.md))and [onMove](CrossProcessCursorWrapper.md))to it. Otherwise, the wrapper provides default implementations of these methods that traverse the contents of the cursor similar to [AbstractCursor.fillWindow](AbstractCursor.md)).

This wrapper can be used to adapt an ordinary [Cursor](Cursor.md) into a [CrossProcessCursor](CrossProcessCursor.md).

## Summary

| Inherited constants ||
|---|---|
| From class [Cursor](Cursor.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is blob <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is float <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is integer <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column is null <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is string <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md))`(`cursor:` ` [Cursor](Cursor.md)!`)` Creates a cross process cursor wrapper. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillWindow](CrossProcessCursorWrapper.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `window:` ` [CursorWindow](CursorWindow.md)!`)` <br /> |
| open [CursorWindow](CursorWindow.md)! | [getWindow](CrossProcessCursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMove](CrossProcessCursorWrapper.md))`(`oldPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CursorWrapper](CursorWrapper.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](CursorWrapper.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](CharArrayBuffer.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](CursorWrapper.md))`()` <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getColumnNames](CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](CursorWrapper.md))`()` <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Bundle](../android.os/Bundle.md)! | [getExtras](CursorWrapper.md))`()` <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Uri](../android.net/Uri.md)! | [getNotificationUri](CursorWrapper.md))`()` <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>? | [getNotificationUris](CursorWrapper.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](CursorWrapper.md))`()` <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](CursorWrapper.md))`()` <br /> | | [Cursor](Cursor.md)! | [getWrappedCursor](CursorWrapper.md))`()` <br /> Gets the underlying cursor that is wrapped by this instance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](CursorWrapper.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](CursorWrapper.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](CursorWrapper.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](CursorWrapper.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](CursorWrapper.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](CursorWrapper.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](CursorWrapper.md))`()` <br /> | | [Bundle](../android.os/Bundle.md)! | [respond](CursorWrapper.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](CursorWrapper.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](CursorWrapper.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](CursorWrapper.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](CursorWrapper.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](CursorWrapper.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> | ||

## Public constructors

### CrossProcessCursorWrapper

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CrossProcessCursorWrapper(cursor: Cursor!)
```

Creates a cross process cursor wrapper.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](Cursor.md)!:The underlying cursor to wrap. |

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
| `window` | [CursorWindow](CursorWindow.md)!:The window to fill. |

### getWindow

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindow(): CursorWindow!
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------|
| [CursorWindow](CursorWindow.md)! | The pre-filled window, or null if none. |

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
