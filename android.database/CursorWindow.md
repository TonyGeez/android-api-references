# CursorWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorWindow

Kotlin| [Java](../android/database/CursorWindow.md) 
| --- | --- |

```
open class CursorWindow : SQLiteClosable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) ||
| | ↳ | [android.database.CursorWindow](../android/database/CursorWindow.md) |

A buffer containing multiple cursor rows.

A [CursorWindow](../android/database/CursorWindow.md) is read-write when initially created and used locally. When sent to a remote process (by writing it to a [Parcel](../android/os/Parcel.md)), the remote process receives a read-only view of the cursor window. Typically the cursor window will be allocated by the producer, filled with data, and then sent to the consumer for reading.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorWindow](../android/database/CursorWindow.md))`(`localWindow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new empty cursor window. |
| [CursorWindow](../android/database/CursorWindow.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new empty cursor window and gives it a name. |
| [CursorWindow](../android/database/CursorWindow.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `windowSizeBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new empty cursor window and gives it a name. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allocRow](../android/database/CursorWindow.md))`()` Allocates a new row at the end of this cursor window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/database/CursorWindow.md))`()` Clears out the existing contents of the window, making it safe to reuse for new data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copyStringToBuffer](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [CharArrayBuffer](../android/database/CharArrayBuffer.md)!`)` Copies the text of the field at the specified row and column index into a [CharArrayBuffer](../android/database/CharArrayBuffer.md). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/database/CursorWindow.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [freeLastRow](../android/database/CursorWindow.md))`()` Frees the last row in this cursor window. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBlob](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a byte array. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`double`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`float`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as an`int`. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`long`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumRows](../android/database/CursorWindow.md))`()` Gets the number of rows in this window. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a`short`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartPosition](../android/database/CursorWindow.md))`()` Gets the start position of this cursor window. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value of the field at the specified row and column index as a string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the type of the field at the specified row and column index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlob](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFloat](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLong](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isString](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |
| openstatic [CursorWindow](../android/database/CursorWindow.md)! | [newFromParcel](../android/database/CursorWindow.md))`(`p:` ` [Parcel](../android/os/Parcel.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putBlob](../android/database/CursorWindow.md))`(`value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copies a byte array into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putDouble](../android/database/CursorWindow.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a double-precision floating point value into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putLong](../android/database/CursorWindow.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a long integer into the field at the specified row and column index. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putNull](../android/database/CursorWindow.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Puts a null value into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [putString](../android/database/CursorWindow.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Copies a string into the field at the specified row and column index. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setNumColumns](../android/database/CursorWindow.md))`(`columnNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of columns in this window. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartPosition](../android/database/CursorWindow.md))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the start position of this cursor window. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/database/CursorWindow.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/database/CursorWindow.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/database/CursorWindow.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](../android/database/CursorWindow.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](../android/database/sqlite/SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](../android/database/sqlite/SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CursorWindow](../android/database/CursorWindow.md)!\> | [CREATOR](../android/database/CursorWindow.md) <br /> |

## Public constructors

### CursorWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindow(localWindow: Boolean)
```

**Deprecated:** *There is no longer a distinction between local and remote cursor windows. Use the [CursorWindow(java.lang.String)](../android/database/CursorWindow.md))constructor instead.*

Creates a new empty cursor window.

The cursor initially has no rows or columns. Call [setNumColumns(int)](../android/database/CursorWindow.md))to set the number of columns before adding any rows to the cursor.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localWindow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if this window will be used in this process only, false if it might be sent to another processes. This argument is ignored. |

### CursorWindow

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorWindow(name: String!)
```

Creates a new empty cursor window and gives it a name.

The cursor initially has no rows or columns. Call [setNumColumns(int)](../android/database/CursorWindow.md))to set the number of columns before adding any rows to the cursor.

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

The cursor initially has no rows or columns. Call [setNumColumns(int)](../android/database/CursorWindow.md))to set the number of columns before adding any rows to the cursor.

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

The start position ([getStartPosition()](../android/database/CursorWindow.md))), number of rows ([getNumRows()](../android/database/CursorWindow.md))), and number of columns in the cursor are all reset to zero. 

### copyStringToBuffer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun copyStringToBuffer(
    row: Int, 
    column: Int, 
    buffer: CharArrayBuffer!
): Unit
```

Copies the text of the field at the specified row and column index into a [CharArrayBuffer](../android/database/CharArrayBuffer.md).

The buffer is populated as follows:

- If the buffer is too small for the value to be copied, then it is automatically resized.
- If the field is of type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md), then the buffer is set to an empty string.
- If the field is of type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md), then the buffer is set to the contents of the string.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md), then the buffer is set to a string representation of the integer in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%lld`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md), then the buffer is set to a string representation of the floating-point value in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%g`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md), then a [SQLiteException](../android/database/sqlite/SQLiteException.md) is thrown.

<br />

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |
| `buffer` | [CharArrayBuffer](../android/database/CharArrayBuffer.md)!:The [CharArrayBuffer](../android/database/CharArrayBuffer.md) to hold the string. It is automatically resized if the requested string is larger than the buffer's current capacity. |
| --- | --- |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

- If the field is of type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md), then the result is`null`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md), then the result is the blob value.
- If the field is of type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md), then the result is the array of bytes that make up the internal representation of the string value.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md), then a [SQLiteException](../android/database/sqlite/SQLiteException.md) is thrown.

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

- If the field is of type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md), then the result is`0.0`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md), then the result is the value obtained by parsing the string value with`strtod`.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md), then the result is the integer value converted to a`double`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md), then the result is the`double`value.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md), then a [SQLiteException](../android/database/sqlite/SQLiteException.md) is thrown.

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

The result is determined by invoking [getDouble](../android/database/CursorWindow.md))and converting the result to`float`.

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

The result is determined by invoking [getLong](../android/database/CursorWindow.md))and converting the result to`int`.

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

- If the field is of type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md), then the result is`0L`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md), then the result is the value obtained by parsing the string value with`strtoll`.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md), then the result is the`long`value.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md), then the result is the floating-point value converted to a`long`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md), then a [SQLiteException](../android/database/sqlite/SQLiteException.md) is thrown.

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

The result is determined by invoking [getLong](../android/database/CursorWindow.md))and converting the result to`short`.

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

The start position is the zero-based index of the first row that this window contains relative to the entire result set of the [Cursor](../android/database/Cursor.md).

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

- If the field is of type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md), then the result is`null`.
- If the field is of type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md), then the result is the string value.
- If the field is of type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md), then the result is a string representation of the integer in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%lld`.
- If the field is of type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md), then the result is a string representation of the floating-point value in decimal, obtained by formatting the value with the`printf`family of functions using format specifier`%g`.
- If the field is of type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md), then a [SQLiteException](../android/database/sqlite/SQLiteException.md) is thrown.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The field type. Value is [android.database.Cursor#FIELD_TYPE_NULL](../android/database/Cursor.md), [android.database.Cursor#FIELD_TYPE_INTEGER](../android/database/Cursor.md), [android.database.Cursor#FIELD_TYPE_FLOAT](../android/database/Cursor.md), [android.database.Cursor#FIELD_TYPE_STRING](../android/database/Cursor.md), or [android.database.Cursor#FIELD_TYPE_BLOB](../android/database/Cursor.md) |

### isBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBlob(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](../android/database/CursorWindow.md))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_BLOB](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |

### isFloat

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFloat(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](../android/database/CursorWindow.md))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_FLOAT](../android/database/Cursor.md). |

### isLong

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLong(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](../android/database/CursorWindow.md))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_INTEGER](../android/database/Cursor.md). |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](../android/database/CursorWindow.md))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |

### isString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isString(
    row: Int, 
    column: Int
): Boolean
```

**Deprecated:** *Use [getType(int,int)](../android/database/CursorWindow.md))instead.*

Returns true if the field at the specified row and column index has type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based row index. Value is 0 or greater |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The zero-based column index. Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the field has type [Cursor.FIELD_TYPE_STRING](../android/database/Cursor.md) or [Cursor.FIELD_TYPE_NULL](../android/database/Cursor.md). |

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

The start position is the zero-based index of the first row that this window contains relative to the entire result set of the [Cursor](../android/database/Cursor.md).

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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
