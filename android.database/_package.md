# android.database

# android.database

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [CrossProcessCursor](CrossProcessCursor.md) | A cross process cursor is an extension of a [Cursor](Cursor.md) that also supports usage from remote processes. |
| --- | --- |
| [Cursor](Cursor.md) | This interface provides random read-write access to the result set returned by a database query. |
| [DatabaseErrorHandler](DatabaseErrorHandler.md) | An interface to let apps define an action to take when database corruption is detected. |

## Classes

| [AbstractCursor](AbstractCursor.md) | This is an abstract cursor class that handles a lot of the common code that all cursors need to deal with and is provided for convenience reasons. |
| --- | --- |
| [AbstractWindowedCursor](AbstractWindowedCursor.md) | A base class for Cursors that store their data in [CursorWindow](CursorWindow.md) s. |
| [CharArrayBuffer](CharArrayBuffer.md) | This is used for [Cursor.copyStringToBuffer](Cursor.md)) |
| [ContentObservable](ContentObservable.md) | A specialization of [Observable](Observable.md) for [ContentObserver](ContentObserver.md) that provides methods for sending notifications to a list of [ContentObserver](ContentObserver.md) objects. |
| --- | --- |
| [ContentObserver](ContentObserver.md) | Receives call backs for changes to content. |
| [CrossProcessCursorWrapper](CrossProcessCursorWrapper.md) | Cursor wrapper that implements [CrossProcessCursor](CrossProcessCursor.md). |
| [CursorJoiner](CursorJoiner.md) | Does a join on two cursors using the specified columns. |
| --- | --- |
| [CursorWindow](CursorWindow.md) | A buffer containing multiple cursor rows. |
| [CursorWrapper](CursorWrapper.md) | Wrapper class for Cursor that delegates all calls to the actual cursor object. |
| [DatabaseUtils](DatabaseUtils.md) | Static utility methods for dealing with databases and [Cursor](Cursor.md) s. |
| --- | --- |
| [DataSetObservable](DataSetObservable.md) | A specialization of [Observable](Observable.md) for [DataSetObserver](DataSetObserver.md) that provides methods for sending notifications to a list of [DataSetObserver](DataSetObserver.md) objects. |
| [DataSetObserver](DataSetObserver.md) | Receives call backs when a data set has been changed, or made invalid. |
| [DefaultDatabaseErrorHandler](DefaultDatabaseErrorHandler.md) | Default class used to define the action to take when database corruption is reported by sqlite. |
| --- | --- |
| [MatrixCursor](MatrixCursor.md) | A mutable cursor implementation backed by an array of`Object`s. |
| [MergeCursor](MergeCursor.md) | A convenience class that lets you present an array of Cursors as a single linear Cursor. |
| [Observable](Observable.md) | Provides methods for registering or unregistering arbitrary observers in an [ArrayList](../java.util/ArrayList.md). |
| --- | --- |

## Exceptions

| [CursorIndexOutOfBoundsException](CursorIndexOutOfBoundsException.md) | An exception indicating that a cursor is out of bounds. |
| --- | --- |
| [CursorWindowAllocationException](CursorWindowAllocationException.md) | This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available. |
| [SQLException](SQLException.md) | An exception that indicates there was an error with SQL parsing or execution. |
| [StaleDataException](StaleDataException.md) | This exception is thrown when a Cursor contains stale data and must be requeried before being used again. |
| --- | --- |
