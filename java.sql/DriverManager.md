# DriverManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DriverManager

```
open class DriverManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.sql.DriverManager](../java/sql/DriverManager.md) |

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
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deregisterDriver](../java/sql/DriverManager.md))`(`driver:` ` [Driver](../java/sql/Driver.md)!`)` Drops a driver from the`DriverManager`'s list. |
| openstatic [Connection](../java/sql/Connection.md)! | [getConnection](../java/sql/DriverManager.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to establish a connection to the given database URL. |
| openstatic [Connection](../java/sql/Connection.md)! | [getConnection](../java/sql/DriverManager.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `user:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to establish a connection to the given database URL. |
| --- | --- |
| openstatic [Connection](../java/sql/Connection.md)! | [getConnection](../java/sql/DriverManager.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `info:` ` [Properties](../java/util/Properties.md)!`)` Attempts to establish a connection to the given database URL. |
| openstatic [Driver](../java/sql/Driver.md)! | [getDriver](../java/sql/DriverManager.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to locate a driver that understands the given URL. |
| openstatic [Enumeration](../java/util/Enumeration.md)\< [Driver](../java/sql/Driver.md)!\>! | [getDrivers](../java/sql/DriverManager.md))`()` Retrieves an Enumeration with all of the currently loaded JDBC drivers to which the current caller has access. |
| --- | --- |
| openstatic [PrintStream](../java/io/PrintStream.md)! | [getLogStream](../java/sql/DriverManager.md))`()` Retrieves the logging/tracing PrintStream that is used by the`DriverManager`and all drivers. |
| openstatic [PrintWriter](../java/io/PrintWriter.md)! | [getLogWriter](../java/sql/DriverManager.md))`()` Retrieves the log writer. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoginTimeout](../java/sql/DriverManager.md))`()` Gets the maximum time in seconds that a driver can wait when attempting to log in to a database. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [println](../java/sql/DriverManager.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Prints a message to the current JDBC log stream. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDriver](../java/sql/DriverManager.md))`(`driver:` ` [Driver](../java/sql/Driver.md)!`)` Registers the given driver with the`DriverManager`. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogStream](../java/sql/DriverManager.md))`(`out:` ` [PrintStream](../java/io/PrintStream.md)!`)` Sets the logging/tracing PrintStream that is used by the`DriverManager`and all drivers. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogWriter](../java/sql/DriverManager.md))`(`out:` ` [PrintWriter](../java/io/PrintWriter.md)!`)` Sets the logging/tracing`PrintWriter`object that is used by the`DriverManager`and all drivers. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoginTimeout](../java/sql/DriverManager.md))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum time in seconds that a driver will wait while attempting to connect to a database. |

## Public methods

### deregisterDriver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deregisterDriver(driver: Driver!): Unit
```

Drops a driver from the`DriverManager`'s list. Applets can only deregister drivers from their own classloaders.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------|
| `driver` | [Driver](../java/sql/Driver.md)!:the JDBC Driver to drop |

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
| [Connection](../java/sql/Connection.md)! | a connection to the URL |

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
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Connection](../java/sql/Connection.md)! | a connection to the URL |

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
| `info` | [Properties](../java/util/Properties.md)!:a list of arbitrary string tag/value pairs as connection arguments; normally at least a "user" and "password" property should be included |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Connection](../java/sql/Connection.md)! | a Connection to the URL |

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
| [Driver](../java/sql/Driver.md)! | a`Driver`object representing a driver that can connect to the given URL |

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
| [Enumeration](../java/util/Enumeration.md)< [Driver](../java/sql/Driver.md)!>! | the list of JDBC Drivers loaded by the caller's class loader |

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
| [PrintStream](../java/io/PrintStream.md)! | the logging/tracing PrintStream; if disabled, is`null` |

**See Also**

- [#setLogStream](../java/sql/DriverManager.md)) 

### getLogWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLogWriter(): PrintWriter!
```

Retrieves the log writer. The`getLogWriter`and`setLogWriter`methods should be used instead of the`get/setlogStream`methods, which are deprecated.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------|
| [PrintWriter](../java/io/PrintWriter.md)! | a`java.io.PrintWriter`object |

**See Also**

- [#setLogWriter](../java/sql/DriverManager.md)) 

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

- [#setLoginTimeout](../java/sql/DriverManager.md)) 

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
| `driver` | [Driver](../java/sql/Driver.md)!:the new JDBC Driver that is to be registered with the`DriverManager` |

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
| `out` | [PrintStream](../java/io/PrintStream.md)!:the new logging/tracing PrintStream; to disable, set to`null` |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies setting the log stream |

**See Also**

- [#getLogStream](../java/sql/DriverManager.md)) 

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
| `out` | [PrintWriter](../java/io/PrintWriter.md)!:the new logging/tracing`PrintStream`object;`null`to disable logging and tracing |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkPermission`method denies setting the log writer |

**See Also**

- [#getLogWriter](../java/sql/DriverManager.md)) 

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

- [#getLoginTimeout](../java/sql/DriverManager.md))
