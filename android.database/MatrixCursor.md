Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MatrixCursor

Kotlin | [Java](https://developer.android.com/reference/android/database/MatrixCursor "View this page in Java")

```
open class MatrixCursor : AbstractCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.database.AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) ||
| | ↳ | [android.database.MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor#) |

A mutable cursor implementation backed by an array of `Object`s. Use `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#newRow()` to add rows. Automatically expands internal capacity as needed.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor.RowBuilder` Builds a row of values using either of these approaches: - Values can be added with explicit column ordering using `https://developer.android.com/reference/kotlin/android/database/MatrixCursor.RowBuilder#add(kotlin.Any)`, which starts from the left-most column and adds one column value at a time. This follows the same ordering as the column names specified at cursor construction time. - Column and value pairs can be offered for possible inclusion using `https://developer.android.com/reference/kotlin/android/database/MatrixCursor.RowBuilder#add(kotlin.String,%20kotlin.Any)`. If the cursor includes the given column, the value will be set for that column, otherwise the value is ignored. This approach is useful when matching data to a custom projection. Undefined values are left as `null`. <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#MatrixCursor(kotlin.Array)(columnNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Constructs a new cursor. |
| `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#MatrixCursor(kotlin.Array,%20kotlin.Int)(columnNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, initialCapacity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new cursor with the given initial capacity. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#addRow(kotlin.collections.MutableIterable)(columnValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html<*>!)` Adds a new row to the end with the given column values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#addRow(kotlin.Array)(columnValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!)` Adds a new row to the end with the given column values. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getBlob(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a byte array. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getColumnNames()()` Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getCount()()` Returns the numbers of rows in the cursor. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getDouble(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a double. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getFloat(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a float. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getInt(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as an int. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getLong(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a long. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getShort(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a short. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getString(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the requested column as a String. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#getType(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns data type of the given column's value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#isNull(kotlin.Int)(column: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `true` if the value in the indicated column is null. |
| open [MatrixCursor.RowBuilder](https://developer.android.com/reference/kotlin/android/database/MatrixCursor.RowBuilder)! | `https://developer.android.com/reference/kotlin/android/database/MatrixCursor#newRow()()` Adds a new row to the end and returns a builder for that row. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractCursor` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#checkPosition()()` This function throws CursorIndexOutOfBoundsException if the cursor position is out of bounds. Subclass implementations of the get functions should call this before attempting to retrieve data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#close()()` Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike `https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()` a call to `https://developer.android.com/reference/kotlin/android/database/Cursor#requery()` will not make the Cursor valid again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, buffer: https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer!)` Retrieves the requested column text and stores it in the buffer provided. If the buffer size is not sufficient, a new char buffer will be allocated and assigned to CharArrayBuffer.data <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#deactivate()()` Deactivates the Cursor, making all calls on it fail until `https://developer.android.com/reference/kotlin/android/database/Cursor#requery()` is called. Inactive Cursors use fewer resources than active Cursors. Calling `https://developer.android.com/reference/kotlin/android/database/Cursor#requery()` will make the cursor active again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#fillWindow(kotlin.Int,%20android.database.CursorWindow)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, window: https://developer.android.com/reference/kotlin/android/database/CursorWindow!)` Copies cursor data into the window. Clears the window and fills it with data beginning at the requested row position until all of the data in the cursor is exhausted or the window runs out of space. The filled window uses the same row indices as the original cursor. For example, if you fill a window starting from row 5 from the cursor, you can query the contents of row 5 from the window just by asking it for row 5 because there is a direct correspondence between the row indices used by the cursor and the window. The current position of the cursor, as returned by `https://developer.android.com/reference/kotlin/android/database/Cursor#getPosition()`, is not changed by this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnCount()()` Return total number of columns <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndex(kotlin.String)(columnName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use `https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndexOrThrow(kotlin.String)` instead, which will make the error more clear. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnIndexOrThrow(kotlin.String)(columnName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the zero-based index for the given column name, or throws `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the column doesn't exist. If you're not sure if a column will exist or not use `https://developer.android.com/reference/kotlin/android/database/Cursor#getColumnIndex(kotlin.String)` and check for -1, which is more efficient than catching the exceptions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getColumnName(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the column name at the given zero-based column index. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getExtras()()` Returns a bundle of extra values. This is an optional way for cursors to provide out-of-band metadata to their users. One use of this is for reporting on the progress of network requests that are required to fetch data for the cursor. These values may only change when requery is called. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUri()()` Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by `https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getNotificationUris()()` Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by `https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)`. If this is not implemented, this is equivalent to calling `https://developer.android.com/reference/kotlin/android/database/Cursor#getNotificationUri()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getPosition()()` Returns the current position of the cursor in the row set. The value is zero-based. When the row set is first returned the cursor will be at positon -1, which is before the first row. After the last row is returned another call to next() will leave the cursor past the last entry, at a position of count(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getUpdatedField(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getWantsAllOnMoveCalls()()` onMove() will only be called across processes if this method returns true. <br /> | | `https://developer.android.com/reference/kotlin/android/database/CursorWindow!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#getWindow()()` If the cursor is backed by a `https://developer.android.com/reference/kotlin/android/database/CursorWindow`, returns a pre-filled window with the contents of the cursor, otherwise null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isAfterLast()()` Returns whether the cursor is pointing to the position after the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isBeforeFirst()()` Returns whether the cursor is pointing to the position before the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isClosed()()` return true if the cursor is closed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFieldUpdated(kotlin.Int)(columnIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isFirst()()` Returns whether the cursor is pointing to the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#isLast()()` Returns whether the cursor is pointing to the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#move(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the cursor by a relative amount, forward or backward, from the current position. Positive offsets move forwards, negative offsets move backwards. If the final position is outside of the bounds of the result set then the resultant position will be pinned to -1 or count() depending on whether the value is off the front or end of the set, respectively. This method will return true if the requested destination was reachable, otherwise, it returns false. For example, if the cursor is at currently on the second entry in the result set and move(-5) is called, the position will be pinned at -1, and false will be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToFirst()()` Move the cursor to the first row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToLast()()` Move the cursor to the last row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToNext()()` Move the cursor to the next row. This method will return false if the cursor is already past the last entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPosition(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the cursor to an absolute position. The valid range of values is -1 \<= position \<= count. This method will return true if the request destination was reachable, otherwise, it returns false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#moveToPrevious()()` Move the cursor to the previous row. This method will return false if the cursor is already before the first entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onChange(kotlin.Boolean)(selfChange: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Subclasses must call this method when they finish committing updates to notify all observers. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#onMove(kotlin.Int,%20kotlin.Int)(oldPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newPosition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerContentObserver(android.database.ContentObserver)(observer: https://developer.android.com/reference/kotlin/android/database/ContentObserver!)` Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until `https://developer.android.com/reference/kotlin/android/database/Cursor#requery()` is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#registerDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver!)` Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via `https://developer.android.com/reference/kotlin/android/database/Cursor#requery()`, `https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()`, or #close(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#requery()()` Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to `https://developer.android.com/reference/kotlin/android/database/Cursor#deactivate()`. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#respond(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` This is an out-of-band way for the user of a cursor to communicate with the cursor. The structure of each bundle is entirely defined by the cursor. One use of this is to tell a cursor that it should retry its network request after it reported an error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Sets a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that will be returned by `https://developer.android.com/reference/kotlin/android/database/Cursor#getExtras()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)(cr: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!, notifyUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Specifies a content URI to watch for changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#setNotificationUris(android.content.ContentResolver,%20kotlin.collections.MutableList)(cr: https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#, notifyUris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>)` Similar to `https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`, except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling `https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)` with the first URI in `uris`. Calling this overrides any previous call to `https://developer.android.com/reference/kotlin/android/database/Cursor#setNotificationUri(android.content.ContentResolver,%20android.net.Uri)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterContentObserver(android.database.ContentObserver)(observer: https://developer.android.com/reference/kotlin/android/database/ContentObserver!)` Unregister an observer that has previously been registered with this cursor via `https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#unregisterDataSetObserver(android.database.DataSetObserver)(observer: https://developer.android.com/reference/kotlin/android/database/DataSetObserver!)` Unregister an observer that has previously been registered with this cursor via `https://developer.android.com/reference/kotlin/android/database/Cursor#registerContentObserver(android.database.ContentObserver)`. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractCursor` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mClosed:kotlin.Boolean` <br /> | | `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#!` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mContentResolver:android.content.ContentResolver` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/database/AbstractCursor#mPos:kotlin.Int` <br /> | ||

## Public constructors

### MatrixCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MatrixCursor(columnNames: Array<String!>!)
```

Constructs a new cursor.

| Parameters ||
|---|---|
| `columnNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: names of the columns, the ordering of which determines column ordering elsewhere in this cursor |

### MatrixCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MatrixCursor(
    columnNames: Array<String!>!, 
    initialCapacity: Int)
```

Constructs a new cursor with the given initial capacity.

| Parameters ||
|---|---|
| `columnNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: names of the columns, the ordering of which determines column ordering elsewhere in this cursor |
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): in rows |

## Public methods

### addRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRow(columnValues: MutableIterable<*>!): Unit
```

Adds a new row to the end with the given column values. Not safe for concurrent use.

| Parameters ||
|---|---|
| `columnValues` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\<\*\>!: in the same order as the the column names specified at cursor construction time |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `columnValues.size() != columnNames.length` |

### addRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addRow(columnValues: Array<Any!>!): Unit
```

Adds a new row to the end with the given column values. Not safe for concurrent use.

| Parameters ||
|---|---|
| `columnValues` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: in the same order as the the column names specified at cursor construction time |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `columnValues.length != columnNames.length` |

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBlob(column: Int): ByteArray!
```

Returns the value of the requested column as a byte array.

The result and whether this method throws an exception when the column value is null or the column type is not a blob type is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the value of that column as a byte array. |

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

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDouble(column: Int): Double
```

Returns the value of the requested column as a double.

The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `double` value is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value of that column as a double. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFloat(column: Int): Float
```

Returns the value of the requested column as a float.

The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `float` value is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the value of that column as a float. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInt(column: Int): Int
```

Returns the value of the requested column as an int.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Integer.MIN_VALUE`, `Integer.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of that column as an int. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLong(column: Int): Long
```

Returns the value of the requested column as a long.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Long.MIN_VALUE`, `Long.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value of that column as a long. |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShort(column: Int): Short
```

Returns the value of the requested column as a short.

The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Short.MIN_VALUE`, `Short.MAX_VALUE`\] is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the value of that column as a short. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(column: Int): String!
```

Returns the value of the requested column as a String.

The result and whether this method throws an exception when the column value is null or the column type is not a string type is implementation-defined.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the value of that column as a String. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(column: Int): Int
```

Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as `https://developer.android.com/reference/kotlin/android/database/Cursor#getInt(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/database/Cursor#getFloat(kotlin.Int)` etc.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | column value type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_NULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_INTEGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_FLOAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_STRING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/database/Cursor#FIELD_TYPE_BLOB:kotlin.Int` |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNull(column: Int): Boolean
```

Returns `true` if the value in the indicated column is null.

| Parameters ||
|---|---|
| `columnIndex` | the zero-based index of the target column. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the column value is null. |

### newRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newRow(): MatrixCursor.RowBuilder!
```

Adds a new row to the end and returns a builder for that row. Not safe for concurrent use.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/MatrixCursor.RowBuilder!` | builder which can be used to set the column values for the new row |
