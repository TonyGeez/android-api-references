Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteCursor

Kotlin | [Java](../android/database/sqlite/SQLiteCursor.md)
| --- | --- |

```
open class SQLiteCursor : AbstractWindowedCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.AbstractCursor](../android/database/AbstractCursor.md) |||
| | ↳ | [android.database.AbstractWindowedCursor](../android/database/AbstractWindowedCursor.md) ||
| | | ↳ | [android.database.sqlite.SQLiteCursor](../android/database/sqlite/SQLiteCursor.md) |
| --- | --- | --- | --- |

A Cursor implementation that exposes results from a query on a `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase`. SQLiteCursor is not internally synchronized so code using a SQLiteCursor from multiple threads should perform its own synchronization when using the SQLiteCursor.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#SQLiteCursor(android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery)(driver: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver!, editTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, query: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery!)` Execute a query and provide access to its result set through a Cursor interface. |
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#SQLiteCursor(android.database.sqlite.SQLiteDatabase,%20android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery)(db: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!, driver: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursorDriver!, editTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, query: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery!)` Execute a query and provide access to its result set through a Cursor interface. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#close()()` Closes the Cursor, releasing all of its resources and making it completely invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#deactivate()()` Deactivates the Cursor, making all calls on it fail until `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` is called. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#getColumnIndex(kotlin.String)(columnName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the zero-based index for the given column name, or -1 if the column doesn't exist. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#getColumnNames()()` Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#getCount()()` Returns the numbers of rows in the cursor. |
| open [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#getDatabase()()` Get the database that this cursor is associated with. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#onMove(kotlin.Int,%20kotlin.Int)(oldPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#requery()()` Performs the query that created the cursor again, refreshing its contents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#setFillWindowForwardOnly(kotlin.Boolean)(fillWindowForwardOnly: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls fetching of rows relative to requested position. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#setSelectionArguments(kotlin.Array)(selectionArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Changes the selection arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#setWindow(android.database.CursorWindow)(window: https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#!)` Sets a new cursor window for the cursor to use. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#finalize()()` Release the native resources, if they haven't been released yet. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#checkPosition()()` This function throws CursorIndexOutOfBoundsException if the cursor position is out of bounds. Subclass implementations of the get functions should call this before attempting to retrieve data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, buffer: https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer.html#!)` Retrieves the requested column text and stores it in the buffer provided. If the buffer size is not sufficient, a new char buffer will be allocated and assigned to CharArrayBuffer.data <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getBlob(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a byte array. The result and whether this method throws an exception when the column value is null or the column type is not a blob type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getDouble(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a double. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `double` value is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getFloat(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a float. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `float` value is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getInt(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as an int. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Integer.MIN_VALUE`, `Integer.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getLong(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a long. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Long.MIN_VALUE`, `Long.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getShort(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a short. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Short.MIN_VALUE`, `Short.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getString(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a String. The result and whether this method throws an exception when the column value is null or the column type is not a string type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getType(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getInt(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getFloat(kotlin.Int)` etc. <br /> | | `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#getWindow()()` If the cursor is backed by a `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#`, returns a pre-filled window with the contents of the cursor, otherwise null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#hasWindow()()` Returns true if the cursor has an associated cursor window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#isBlob(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#isFloat(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#isLong(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#isNull(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `true` if the value in the indicated column is null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#isString(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#close()()` Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()` a call to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` will not make the Cursor valid again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#deactivate()()` Deactivates the Cursor, making all calls on it fail until `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` is called. Inactive Cursors use fewer resources than active Cursors. Calling `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` will make the cursor active again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#fillWindow(kotlin.Int,%20android.database.CursorWindow)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, window: https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#!)` Copies cursor data into the window. Clears the window and fills it with data beginning at the requested row position until all of the data in the cursor is exhausted or the window runs out of space. The filled window uses the same row indices as the original cursor. For example, if you fill a window starting from row 5 from the cursor, you can query the contents of row 5 from the window just by asking it for row 5 because there is a direct correspondence between the row indices used by the cursor and the window. The current position of the cursor, as returned by `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getPosition()`, is not changed by this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getColumnCount()()` Return total number of columns <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getColumnIndex(kotlin.String)(columnName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getColumnIndexOrThrow(kotlin.String)` instead, which will make the error more clear. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getColumnIndexOrThrow(kotlin.String)(columnName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the zero-based index for the given column name, or throws `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the column doesn't exist. If you're not sure if a column will exist or not use `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getColumnIndex(kotlin.String)` and check for -1, which is more efficient than catching the exceptions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getColumnName(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the column name at the given zero-based column index. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getColumnNames()()` Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getCount()()` Returns the numbers of rows in the cursor. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getExtras()()` Returns a bundle of extra values. This is an optional way for cursors to provide out-of-band metadata to their users. One use of this is for reporting on the progress of network requests that are required to fetch data for the cursor. These values may only change when requery is called. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getNotificationUri()()` Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getNotificationUris()()` Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)`. If this is not implemented, this is equivalent to calling `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getNotificationUri()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getPosition()()` Returns the current position of the cursor in the row set. The value is zero-based. When the row set is first returned the cursor will be at positon -1, which is before the first row. After the last row is returned another call to next() will leave the cursor past the last entry, at a position of count(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getUpdatedField(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#getWantsAllOnMoveCalls()()` onMove() will only be called across processes if this method returns true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isAfterLast()()` Returns whether the cursor is pointing to the position after the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isBeforeFirst()()` Returns whether the cursor is pointing to the position before the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isClosed()()` return true if the cursor is closed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isFieldUpdated(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isFirst()()` Returns whether the cursor is pointing to the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#isLast()()` Returns whether the cursor is pointing to the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#move(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the cursor by a relative amount, forward or backward, from the current position. Positive offsets move forwards, negative offsets move backwards. If the final position is outside of the bounds of the result set then the resultant position will be pinned to -1 or count() depending on whether the value is off the front or end of the set, respectively. This method will return true if the requested destination was reachable, otherwise, it returns false. For example, if the cursor is at currently on the second entry in the result set and move(-5) is called, the position will be pinned at -1, and false will be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#moveToFirst()()` Move the cursor to the first row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#moveToLast()()` Move the cursor to the last row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#moveToNext()()` Move the cursor to the next row. This method will return false if the cursor is already past the last entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#moveToPosition(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the cursor to an absolute position. The valid range of values is -1 \<= position \<= count. This method will return true if the request destination was reachable, otherwise, it returns false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#moveToPrevious()()` Move the cursor to the previous row. This method will return false if the cursor is already before the first entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#onChange(kotlin.Boolean)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Subclasses must call this method when they finish committing updates to notify all observers. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#onMove(kotlin.Int,%20kotlin.Int)(oldPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#registerContentObserver(android.database.ContentObserver)(observer: https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#!)` Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#registerDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()`, `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()`, or #close(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#requery()()` Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()`. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#respond(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` This is an out-of-band way for the user of a cursor to communicate with the cursor. The structure of each bundle is entirely defined by the cursor. One use of this is to tell a cursor that it should retry its network request after it reported an error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#setExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Sets a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that will be returned by `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getExtras()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)(cr: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!, notifyUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Specifies a content URI to watch for changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)(cr: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, notifyUris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Similar to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`, except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with the first URI in `uris`. Calling this overrides any previous call to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#unregisterContentObserver(android.database.ContentObserver)(observer: https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#!)` Unregister an observer that has previously been registered with this cursor via `https://developer.android.com/reference/kotlin/android/database/Cursor.html#registerContentObserver(android.database.ContentObserver)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#unregisterDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#!)` Unregister an observer that has previously been registered with this cursor via `https://developer.android.com/reference/kotlin/android/database/Cursor.html#registerContentObserver(android.database.ContentObserver)`. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#mClosed:kotlin.Boolean` <br /> | | `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#mContentResolver:android.content.ContentResolver` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#mPos:kotlin.Int` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#` |---|---| | `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#mWindow:android.database.CursorWindow` The cursor window owned by this cursor. <br /> | ||

## Public constructors

### SQLiteCursor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteCursor(
    driver: SQLiteCursorDriver!, 
    editTable: String!, 
    query: SQLiteQuery!)
```

Execute a query and provide access to its result set through a Cursor interface. For a query such as: `SELECT name, birth, phone FROM myTable WHERE ... LIMIT 1,20 ORDER BY...` the column names (name, birth, phone) would be in the projection argument and everything from `FROM` onward would be in the params argument.

| Parameters ||
|---|---|
| `editTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table used for this query |
| `query` | [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md)!: the `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery` object associated with this cursor object. |

### SQLiteCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteCursor(
    db: SQLiteDatabase!, 
    driver: SQLiteCursorDriver!, 
    editTable: String!, 
    query: SQLiteQuery!)
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#SQLiteCursor(android.database.sqlite.SQLiteCursorDriver,%20kotlin.String,%20android.database.sqlite.SQLiteQuery)` instead*

Execute a query and provide access to its result set through a Cursor interface. For a query such as: `SELECT name, birth, phone FROM myTable WHERE ... LIMIT 1,20 ORDER BY...` the column names (name, birth, phone) would be in the projection argument and everything from `FROM` onward would be in the params argument.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)!: a reference to a Database object that is already constructed and opened. This param is not used any longer |
| `editTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table used for this query |
| `query` | [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md)!: the rest of the query terms cursor is finalized |
| --- | --- |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()` a call to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` will not make the Cursor valid again.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deactivate(): Unit
```

Deactivates the Cursor, making all calls on it fail until `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` is called. Inactive Cursors use fewer resources than active Cursors. Calling `https://developer.android.com/reference/kotlin/android/database/Cursor.html#requery()` will make the cursor active again.

### getColumnIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColumnIndex(columnName: String!): Int
```

Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use `https://developer.android.com/reference/kotlin/android/database/Cursor.html#getColumnIndexOrThrow(kotlin.String)` instead, which will make the error more clear.

| Parameters ||
|---|---|
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the target column. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the zero-based column index for the given column name, or -1 if the column name does not exist. Value is -1 or greater |

### getColumnNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColumnNames(): Array<String!>!
```

Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the names of the columns returned in this query. |

### getCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCount(): Int
```

Returns the numbers of rows in the cursor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of rows in the cursor. Value is 0 or greater |

### getDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDatabase(): SQLiteDatabase!
```

Get the database that this cursor is associated with.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase!` | the SQLiteDatabase that this cursor is associated with. |

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
|---|---|
| `oldPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position that we're moving from |
| `newPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position that we're moving to |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the move is successful, false otherwise |

### requery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requery(): Boolean
```

Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to `https://developer.android.com/reference/kotlin/android/database/Cursor.html#deactivate()`. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the requery succeeded, false if not, in which case the cursor becomes invalid. |

### setFillWindowForwardOnly

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillWindowForwardOnly(fillWindowForwardOnly: Boolean): Unit
```

Controls fetching of rows relative to requested position.

Calling this method defines how rows will be loaded, but it doesn't affect rows that are already in the window. This setting is preserved if a new window is `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCursor#setWindow(android.database.CursorWindow)`

| Parameters ||
|---|---|
| `fillWindowForwardOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, rows will be fetched starting from requested position up to the window's capacity. Default value is false. |

### setSelectionArguments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelectionArguments(selectionArgs: Array<String!>!): Unit
```

Changes the selection arguments. The new values take effect after a call to requery().

### setWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWindow(window: CursorWindow!): Unit
```

Sets a new cursor window for the cursor to use.

The cursor takes ownership of the provided cursor window; the cursor window will be closed when the cursor is closed or when the cursor adopts a new cursor window.

If the cursor previously had a cursor window, then it is closed when the new cursor window is assigned.

| Parameters ||
|---|---|
| `window` | [CursorWindow](../android/database/CursorWindow.md)!: The new cursor window, typically a remote cursor window. |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun finalize(): Unit
```

Release the native resources, if they haven't been released yet.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
