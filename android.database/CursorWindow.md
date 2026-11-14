# CursorWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWindow

Kotlin| [Java](https://developer.android.com/reference/android/database/CursorWindow "View this page in Java") 
| --- | --- |

```
open class CursorWindow : SQLiteClosable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) ||
| | ↳ | [android.database.CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#) |

A buffer containing multiple cursor rows.

A [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#) is read-write when initially created and used locally. When sent to a remote process (by writing it to a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)), the remote process receives a read-only view of the cursor window. Typically the cursor window will be allocated by the producer, filled with data, and then sent to the consumer for reading.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#CursorWindow(kotlin.Boolean))`(`localWindow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new empty cursor window. |
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#CursorWindow(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new empty cursor window and gives it a name. |
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#CursorWindow(kotlin.String,%20kotlin.Long))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `windowSizeBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new empty cursor window and gives it a name. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allocRow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#allocRow())`()` Allocates a new row at the end of this cursor window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/database/CursorWindow#clear())`()` Clears out the existing contents of the window, making it safe to reuse for new data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/CursorWindow#copyStringToBuffer(kotlin.Int,%20kotlin.Int,%20android.database.CharArrayBuffer))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!`)` Copies the text of the field at the specified row and column index into a [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/database/CursorWindow#describeContents())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [freeLastRow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#freeLastRow())`()` Frees the last row in this cursor window. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getBlob(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a byte array. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getDouble(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`double`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getFloat(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`float`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getInt(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as an`int`. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getLong(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`long`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumRows](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getNumRows())`()` Gets the number of rows in this window. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getShort(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`short`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartPosition](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getStartPosition())`()` Gets the start position of this cursor window. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getString(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the type of the field at the specified row and column index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlob](https://developer.android.com/reference/kotlin/android/database/CursorWindow#isBlob(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFloat](https://developer.android.com/reference/kotlin/android/database/CursorWindow#isFloat(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLong](https://developer.android.com/reference/kotlin/android/database/CursorWindow#isLong(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/android/database/CursorWindow#isNull(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isString](https://developer.android.com/reference/kotlin/android/database/CursorWindow#isString(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |
| openstatic [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#)! | [newFromParcel](https://developer.android.com/reference/kotlin/android/database/CursorWindow#newFromParcel(android.os.Parcel))`(`p:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putBlob](https://developer.android.com/reference/kotlin/android/database/CursorWindow#putBlob(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copies a byte array into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putDouble](https://developer.android.com/reference/kotlin/android/database/CursorWindow#putDouble(kotlin.Double,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a double-precision floating point value into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putLong](https://developer.android.com/reference/kotlin/android/database/CursorWindow#putLong(kotlin.Long,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a long integer into the field at the specified row and column index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putNull](https://developer.android.com/reference/kotlin/android/database/CursorWindow#putNull(kotlin.Int,%20kotlin.Int))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a null value into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putString](https://developer.android.com/reference/kotlin/android/database/CursorWindow#putString(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copies a string into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setNumColumns](https://developer.android.com/reference/kotlin/android/database/CursorWindow#setNumColumns(kotlin.Int))`(`columnNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of columns in this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartPosition](https://developer.android.com/reference/kotlin/android/database/CursorWindow#setStartPosition(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the start position of this cursor window. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/database/CursorWindow#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/database/CursorWindow#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/database/CursorWindow#finalize())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](https://developer.android.com/reference/kotlin/android/database/CursorWindow#onAllReferencesReleased())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#acquireReference())`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#close())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer())`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer())`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/database/CursorWindow#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### CursorWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindow(localWindow: Boolean)
```

**Deprecated:** *There is no longer a distinction between local and remote cursor windows. Use the [CursorWindow(java.lang.String)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#CursorWindow(kotlin.String))constructor instead.*

Creates a new empty cursor window.

The cursor initially has no rows or columns. Call [setNumColumns(int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#setNumColumns(kotlin.Int))to set the number of columns before adding any rows to the cursor.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localWindow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if this window will be used in this process only, false if it might be sent to another processes. This argument is ignored. |

### CursorWindow

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindow(name: String!)
```

Creates a new empty cursor window and gives it a name.

The cursor initially has no rows or columns. Call [setNumColumns(int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#setNumColumns(kotlin.Int))to set the number of columns before adding any rows to the cursor.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the cursor window, or null if none. |

### CursorWindow

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindow(
    name: String!, 
    windowSizeBytes: Long)
```

Creates a new empty cursor window and gives it a name.

The cursor initially has no rows or columns. Call [setNumColumns(int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#setNumColumns(kotlin.Int))to set the number of columns before adding any rows to the cursor.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the cursor window, or null if none. |
| `windowSizeBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Size of cursor window in bytes. Value is a non-negative number of bytes. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`windowSizeBytes`is less than 0 |
| `java.lang.AssertionError` | if created window pointer is 0 **Note:**Memory is dynamically allocated as data rows are added to the window. Depending on the amount of data stored, the actual amount of memory allocated can be lower than specified size, but cannot exceed it. |

## Public methods

### allocRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allocRow(): Boolean
```

Allocates a new row at the end of this cursor window.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful, false if the cursor window is out of memory. |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Clears out the existing contents of the window, making it safe to reuse for new data.

The start position ([getStartPosition()](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getStartPosition())), number of rows ([getNumRows()](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getNumRows())), and number of columns in the cursor are all reset to zero. 

### copyStringToBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun copyStringToBuffer(
    row: Int, 
    column: Int, 
    buffer: CharArrayBuffer!
): Unit
```

Copies the text of the field at the specified row and column index into a [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer).

The buffer is populated as follows:

- If the buffer is too small for the value to be copied, then it is automatically resized.
- If the field is of type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), then the buffer is set to an empty string.
- If the field is of type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), then the buffer is set to the contents of the string.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), then the buffer is set to a string representation of the integer in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%lld`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), then the buffer is set to a string representation of the floating-point value in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%g`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int), then a [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) is thrown.

<br />

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| `buffer` | [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer)!:The [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer) to hold the string. It is automatically resized if the requested string is larger than the buffer's current capacity. |
| --- | --- |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### freeLastRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun freeLastRow(): Unit
```

Frees the last row in this cursor window. 

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlob(
    row: Int, 
    column: Int
): ByteArray!
```

Gets the value of the field at the specified row and column index as a byte array.

The result is determined as follows:

- If the field is of type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), then the result is`null`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int), then the result is the blob value.
- If the field is of type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), then the result is the array of bytes that make up the internal representation of the string value.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int) or [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), then a [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) is thrown.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | The value of the field as a byte array. |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(
    row: Int, 
    column: Int
): Double
```

Gets the value of the field at the specified row and column index as a`double`.

The result is determined as follows:

- If the field is of type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), then the result is`0.0`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), then the result is the value obtained by parsing the string value with`strtod`.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), then the result is the integer value converted to a`double`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), then the result is the`double`value.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int), then a [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) is thrown.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | The value of the field as a`double`. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFloat(
    row: Int, 
    column: Int
): Float
```

Gets the value of the field at the specified row and column index as a`float`.

The result is determined by invoking [getDouble](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getDouble(kotlin.Int,%20kotlin.Int))and converting the result to`float`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The value of the field as an`float`. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(
    row: Int, 
    column: Int
): Int
```

Gets the value of the field at the specified row and column index as an`int`.

The result is determined by invoking [getLong](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getLong(kotlin.Int,%20kotlin.Int))and converting the result to`int`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The value of the field as an`int`. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(
    row: Int, 
    column: Int
): Long
```

Gets the value of the field at the specified row and column index as a`long`.

The result is determined as follows:

- If the field is of type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), then the result is`0L`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), then the result is the value obtained by parsing the string value with`strtoll`.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), then the result is the`long`value.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), then the result is the floating-point value converted to a`long`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int), then a [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) is thrown.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The value of the field as a`long`. |

### getNumRows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumRows(): Int
```

Gets the number of rows in this window.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rows in this cursor window. Value is 0 or greater |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShort(
    row: Int, 
    column: Int
): Short
```

Gets the value of the field at the specified row and column index as a`short`.

The result is determined by invoking [getLong](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getLong(kotlin.Int,%20kotlin.Int))and converting the result to`short`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | The value of the field as a`short`. |

### getStartPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartPosition(): Int
```

Gets the start position of this cursor window.

The start position is the zero-based index of the first row that this window contains relative to the entire result set of the [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The zero-based start position. Value is 0 or greater |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(
    row: Int, 
    column: Int
): String!
```

Gets the value of the field at the specified row and column index as a string.

The result is determined as follows:

- If the field is of type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), then the result is`null`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), then the result is the string value.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), then the result is a string representation of the integer in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%lld`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), then the result is a string representation of the floating-point value in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%g`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int), then a [SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException) is thrown.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The value of the field as a string. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(
    row: Int, 
    column: Int
): Int
```

Returns the type of the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The field type. Value is [android.database.Cursor#FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int), [android.database.Cursor#FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int), [android.database.Cursor#FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int), [android.database.Cursor#FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int), or [android.database.Cursor#FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) |

### isBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBlob(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_BLOB](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |

### isFloat

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFloat(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int). |

### isLong

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLong(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_INTEGER](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int). |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |

### isString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isString(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](https://developer.android.com/reference/kotlin/android/database/CursorWindow#getType(kotlin.Int,%20kotlin.Int))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_STRING](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int) or [Cursor.FIELD_TYPE_NULL](https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int). |

### newFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newFromParcel(p: Parcel!): CursorWindow!
```  

### putBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putBlob(
    value: ByteArray!, 
    row: Int, 
    column: Int
): Boolean
```

Copies a byte array into the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The value to store. |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### putDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putDouble(
    value: Double, 
    row: Int, 
    column: Int
): Boolean
```

Puts a double-precision floating point value into the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The value to store. |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### putLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLong(
    value: Long, 
    row: Int, 
    column: Int
): Boolean
```

Puts a long integer into the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The value to store. |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### putNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putNull(
    row: Int, 
    column: Int
): Boolean
```

Puts a null value into the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### putString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putString(
    value: String!, 
    row: Int, 
    column: Int
): Boolean
```

Copies a string into the field at the specified row and column index.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value to store. |
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### setNumColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumColumns(columnNum: Int): Boolean
```

Sets the number of columns in this window.

This method must be called before any rows are added to the window, otherwise it will fail to set the number of columns if it differs from the current number of columns.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `columnNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new number of columns. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if successful. |

### setStartPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartPosition(pos: Int): Unit
```

Sets the start position of this cursor window.

The start position is the zero-based index of the first row that this window contains relative to the entire result set of the [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new zero-based start position. Value is 0 or greater |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

### onAllReferencesReleased

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAllReferencesReleased(): Unit
```

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CursorWindow!>
```
