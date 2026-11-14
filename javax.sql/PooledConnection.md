# PooledConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PooledConnection

```
interface PooledConnection
```

| [javax.sql.PooledConnection](../javax/sql/PooledConnection.md) |

An object that provides hooks for connection pool management. A`PooledConnection`object represents a physical connection to a data source. The connection can be recycled rather than being closed when an application is finished with it, thus reducing the number of connections that need to be made.

An application programmer does not use the`PooledConnection`interface directly; rather, it is used by a middle tier infrastructure that manages the pooling of connections.

When an application calls the method`DataSource.getConnection`, it gets back a`Connection`object. If connection pooling is being done, that`Connection`object is actually a handle to a`PooledConnection`object, which is a physical connection.

The connection pool manager, typically the application server, maintains a pool of`PooledConnection`objects. If there is a`PooledConnection`object available in the pool, the connection pool manager returns a`Connection`object that is a handle to that physical connection. If no`PooledConnection`object is available, the connection pool manager calls the`ConnectionPoolDataSource`method`getPoolConnection`to create a new physical connection. The JDBC driver implementing`ConnectionPoolDataSource`creates a new`PooledConnection`object and returns a handle to it.

When an application closes a connection, it calls the`Connection`method`close`. When connection pooling is being done, the connection pool manager is notified because it has registered itself as a`ConnectionEventListener`object using the`ConnectionPool`method`addConnectionEventListener`. The connection pool manager deactivates the handle to the`PooledConnection`object and returns the`PooledConnection`object to the pool of connections so that it can be used again. Thus, when an application closes its connection, the underlying physical connection is recycled rather than being closed.

The physical connection is not closed until the connection pool manager calls the`PooledConnection`method`close`. This method is generally called to have an orderly shutdown of the server or if a fatal error has made the connection unusable.

A connection pool manager is often also a statement pool manager, maintining a pool of`PreparedStatement`objects. When an application closes a prepared statement, it calls the`PreparedStatement`method`close`. When`Statement`pooling is being done, the pool manager is notified because it has registered itself as a`StatementEventListener`object using the`ConnectionPool`method`addStatementEventListener`. Thus, when an application closes its`PreparedStatement`, the underlying prepared statement is recycled rather than being closed.

<br />

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addConnectionEventListener](../javax/sql/PooledConnection.md))`(`listener:` ` [ConnectionEventListener](../javax/sql/ConnectionEventListener.md)!`)` Registers the given event listener so that it will be notified when an event occurs on this`PooledConnection`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addStatementEventListener](../javax/sql/PooledConnection.md))`(`listener:` ` [StatementEventListener](../javax/sql/StatementEventListener.md)!`)` Registers a`StatementEventListener`with this`PooledConnection`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../javax/sql/PooledConnection.md))`()` Closes the physical connection that this`PooledConnection`object represents. |
| --- | --- |
| abstract [Connection](../java/sql/Connection.md)! | [getConnection](../javax/sql/PooledConnection.md))`()` Creates and returns a`Connection`object that is a handle for the physical connection that this`PooledConnection`object represents. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeConnectionEventListener](../javax/sql/PooledConnection.md))`(`listener:` ` [ConnectionEventListener](../javax/sql/ConnectionEventListener.md)!`)` Removes the given event listener from the list of components that will be notified when an event occurs on this`PooledConnection`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeStatementEventListener](../javax/sql/PooledConnection.md))`(`listener:` ` [StatementEventListener](../javax/sql/StatementEventListener.md)!`)` Removes the specified`StatementEventListener`from the list of components that will be notified when the driver detects that a`PreparedStatement`has been closed or is invalid. |
| --- | --- |

## Public methods

### addConnectionEventListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addConnectionEventListener(listener: ConnectionEventListener!): Unit
```

Registers the given event listener so that it will be notified when an event occurs on this`PooledConnection`object.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ConnectionEventListener](../javax/sql/ConnectionEventListener.md)!:a component, usually the connection pool manager, that has implemented the`ConnectionEventListener`interface and wants to be notified when the connection is closed or has an error |

**See Also**

- [#removeConnectionEventListener](../javax/sql/PooledConnection.md)) 

### addStatementEventListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addStatementEventListener(listener: StatementEventListener!): Unit
```

Registers a`StatementEventListener`with this`PooledConnection`object. Components that wish to be notified when`PreparedStatement`s created by the connection are closed or are detected to be invalid may use this method to register a`StatementEventListener`with this`PooledConnection`object.

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [StatementEventListener](../javax/sql/StatementEventListener.md)!:an component which implements the`StatementEventListener`interface that is to be registered with this`PooledConnection`object <br /> |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the physical connection that this`PooledConnection`object represents. An application never calls this method directly; it is called by the connection pool module, or manager.

See the [interface description](../javax/sql/PooledConnection.md) for more information.

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnection(): Connection!
```

Creates and returns a`Connection`object that is a handle for the physical connection that this`PooledConnection`object represents. The connection pool manager calls this method when an application has called the method`DataSource.getConnection`and there are no`PooledConnection`objects available. See the [interface description](../javax/sql/PooledConnection.md) for more information.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Connection](../java/sql/Connection.md)! | a`Connection`object that is a handle to this`PooledConnection`object |

| Exceptions ||
|-----------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### removeConnectionEventListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeConnectionEventListener(listener: ConnectionEventListener!): Unit
```

Removes the given event listener from the list of components that will be notified when an event occurs on this`PooledConnection`object.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ConnectionEventListener](../javax/sql/ConnectionEventListener.md)!:a component, usually the connection pool manager, that has implemented the`ConnectionEventListener`interface and been registered with this`PooledConnection`object as a listener |

**See Also**

- [#addConnectionEventListener](../javax/sql/PooledConnection.md)) 

### removeStatementEventListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeStatementEventListener(listener: StatementEventListener!): Unit
```

Removes the specified`StatementEventListener`from the list of components that will be notified when the driver detects that a`PreparedStatement`has been closed or is invalid.

<br />

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [StatementEventListener](../javax/sql/StatementEventListener.md)!:the component which implements the`StatementEventListener`interface that was previously registered with this`PooledConnection`object <br /> |
