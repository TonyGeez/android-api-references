# DriverManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DriverManager

```
open class DriverManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.sql.DriverManager](https://developer.android.com/reference/kotlin/java/sql/DriverManager#) |

The basic service for managing a set of JDBC drivers. 
**NOTE:** The`DataSource`interface, new in the JDBC 2.0 API, provides another way to connect to a data source. The use of a`DataSource`object is the preferred means of connecting to a data source.

As part of its initialization, the`DriverManager`class will attempt to load the driver classes referenced in the "jdbc.drivers" system property. This allows a user to customize the JDBC Drivers used by their applications. For example in your \~/.hotjava/properties file you might specify: 

```kotlin
<code>jdbc.drivers=foo.bah.Driver:wombat.sql.Driver:bad.taste.ourDriver</code>
```

The`DriverManager`methods`getConnection`and`getDrivers`have been enhanced to support the Java Standard Edition [Service Provider](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html#Service%20Provider) mechanism. JDBC 4.0 Drivers must include the file`META-INF/services/java.sql.Driver`. This file contains the name of the JDBC drivers implementation of`java.sql.Driver`. For example, to load the`my.sql.Driver`class, the`META-INF/services/java.sql.Driver`file would contain the entry: 

```kotlin
<code>my.sql.Driver</code>
```

Applications no longer need to explictly load JDBC drivers using`Class.forName()`. Existing programs which currently load JDBC drivers using`Class.forName()`will continue to work without modification.

When the method`getConnection`is called, the`DriverManager`will attempt to locate a suitable driver from amongst those loaded at initialization and those loaded explicitly using the same classloader as the current applet or application.

Starting with the Java 2 SDK, Standard Edition, version 1.3, a logging stream can be set only if the proper permission has been granted. Normally this will be done with the tool PolicyTool, which can be used to grant`permission java.sql.SQLPermission "setLog"`.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deregisterDriver](https://developer.android.com/reference/kotlin/java/sql/DriverManager#deregisterDriver(java.sql.Driver))`(`driver:` ` [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!`)` Drops a driver from the`DriverManager`'s list. |
| openstatic [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getConnection(kotlin.String))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to establish a connection to the given database URL. |
| openstatic [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getConnection(kotlin.String,%20kotlin.String,%20kotlin.String))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `user:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to establish a connection to the given database URL. |
| openstatic [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getConnection(kotlin.String,%20java.util.Properties))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `info:` ` [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)!`)` Attempts to establish a connection to the given database URL. |
| openstatic [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)! | [getDriver](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getDriver(kotlin.String))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to locate a driver that understands the given URL. |
| openstatic [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!\>! | [getDrivers](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getDrivers())`()` Retrieves an Enumeration with all of the currently loaded JDBC drivers to which the current caller has access. |
| openstatic [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)! | [getLogStream](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLogStream())`()` Retrieves the logging/tracing PrintStream that is used by the`DriverManager`and all drivers. |
| openstatic [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)! | [getLogWriter](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLogWriter())`()` Retrieves the log writer. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoginTimeout](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLoginTimeout())`()` Gets the maximum time in seconds that a driver can wait when attempting to log in to a database. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](https://developer.android.com/reference/kotlin/java/sql/DriverManager#println(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Prints a message to the current JDBC log stream. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDriver](https://developer.android.com/reference/kotlin/java/sql/DriverManager#registerDriver(java.sql.Driver))`(`driver:` ` [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!`)` Registers the given driver with the`DriverManager`. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogStream](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLogStream(java.io.PrintStream))`(`out:` ` [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)!`)` Sets the logging/tracing PrintStream that is used by the`DriverManager`and all drivers. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogWriter](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLogWriter(java.io.PrintWriter))`(`out:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`)` Sets the logging/tracing`PrintWriter`object that is used by the`DriverManager`and all drivers. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoginTimeout](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLoginTimeout(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum time in seconds that a driver will wait while attempting to connect to a database. |

## Public methods

### deregisterDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deregisterDriver(driver: Driver!): Unit
```

Drops a driver from the`DriverManager`'s list. Applets can only deregister drivers from their own classloaders.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `driver` | [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!:the JDBC Driver to drop |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getConnection(url: String!): Connection!
```

Attempts to establish a connection to the given database URL. The`DriverManager`attempts to select an appropriate driver from the set of registered JDBC drivers.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a database url of the form` jdbc:`*subprotocol* `:`*subname* |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | a connection to the URL |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getConnection(
    url: String!, 
    user: String!, 
    password: String!
): Connection!
```

Attempts to establish a connection to the given database URL. The`DriverManager`attempts to select an appropriate driver from the set of registered JDBC drivers.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a database url of the form`jdbc:`*subprotocol* `:`*subname* |
| `user` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the database user on whose behalf the connection is being made |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user's password |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | a connection to the URL |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getConnection(
    url: String!, 
    info: Properties!
): Connection!
```

Attempts to establish a connection to the given database URL. The`DriverManager`attempts to select an appropriate driver from the set of registered JDBC drivers.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a database url of the form` jdbc:`*subprotocol* `:`*subname* |
| `info` | [Properties](https://developer.android.com/reference/kotlin/java/util/Properties.html#)!:a list of arbitrary string tag/value pairs as connection arguments; normally at least a "user" and "password" property should be included |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | a Connection to the URL |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDriver(url: String!): Driver!
```

Attempts to locate a driver that understands the given URL. The`DriverManager`attempts to select an appropriate driver from the set of registered JDBC drivers.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a database URL of the form`jdbc:`*subprotocol* `:`*subname* |

| Return ||
|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)! | a`Driver`object representing a driver that can connect to the given URL |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getDrivers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDrivers(): Enumeration<Driver!>!
```

Retrieves an Enumeration with all of the currently loaded JDBC drivers to which the current caller has access.

**Note:** The classname of a driver can be found using`d.getClass().getName()`

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)< [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!>! | the list of JDBC Drivers loaded by the caller's class loader |

### getLogStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogStream(): PrintStream!
```

**Deprecated:** *Use`getLogWriter`instead.*

Retrieves the logging/tracing PrintStream that is used by the`DriverManager`and all drivers.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)! | the logging/tracing PrintStream; if disabled, is`null` |

**See Also**

- [#setLogStream](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLogStream(java.io.PrintStream)) 

### getLogWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogWriter(): PrintWriter!
```

Retrieves the log writer. The`getLogWriter`and`setLogWriter`methods should be used instead of the`get/setlogStream`methods, which are deprecated.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)! | a`java.io.PrintWriter`object |

**See Also**

- [#setLogWriter](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLogWriter(java.io.PrintWriter)) 

### getLoginTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLoginTimeout(): Int
```

Gets the maximum time in seconds that a driver can wait when attempting to log in to a database.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the driver login time limit in seconds |

**See Also**

- [#setLoginTimeout](https://developer.android.com/reference/kotlin/java/sql/DriverManager#setLoginTimeout(kotlin.Int)) 

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun println(message: String!): Unit
```

Prints a message to the current JDBC log stream.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a log or tracing message |

### registerDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun registerDriver(driver: Driver!): Unit
```

Registers the given driver with the`DriverManager`. A newly-loaded driver class should call the method`registerDriver`to make itself known to the`DriverManager`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `driver` | [Driver](https://developer.android.com/reference/kotlin/java/sql/Driver)!:the new JDBC Driver that is to be registered with the`DriverManager` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setLogStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setLogStream(out: PrintStream!): Unit
```

**Deprecated:** *Use`setLogWriter`instead.*

Sets the logging/tracing PrintStream that is used by the`DriverManager`and all drivers.

In the Java 2 SDK, Standard Edition, version 1.3 release, this method checks to see that there is an`SQLPermission`object before setting the logging stream. If a`SecurityManager`exists and its`checkPermission`method denies setting the log writer, this method throws a`java.lang.SecurityException`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)!:the new logging/tracing PrintStream; to disable, set to`null` |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies setting the log stream |

**See Also**

- [#getLogStream](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLogStream()) 

### setLogWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setLogWriter(out: PrintWriter!): Unit
```

Sets the logging/tracing`PrintWriter`object that is used by the`DriverManager`and all drivers.

There is a minor versioning problem created by the introduction of the method`setLogWriter`. The method`setLogWriter`cannot create a`PrintStream`object that will be returned by`getLogStream`---the Java platform does not provide a backward conversion. As a result, a new application that uses`setLogWriter`and also uses a JDBC 1.0 driver that uses`getLogStream`will likely not see debugging information written by that driver.

Starting with the Java 2 SDK, Standard Edition, version 1.3 release, this method checks to see that there is an`SQLPermission`object before setting the logging stream. If a`SecurityManager`exists and its`checkPermission`method denies setting the log writer, this method throws a`java.lang.SecurityException`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:the new logging/tracing`PrintStream`object;`null`to disable logging and tracing |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies setting the log writer |

**See Also**

- [#getLogWriter](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLogWriter()) 

### setLoginTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setLoginTimeout(seconds: Int): Unit
```

Sets the maximum time in seconds that a driver will wait while attempting to connect to a database.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the login time limit in seconds; zero means there is no limit |

**See Also**

- [#getLoginTimeout](https://developer.android.com/reference/kotlin/java/sql/DriverManager#getLoginTimeout())
