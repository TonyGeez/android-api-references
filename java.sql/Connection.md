# Connection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Connection

```
interface Connection : AutoCloseable, Wrapper
```

| [java.sql.Connection](Connection.md) |

A connection (session) with a specific database. SQL statements are executed and results are returned within the context of a connection.

A`Connection`object's database is able to provide information describing its tables, its supported SQL grammar, its stored procedures, the capabilities of this connection, and so on. This information is obtained with the`getMetaData`method.

**Note:** When configuring a`Connection`, JDBC applications should use the appropriate`Connection`method such as`setAutoCommit`or`setTransactionIsolation`. Applications should not invoke SQL commands directly to change the connection's configuration when there is a JDBC method available. By default a`Connection`object is in auto-commit mode, which means that it automatically commits changes after executing each statement. If auto-commit mode has been disabled, the method`commit`must be called explicitly in order to commit changes; otherwise, database changes will not be saved.

A new`Connection`object created using the JDBC 2.1 core API has an initially empty type map associated with it. A user may enter a custom mapping for a UDT in this type map. When a UDT is retrieved from a data source with the method`ResultSet.getObject`, the`getObject`method will check the connection's type map to see if there is an entry for that UDT. If so, the`getObject`method will map the UDT to the class indicated. If there is no entry, the UDT will be mapped using the standard mapping.

A user may create a new type map, which is a`java.util.Map`object, make an entry in it, and pass it to the`java.sql`methods that can perform custom mapping. In this case, the method will use the given type map instead of the one associated with the connection.

For example, the following code fragment specifies that the SQL type`ATHLETES`will be mapped to the class`Athletes`in the Java programming language. The code fragment retrieves the type map for the`Connection `object`con`, inserts the entry into it, and then sets the type map with the new entry as the connection's type map. 

```kotlin
java.util.Map map = con.getTypeMap();
       map.put("mySchemaName.ATHLETES", Class.forName("Athletes"));
       con.setTypeMap(map);
  
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_NONE](Connection.md) A constant indicating that transactions are not supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_READ_COMMITTED](Connection.md) A constant indicating that dirty reads are prevented; non-repeatable reads and phantom reads can occur. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_READ_UNCOMMITTED](Connection.md) A constant indicating that dirty reads, non-repeatable reads and phantom reads can occur. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_REPEATABLE_READ](Connection.md) A constant indicating that dirty reads and non-repeatable reads are prevented; phantom reads can occur. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSACTION_SERIALIZABLE](Connection.md) A constant indicating that dirty reads, non-repeatable reads and phantom reads are prevented. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearWarnings](Connection.md))`()` Clears all warnings reported for this`Connection`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](Connection.md))`()` Releases this`Connection`object's database and JDBC resources immediately instead of waiting for them to be automatically released. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commit](Connection.md))`()` Makes all changes made since the previous commit/rollback permanent and releases any database locks currently held by this`Connection`object. |
| --- | --- |
| abstract [Array](Array.md)! | [createArrayOf](Connection.md))`(`typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `elements:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Factory method for creating Array objects. |
| abstract [Blob](Blob.md)! | [createBlob](Connection.md))`()` Constructs an object that implements the`Blob`interface. |
| abstract [Clob](Clob.md)! | [createClob](Connection.md))`()` Constructs an object that implements the`Clob`interface. |
| --- | --- |
| abstract [NClob](NClob.md)! | [createNClob](Connection.md))`()` Constructs an object that implements the`NClob`interface. |
| abstract [SQLXML](SQLXML.md)! | [createSQLXML](Connection.md))`()` Constructs an object that implements the`SQLXML`interface. |
| abstract [Statement](Statement.md)! | [createStatement](Connection.md))`()` Creates a`Statement`object for sending SQL statements to the database. |
| --- | --- |
| abstract [Statement](Statement.md)! | [createStatement](Connection.md))`(`resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`Statement`object that will generate`ResultSet`objects with the given type and concurrency. |
| abstract [Statement](Statement.md)! | [createStatement](Connection.md))`(`resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetHoldability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`Statement`object that will generate`ResultSet`objects with the given type, concurrency, and holdability. |
| abstract [Struct](Struct.md)! | [createStruct](Connection.md))`(`typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attributes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Factory method for creating Struct objects. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAutoCommit](Connection.md))`()` Retrieves the current auto-commit mode for this`Connection`object. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCatalog](Connection.md))`()` Retrieves this`Connection`object's current catalog name. |
| abstract [Properties](../java.util/Properties.md)! | [getClientInfo](Connection.md))`()` Returns a list containing the name and current value of each client info property supported by the driver. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getClientInfo](Connection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of the client info property specified by name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHoldability](Connection.md))`()` Retrieves the current holdability of`ResultSet`objects created using this`Connection`object. |
| abstract [DatabaseMetaData](DatabaseMetaData.md)! | [getMetaData](Connection.md))`()` Retrieves a`DatabaseMetaData`object that contains metadata about the database to which this`Connection`object represents a connection. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransactionIsolation](Connection.md))`()` Retrieves this`Connection`object's current transaction isolation level. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>! | [getTypeMap](Connection.md))`()` Retrieves the`Map`object associated with this`Connection`object. |
| abstract [SQLWarning](SQLWarning.md)! | [getWarnings](Connection.md))`()` Retrieves the first warning reported by calls on this`Connection`object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](Connection.md))`()` Retrieves whether this`Connection`object has been closed. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](Connection.md))`()` Retrieves whether this`Connection`object is in read-only mode. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](Connection.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the connection has not been closed and is still valid. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nativeSQL](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts the given SQL statement into the system's native SQL grammar. |
| abstract [CallableStatement](CallableStatement.md)! | [prepareCall](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CallableStatement`object for calling database stored procedures. |
| abstract [CallableStatement](CallableStatement.md)! | [prepareCall](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`CallableStatement`object that will generate`ResultSet`objects with the given type and concurrency. |
| --- | --- |
| abstract [CallableStatement](CallableStatement.md)! | [prepareCall](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetHoldability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`CallableStatement`object that will generate`ResultSet`objects with the given type and concurrency. |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`PreparedStatement`object for sending parameterized SQL statements to the database. |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `autoGeneratedKeys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a default`PreparedStatement`object that has the capability to retrieve auto-generated keys. |
| --- | --- |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PreparedStatement`object that will generate`ResultSet`objects with the given type and concurrency. |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultSetType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetConcurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultSetHoldability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PreparedStatement`object that will generate`ResultSet`objects with the given type, concurrency, and holdability. |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnIndexes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Creates a default`PreparedStatement`object capable of returning the auto-generated keys designated by the given array. |
| --- | --- |
| abstract [PreparedStatement](PreparedStatement.md)! | [prepareStatement](Connection.md))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Creates a default`PreparedStatement`object capable of returning the auto-generated keys designated by the given array. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseSavepoint](Connection.md))`(`savepoint:` ` [Savepoint](Savepoint.md)!`)` Removes the specified`Savepoint`and subsequent`Savepoint`objects from the current transaction. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollback](Connection.md))`()` Undoes all changes made in the current transaction and releases any database locks currently held by this`Connection`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rollback](Connection.md))`(`savepoint:` ` [Savepoint](Savepoint.md)!`)` Undoes all changes made after the given`Savepoint`object was set. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoCommit](Connection.md))`(`autoCommit:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets this connection's auto-commit mode to the given state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCatalog](Connection.md))`(`catalog:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the given catalog name in order to select a subspace of this`Connection`object's database in which to work. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientInfo](Connection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the value of the client info property specified by name to the value specified by value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientInfo](Connection.md))`(`properties:` ` [Properties](../java.util/Properties.md)!`)` Sets the value of the connection's client info properties. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHoldability](Connection.md))`(`holdability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the default holdability of`ResultSet`objects created using this`Connection`object to the given holdability. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadOnly](Connection.md))`(`readOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Puts this connection in read-only mode as a hint to the driver to enable database optimizations. |
| abstract [Savepoint](Savepoint.md)! | [setSavepoint](Connection.md))`()` Creates an unnamed savepoint in the current transaction and returns the new`Savepoint`object that represents it. |
| abstract [Savepoint](Savepoint.md)! | [setSavepoint](Connection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a savepoint with the given name in the current transaction and returns the new`Savepoint`object that represents it. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransactionIsolation](Connection.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to change the transaction isolation level for this`Connection`object to the one given. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTypeMap](Connection.md))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Installs the given`TypeMap`object as the type map for this`Connection`object. |

| Inherited functions ||
|---|---|
| From class [Wrapper](Wrapper.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Constants

### TRANSACTION_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_NONE: Int
```

A constant indicating that transactions are not supported. 

 Value: 0

### TRANSACTION_READ_COMMITTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_READ_COMMITTED: Int
```

A constant indicating that dirty reads are prevented; non-repeatable reads and phantom reads can occur. This level only prohibits a transaction from reading a row with uncommitted changes in it. 

 Value: 2

### TRANSACTION_READ_UNCOMMITTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_READ_UNCOMMITTED: Int
```

A constant indicating that dirty reads, non-repeatable reads and phantom reads can occur. This level allows a row changed by one transaction to be read by another transaction before any changes in that row have been committed (a "dirty read"). If any of the changes are rolled back, the second transaction will have retrieved an invalid row. 

 Value: 1

### TRANSACTION_REPEATABLE_READ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_REPEATABLE_READ: Int
```

A constant indicating that dirty reads and non-repeatable reads are prevented; phantom reads can occur. This level prohibits a transaction from reading a row with uncommitted changes in it, and it also prohibits the situation where one transaction reads a row, a second transaction alters the row, and the first transaction rereads the row, getting different values the second time (a "non-repeatable read"). 

 Value: 4

### TRANSACTION_SERIALIZABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSACTION_SERIALIZABLE: Int
```

A constant indicating that dirty reads, non-repeatable reads and phantom reads are prevented. This level includes the prohibitions in`TRANSACTION_REPEATABLE_READ`and further prohibits the situation where one transaction reads all rows that satisfy a`WHERE`condition, a second transaction inserts a row that satisfies that`WHERE`condition, and the first transaction rereads for the same condition, retrieving the additional "phantom" row in the second read. 

 Value: 8

## Public methods

### clearWarnings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearWarnings(): Unit
```

Clears all warnings reported for this`Connection`object. After a call to this method, the method`getWarnings`returns`null`until a new warning is reported for this`Connection`object.

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | SQLException if a database access error occurs or this method is called on a closed connection |

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Releases this`Connection`object's database and JDBC resources immediately instead of waiting for them to be automatically released.

Calling the method`close`on a`Connection`object that is already closed is a no-op.

It is**strongly recommended** that an application explicitly commits or rolls back an active transaction prior to calling the`close`method. If the`close`method is called and there is an active transaction, the results are implementation-defined.

<br />

| Exceptions ||
|-------------------------|------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.sql.SQLException` | SQLException if a database access error occurs |

### commit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun commit(): Unit
```

Makes all changes made since the previous commit/rollback permanent and releases any database locks currently held by this`Connection`object. This method should be used only when auto-commit mode has been disabled.

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called while participating in a distributed transaction, if this method is called on a closed conection or this`Connection`object is in auto-commit mode |

**See Also**

- [#setAutoCommit](Connection.md)) 

### createArrayOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createArrayOf(
    typeName: String!, 
    elements: Array<Any!>!
): Array!
```

Factory method for creating Array objects.

**Note:** When`createArrayOf`is used to create an array object that maps to a primitive data type, then it is implementation-defined whether the`Array`object is an array of that primitive data type or an array of`Object`.

**Note:** The JDBC driver is responsible for mapping the elements`Object`array to the default JDBC SQL type defined in java.sql.Types for the given class of`Object`. The default mapping is specified in Appendix B of the JDBC specification. If the resulting JDBC type is not the appropriate type for the given typeName then it is implementation defined whether an`SQLException`is thrown or the driver supports the resulting conversion.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the SQL name of the type the elements of the array map to. The typeName is a database-specific name which may be the name of a built-in type, a user-defined type or a standard SQL type supported by this database. This is the value returned by`Array.getBaseTypeName` |
| `elements` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the elements that populate the returned object |

| Return ||
|-------------------------------------------------------------------------|--------------------------------------------------------------|
| [Array](Array.md)! | an Array object whose elements map to the specified SQL type |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database error occurs, the JDBC type is not appropriate for the typeName and the conversion is not supported, the typeName is null or this method is called on a closed connection |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### createBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createBlob(): Blob!
```

Constructs an object that implements the`Blob`interface. The object returned initially contains no data. The`setBinaryStream`and`setBytes`methods of the`Blob`interface may be used to add data to the`Blob`.

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------|
| [Blob](Blob.md)! | An object that implements the`Blob`interface |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if an object that implements the`Blob`interface can not be constructed, this method is called on a closed connection or a database access error occurs. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### createClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createClob(): Clob!
```

Constructs an object that implements the`Clob`interface. The object returned initially contains no data. The`setAsciiStream`,`setCharacterStream`and`setString`methods of the`Clob`interface may be used to add data to the`Clob`.

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------|
| [Clob](Clob.md)! | An object that implements the`Clob`interface |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if an object that implements the`Clob`interface can not be constructed, this method is called on a closed connection or a database access error occurs. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### createNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createNClob(): NClob!
```

Constructs an object that implements the`NClob`interface. The object returned initially contains no data. The`setAsciiStream`,`setCharacterStream`and`setString`methods of the`NClob`interface may be used to add data to the`NClob`.

| Return ||
|-------------------------------------------------------------------------|-----------------------------------------------|
| [NClob](NClob.md)! | An object that implements the`NClob`interface |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if an object that implements the`NClob`interface can not be constructed, this method is called on a closed connection or a database access error occurs. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### createSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createSQLXML(): SQLXML!
```

Constructs an object that implements the`SQLXML`interface. The object returned initially contains no data. The`createXmlStreamWriter`object and`setString`method of the`SQLXML`interface may be used to add data to the`SQLXML`object.

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------|
| [SQLXML](SQLXML.md)! | An object that implements the`SQLXML`interface |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if an object that implements the`SQLXML`interface can not be constructed, this method is called on a closed connection or a database access error occurs. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### createStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createStatement(): Statement!
```

Creates a`Statement`object for sending SQL statements to the database. SQL statements without parameters are normally executed using`Statement`objects. If the same SQL statement is executed many times, it may be more efficient to use a`PreparedStatement`object.

Result sets created using the returned`Statement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Return ||
|---------------------------------------------------------------------------------|--------------------------------|
| [Statement](Statement.md)! | a new default`Statement`object |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

### createStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createStatement(
    resultSetType: Int, 
    resultSetConcurrency: Int
): Statement!
```

Creates a`Statement`object that will generate`ResultSet`objects with the given type and concurrency. This method is the same as the`createStatement`method above, but it allows the default result set type and concurrency to be overridden. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a result set type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a concurrency type; one of`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Statement](Statement.md)! | a new`Statement`object that will generate`ResultSet`objects with the given type and concurrency |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type and concurrency |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type and result set concurrency. |

### createStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createStatement(
    resultSetType: Int, 
    resultSetConcurrency: Int, 
    resultSetHoldability: Int
): Statement!
```

Creates a`Statement`object that will generate`ResultSet`objects with the given type, concurrency, and holdability. This method is the same as the`createStatement`method above, but it allows the default result set type, concurrency, and holdability to be overridden.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |
| `resultSetHoldability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Statement](Statement.md)! | a new`Statement`object that will generate`ResultSet`objects with the given type, concurrency, and holdability |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type, concurrency, and holdability |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type, result set holdability and result set concurrency. |

**See Also**

- [java.sql.ResultSet](ResultSet.md) 

### createStruct

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createStruct(
    typeName: String!, 
    attributes: Array<Any!>!
): Struct!
```

Factory method for creating Struct objects.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the SQL type name of the SQL structured type that this`Struct`object maps to. The typeName is the name of a user-defined type that has been defined for this database. It is the value returned by`Struct.getSQLTypeName`. |
| `attributes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the attributes that populate the returned object |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Struct](Struct.md)! | a Struct object that maps to the given SQL type and is populated with the given attributes |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database error occurs, the typeName is null or this method is called on a closed connection |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this data type |

### getAutoCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAutoCommit(): Boolean
```

Retrieves the current auto-commit mode for this`Connection`object.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the current state of this`Connection`object's auto-commit mode |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [#setAutoCommit](Connection.md)) 

### getCatalog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCatalog(): String!
```

Retrieves this`Connection`object's current catalog name.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the current catalog name or`null`if there is none |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [#setCatalog](Connection.md)) 

### getClientInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClientInfo(): Properties!
```

Returns a list containing the name and current value of each client info property supported by the driver. The value of a client info property may be null if the property has not been set and does not have a default value.

<br />

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Properties](../java.util/Properties.md)! | A`Properties`object that contains the name and current value of each of the client info properties supported by the driver. <br /> |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the database server returns an error when fetching the client info values from the database or this method is called on a closed connection <br /> |

### getClientInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClientInfo(name: String!): String!
```

Returns the value of the client info property specified by name. This method may return null if the specified client info property has not been set and does not have a default value. This method will also return null if the specified client info property name is not supported by the driver.

Applications may use the`DatabaseMetaData.getClientInfoProperties`method to determine the client info properties supported by the driver.

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the client info property to retrieve <br /> |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The value of the client info property specified <br /> |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the database server returns an error when fetching the client info value from the database or this method is called on a closed connection <br /> |

**See Also**

- [java.sql.DatabaseMetaData#getClientInfoProperties](DatabaseMetaData.md)) 

### getHoldability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getHoldability(): Int
```

Retrieves the current holdability of`ResultSet`objects created using this`Connection`object.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the holdability, one of`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [#setHoldability](Connection.md))
- [java.sql.DatabaseMetaData#getResultSetHoldability](DatabaseMetaData.md))
- [java.sql.ResultSet](ResultSet.md) 

### getMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMetaData(): DatabaseMetaData!
```

Retrieves a`DatabaseMetaData`object that contains metadata about the database to which this`Connection`object represents a connection. The metadata includes information about the database's tables, its supported SQL grammar, its stored procedures, the capabilities of this connection, and so on.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| [DatabaseMetaData](DatabaseMetaData.md)! | a`DatabaseMetaData`object for this`Connection`object |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

### getTransactionIsolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTransactionIsolation(): Int
```

Retrieves this`Connection`object's current transaction isolation level.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current transaction isolation level, which will be one of the following constants:`Connection.TRANSACTION_READ_UNCOMMITTED`,`Connection.TRANSACTION_READ_COMMITTED`,`Connection.TRANSACTION_REPEATABLE_READ`,`Connection.TRANSACTION_SERIALIZABLE`, or`Connection.TRANSACTION_NONE`. |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [#setTransactionIsolation](Connection.md)) 

### getTypeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTypeMap(): MutableMap<String!, Class<*>!>!
```

Retrieves the`Map`object associated with this`Connection`object. Unless the application has added an entry, the type map returned will be empty.

You must invoke`setTypeMap`after making changes to the`Map`object returned from`getTypeMap`as a JDBC driver may create an internal copy of the`Map`object passed to`setTypeMap`:

<br />

```kotlin
Map<String,Class<?>> myMap = con.getTypeMap();
       myMap.put("mySchemaName.ATHLETES", Athletes.class);
       con.setTypeMap(myMap);
  
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>! | the`java.util.Map`object associated with this`Connection`object |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setTypeMap](Connection.md)) 

### getWarnings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWarnings(): SQLWarning!
```

Retrieves the first warning reported by calls on this`Connection`object. If there is more than one warning, subsequent warnings will be chained to the first one and can be retrieved by calling the method`SQLWarning.getNextWarning`on the warning that was retrieved previously.

This method may not be called on a closed connection; doing so will cause an`SQLException`to be thrown.

**Note:**Subsequent warnings will be chained to this SQLWarning.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [SQLWarning](SQLWarning.md)! | the first`SQLWarning`object or`null`if there are none |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [java.sql.SQLWarning](SQLWarning.md) 

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isClosed(): Boolean
```

Retrieves whether this`Connection`object has been closed. A connection is closed if the method`close`has been called on it or if certain fatal errors have occurred. This method is guaranteed to return`true`only when it is called after the method`Connection.close`has been called.

This method generally cannot be called to determine whether a connection to a database is valid or invalid. A typical client can determine that a connection is invalid by catching any exceptions that might be thrown when an operation is attempted.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`Connection`object is closed;`false`if it is still open |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Retrieves whether this`Connection`object is in read-only mode.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`Connection`object is read-only;`false`otherwise |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | SQLException if a database access error occurs or this method is called on a closed connection |

### isValid

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(timeout: Int): Boolean
```

Returns true if the connection has not been closed and is still valid. The driver shall submit a query on the connection or use some other mechanism that positively verifies the connection is still valid when this method is called.

The query submitted by the driver to validate the connection shall be executed in the context of the current transaction.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):- The time in seconds to wait for the database operation used to validate the connection to complete. If the timeout period expires before the operation completes, this method returns false. A value of 0 indicates a timeout is not applied to the database operation. <br /> |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the connection is valid, false otherwise |

| Exceptions ||
|-------------------------|--------------------------------------------------|
| `java.sql.SQLException` | if the value supplied for`timeout`is less then 0 |

**See Also**

- [java.sql.DatabaseMetaData#getClientInfoProperties](DatabaseMetaData.md)) 

### nativeSQL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nativeSQL(sql: String!): String!
```

Converts the given SQL statement into the system's native SQL grammar. A driver may convert the JDBC SQL grammar into its system's native SQL grammar prior to sending it. This method returns the native form of the statement that the driver would have sent.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' parameter placeholders |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the native form of this statement |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

### prepareCall

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareCall(sql: String!): CallableStatement!
```

Creates a`CallableStatement`object for calling database stored procedures. The`CallableStatement`object provides methods for setting up its IN and OUT parameters, and methods for executing the call to a stored procedure.

**Note:** This method is optimized for handling stored procedure call statements. Some drivers may send the call statement to the database when the method`prepareCall`is done; others may wait until the`CallableStatement`object is executed. This has no direct effect on users; however, it does affect which method throws certain SQLExceptions.

Result sets created using the returned`CallableStatement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' parameter placeholders. Typically this statement is specified using JDBC call escape syntax. |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [CallableStatement](CallableStatement.md)! | a new default`CallableStatement`object containing the pre-compiled SQL statement |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

### prepareCall

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareCall(
    sql: String!, 
    resultSetType: Int, 
    resultSetConcurrency: Int
): CallableStatement!
```

Creates a`CallableStatement`object that will generate`ResultSet`objects with the given type and concurrency. This method is the same as the`prepareCall`method above, but it allows the default result set type and concurrency to be overridden. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`object that is the SQL statement to be sent to the database; may contain on or more '?' parameters |
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a result set type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a concurrency type; one of`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [CallableStatement](CallableStatement.md)! | a new`CallableStatement`object containing the pre-compiled SQL statement that will produce`ResultSet`objects with the given type and concurrency |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type and concurrency |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type and result set concurrency. |

### prepareCall

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareCall(
    sql: String!, 
    resultSetType: Int, 
    resultSetConcurrency: Int, 
    resultSetHoldability: Int
): CallableStatement!
```

Creates a`CallableStatement`object that will generate`ResultSet`objects with the given type and concurrency. This method is the same as the`prepareCall`method above, but it allows the default result set type, result set concurrency type and holdability to be overridden.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`object that is the SQL statement to be sent to the database; may contain on or more '?' parameters |
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |
| --- | --- |
| `resultSetHoldability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CallableStatement](CallableStatement.md)! | a new`CallableStatement`object, containing the pre-compiled SQL statement, that will generate`ResultSet`objects with the given type, concurrency, and holdability |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type, concurrency, and holdability |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type, result set holdability and result set concurrency. |

**See Also**

- [java.sql.ResultSet](ResultSet.md) 

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(sql: String!): PreparedStatement!
```

Creates a`PreparedStatement`object for sending parameterized SQL statements to the database.

A SQL statement with or without IN parameters can be pre-compiled and stored in a`PreparedStatement`object. This object can then be used to efficiently execute this statement multiple times.

**Note:** This method is optimized for handling parametric SQL statements that benefit from precompilation. If the driver supports precompilation, the method`prepareStatement`will send the statement to the database for precompilation. Some drivers may not support precompilation. In this case, the statement may not be sent to the database until the`PreparedStatement`object is executed. This has no direct effect on users; however, it does affect which methods throw certain`SQLException`objects.

Result sets created using the returned`PreparedStatement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' IN parameter placeholders |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new default`PreparedStatement`object containing the pre-compiled SQL statement |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(
    sql: String!, 
    autoGeneratedKeys: Int
): PreparedStatement!
```

Creates a default`PreparedStatement`object that has the capability to retrieve auto-generated keys. The given constant tells the driver whether it should make auto-generated keys available for retrieval. This parameter is ignored if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific).

**Note:** This method is optimized for handling parametric SQL statements that benefit from precompilation. If the driver supports precompilation, the method`prepareStatement`will send the statement to the database for precompilation. Some drivers may not support precompilation. In this case, the statement may not be sent to the database until the`PreparedStatement`object is executed. This has no direct effect on users; however, it does affect which methods throw certain SQLExceptions.

Result sets created using the returned`PreparedStatement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' IN parameter placeholders |
| `autoGeneratedKeys` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a flag indicating whether auto-generated keys should be returned; one of`Statement.RETURN_GENERATED_KEYS`or`Statement.NO_GENERATED_KEYS` |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new`PreparedStatement`object, containing the pre-compiled SQL statement, that will have the capability of returning auto-generated keys |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameter is not a`Statement`constant indicating whether auto-generated keys should be returned |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method with a constant of Statement.RETURN_GENERATED_KEYS |

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(
    sql: String!, 
    resultSetType: Int, 
    resultSetConcurrency: Int
): PreparedStatement!
```

Creates a`PreparedStatement`object that will generate`ResultSet`objects with the given type and concurrency. This method is the same as the`prepareStatement`method above, but it allows the default result set type and concurrency to be overridden. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`object that is the SQL statement to be sent to the database; may contain one or more '?' IN parameters |
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a result set type; one of`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a concurrency type; one of`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new PreparedStatement object containing the pre-compiled SQL statement that will produce`ResultSet`objects with the given type and concurrency |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type and concurrency |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type and result set concurrency. |

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(
    sql: String!, 
    resultSetType: Int, 
    resultSetConcurrency: Int, 
    resultSetHoldability: Int
): PreparedStatement!
```

Creates a`PreparedStatement`object that will generate`ResultSet`objects with the given type, concurrency, and holdability.

This method is the same as the`prepareStatement`method above, but it allows the default result set type, concurrency, and holdability to be overridden.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`object that is the SQL statement to be sent to the database; may contain one or more '?' IN parameters |
| `resultSetType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |
| `resultSetConcurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |
| --- | --- |
| `resultSetHoldability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`ResultSet`constants:`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new`PreparedStatement`object, containing the pre-compiled SQL statement, that will generate`ResultSet`objects with the given type, concurrency, and holdability |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameters are not`ResultSet`constants indicating type, concurrency, and holdability |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method or this method is not supported for the specified result set type, result set holdability and result set concurrency. |

**See Also**

- [java.sql.ResultSet](ResultSet.md) 

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(
    sql: String!, 
    columnIndexes: IntArray!
): PreparedStatement!
```

Creates a default`PreparedStatement`object capable of returning the auto-generated keys designated by the given array. This array contains the indexes of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific).

An SQL statement with or without IN parameters can be pre-compiled and stored in a`PreparedStatement`object. This object can then be used to efficiently execute this statement multiple times.

**Note:** This method is optimized for handling parametric SQL statements that benefit from precompilation. If the driver supports precompilation, the method`prepareStatement`will send the statement to the database for precompilation. Some drivers may not support precompilation. In this case, the statement may not be sent to the database until the`PreparedStatement`object is executed. This has no direct effect on users; however, it does affect which methods throw certain SQLExceptions.

Result sets created using the returned`PreparedStatement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' IN parameter placeholders |
| `columnIndexes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of column indexes indicating the columns that should be returned from the inserted row or rows |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new`PreparedStatement`object, containing the pre-compiled statement, that is capable of returning the auto-generated keys designated by the given array of column indexes |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### prepareStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun prepareStatement(
    sql: String!, 
    columnNames: Array<String!>!
): PreparedStatement!
```

Creates a default`PreparedStatement`object capable of returning the auto-generated keys designated by the given array. This array contains the names of the columns in the target table that contain the auto-generated keys that should be returned. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific).

An SQL statement with or without IN parameters can be pre-compiled and stored in a`PreparedStatement`object. This object can then be used to efficiently execute this statement multiple times.

**Note:** This method is optimized for handling parametric SQL statements that benefit from precompilation. If the driver supports precompilation, the method`prepareStatement`will send the statement to the database for precompilation. Some drivers may not support precompilation. In this case, the statement may not be sent to the database until the`PreparedStatement`object is executed. This has no direct effect on users; however, it does affect which methods throw certain SQLExceptions.

Result sets created using the returned`PreparedStatement`object will by default be type`TYPE_FORWARD_ONLY`and have a concurrency level of`CONCUR_READ_ONLY`. The holdability of the created result sets can be determined by calling [getHoldability](Connection.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an SQL statement that may contain one or more '?' IN parameter placeholders |
| `columnNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an array of column names indicating the columns that should be returned from the inserted row or rows |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreparedStatement](PreparedStatement.md)! | a new`PreparedStatement`object, containing the pre-compiled statement, that is capable of returning the auto-generated keys designated by the given array of column names |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### releaseSavepoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun releaseSavepoint(savepoint: Savepoint!): Unit
```

Removes the specified`Savepoint`and subsequent`Savepoint`objects from the current transaction. Any reference to the savepoint after it have been removed will cause an`SQLException`to be thrown.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------|
| `savepoint` | [Savepoint](Savepoint.md)!:the`Savepoint`object to be removed |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given`Savepoint`object is not a valid savepoint in the current transaction |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### rollback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rollback(): Unit
```

Undoes all changes made in the current transaction and releases any database locks currently held by this`Connection`object. This method should be used only when auto-commit mode has been disabled.

| Exceptions ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called while participating in a distributed transaction, this method is called on a closed connection or this`Connection`object is in auto-commit mode |

**See Also**

- [#setAutoCommit](Connection.md)) 

### rollback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rollback(savepoint: Savepoint!): Unit
```

Undoes all changes made after the given`Savepoint`object was set.

This method should be used only when auto-commit has been disabled.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `savepoint` | [Savepoint](Savepoint.md)!:the`Savepoint`object to roll back to |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called while participating in a distributed transaction, this method is called on a closed connection, the`Savepoint`object is no longer valid, or this`Connection`object is currently in auto-commit mode |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [java.sql.Savepoint](Savepoint.md) 

### setAutoCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAutoCommit(autoCommit: Boolean): Unit
```

Sets this connection's auto-commit mode to the given state. If a connection is in auto-commit mode, then all its SQL statements will be executed and committed as individual transactions. Otherwise, its SQL statements are grouped into transactions that are terminated by a call to either the method`commit`or the method`rollback`. By default, new connections are in auto-commit mode.

The commit occurs when the statement completes. The time when the statement completes depends on the type of SQL Statement:

- For DML statements, such as Insert, Update or Delete, and DDL statements, the statement is complete as soon as it has finished executing.
- For Select statements, the statement is complete when the associated result set is closed.
- For`CallableStatement`objects or for statements that return multiple results, the statement is complete when all of the associated result sets have been closed, and all update counts and output parameters have been retrieved.

**NOTE:** If this method is called during a transaction and the auto-commit mode is changed, the transaction is committed. If`setAutoCommit`is called and the auto-commit mode is not changed, the call is a no-op.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `autoCommit` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable auto-commit mode;`false`to disable it |

| Exceptions ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, setAutoCommit(true) is called while participating in a distributed transaction, or this method is called on a closed connection |

**See Also**

- [#getAutoCommit](Connection.md)) 

### setCatalog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCatalog(catalog: String!): Unit
```

Sets the given catalog name in order to select a subspace of this`Connection`object's database in which to work.

If the driver does not support catalogs, it will silently ignore this request.

Calling`setCatalog`has no effect on previously created or prepared`Statement`objects. It is implementation defined whether a DBMS prepare operation takes place immediately when the`Connection`method`prepareStatement`or`prepareCall`is invoked. For maximum portability,`setCatalog`should be called before a`Statement`is created or prepared.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `catalog` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of a catalog (subspace in this`Connection`object's database) in which to work |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed connection |

**See Also**

- [#getCatalog](Connection.md)) 

### setClientInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClientInfo(
    name: String!, 
    value: String!
): Unit
```

Sets the value of the client info property specified by name to the value specified by value.

Applications may use the`DatabaseMetaData.getClientInfoProperties`method to determine the client info properties supported by the driver and the maximum length that may be specified for each property.

The driver stores the value specified in a suitable location in the database. For example in a special register, session parameter, or system table column. For efficiency the driver may defer setting the value in the database until the next time a statement is executed or prepared. Other than storing the client information in the appropriate place in the database, these methods shall not alter the behavior of the connection in anyway. The values supplied to these methods are used for accounting, diagnostics and debugging purposes only.

The driver shall generate a warning if the client info name specified is not recognized by the driver.

If the value specified to this method is greater than the maximum length for the property the driver may either truncate the value and generate a warning or generate a`SQLClientInfoException`. If the driver generates a`SQLClientInfoException`, the value specified was not set on the connection.

The following are standard client info properties. Drivers are not required to support these properties however if the driver supports a client info property that can be described by one of the standard properties, the standard property name should be used.

<br />

- ApplicationName - The name of the application currently utilizing the connection
- ClientUser - The name of the user that the application using the connection is performing work for. This may not be the same as the user name that was used in establishing the connection.
- ClientHostname - The hostname of the computer the application using the connection is running on.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the client info property to set |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value to set the client info property to. If the value is null, the current value of the specified property is cleared. <br /> |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLClientInfoException` | if the database server returns an error while setting the client info value on the database server or this method is called on a closed connection <br /> |

### setClientInfo

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClientInfo(properties: Properties!): Unit
```

Sets the value of the connection's client info properties. The`Properties`object contains the names and values of the client info properties to be set. The set of client info properties contained in the properties list replaces the current set of client info properties on the connection. If a property that is currently set on the connection is not present in the properties list, that property is cleared. Specifying an empty properties list will clear all of the properties on the connection. See`setClientInfo (String, String)`for more information.

If an error occurs in setting any of the client info properties, a`SQLClientInfoException`is thrown. The`SQLClientInfoException`contains information indicating which client info properties were not set. The state of the client information is unknown because some databases do not allow multiple client info properties to be set atomically. For those databases, one or more properties may have been set before the error occurred.

<br />

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `properties` | [Properties](../java.util/Properties.md)!:the list of client info properties to set <br /> |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLClientInfoException` | if the database server returns an error while setting the clientInfo values on the database server or this method is called on a closed connection <br /> |

**See Also**

- [java.sql.Connection#setClientInfo(String, String)](Connection.md)) 

### setHoldability

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHoldability(holdability: Int): Unit
```

Changes the default holdability of`ResultSet`objects created using this`Connection`object to the given holdability. The default holdability of`ResultSet`objects can be be determined by invoking [DatabaseMetaData.getResultSetHoldability](DatabaseMetaData.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `holdability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a`ResultSet`holdability constant; one of`ResultSet.HOLD_CURSORS_OVER_COMMIT`or`ResultSet.CLOSE_CURSORS_AT_COMMIT` |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access occurs, this method is called on a closed connection, or the given parameter is not a`ResultSet`constant indicating holdability |
| `java.sql.SQLFeatureNotSupportedException` | if the given holdability is not supported |

**See Also**

- [#getHoldability](Connection.md))
- [java.sql.DatabaseMetaData#getResultSetHoldability](DatabaseMetaData.md))
- [java.sql.ResultSet](ResultSet.md) 

### setReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setReadOnly(readOnly: Boolean): Unit
```

Puts this connection in read-only mode as a hint to the driver to enable database optimizations.

**Note:**This method cannot be called during a transaction.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `readOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`enables read-only mode;`false`disables it |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or this method is called during a transaction |

### setSavepoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSavepoint(): Savepoint!
```

Creates an unnamed savepoint in the current transaction and returns the new`Savepoint`object that represents it.

if setSavepoint is invoked outside of an active transaction, a transaction will be started at this newly created savepoint.

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [Savepoint](Savepoint.md)! | the new`Savepoint`object |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called while participating in a distributed transaction, this method is called on a closed connection or this`Connection`object is currently in auto-commit mode |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [java.sql.Savepoint](Savepoint.md) 

### setSavepoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSavepoint(name: String!): Savepoint!
```

Creates a savepoint with the given name in the current transaction and returns the new`Savepoint`object that represents it.

if setSavepoint is invoked outside of an active transaction, a transaction will be started at this newly created savepoint.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`containing the name of the savepoint |

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [Savepoint](Savepoint.md)! | the new`Savepoint`object |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called while participating in a distributed transaction, this method is called on a closed connection or this`Connection`object is currently in auto-commit mode |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [java.sql.Savepoint](Savepoint.md) 

### setTransactionIsolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTransactionIsolation(level: Int): Unit
```

Attempts to change the transaction isolation level for this`Connection`object to the one given. The constants defined in the interface`Connection`are the possible transaction isolation levels.

**Note:**If this method is called during a transaction, the result is implementation-defined.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following`Connection`constants:`Connection.TRANSACTION_READ_UNCOMMITTED`,`Connection.TRANSACTION_READ_COMMITTED`,`Connection.TRANSACTION_REPEATABLE_READ`, or`Connection.TRANSACTION_SERIALIZABLE`. (Note that`Connection.TRANSACTION_NONE`cannot be used because it specifies that transactions are not supported.) |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameter is not one of the`Connection`constants |

**See Also**

- [java.sql.DatabaseMetaData#supportsTransactionIsolationLevel](DatabaseMetaData.md))
- [#getTransactionIsolation](Connection.md)) 

### setTypeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTypeMap(map: MutableMap<String!, Class<*>!>!): Unit
```

Installs the given`TypeMap`object as the type map for this`Connection`object. The type map will be used for the custom mapping of SQL structured types and distinct types.

You must set the the values for the`TypeMap`prior to callng`setMap`as a JDBC driver may create an internal copy of the`TypeMap`:

<br />

```kotlin
Map myMap<String,Class<?>> = new HashMap<String,Class<?>>();
       myMap.put("mySchemaName.ATHLETES", Athletes.class);
       con.setTypeMap(myMap);
  
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!:the`java.util.Map`object to install as the replacement for this`Connection`object's default type map |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed connection or the given parameter is not a`java.util.Map`object |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#getTypeMap](Connection.md))
