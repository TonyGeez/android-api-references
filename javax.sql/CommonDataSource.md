# CommonDataSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CommonDataSource

```
interface CommonDataSource
```

| [javax.sql.CommonDataSource](../javax/sql/CommonDataSource.md) |

| Known Direct Subclasses [ConnectionPoolDataSource](../javax/sql/ConnectionPoolDataSource.md), [DataSource](../javax/sql/DataSource.md) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [ConnectionPoolDataSource](../javax/sql/ConnectionPoolDataSource.md) | A factory for`PooledConnection`objects. | | [DataSource](../javax/sql/DataSource.md) | A factory for connections to the physical data source that this`DataSource`object represents. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface that defines the methods which are common between`DataSource`,`XADataSource`and`ConnectionPoolDataSource`.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [PrintWriter](../java/io/PrintWriter.md)! | [getLogWriter](../javax/sql/CommonDataSource.md))`()` Retrieves the log writer for this`DataSource`object. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoginTimeout](../javax/sql/CommonDataSource.md))`()` Gets the maximum time in seconds that this data source can wait while attempting to connect to a database. |
| abstract [Logger](../java/util/logging/Logger.md)! | [getParentLogger](../javax/sql/CommonDataSource.md))`()` Return the parent Logger of all the Loggers used by this data source. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogWriter](../javax/sql/CommonDataSource.md))`(`out:` ` [PrintWriter](../java/io/PrintWriter.md)!`)` Sets the log writer for this`DataSource`object to the given`java.io.PrintWriter`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoginTimeout](../javax/sql/CommonDataSource.md))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum time in seconds that this data source will wait while attempting to connect to a database. |

## Public methods

### getLogWriter

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLogWriter(): PrintWriter!
```

Retrieves the log writer for this`DataSource`object.

The log writer is a character output stream to which all logging and tracing messages for this data source will be printed. This includes messages printed by the methods of this object, messages printed by methods of other objects manufactured by this object, and so on. Messages printed to a data source specific log writer are not printed to the log writer associated with the`java.sql.DriverManager`class. When a`DataSource`object is created, the log writer is initially null; in other words, the default is for logging to be disabled.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [PrintWriter](../java/io/PrintWriter.md)! | the log writer for this data source or null if logging is disabled |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setLogWriter](../javax/sql/CommonDataSource.md)) 

### getLoginTimeout

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLoginTimeout(): Int
```

Gets the maximum time in seconds that this data source can wait while attempting to connect to a database. A value of zero means that the timeout is the default system timeout if there is one; otherwise, it means that there is no timeout. When a`DataSource`object is created, the login timeout is initially zero.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the data source login time limit |

| Exceptions ||
|-------------------------|------------------------------------|
| `java.sql.SQLException` | if a database access error occurs. |

**See Also**

- [#setLoginTimeout](../javax/sql/CommonDataSource.md)) 

### getParentLogger

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentLogger(): Logger!
```

Return the parent Logger of all the Loggers used by this data source. This should be the Logger farthest from the root Logger that is still an ancestor of all of the Loggers used by this data source. Configuring this Logger will affect all of the log messages generated by the data source. In the worst case, this may be the root Logger.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------|
| [Logger](../java/util/logging/Logger.md)! | the parent Logger for this data source |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the data source does not use`java.util.logging``.` |

### setLogWriter

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLogWriter(out: PrintWriter!): Unit
```

Sets the log writer for this`DataSource`object to the given`java.io.PrintWriter`object.

The log writer is a character output stream to which all logging and tracing messages for this data source will be printed. This includes messages printed by the methods of this object, messages printed by methods of other objects manufactured by this object, and so on. Messages printed to a data source- specific log writer are not printed to the log writer associated with the`java.sql.DriverManager`class. When a`DataSource`object is created the log writer is initially null; in other words, the default is for logging to be disabled.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [PrintWriter](../java/io/PrintWriter.md)!:the new log writer; to disable logging, set to null |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getLogWriter](../javax/sql/CommonDataSource.md)) 

### setLoginTimeout

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLoginTimeout(seconds: Int): Unit
```

Sets the maximum time in seconds that this data source will wait while attempting to connect to a database. A value of zero specifies that the timeout is the default system timeout if there is one; otherwise, it specifies that there is no timeout. When a`DataSource`object is created, the login timeout is initially zero.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the data source login time limit |

| Exceptions ||
|-------------------------|------------------------------------|
| `java.sql.SQLException` | if a database access error occurs. |

**See Also**

- [#getLoginTimeout](../javax/sql/CommonDataSource.md))
