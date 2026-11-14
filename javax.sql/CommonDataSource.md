# CommonDataSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CommonDataSource

```
interface CommonDataSource
```

| [javax.sql.CommonDataSource](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#) |

| Known Direct Subclasses [ConnectionPoolDataSource](https://developer.android.com/reference/kotlin/javax/sql/ConnectionPoolDataSource), [DataSource](https://developer.android.com/reference/kotlin/javax/sql/DataSource) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [ConnectionPoolDataSource](https://developer.android.com/reference/kotlin/javax/sql/ConnectionPoolDataSource) | A factory for`PooledConnection`objects. | | [DataSource](https://developer.android.com/reference/kotlin/javax/sql/DataSource) | A factory for connections to the physical data source that this`DataSource`object represents. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface that defines the methods which are common between`DataSource`,`XADataSource`and`ConnectionPoolDataSource`.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)! | [getLogWriter](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#getLogWriter())`()` Retrieves the log writer for this`DataSource`object. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoginTimeout](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#getLoginTimeout())`()` Gets the maximum time in seconds that this data source can wait while attempting to connect to a database. |
| abstract [Logger](https://developer.android.com/reference/kotlin/java/util/logging/Logger.html#)! | [getParentLogger](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#getParentLogger())`()` Return the parent Logger of all the Loggers used by this data source. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogWriter](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#setLogWriter(java.io.PrintWriter))`(`out:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`)` Sets the log writer for this`DataSource`object to the given`java.io.PrintWriter`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoginTimeout](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#setLoginTimeout(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum time in seconds that this data source will wait while attempting to connect to a database. |

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
| [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)! | the log writer for this data source or null if logging is disabled |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setLogWriter](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#setLogWriter(java.io.PrintWriter)) 

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

- [#setLoginTimeout](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#setLoginTimeout(kotlin.Int)) 

### getParentLogger

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentLogger(): Logger!
```

Return the parent Logger of all the Loggers used by this data source. This should be the Logger farthest from the root Logger that is still an ancestor of all of the Loggers used by this data source. Configuring this Logger will affect all of the log messages generated by the data source. In the worst case, this may be the root Logger.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------|
| [Logger](https://developer.android.com/reference/kotlin/java/util/logging/Logger.html#)! | the parent Logger for this data source |

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
| `out` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:the new log writer; to disable logging, set to null |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getLogWriter](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#getLogWriter()) 

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

- [#getLoginTimeout](https://developer.android.com/reference/kotlin/javax/sql/CommonDataSource#getLoginTimeout())
