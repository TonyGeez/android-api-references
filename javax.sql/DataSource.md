# DataSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSource

```
interface DataSource : CommonDataSource, Wrapper
```

| [javax.sql.DataSource](DataSource.md) |

A factory for connections to the physical data source that this`DataSource`object represents. An alternative to the`DriverManager`facility, a`DataSource`object is the preferred means of getting a connection. An object that implements the`DataSource`interface will typically be registered with a naming service based on the JavaTM Naming and Directory (JNDI) API.

The`DataSource`interface is implemented by a driver vendor. There are three types of implementations:

1. Basic implementation -- produces a standard`Connection`object
2. Connection pooling implementation -- produces a`Connection`object that will automatically participate in connection pooling. This implementation works with a middle-tier connection pooling manager.
3. Distributed transaction implementation -- produces a`Connection`object that may be used for distributed transactions and almost always participates in connection pooling. This implementation works with a middle-tier transaction manager and almost always with a connection pooling manager.

A`DataSource`object has properties that can be modified when necessary. For example, if the data source is moved to a different server, the property for the server can be changed. The benefit is that because the data source's properties can be changed, any code accessing that data source does not need to be changed.

A driver that is accessed via a`DataSource`object does not register itself with the`DriverManager`. Rather, a`DataSource`object is retrieved though a lookup operation and then used to create a`Connection`object. With a basic implementation, the connection obtained through a`DataSource`object is identical to a connection obtained through the`DriverManager`facility.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Connection](../java.sql/Connection.md)! | [getConnection](DataSource.md))`()` Attempts to establish a connection with the data source that this`DataSource`object represents. |
| abstract [Connection](../java.sql/Connection.md)! | [getConnection](DataSource.md))`(`username:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to establish a connection with the data source that this`DataSource`object represents. |

| Inherited functions ||
|---|---|
| From class [CommonDataSource](CommonDataSource.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [PrintWriter](../java.io/PrintWriter.md)! | [getLogWriter](CommonDataSource.md))`()` <br /> Retrieves the log writer for this`DataSource`object. The log writer is a character output stream to which all logging and tracing messages for this data source will be printed. This includes messages printed by the methods of this object, messages printed by methods of other objects manufactured by this object, and so on. Messages printed to a data source specific log writer are not printed to the log writer associated with the`java.sql.DriverManager`class. When a`DataSource`object is created, the log writer is initially null; in other words, the default is for logging to be disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoginTimeout](CommonDataSource.md))`()` <br /> Gets the maximum time in seconds that this data source can wait while attempting to connect to a database. A value of zero means that the timeout is the default system timeout if there is one; otherwise, it means that there is no timeout. When a`DataSource`object is created, the login timeout is initially zero. <br /> | | [Logger](../java.util.logging/Logger.md)! | [getParentLogger](CommonDataSource.md))`()` <br /> Return the parent Logger of all the Loggers used by this data source. This should be the Logger farthest from the root Logger that is still an ancestor of all of the Loggers used by this data source. Configuring this Logger will affect all of the log messages generated by the data source. In the worst case, this may be the root Logger. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogWriter](CommonDataSource.md))`(`out:` ` [PrintWriter](../java.io/PrintWriter.md)!`)` <br /> Sets the log writer for this`DataSource`object to the given`java.io.PrintWriter`object. The log writer is a character output stream to which all logging and tracing messages for this data source will be printed. This includes messages printed by the methods of this object, messages printed by methods of other objects manufactured by this object, and so on. Messages printed to a data source- specific log writer are not printed to the log writer associated with the`java.sql.DriverManager`class. When a`DataSource`object is created the log writer is initially null; in other words, the default is for logging to be disabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoginTimeout](CommonDataSource.md))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the maximum time in seconds that this data source will wait while attempting to connect to a database. A value of zero specifies that the timeout is the default system timeout if there is one; otherwise, it specifies that there is no timeout. When a`DataSource`object is created, the login timeout is initially zero. <br /> | ||
| From class [Wrapper](../java.sql/Wrapper.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Public methods

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnection(): Connection!
```

Attempts to establish a connection with the data source that this`DataSource`object represents.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------|
| [Connection](../java.sql/Connection.md)! | a connection to the data source |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnection(
    username: String!, 
    password: String!
): Connection!
```

Attempts to establish a connection with the data source that this`DataSource`object represents.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `username` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the database user on whose behalf the connection is being made |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user's password |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------|
| [Connection](../java.sql/Connection.md)! | a connection to the data source |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
