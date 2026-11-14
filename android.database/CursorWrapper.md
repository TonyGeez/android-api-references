# CursorWrapper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWrapper

Kotlin| [Java](https://developer.android.com/reference/android/database/CursorWrapper "View this page in Java") 
| --- | --- |

```
open class CursorWrapper : Cursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.CursorWrapper](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#) |

| Known Direct Subclasses [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper) |------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------| | [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper) | Cursor wrapper that implements [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor). | |
| --- | --- | --- | --- | --- | --- | --- |

Wrapper class for Cursor that delegates all calls to the actual cursor object. The primary use for this class is to extend a cursor while overriding only a subset of its methods.

## Summary

| Inherited constants ||
|---|---|
| From class [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) <br /> Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is blob <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int) <br /> Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is float <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int) <br /> Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is integer <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int) <br /> Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column is null <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int) <br /> Value returned by [getType(int)](https://developer.android.com/reference/kotlin/android/database/Cursor#getType(kotlin.Int))if the specified column type is string <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWrapper](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#CursorWrapper(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor)!`)` Creates a cursor wrapper. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#close())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deactivate](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#deactivate())`()` <br /> |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getBlob(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getColumnCount())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndex](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getColumnIndex(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnIndexOrThrow](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getColumnIndexOrThrow(kotlin.String))`(`columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getColumnName(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getColumnNames](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getColumnNames())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCount](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getCount())`()` <br /> |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getDouble(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getExtras())`()` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getFloat(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getInt(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getLong(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getNotificationUri](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getNotificationUri())`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>? | [getNotificationUris](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getNotificationUris())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getPosition())`()` <br /> |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getShort(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getString(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getType(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getWantsAllOnMoveCalls](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getWantsAllOnMoveCalls())`()` <br /> |
| open [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor)! | [getWrappedCursor](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#getWrappedCursor())`()` Gets the underlying cursor that is wrapped by this instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isAfterLast())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isBeforeFirst())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isClosed())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isFirst())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isLast())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#isNull(kotlin.Int))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [move](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#move(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToFirst](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#moveToFirst())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToLast](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#moveToLast())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToNext](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#moveToNext())`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPosition](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#moveToPosition(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [moveToPrevious](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#moveToPrevious())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#registerContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#registerDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requery](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#requery())`()` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [respond](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#respond(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExtras](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#setExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUri](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#setNotificationUri(android.content.ContentResolver,%20android.net.Uri))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNotificationUris](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList))`(`cr:` ` [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)`, `uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#unregisterContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](https://developer.android.com/reference/kotlin/android/database/CursorWrapper#unregisterDataSetObserver(android.database.DataSetObserver))`(`observer:` ` [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver)!`)` <br /> |

## Public constructors

### CursorWrapper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWrapper(cursor: Cursor!)
```

Creates a cursor wrapper.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor)!:The underlying cursor to wrap. |

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
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | cursor-defined values, or [Bundle.EMPTY](https://developer.android.com/reference/kotlin/android/os/Bundle.html#EMPTY:android.os.Bundle) if there are no values. Never`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | column value type Value is [android.database.Cursor#FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), [android.database.Cursor#FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), [android.database.Cursor#FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), [android.database.Cursor#FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), or [android.database.Cursor#FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) |

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
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor)! | The wrapped cursor. |

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
    uri: Uri!
): Unit
```

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

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cr` | [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#):The content resolver from the caller's context. The listener attached to this resolver will be notified. This value cannot be`null`. |
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:The content URIs to watch. This value cannot be`null`. |

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
