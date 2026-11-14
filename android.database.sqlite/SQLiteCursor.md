Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteCursor

Kotlin | [Java](SQLiteCursor.md)
| --- | --- |

```
open class SQLiteCursor : AbstractWindowedCursor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.AbstractCursor](../android.database/AbstractCursor.md) |||
| | ↳ | [android.database.AbstractWindowedCursor](../android.database/AbstractWindowedCursor.md) ||
| | | ↳ | [android.database.sqlite.SQLiteCursor](SQLiteCursor.md) |
| --- | --- | --- | --- |

A Cursor implementation that exposes results from a query on a SQLiteDatabase. SQLiteCursor is not internally synchronized so code using a SQLiteCursor from multiple threads should perform its own synchronization when using the SQLiteCursor.

## Summary

| Public constructors ||
|---|---|
| SQLiteCursor Execute a query and provide access to its result set through a Cursor interface. |
| SQLiteCursor Execute a query and provide access to its result set through a Cursor interface. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes the Cursor, releasing all of its resources and making it completely invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | deactivate Deactivates the Cursor, making all calls on it fail until requery is called. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getColumnIndex Returns the zero-based index for the given column name, or -1 if the column doesn't exist. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getColumnNames Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCount Returns the numbers of rows in the cursor. |
| open [SQLiteDatabase](SQLiteDatabase.md)! | getDatabase Get the database that this cursor is associated with. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onMove This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | requery Performs the query that created the cursor again, refreshing its contents. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFillWindowForwardOnly Controls fetching of rows relative to requested position. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSelectionArguments Changes the selection arguments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWindow Sets a new cursor window for the cursor to use. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Release the native resources, if they haven't been released yet. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | checkPosition This function throws CursorIndexOutOfBoundsException if the cursor position is out of bounds. Subclass implementations of the get functions should call this before attempting to retrieve data. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | copyStringToBuffer Retrieves the requested column text and stores it in the buffer provided. If the buffer size is not sufficient, a new char buffer will be allocated and assigned to CharArrayBuffer.data <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | getBlob Returns the value of the requested column as a byte array. The result and whether this method throws an exception when the column value is null or the column type is not a blob type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | getDouble Returns the value of the requested column as a double. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `double` value is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | getFloat Returns the value of the requested column as a float. The result and whether this method throws an exception when the column value is null, the column type is not a floating-point type, or the floating-point value is not representable as a `float` value is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getInt Returns the value of the requested column as an int. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Integer.MIN_VALUE`, `Integer.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getLong Returns the value of the requested column as a long. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Long.MIN_VALUE`, `Long.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | getShort Returns the value of the requested column as a short. The result and whether this method throws an exception when the column value is null, the column type is not an integral type, or the integer value is outside the range \[`Short.MIN_VALUE`, `Short.MAX_VALUE`\] is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getString Returns the value of the requested column as a String. The result and whether this method throws an exception when the column value is null or the column type is not a string type is implementation-defined. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getType Returns data type of the given column's value. The preferred type of the column is returned but the data may be converted to other types as documented in the get-type methods such as getInt, getFloat etc. <br /> | | `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#!` | getWindow If the cursor is backed by a `https://developer.android.com/reference/kotlin/android/database/CursorWindow.html#`, returns a pre-filled window with the contents of the cursor, otherwise null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasWindow Returns true if the cursor has an associated cursor window. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isBlob <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFloat <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isLong <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isNull Returns `true` if the value in the indicated column is null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isString <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/database/AbstractCursor.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | close Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike deactivate a call to requery will not make the Cursor valid again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | deactivate Deactivates the Cursor, making all calls on it fail until requery is called. Inactive Cursors use fewer resources than active Cursors. Calling requery will make the cursor active again. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | fillWindow Copies cursor data into the window. Clears the window and fills it with data beginning at the requested row position until all of the data in the cursor is exhausted or the window runs out of space. The filled window uses the same row indices as the original cursor. For example, if you fill a window starting from row 5 from the cursor, you can query the contents of row 5 from the window just by asking it for row 5 because there is a direct correspondence between the row indices used by the cursor and the window. The current position of the cursor, as returned by getPosition, is not changed by this method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnCount Return total number of columns <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnIndex Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use getColumnIndexOrThrow instead, which will make the error more clear. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getColumnIndexOrThrow Returns the zero-based index for the given column name, or throws `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the column doesn't exist. If you're not sure if a column will exist or not use getColumnIndex and check for -1, which is more efficient than catching the exceptions. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getColumnName Returns the column name at the given zero-based column index. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | getColumnNames Returns a string array holding the names of all of the columns in the result set in the order in which they were listed in the result. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getCount Returns the numbers of rows in the cursor. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | getExtras Returns a bundle of extra values. This is an optional way for cursors to provide out-of-band metadata to their users. One use of this is for reporting on the progress of network requests that are required to fetch data for the cursor. These values may only change when requery is called. <br /> | | `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | getNotificationUri Return the URI at which notifications of changes in this Cursor's data will be delivered, as previously set by setNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?` | getNotificationUris Return the URIs at which notifications of changes in this Cursor's data will be delivered, as previously set by setNotificationUris. If this is not implemented, this is equivalent to calling getNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getPosition Returns the current position of the cursor in the row set. The value is zero-based. When the row set is first returned the cursor will be at positon -1, which is before the first row. After the last row is returned another call to next() will leave the cursor past the last entry, at a position of count(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | getUpdatedField <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getWantsAllOnMoveCalls onMove() will only be called across processes if this method returns true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isAfterLast Returns whether the cursor is pointing to the position after the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isBeforeFirst Returns whether the cursor is pointing to the position before the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isClosed return true if the cursor is closed <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFieldUpdated <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isFirst Returns whether the cursor is pointing to the first row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isLast Returns whether the cursor is pointing to the last row. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | move Move the cursor by a relative amount, forward or backward, from the current position. Positive offsets move forwards, negative offsets move backwards. If the final position is outside of the bounds of the result set then the resultant position will be pinned to -1 or count() depending on whether the value is off the front or end of the set, respectively. This method will return true if the requested destination was reachable, otherwise, it returns false. For example, if the cursor is at currently on the second entry in the result set and move(-5) is called, the position will be pinned at -1, and false will be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToFirst Move the cursor to the first row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToLast Move the cursor to the last row. This method will return false if the cursor is empty. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToNext Move the cursor to the next row. This method will return false if the cursor is already past the last entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToPosition Move the cursor to an absolute position. The valid range of values is -1 \<= position \<= count. This method will return true if the request destination was reachable, otherwise, it returns false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | moveToPrevious Move the cursor to the previous row. This method will return false if the cursor is already before the first entry in the result set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onChange Subclasses must call this method when they finish committing updates to notify all observers. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onMove This function is called every time the cursor is successfully scrolled to a new position, giving the subclass a chance to update any state it may have. If it returns false the move function will also do so and the cursor will scroll to the beforeFirst position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerContentObserver Register an observer that is called when changes happen to the content backing this cursor. Typically the data set won't change until requery is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerDataSetObserver Register an observer that is called when changes happen to the contents of the this cursors data set, for example, when the data set is changed via requery, deactivate, or #close(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | requery Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to deactivate. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | respond This is an out-of-band way for the user of a cursor to communicate with the cursor. The structure of each bundle is entirely defined by the cursor. One use of this is to tell a cursor that it should retry its network request after it reported an error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setExtras Sets a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` that will be returned by getExtras. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setNotificationUri Specifies a content URI to watch for changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setNotificationUris Similar to setNotificationUri, except this version allows to watch multiple content URIs for changes. If this is not implemented, this is equivalent to calling setNotificationUri with the first URI in `uris`. Calling this overrides any previous call to setNotificationUri. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterContentObserver Unregister an observer that has previously been registered with this cursor via registerContentObserver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterDataSetObserver Unregister an observer that has previously been registered with this cursor via registerContentObserver. <br /> | ||

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
| `query` | [SQLiteQuery](SQLiteQuery.md)!: the SQLiteQuery object associated with this cursor object. |

### SQLiteCursor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SQLiteCursor(
    db: SQLiteDatabase!, 
    driver: SQLiteCursorDriver!, 
    editTable: String!, 
    query: SQLiteQuery!)
```

**Deprecated:** *use SQLiteCursor instead*

Execute a query and provide access to its result set through a Cursor interface. For a query such as: `SELECT name, birth, phone FROM myTable WHERE ... LIMIT 1,20 ORDER BY...` the column names (name, birth, phone) would be in the projection argument and everything from `FROM` onward would be in the params argument.

| Parameters ||
|---|---|
| `db` | [SQLiteDatabase](SQLiteDatabase.md)!: a reference to a Database object that is already constructed and opened. This param is not used any longer |
| `editTable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the table used for this query |
| `query` | [SQLiteQuery](SQLiteQuery.md)!: the rest of the query terms cursor is finalized |
| --- | --- |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Closes the Cursor, releasing all of its resources and making it completely invalid. Unlike deactivate a call to requery will not make the Cursor valid again.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### deactivate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deactivate(): Unit
```

Deactivates the Cursor, making all calls on it fail until requery is called. Inactive Cursors use fewer resources than active Cursors. Calling requery will make the cursor active again.

### getColumnIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColumnIndex(columnName: String!): Int
```

Returns the zero-based index for the given column name, or -1 if the column doesn't exist. If you expect the column to exist use getColumnIndexOrThrow instead, which will make the error more clear.

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

Performs the query that created the cursor again, refreshing its contents. This may be done at any time, including after a call to deactivate. Since this method could execute a query on the database and potentially take a while, it could cause ANR if it is called on Main (UI) thread. A warning is printed if this method is being executed on Main thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the requery succeeded, false if not, in which case the cursor becomes invalid. |

### setFillWindowForwardOnly

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFillWindowForwardOnly(fillWindowForwardOnly: Boolean): Unit
```

Controls fetching of rows relative to requested position.

Calling this method defines how rows will be loaded, but it doesn't affect rows that are already in the window. This setting is preserved if a new window is setWindow

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
| `window` | [CursorWindow](../android.database/CursorWindow.md)!: The new cursor window, typically a remote cursor window. |

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
