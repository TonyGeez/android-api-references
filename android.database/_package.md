# android.database

# android.database

Kotlin| [Java](../android/database/_package.md)
| --- | --- |

## Interfaces

| [CrossProcessCursor](../android/database/CrossProcessCursor.md) | A cross process cursor is an extension of a [Cursor](../android/database/Cursor.md) that also supports usage from remote processes. |
| --- | --- |
| [Cursor](../android/database/Cursor.md) | This interface provides random read-write access to the result set returned by a database query. |
| [DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md) | An interface to let apps define an action to take when database corruption is detected. |

## Classes

| [AbstractCursor](../android/database/AbstractCursor.md) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. |
| --- | --- |
| [AbstractWindowedCursor](../android/database/AbstractWindowedCursor.md) | A base class for Cursors that store their data in [CursorWindow](../android/database/CursorWindow.md) s. |
| [CharArrayBuffer](../android/database/CharArrayBuffer.md) | This is used for [Cursor.copyStringToBuffer](../android/database/Cursor.md)) |
| [ContentObservable](../android/database/ContentObservable.md) | A specialization of [Observable](../android/database/Observable.md) for [ContentObserver](../android/database/ContentObserver.md) that provides methods for sending notifications to a list of [ContentObserver](../android/database/ContentObserver.md) objects. |
| --- | --- |
| [ContentObserver](../android/database/ContentObserver.md) | Receives call backs for changes to content. |
| [CrossProcessCursorWrapper](../android/database/CrossProcessCursorWrapper.md) | Cursor wrapper that implements [CrossProcessCursor](../android/database/CrossProcessCursor.md). |
| [CursorJoiner](../android/database/CursorJoiner.md) | Does a join on two cursors using the specified columns. |
| --- | --- |
| [CursorWindow](../android/database/CursorWindow.md) | A buffer containing multiple cursor rows. |
| [CursorWrapper](../android/database/CursorWrapper.md) | Wrapper class for Cursor that delegates all calls to the actual cursor object. |
| [DatabaseUtils](../android/database/DatabaseUtils.md) | Static utility methods for dealing with databases and [Cursor](../android/database/Cursor.md) s. |
| --- | --- |
| [DataSetObservable](../android/database/DataSetObservable.md) | A specialization of [Observable](../android/database/Observable.md) for [DataSetObserver](../android/database/DataSetObserver.md) that provides methods for sending notifications to a list of [DataSetObserver](../android/database/DataSetObserver.md) objects. |
| [DataSetObserver](../android/database/DataSetObserver.md) | Receives call backs when a data set has been changed, or made invalid. |
| [DefaultDatabaseErrorHandler](../android/database/DefaultDatabaseErrorHandler.md) | Default class used to define the action to take when database corruption is reported by sqlite. |
| --- | --- |
| [MatrixCursor](../android/database/MatrixCursor.md) | A mutable cursor implementation backed by an array of`Object`s. |
| [MergeCursor](../android/database/MergeCursor.md) | A convenience class that lets you present an array of Cursors as a single linear Cursor. |
| [Observable](../android/database/Observable.md) | Provides methods for registering or unregistering arbitrary observers in an [ArrayList](../java/util/ArrayList.md). |
| --- | --- |

## Exceptions

| [CursorIndexOutOfBoundsException](../android/database/CursorIndexOutOfBoundsException.md) | An exception indicating that a cursor is out of bounds. |
| --- | --- |
| [CursorWindowAllocationException](../android/database/CursorWindowAllocationException.md) | This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available. |
| [SQLException](../android/database/SQLException.md) | An exception that indicates there was an error with SQL parsing or execution. |
| [StaleDataException](../android/database/StaleDataException.md) | This exception is thrown when a Cursor contains stale data and must be requeried before being used again. |
| --- | --- |
