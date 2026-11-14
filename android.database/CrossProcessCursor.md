Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CrossProcessCursor

Kotlin | [Java](CrossProcessCursor.md)
| --- | --- |

```
interface CrossProcessCursor : Cursor
```

| [android.database.CrossProcessCursor](CrossProcessCursor.md) |

| Known Direct Subclasses [AbstractCursor](AbstractCursor.md), [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) |---|---| | [AbstractCursor](AbstractCursor.md) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. | | [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) | Cursor wrapper that implements CrossProcessCursor. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractWindowedCursor](AbstractWindowedCursor.md), [MatrixCursor](MatrixCursor.md), [MergeCursor](MergeCursor.md), [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) |---|---| | [AbstractWindowedCursor](AbstractWindowedCursor.md) | A base class for Cursors that store their data in CursorWindows. | | [MatrixCursor](MatrixCursor.md) | A mutable cursor implementation backed by an array of `Object`s. | | [MergeCursor](MergeCursor.md) | A convenience class that lets you present an array of Cursors as a single linear Cursor. | | [SQLiteCursor](../android.database.sqlite/SQLiteCursor.md) | A Cursor implementation that exposes results from a query on a SQLiteDatabase. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A cross process cursor is an extension of a Cursor that also supports usage from remote processes.

The contents of a cross process cursor are marshalled to the remote process by filling CursorWindow objects using fillWindow. As an optimization, the cursor can provide a pre-filled window to use via getWindow thereby obviating the need to copy the data to yet another cursor window.

## Summary

| Inherited constants ||
|---|---|
| From class Cursor |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int` Value returned by getType if the specified column type is blob <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int` Value returned by getType if the specified column type is float <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int` Value returned by getType if the specified column type is integer <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int` Value returned by getType if the specified column is null <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int` Value returned by getType if the specified column type is string <br /> | ||

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fillWindow Copies cursor data into the window. |
| abstract [CursorWindow](CursorWindow.md)! | getWindow Returns a pre-filled window that contains the data within this cursor. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onMove This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class Cursor |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | close Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike deactivate a call to requery will not make the Cursor valid again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | copyStringToBuffer Retrieves the requested column text and stores it in the buffer provided. If the buffer size is not sufficient, a new char buffer will be allocated and assigned to CharArrayBuffer.data <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | deactivate Deactivates the Cursor, making all calls on it fail until requery is called. Inactive Cursors use fewer resources than active Cursors. Calling requery will make the cursor active again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | getBlob Returns the value of the requested column as a byte array. The result and whether this method throws an exception when the column value is null or the column type is not a blob type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnCount Return total number of columns <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnIndex Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use getColumnIndexOrThrow instead, which will make the error more clear. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnIndexOrThrow Returns the zero-based index for the given column name, or throws `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the column doesn't exist. If you're not sure if a column will exist or not use getColumnIndex and check for -1, which is more efficient than catching the exceptions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getColumnName Returns the column name at the given zero-based column index. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | getColumnNames Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getCount Returns the numbers of rows in the cursor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | getDouble Returns the value of the requested column as a double. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `double` value is implementation-defined. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | getExtras Returns a bundle of extra values. This is an optional way for cursors to provide out-of-band metadata to their users. One use of this is for reporting on the progress of network requests that are required to fetch data for the cursor. These values may only change when requery is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | getFloat Returns the value of the requested column as a float. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `float` value is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getInt Returns the value of the requested column as an int. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Integer.MIN_VALUE`, `Integer.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getLong Returns the value of the requested column as a long. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Long.MIN_VALUE`, `Long.MAX_VALUE`\] is implementation-defined. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | getNotificationUri Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by setNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?` | getNotificationUris Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by setNotificationUris. If this is not implemented, this is equivalent to calling getNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getPosition Returns the current position of the cursor in the row set. The value is zero-based. When the row set is first returned the cursor will be at positon -1, which is before the first row. After the last row is returned another call to next() will leave the cursor past the last entry, at a position of count(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | getShort Returns the value of the requested column as a short. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Short.MIN_VALUE`, `Short.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getString Returns the value of the requested column as a String. The result and whether this method throws an exception when the column value is null or the column type is not a string type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getType Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as getInt, getFloat etc. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getWantsAllOnMoveCalls onMove() will only be called across processes if this method returns true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isAfterLast Returns whether the cursor is pointing to the position after the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isBeforeFirst Returns whether the cursor is pointing to the position before the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isClosed return true if the cursor is closed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFirst Returns whether the cursor is pointing to the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isLast Returns whether the cursor is pointing to the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isNull Returns `true` if the value in the indicated column is null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | move Move the cursor by a relative amount, forward or backward, from the current position. Positive offsets move forwards, negative offsets move backwards. If the final position is outside of the bounds of the result set then the resultant position will be pinned to -1 or count() depending on whether the value is off the front or end of the set, respectively. This method will return true if the requested destination was reachable, otherwise, it returns false. For example, if the cursor is at currently on the second entry in the result set and move(-5) is called, the position will be pinned at -1, and false will be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToFirst Move the cursor to the first row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToLast Move the cursor to the last row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToNext Move the cursor to the next row. This method will return false if the cursor is already past the last entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToPosition Move the cursor to an absolute position. The valid range of values is -1 \<= position \<= count. This method will return true if the request destination was reachable, otherwise, it returns false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToPrevious Move the cursor to the previous row. This method will return false if the cursor is already before the first entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerContentObserver Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until requery is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerDataSetObserver Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via requery, deactivate, or #close(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | requery Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to deactivate. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | respond This is an out-of-band way for the user of a cursor to communicate with the cursor. The structure of each bundle is entirely defined by the cursor. One use of this is to tell a cursor that it should retry its network request after it reported an error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setExtras Sets a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that will be returned by getExtras. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setNotificationUri Register to watch a content URI for changes. This can be the URI of a specific data row (for example, "content://my_provider_type/23"), or a a generic URI for a content type. Calling this overrides any previous call to setNotificationUris. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setNotificationUris Similar to setNotificationUri, except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling setNotificationUri with the first URI in `uris`. Calling this overrides any previous call to setNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterContentObserver Unregister an observer that has previously been registered with this cursor via registerContentObserver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterDataSetObserver Unregister an observer that has previously been registered with this cursor via registerContentObserver. <br /> | ||

## Public methods

### fillWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun fillWindow(
    position: Int, 
    window: CursorWindow!
): Unit
```

Copies cursor data into the window.

Clears the window and fills it with data beginning at the requested row position until all of the data in the cursor is exhausted or the window runs out of space.

The filled window uses the same row indices as the original cursor. For example, if you fill a window starting from row 5 from the cursor, you can query the contents of row 5 from the window just by asking it for row 5 because there is a direct correspondence between the row indices used by the cursor and the window.

The current position of the cursor, as returned by getPosition, is not changed by this method.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The zero-based index of the first row to copy into the window. |
| `window` | [CursorWindow](CursorWindow.md)!: The window to fill. |

### getWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getWindow(): CursorWindow!
```

Returns a pre-filled window that contains the data within this cursor.

In particular, the window contains the row indicated by getPosition. The window's contents are automatically scrolled whenever the current row moved outside the range covered by the window.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/CursorWindow!` | The pre-filled window, or null if none. |

### onMove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onMove(
    oldPosition: Int, 
    newPosition: Int
): Boolean
```

This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position.

This function should be called by methods such as moveToPosition, so it will typically not be called from outside of the cursor class itself.

| Parameters ||
|---|---|
| `oldPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position that we're moving from. |
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position that we're moving to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the move is successful, false otherwise. |
