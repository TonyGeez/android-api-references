# CursorWrapper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWrapper

Kotlin| [Java](CursorWrapper.md) 
| --- | --- |

```
open class CursorWrapper : Cursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.CursorWrapper](CursorWrapper.md) |

| Known Direct Subclasses [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) |------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------| | [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) | Cursor wrapper that implements [CrossProcessCursor](CrossProcessCursor.md). | |
| --- | --- | --- | --- | --- | --- | --- |

Wrapper class for Cursor that delegates all calls to the actual cursor object. The primary use for this class is to extend a cursor while overriding only a subset of its methods.

## Summary

| Inherited constants ||
|---|---|
| From class [Cursor](Cursor.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is blob <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is float <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is integer <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column is null <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](Cursor.md) <br /> Value returned by [getType(int)](Cursor.md))if the specified column type is string <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWrapper](CursorWrapper.md))`(`cursor:` ` [Cursor](Cursor.md)!`)` Creates a cursor wrapper. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](CursorWrapper.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](CharArrayBuffer.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](CursorWrapper.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](CursorWrapper.md))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getColumnNames](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](CursorWrapper.md))`()` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Bundle](../android.os/Bundle.md)! | [getExtras](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Uri](../android.net/Uri.md)! | [getNotificationUri](CursorWrapper.md))`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>? | [getNotificationUris](CursorWrapper.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](CursorWrapper.md))`()` <br /> |
| open [Cursor](Cursor.md)! | [getWrappedCursor](CursorWrapper.md))`()` Gets the underlying cursor that is wrapped by this instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](CursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](CursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](CursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](CursorWrapper.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](CursorWrapper.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](CursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](CursorWrapper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](CursorWrapper.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](CursorWrapper.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](CursorWrapper.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](CursorWrapper.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](CursorWrapper.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](CursorWrapper.md))`()` <br /> |
| open [Bundle](../android.os/Bundle.md)! | [respond](CursorWrapper.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](CursorWrapper.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](CursorWrapper.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)!`, `uri:` ` [Uri](../android.net/Uri.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](CursorWrapper.md))`(`cr:` ` [ContentResolver](../android.content/ContentResolver.md)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](CursorWrapper.md))`(`observer:` ` [ContentObserver](ContentObserver.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](CursorWrapper.md))`(`observer:` ` [DataSetObserver](DataSetObserver.md)!`)` <br /> |

## Public constructors

### CursorWrapper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWrapper(cursor: Cursor!)
```

Creates a cursor wrapper.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](Cursor.md)!:The underlying cursor to wrap. |

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
| `buffer` | [CharArrayBuffer](CharArrayBuffer.md)!:the buffer to copy the text into. |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deactivate(): Unit
```

**Deprecated:** *Deprecated in Java.* 

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
open fun getColumnNames(): Array<String!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the names of the columns returned in this query. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows in the cursor. Value is 0 or greater |

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

### getExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle!
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md)! | cursor-defined values, or [Bundle.EMPTY](../android.os/Bundle.md) if there are no values. Never`null`. |

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

### getNotificationUri

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUri(): Uri!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android.net/Uri.md)! | Returns a URI that can be used with [ContentResolver.registerContentObserver](../android.content/ContentResolver.md))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getNotificationUris

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNotificationUris(): MutableList<Uri!>?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>? | Returns URIs that can be used with [ContentResolver.registerContentObserver](../android.content/ContentResolver.md))to find out about changes to this Cursor's data. May be null if no notification URI has been set. |

### getPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPosition(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current cursor position. Value is -1 or greater |

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

### getWantsAllOnMoveCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWantsAllOnMoveCalls(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether all cursor movement should result in a call to onMove(). |

### getWrappedCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWrappedCursor(): Cursor!
```

Gets the underlying cursor that is wrapped by this instance.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [Cursor](Cursor.md)! | The wrapped cursor. |

### isAfterLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAfterLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is after the last result. |

### isBeforeFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBeforeFirst(): Boolean
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
open fun isFirst(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the first entry. |

### isLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the cursor is pointing at the last entry. |

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

### move

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun move(offset: Int): Boolean
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
open fun moveToFirst(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun moveToLast(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun moveToNext(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### moveToPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun moveToPosition(position: Int): Boolean
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
open fun moveToPrevious(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the move succeeded. |

### registerContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerContentObserver(observer: ContentObserver!): Unit
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](ContentObserver.md)!:the object that gets notified when the content backing the cursor changes. |

### registerDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](DataSetObserver.md)!:the object that gets notified when the cursors data set changes. |

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requery(): Boolean
```

**Deprecated:** *Deprecated in Java.*

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
| `extras` | [Bundle](../android.os/Bundle.md)!:extra values, or [Bundle.EMPTY](../android.os/Bundle.md). Never`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md)! | extra values, or [Bundle.EMPTY](../android.os/Bundle.md). Never`null`. |

### setExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExtras(extras: Bundle!): Unit
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android.os/Bundle.md)!: [Bundle](../android.os/Bundle.md) to set, or null to set an empty bundle. |

### setNotificationUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNotificationUri(
    cr: ContentResolver!, 
    uri: Uri!
): Unit
```

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

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](../android.content/ContentResolver.md):The content resolver from the caller's context. The listener attached to this resolver will be notified. This value cannot be`null`. |
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>:The content URIs to watch. This value cannot be`null`. |

### unregisterContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterContentObserver(observer: ContentObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](ContentObserver.md)!:the object to unregister. |

### unregisterDataSetObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterDataSetObserver(observer: DataSetObserver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [DataSetObserver](DataSetObserver.md)!:the object to unregister. |
