# android.database

# android.database

Kotlin| [Java](https://developer.android.com/reference/android/database/package-summary "View this page in Java")

## Interfaces

| [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor) | A cross process cursor is an extension of a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor) that also supports usage from remote processes. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor) | This interface provides random read-write access to the result set returned by a database query. |
| [DatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler) | An interface to let apps define an action to take when database corruption is detected. |

## Classes

| [AbstractCursor](https://developer.android.com/reference/kotlin/android/database/AbstractCursor) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. |
| [AbstractWindowedCursor](https://developer.android.com/reference/kotlin/android/database/AbstractWindowedCursor) | A base class for Cursors that store their data in [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow) s. |
| [CharArrayBuffer](https://developer.android.com/reference/kotlin/android/database/CharArrayBuffer) | This is used for [Cursor.copyStringToBuffer](https://developer.android.com/reference/kotlin/android/database/Cursor#copyStringToBuffer(kotlin.Int,%20android.database.CharArrayBuffer)) |
| [ContentObservable](https://developer.android.com/reference/kotlin/android/database/ContentObservable) | A specialization of [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) for [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver) that provides methods for sending notifications to a list of [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver) objects. |
| [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver) | Receives call backs for changes to content. |
| [CrossProcessCursorWrapper](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursorWrapper) | Cursor wrapper that implements [CrossProcessCursor](https://developer.android.com/reference/kotlin/android/database/CrossProcessCursor). |
| [CursorJoiner](https://developer.android.com/reference/kotlin/android/database/CursorJoiner) | Does a join on two cursors using the specified columns. |
| [CursorWindow](https://developer.android.com/reference/kotlin/android/database/CursorWindow) | A buffer containing multiple cursor rows. |
| [CursorWrapper](https://developer.android.com/reference/kotlin/android/database/CursorWrapper) | Wrapper class for Cursor that delegates all calls to the actual cursor object. |
| [DatabaseUtils](https://developer.android.com/reference/kotlin/android/database/DatabaseUtils) | Static utility methods for dealing with databases and [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor) s. |
| [DataSetObservable](https://developer.android.com/reference/kotlin/android/database/DataSetObservable) | A specialization of [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) for [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) that provides methods for sending notifications to a list of [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) objects. |
| [DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver) | Receives call backs when a data set has been changed, or made invalid. |
| [DefaultDatabaseErrorHandler](https://developer.android.com/reference/kotlin/android/database/DefaultDatabaseErrorHandler) | Default class used to define the action to take when database corruption is reported by sqlite. |
| [MatrixCursor](https://developer.android.com/reference/kotlin/android/database/MatrixCursor) | A mutable cursor implementation backed by an array of`Object`s. |
| [MergeCursor](https://developer.android.com/reference/kotlin/android/database/MergeCursor) | A convenience class that lets you present an array of Cursors as a single linear Cursor. |
| [Observable](https://developer.android.com/reference/kotlin/android/database/Observable) | Provides methods for registering or unregistering arbitrary observers in an [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#). |

## Exceptions

| [CursorIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/android/database/CursorIndexOutOfBoundsException) | An exception indicating that a cursor is out of bounds. |
| [CursorWindowAllocationException](https://developer.android.com/reference/kotlin/android/database/CursorWindowAllocationException) | This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available. |
| [SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException) | An exception that indicates there was an error with SQL parsing or execution. |
| [StaleDataException](https://developer.android.com/reference/kotlin/android/database/StaleDataException) | This exception is thrown when a Cursor contains stale data and must be requeried before being used again. |
