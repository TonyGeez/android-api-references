# RowSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSet

```
interface RowSet : ResultSet
```

| [javax.sql.RowSet](RowSet.md) |

The interface that adds support to the JDBC API for the JavaBeansTM component model. A rowset, which can be used as a JavaBeans component in a visual Bean development environment, can be created and configured at design time and executed at run time.

The`RowSet`interface provides a set of JavaBeans properties that allow a`RowSet`instance to be configured to connect to a JDBC data source and read some data from the data source. A group of setter methods (`setInt`,`setBytes`,`setString`, and so on) provide a way to pass input parameters to a rowset's command property. This command is the SQL query the rowset uses when it gets its data from a relational database, which is generally the case.

The`RowSet`interface supports JavaBeans events, allowing other components in an application to be notified when an event occurs on a rowset, such as a change in its value.

The`RowSet`interface is unique in that it is intended to be implemented using the rest of the JDBC API. In other words, a`RowSet`implementation is a layer of software that executes "on top" of a JDBC driver. Implementations of the`RowSet`interface can be provided by anyone, including JDBC driver vendors who want to provide a`RowSet`implementation as part of their JDBC products.

A`RowSet`object may make a connection with a data source and maintain that connection throughout its life cycle, in which case it is called a*connected* rowset. A rowset may also make a connection with a data source, get data from it, and then close the connection. Such a rowset is called a*disconnected*rowset. A disconnected rowset may make changes to its data while it is disconnected and then send the changes back to the original source of the data, but it must reestablish a connection to do so.

A disconnected rowset may have a reader (a`RowSetReader`object) and a writer (a`RowSetWriter`object) associated with it. The reader may be implemented in many different ways to populate a rowset with data, including getting data from a non-relational data source. The writer can also be implemented in many different ways to propagate changes made to the rowset's data back to the underlying data source.

Rowsets are easy to use. The`RowSet`interface extends the standard`java.sql.ResultSet`interface. The`RowSetMetaData`interface extends the`java.sql.ResultSetMetaData`interface. Thus, developers familiar with the JDBC API will have to learn a minimal number of new APIs to use rowsets. In addition, third-party software tools that work with JDBC`ResultSet`objects will also easily be made to work with rowsets.

## Summary

| Inherited constants ||
|---|---|
| From class [ResultSet](../java.sql/ResultSet.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_CURSORS_AT_COMMIT](../java.sql/ResultSet.md) <br /> The constant indicating that open`ResultSet`objects with this holdability will be closed when the current transaction is commited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCUR_READ_ONLY](../java.sql/ResultSet.md) <br /> The constant indicating the concurrency mode for a`ResultSet`object that may NOT be updated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONCUR_UPDATABLE](../java.sql/ResultSet.md) <br /> The constant indicating the concurrency mode for a`ResultSet`object that may be updated. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FETCH_FORWARD](../java.sql/ResultSet.md) <br /> The constant indicating that the rows in a result set will be processed in a forward direction; first-to-last. This constant is used by the method`setFetchDirection`as a hint to the driver, which the driver may ignore. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FETCH_REVERSE](../java.sql/ResultSet.md) <br /> The constant indicating that the rows in a result set will be processed in a reverse direction; last-to-first. This constant is used by the method`setFetchDirection`as a hint to the driver, which the driver may ignore. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FETCH_UNKNOWN](../java.sql/ResultSet.md) <br /> The constant indicating that the order in which rows in a result set will be processed is unknown. This constant is used by the method`setFetchDirection`as a hint to the driver, which the driver may ignore. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOLD_CURSORS_OVER_COMMIT](../java.sql/ResultSet.md) <br /> The constant indicating that open`ResultSet`objects with this holdability will remain open when the current transaction is commited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FORWARD_ONLY](../java.sql/ResultSet.md) <br /> The constant indicating the type for a`ResultSet`object whose cursor may move only forward. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCROLL_INSENSITIVE](../java.sql/ResultSet.md) <br /> The constant indicating the type for a`ResultSet`object that is scrollable but generally not sensitive to changes to the data that underlies the`ResultSet`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCROLL_SENSITIVE](../java.sql/ResultSet.md) <br /> The constant indicating the type for a`ResultSet`object that is scrollable and generally sensitive to changes to the data that underlies the`ResultSet`. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addRowSetListener](RowSet.md))`(`listener:` ` [RowSetListener](RowSetListener.md)!`)` Registers the given listener so that it will be notified of events that occur on this`RowSet`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearParameters](RowSet.md))`()` Clears the parameters set for this`RowSet`object's command. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](RowSet.md))`()` Fills this`RowSet`object with data. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCommand](RowSet.md))`()` Retrieves this`RowSet`object's command property. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDataSourceName](RowSet.md))`()` Retrieves the logical name that identifies the data source for this`RowSet`object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEscapeProcessing](RowSet.md))`()` Retrieves whether escape processing is enabled for this`RowSet`object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxFieldSize](RowSet.md))`()` Retrieves the maximum number of bytes that may be returned for certain column values. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxRows](RowSet.md))`()` Retrieves the maximum number of rows that this`RowSet`object can contain. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPassword](RowSet.md))`()` Retrieves the password used to create a database connection. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueryTimeout](RowSet.md))`()` Retrieves the maximum number of seconds the driver will wait for a statement to execute. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransactionIsolation](RowSet.md))`()` Retrieves the transaction isolation level set for this`RowSet`object. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>! | [getTypeMap](RowSet.md))`()` Retrieves the`Map`object associated with this`RowSet`object, which specifies the custom mapping of SQL user-defined types, if any. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUrl](RowSet.md))`()` Retrieves the url property this`RowSet`object will use to create a connection if it uses the`DriverManager`instead of a`DataSource`object to establish the connection. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUsername](RowSet.md))`()` Retrieves the username used to create a database connection for this`RowSet`object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](RowSet.md))`()` Retrieves whether this`RowSet`object is read-only. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeRowSetListener](RowSet.md))`(`listener:` ` [RowSetListener](RowSetListener.md)!`)` Removes the specified listener from the list of components that will be notified when an event occurs on this`RowSet`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArray](RowSet.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Array](../java.sql/Array.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`Array`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given input stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given`java.io.InputStream`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBigDecimal](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given`java.math.BigDeciaml`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBigDecimal](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` Sets the designated parameter to the given`java.math.BigDecimal`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given input stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given`java.io.InputStream`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Blob](../java.sql/Blob.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`Blob`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Blob](../java.sql/Blob.md)!`)` Sets the designated parameter to the given`java.sql.Blob`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`boolean`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the designated parameter to the given Java`boolean`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`byte`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the designated parameter to the given Java`byte`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBytes](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the designated parameter in this`RowSet`object's command to the given Java array of`byte`values. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBytes](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the designated parameter to the given Java array of bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given`java.io.Reader`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to the given`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given`Reader`object, which is the given number of characters long. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Clob](../java.sql/Clob.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`Clob`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Clob](../java.sql/Clob.md)!`)` Sets the designated parameter to the given`java.sql.Clob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCommand](RowSet.md))`(`cmd:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets this`RowSet`object's command property to the given SQL query. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConcurrency](RowSet.md))`(`concurrency:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the concurrency of this`RowSet`object to the given concurrency level. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSourceName](RowSet.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the data source name property for this`RowSet`object to the given`String`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](../java.sql/Date.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Date`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](../java.sql/Date.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Date`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Date](../java.sql/Date.md)!`)` Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Date](../java.sql/Date.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`double`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the designated parameter to the given Java`double`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEscapeProcessing](RowSet.md))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets escape processing for this`RowSet`object on or off. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`float`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the designated parameter to the given Java`float`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`int`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given Java`int`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`long`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given Java`long`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxFieldSize](RowSet.md))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of bytes that can be returned for a column value to the given number of bytes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxRows](RowSet.md))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of rows that this`RowSet`object can contain to the specified number. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter in this`RowSet`object's command to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to a`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [NClob](../java.sql/NClob.md)!`)` Sets the designated parameter to a`java.sql.NClob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` Sets the designated parameter to a`Reader`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [NClob](../java.sql/NClob.md)!`)` Sets the designated parameter to a`java.sql.NClob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNString](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated paramter to the given`String`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNString](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated paramter to the given`String`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's SQL command to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](RowSet.md))`(`paramIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter in this`RowSet`object's SQL command to SQL`NULL`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the designated parameter in this`RowSet`object's command with a Java`Object`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command with a Java`Object`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scaleOrLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter in this`RowSet`object's command with the given Java`Object`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of the designated parameter with the given object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](RowSet.md))`(`password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the database password for this`RowSet`object to the given`String`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQueryTimeout](RowSet.md))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum time the driver will wait for a statement to execute to the given number of seconds. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadOnly](RowSet.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this`RowSet`object is read-only to the given`boolean`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRef](RowSet.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Ref](../java.sql/Ref.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`Ref`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowId](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [RowId](../java.sql/RowId.md)!`)` Sets the designated parameter to the given`java.sql.RowId`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowId](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [RowId](../java.sql/RowId.md)!`)` Sets the designated parameter to the given`java.sql.RowId`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSQLXML](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xmlObject:` ` [SQLXML](../java.sql/SQLXML.md)!`)` Sets the designated parameter to the given`java.sql.SQLXML`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSQLXML](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `xmlObject:` ` [SQLXML](../java.sql/SQLXML.md)!`)` Sets the designated parameter to the given`java.sql.SQLXML`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the designated parameter in this`RowSet`object's command to the given Java`short`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the designated parameter to the given Java`short`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter in this`RowSet`object's command to the given Java`String`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to the given Java`String`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](../java.sql/Time.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Time`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](../java.sql/Time.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Time`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Time](../java.sql/Time.md)!`)` Sets the designated parameter to the given`java.sql.Time`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Time](../java.sql/Time.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`)` Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Timestamp`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Timestamp`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](RowSet.md))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransactionIsolation](RowSet.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the transaction isolation level for this`RowSet`obejct. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](RowSet.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the type of this`RowSet`object to the given type. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTypeMap](RowSet.md))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` Installs the given`java.util.Map`object as the default type map for this`RowSet`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](RowSet.md))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [URL](../java.net/URL.md)!`)` Sets the designated parameter to the given`java.net.URL`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUrl](RowSet.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the URL this`RowSet`object will use when it uses the`DriverManager`to create a connection. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUsername](RowSet.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the username property for this`RowSet`object to the given`String`. |

| Inherited functions ||
|---|---|
| From class [ResultSet](../java.sql/ResultSet.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [absolute](../java.sql/ResultSet.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Moves the cursor to the given row number in this`ResultSet`object. If the row number is positive, the cursor moves to the given row number with respect to the beginning of the result set. The first row is row 1, the second is row 2, and so on. If the given row number is negative, the cursor moves to an absolute row position with respect to the end of the result set. For example, calling the method`absolute(-1)`positions the cursor on the last row; calling the method`absolute(-2)`moves the cursor to the next-to-last row, and so on. If the row number specified is zero, the cursor is moved to before the first row. An attempt to position the cursor beyond the first/last row in the result set leaves the cursor before the first row or after the last row. **Note:** Calling`absolute(1)`is the same as calling`first()`. Calling`absolute(-1)`is the same as calling`last()`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterLast](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the end of this`ResultSet`object, just after the last row. This method has no effect if the result set contains no rows. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeFirst](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the front of this`ResultSet`object, just before the first row. This method has no effect if the result set contains no rows. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelRowUpdates](../java.sql/ResultSet.md))`()` <br /> Cancels the updates made to the current row in this`ResultSet`object. This method may be called after calling an updater method(s) and before calling the method`updateRow`to roll back the updates made to a row. If no updates have been made or`updateRow`has already been called, this method has no effect. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearWarnings](../java.sql/ResultSet.md))`()` <br /> Clears all warnings reported on this`ResultSet`object. After this method is called, the method`getWarnings`returns`null`until a new warning is reported for this`ResultSet`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java.sql/ResultSet.md))`()` <br /> Releases this`ResultSet`object's database and JDBC resources immediately instead of waiting for this to happen when it is automatically closed. The closing of a`ResultSet`object does**not** close the`Blob`,`Clob`or`NClob`objects created by the`ResultSet`.`Blob`,`Clob`or`NClob`objects remain valid for at least the duration of the transaction in which they are creataed, unless their`free`method is invoked. When a`ResultSet`is closed, any`ResultSetMetaData`instances that were created by calling the`getMetaData`method remain accessible. **Note:** A`ResultSet`object is automatically closed by the`Statement`object that generated it when that`Statement`object is closed, re-executed, or is used to retrieve the next result from a sequence of multiple results. Calling the method`close`on a`ResultSet`object that is already closed is a no-op. <br /> <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteRow](../java.sql/ResultSet.md))`()` <br /> Deletes the current row from this`ResultSet`object and from the underlying database. This method cannot be called when the cursor is on the insert row. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findColumn](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Maps the given`ResultSet`column label to its`ResultSet`column index. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [first](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the first row in this`ResultSet`object. <br /> | | [Array](../java.sql/Array.md)! | [getArray](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`Array`object in the Java programming language. <br /> | | [Array](../java.sql/Array.md)! | [getArray](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`Array`object in the Java programming language. <br /> | | [InputStream](../java.io/InputStream.md)! | [getAsciiStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a stream of ASCII characters. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARCHAR`values. The JDBC driver will do any necessary conversion from the database format into ASCII. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`InputStream.available`is called whether there is data available or not. <br /> | | [InputStream](../java.io/InputStream.md)! | [getAsciiStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a stream of ASCII characters. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARCHAR`values. The JDBC driver will do any necessary conversion from the database format into ASCII. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`available`is called whether there is data available or not. <br /> | | [BigDecimal](../java.math/BigDecimal.md)! | [getBigDecimal](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.math.BigDecimal`with full precision. <br /> | | [BigDecimal](../java.math/BigDecimal.md)! | [getBigDecimal](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.BigDecimal`in the Java programming language. <br /> | | [BigDecimal](../java.math/BigDecimal.md)! | [getBigDecimal](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.math.BigDecimal`with full precision. <br /> | | [BigDecimal](../java.math/BigDecimal.md)! | [getBigDecimal](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.math.BigDecimal`in the Java programming language. <br /> | | [InputStream](../java.io/InputStream.md)! | [getBinaryStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a stream of uninterpreted bytes. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARBINARY`values. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`InputStream.available`is called whether there is data available or not. <br /> | | [InputStream](../java.io/InputStream.md)! | [getBinaryStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a stream of uninterpreted`byte`s. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARBINARY`values. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`available`is called whether there is data available or not. <br /> | | [Blob](../java.sql/Blob.md)! | [getBlob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Blob`object in the Java programming language. <br /> | | [Blob](../java.sql/Blob.md)! | [getBlob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Blob`object in the Java programming language. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`boolean`in the Java programming language. If the designated column has a datatype of CHAR or VARCHAR and contains a "0" or has a datatype of BIT, TINYINT, SMALLINT, INTEGER or BIGINT and contains a 0, a value of`false`is returned. If the designated column has a datatype of CHAR or VARCHAR and contains a "1" or has a datatype of BIT, TINYINT, SMALLINT, INTEGER or BIGINT and contains a 1, a value of`true`is returned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`boolean`in the Java programming language. If the designated column has a datatype of CHAR or VARCHAR and contains a "0" or has a datatype of BIT, TINYINT, SMALLINT, INTEGER or BIGINT and contains a 0, a value of`false`is returned. If the designated column has a datatype of CHAR or VARCHAR and contains a "1" or has a datatype of BIT, TINYINT, SMALLINT, INTEGER or BIGINT and contains a 1, a value of`true`is returned. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`byte`in the Java programming language. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`byte`in the Java programming language. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`byte`array in the Java programming language. The bytes represent the raw values returned by the driver. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`byte`array in the Java programming language. The bytes represent the raw values returned by the driver. <br /> | | [Reader](../java.io/Reader.md)! | [getCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.io.Reader`object. <br /> | | [Reader](../java.io/Reader.md)! | [getCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.io.Reader`object. <br /> | | [Clob](../java.sql/Clob.md)! | [getClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Clob`object in the Java programming language. <br /> | | [Clob](../java.sql/Clob.md)! | [getClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Clob`object in the Java programming language. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConcurrency](../java.sql/ResultSet.md))`()` <br /> Retrieves the concurrency mode of this`ResultSet`object. The concurrency used is determined by the`Statement`object that created the result set. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCursorName](../java.sql/ResultSet.md))`()` <br /> Retrieves the name of the SQL cursor used by this`ResultSet`object. In SQL, a result table is retrieved through a cursor that is named. The current row of a result set can be updated or deleted using a positioned update/delete statement that references the cursor name. To insure that the cursor has the proper isolation level to support update, the cursor's`SELECT`statement should be of the form`SELECT FOR UPDATE`. If`FOR UPDATE`is omitted, the positioned updates may fail. The JDBC API supports this SQL feature by providing the name of the SQL cursor used by a`ResultSet`object. The current row of a`ResultSet`object is also the current row of this SQL cursor. <br /> | | [Date](../java.sql/Date.md)! | [getDate](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Date`object in the Java programming language. <br /> | | [Date](../java.sql/Date.md)! | [getDate](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Date`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the date if the underlying database does not store timezone information. <br /> | | [Date](../java.sql/Date.md)! | [getDate](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Date`object in the Java programming language. <br /> | | [Date](../java.sql/Date.md)! | [getDate](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Date`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the date if the underlying database does not store timezone information. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`double`in the Java programming language. <br /> | | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`double`in the Java programming language. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchDirection](../java.sql/ResultSet.md))`()` <br /> Retrieves the fetch direction for this`ResultSet`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchSize](../java.sql/ResultSet.md))`()` <br /> Retrieves the fetch size for this`ResultSet`object. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`float`in the Java programming language. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`float`in the Java programming language. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHoldability](../java.sql/ResultSet.md))`()` <br /> Retrieves the holdability of this`ResultSet`object <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`int`in the Java programming language. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`int`in the Java programming language. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`long`in the Java programming language. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`long`in the Java programming language. <br /> | | [ResultSetMetaData](../java.sql/ResultSetMetaData.md)! | [getMetaData](../java.sql/ResultSet.md))`()` <br /> Retrieves the number, types and properties of this`ResultSet`object's columns. <br /> | | [Reader](../java.io/Reader.md)! | [getNCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.io.Reader`object. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. <br /> | | [Reader](../java.io/Reader.md)! | [getNCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.io.Reader`object. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. <br /> | | [NClob](../java.sql/NClob.md)! | [getNClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`NClob`object in the Java programming language. <br /> | | [NClob](../java.sql/NClob.md)! | [getNClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`NClob`object in the Java programming language. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNString](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`String`in the Java programming language. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNString](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`String`in the Java programming language. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the value of the designated column in the current row of this`ResultSet`object as an`Object`in the Java programming language. This method will return the value of the given column as a Java object. The type of the Java object will be the default Java object type corresponding to the column's SQL type, following the mapping for built-in types specified in the JDBC specification. If the value is an SQL`NULL`, the driver returns a Java`null`. This method may also be used to read database-specific abstract data types. In the JDBC 2.0 API, the behavior of method`getObject`is extended to materialize data of SQL user-defined types. If`Connection.getTypeMap`does not throw a`SQLFeatureNotSupportedException`, then when a column contains a structured or distinct value, the behavior of this method is as if it were a call to:`getObject(columnIndex, this.getStatement().getConnection().getTypeMap())`. If`Connection.getTypeMap`does throw a`SQLFeatureNotSupportedException`, then structured values are not supported, and distinct values are mapped to the default Java class as determined by the underlying SQL type of the DISTINCT type. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`Object`in the Java programming language. If the value is an SQL`NULL`, the driver returns a Java`null`. This method uses the given`Map`object for the custom mapping of the SQL structured or distinct type that is being retrieved. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the value of the designated column in the current row of this`ResultSet`object as an`Object`in the Java programming language. This method will return the value of the given column as a Java object. The type of the Java object will be the default Java object type corresponding to the column's SQL type, following the mapping for built-in types specified in the JDBC specification. If the value is an SQL`NULL`, the driver returns a Java`null`. This method may also be used to read database-specific abstract data types. In the JDBC 2.0 API, the behavior of the method`getObject`is extended to materialize data of SQL user-defined types. When a column contains a structured or distinct value, the behavior of this method is as if it were a call to:`getObject(columnIndex, this.getStatement().getConnection().getTypeMap())`. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as an`Object`in the Java programming language. If the value is an SQL`NULL`, the driver returns a Java`null`. This method uses the specified`Map`object for custom mapping if appropriate. <br /> | | [Ref](../java.sql/Ref.md)! | [getRef](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Ref`object in the Java programming language. <br /> | | [Ref](../java.sql/Ref.md)! | [getRef](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`Ref`object in the Java programming language. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRow](../java.sql/ResultSet.md))`()` <br /> Retrieves the current row number. The first row is number 1, the second number 2, and so on. **Note:** Support for the`getRow`method is optional for`ResultSet`s with a result set type of`TYPE_FORWARD_ONLY` <br /> | | [RowId](../java.sql/RowId.md)! | [getRowId](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.RowId`object in the Java programming language. <br /> | | [RowId](../java.sql/RowId.md)! | [getRowId](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.RowId`object in the Java programming language. <br /> | | [SQLXML](../java.sql/SQLXML.md)! | [getSQLXML](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`as a`java.sql.SQLXML`object in the Java programming language. <br /> | | [SQLXML](../java.sql/SQLXML.md)! | [getSQLXML](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`as a`java.sql.SQLXML`object in the Java programming language. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`short`in the Java programming language. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`short`in the Java programming language. <br /> | | [Statement](../java.sql/Statement.md)! | [getStatement](../java.sql/ResultSet.md))`()` <br /> Retrieves the`Statement`object that produced this`ResultSet`object. If the result set was generated some other way, such as by a`DatabaseMetaData`method, this method may return`null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`String`in the Java programming language. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`String`in the Java programming language. <br /> | | [Time](../java.sql/Time.md)! | [getTime](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Time`object in the Java programming language. <br /> | | [Time](../java.sql/Time.md)! | [getTime](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Time`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the time if the underlying database does not store timezone information. <br /> | | [Time](../java.sql/Time.md)! | [getTime](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Time`object in the Java programming language. <br /> | | [Time](../java.sql/Time.md)! | [getTime](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Time`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the time if the underlying database does not store timezone information. <br /> | | [Timestamp](../java.sql/Timestamp.md)! | [getTimestamp](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Timestamp`object in the Java programming language. <br /> | | [Timestamp](../java.sql/Timestamp.md)! | [getTimestamp](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Timestamp`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the timestamp if the underlying database does not store timezone information. <br /> | | [Timestamp](../java.sql/Timestamp.md)! | [getTimestamp](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Timestamp`object in the Java programming language. <br /> | | [Timestamp](../java.sql/Timestamp.md)! | [getTimestamp](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](../java.util/Calendar.md)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.sql.Timestamp`object in the Java programming language. This method uses the given calendar to construct an appropriate millisecond value for the timestamp if the underlying database does not store timezone information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../java.sql/ResultSet.md))`()` <br /> Retrieves the type of this`ResultSet`object. The type is determined by the`Statement`object that created the result set. <br /> | | [URL](../java.net/URL.md)! | [getURL](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.net.URL`object in the Java programming language. <br /> | | [URL](../java.net/URL.md)! | [getURL](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a`java.net.URL`object in the Java programming language. <br /> | | [InputStream](../java.io/InputStream.md)! | [getUnicodeStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as as a stream of two-byte 3 characters. The first byte is the high byte; the second byte is the low byte. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARCHAR`values. The JDBC driver will do any necessary conversion from the database format into Unicode. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`InputStream.available`is called, whether there is data available or not. <br /> | | [InputStream](../java.io/InputStream.md)! | [getUnicodeStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Retrieves the value of the designated column in the current row of this`ResultSet`object as a stream of two-byte Unicode characters. The first byte is the high byte; the second byte is the low byte. The value can then be read in chunks from the stream. This method is particularly suitable for retrieving large`LONGVARCHAR`values. The JDBC technology-enabled driver will do any necessary conversion from the database format into Unicode. **Note:** All the data in the returned stream must be read prior to getting the value of any other column. The next call to a getter method implicitly closes the stream. Also, a stream may return`0`when the method`InputStream.available`is called, whether there is data available or not. <br /> | | [SQLWarning](../java.sql/SQLWarning.md)! | [getWarnings](../java.sql/ResultSet.md))`()` <br /> Retrieves the first warning reported by calls on this`ResultSet`object. Subsequent warnings on this`ResultSet`object will be chained to the`SQLWarning`object that this method returns. The warning chain is automatically cleared each time a new row is read. This method may not be called on a`ResultSet`object that has been closed; doing so will cause an`SQLException`to be thrown. **Note:** This warning chain only covers warnings caused by`ResultSet`methods. Any warning caused by`Statement`methods (such as reading OUT parameters) will be chained on the`Statement`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [insertRow](../java.sql/ResultSet.md))`()` <br /> Inserts the contents of the insert row into this`ResultSet`object and into the database. The cursor must be on the insert row when this method is called. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAfterLast](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the cursor is after the last row in this`ResultSet`object. **Note:** Support for the`isAfterLast`method is optional for`ResultSet`s with a result set type of`TYPE_FORWARD_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBeforeFirst](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the cursor is before the first row in this`ResultSet`object. **Note:** Support for the`isBeforeFirst`method is optional for`ResultSet`s with a result set type of`TYPE_FORWARD_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../java.sql/ResultSet.md))`()` <br /> Retrieves whether this`ResultSet`object has been closed. A`ResultSet`is closed if the method close has been called on it, or if it is automatically closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFirst](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the cursor is on the first row of this`ResultSet`object. **Note:** Support for the`isFirst`method is optional for`ResultSet`s with a result set type of`TYPE_FORWARD_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLast](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the cursor is on the last row of this`ResultSet`object.**Note:** Calling the method`isLast`may be expensive because the JDBC driver might need to fetch ahead one row in order to determine whether the current row is the last row in the result set. **Note:** Support for the`isLast`method is optional for`ResultSet`s with a result set type of`TYPE_FORWARD_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [last](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the last row in this`ResultSet`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [moveToCurrentRow](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the remembered cursor position, usually the current row. This method has no effect if the cursor is not on the insert row. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [moveToInsertRow](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the insert row. The current cursor position is remembered while the cursor is positioned on the insert row. The insert row is a special row associated with an updatable result set. It is essentially a buffer where a new row may be constructed by calling the updater methods prior to inserting the row into the result set. Only the updater, getter, and`insertRow`methods may be called when the cursor is on the insert row. All of the columns in a result set must be given a value each time this method is called before calling`insertRow`. An updater method must be called before a getter method can be called on a column value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [next](../java.sql/ResultSet.md))`()` <br /> Moves the cursor froward one row from its current position. A`ResultSet`cursor is initially positioned before the first row; the first call to the method`next`makes the first row the current row; the second call makes the second row the current row, and so on. When a call to the`next`method returns`false`, the cursor is positioned after the last row. Any invocation of a`ResultSet`method which requires a current row will result in a`SQLException`being thrown. If the result set type is`TYPE_FORWARD_ONLY`, it is vendor specified whether their JDBC driver implementation will return`false`or throw an`SQLException`on a subsequent call to`next`. If an input stream is open for the current row, a call to the method`next`will implicitly close it. A`ResultSet`object's warning chain is cleared when a new row is read. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previous](../java.sql/ResultSet.md))`()` <br /> Moves the cursor to the previous row in this`ResultSet`object. When a call to the`previous`method returns`false`, the cursor is positioned before the first row. Any invocation of a`ResultSet`method which requires a current row will result in a`SQLException`being thrown. If an input stream is open for the current row, a call to the method`previous`will implicitly close it. A`ResultSet`object's warning change is cleared when a new row is read. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [refreshRow](../java.sql/ResultSet.md))`()` <br /> Refreshes the current row with its most recent value in the database. This method cannot be called when the cursor is on the insert row. The`refreshRow`method provides a way for an application to explicitly tell the JDBC driver to refetch a row(s) from the database. An application may want to call`refreshRow`when caching or prefetching is being done by the JDBC driver to fetch the latest value of a row from the database. The JDBC driver may actually refresh multiple rows at once if the fetch size is greater than one. All values are refetched subject to the transaction isolation level and cursor sensitivity. If`refreshRow`is called after calling an updater method, but before calling the method`updateRow`, then the updates made to the row are lost. Calling the method`refreshRow`frequently will likely slow performance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [relative](../java.sql/ResultSet.md))`(`rows:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Moves the cursor a relative number of rows, either positive or negative. Attempting to move beyond the first/last row in the result set positions the cursor before/after the the first/last row. Calling`relative(0)`is valid, but does not change the cursor position. Note: Calling the method`relative(1)`is identical to calling the method`next()`and calling the method`relative(-1)`is identical to calling the method`previous()`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [rowDeleted](../java.sql/ResultSet.md))`()` <br /> Retrieves whether a row has been deleted. A deleted row may leave a visible "hole" in a result set. This method can be used to detect holes in a result set. The value returned depends on whether or not this`ResultSet`object can detect deletions. **Note:** Support for the`rowDeleted`method is optional with a result set concurrency of`CONCUR_READ_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [rowInserted](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the current row has had an insertion. The value returned depends on whether or not this`ResultSet`object can detect visible inserts. **Note:** Support for the`rowInserted`method is optional with a result set concurrency of`CONCUR_READ_ONLY` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [rowUpdated](../java.sql/ResultSet.md))`()` <br /> Retrieves whether the current row has been updated. The value returned depends on whether or not the result set can detect updates. **Note:** Support for the`rowUpdated`method is optional with a result set concurrency of`CONCUR_READ_ONLY` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchDirection](../java.sql/ResultSet.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives a hint as to the direction in which the rows in this`ResultSet`object will be processed. The initial value is determined by the`Statement`object that produced this`ResultSet`object. The fetch direction may be changed at any time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchSize](../java.sql/ResultSet.md))`(`rows:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives the JDBC driver a hint as to the number of rows that should be fetched from the database when more rows are needed for this`ResultSet`object. If the fetch size specified is zero, the JDBC driver ignores the value and is free to make its own best guess as to what the fetch size should be. The default value is set by the`Statement`object that created the result set. The fetch size may be changed at any time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateArray](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Array](../java.sql/Array.md)!`)` <br /> Updates the designated column with a`java.sql.Array`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateArray](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Array](../java.sql/Array.md)!`)` <br /> Updates the designated column with a`java.sql.Array`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column with an ascii stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateAsciiStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an ascii stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with an ascii stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column with an ascii stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateAsciiStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an ascii stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateAsciiStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with an ascii stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBigDecimal](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` <br /> Updates the designated column with a`java.math.BigDecimal`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBigDecimal](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` <br /> Updates the designated column with a`java.sql.BigDecimal`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column with a binary stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateBinaryStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with a binary stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a binary stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column with a binary stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateBinaryStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with a binary stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBinaryStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a binary stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column using the given input stream. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateBlob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given input stream, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Blob](../java.sql/Blob.md)!`)` <br /> Updates the designated column with a`java.sql.Blob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`)` <br /> Updates the designated column using the given input stream. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateBlob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](../java.io/InputStream.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given input stream, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBlob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Blob](../java.sql/Blob.md)!`)` <br /> Updates the designated column with a`java.sql.Blob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBoolean](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Updates the designated column with a`boolean`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBoolean](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Updates the designated column with a`boolean`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateByte](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Updates the designated column with a`byte`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateByte](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Updates the designated column with a`byte`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBytes](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Updates the designated column with a`byte`array value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateBytes](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Updates the designated column with a byte array value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column with a character stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column with a character stream value. The data will be read from the stream as needed until end-of-stream is reached. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column using the given`Reader`object. The data will be read from the stream as needed until end-of-stream is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Clob](../java.sql/Clob.md)!`)` <br /> Updates the designated column with a`java.sql.Clob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column using the given`Reader`object. The data will be read from the stream as needed until end-of-stream is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Clob](../java.sql/Clob.md)!`)` <br /> Updates the designated column with a`java.sql.Clob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDate](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](../java.sql/Date.md)!`)` <br /> Updates the designated column with a`java.sql.Date`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDate](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Date](../java.sql/Date.md)!`)` <br /> Updates the designated column with a`java.sql.Date`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDouble](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Updates the designated column with a`double`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDouble](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Updates the designated column with a`double`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateFloat](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Updates the designated column with a`float`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateFloat](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Updates the designated column with a`float `value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateInt](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an`int`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateInt](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an`int`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateLong](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a`long`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateLong](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a`long`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column with a character stream value. The data will be read from the stream as needed until end-of-stream is reached. The driver does the necessary conversion from Java character format to the national character set in the database. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateNCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNCharacterStream](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The driver does the necessary conversion from Java character format to the national character set in the database. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column with a character stream value. The data will be read from the stream as needed until end-of-stream is reached. The driver does the necessary conversion from Java character format to the national character set in the database. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateNCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNCharacterStream](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column with a character stream value, which will have the specified number of bytes. The driver does the necessary conversion from Java character format to the national character set in the database. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column using the given`Reader`The data will be read from the stream as needed until end-of-stream is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateNClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nClob:` ` [NClob](../java.sql/NClob.md)!`)` <br /> Updates the designated column with a`java.sql.NClob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`)` <br /> Updates the designated column using the given`Reader`object. The data will be read from the stream as needed until end-of-stream is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`updateNClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](../java.io/Reader.md)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Updates the designated column using the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The JDBC driver will do any necessary conversion from UNICODE to the database char format. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNClob](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `nClob:` ` [NClob](../java.sql/NClob.md)!`)` <br /> Updates the designated column with a`java.sql.NClob`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNString](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Updates the designated column with a`String`value. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNString](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `nString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Updates the designated column with a`String`value. It is intended for use when updating`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNull](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with a`null`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateNull](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Updates the designated column with a`null`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateObject](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Updates the designated column with an`Object`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateObject](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `scaleOrLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an`Object`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. If the second argument is an`InputStream`then the stream must contain the number of bytes specified by scaleOrLength. If the second argument is a`Reader`then the reader must contain the number of characters specified by scaleOrLength. If these conditions are not true the driver will generate a`SQLException`when the statement is executed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateObject](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Updates the designated column with an`Object`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateObject](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `scaleOrLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the designated column with an`Object`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. If the second argument is an`InputStream`then the stream must contain the number of bytes specified by scaleOrLength. If the second argument is a`Reader`then the reader must contain the number of characters specified by scaleOrLength. If these conditions are not true the driver will generate a`SQLException`when the statement is executed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateRef](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Ref](../java.sql/Ref.md)!`)` <br /> Updates the designated column with a`java.sql.Ref`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateRef](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Ref](../java.sql/Ref.md)!`)` <br /> Updates the designated column with a`java.sql.Ref`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateRow](../java.sql/ResultSet.md))`()` <br /> Updates the underlying database with the new contents of the current row of this`ResultSet`object. This method cannot be called when the cursor is on the insert row. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateRowId](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [RowId](../java.sql/RowId.md)!`)` <br /> Updates the designated column with a`RowId`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateRowId](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [RowId](../java.sql/RowId.md)!`)` <br /> Updates the designated column with a`RowId`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSQLXML](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xmlObject:` ` [SQLXML](../java.sql/SQLXML.md)!`)` <br /> Updates the designated column with a`java.sql.SQLXML`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateSQLXML](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `xmlObject:` ` [SQLXML](../java.sql/SQLXML.md)!`)` <br /> Updates the designated column with a`java.sql.SQLXML`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateShort](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Updates the designated column with a`short`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateShort](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Updates the designated column with a`short`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateString](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Updates the designated column with a`String`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateString](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Updates the designated column with a`String`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTime](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](../java.sql/Time.md)!`)` <br /> Updates the designated column with a`java.sql.Time`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTime](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Time](../java.sql/Time.md)!`)` <br /> Updates the designated column with a`java.sql.Time`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTimestamp](../java.sql/ResultSet.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`)` <br /> Updates the designated column with a`java.sql.Timestamp`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateTimestamp](../java.sql/ResultSet.md))`(`columnLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Timestamp](../java.sql/Timestamp.md)!`)` <br /> Updates the designated column with a`java.sql.Timestamp`value. The updater methods are used to update column values in the current row or the insert row. The updater methods do not update the underlying database; instead the`updateRow`or`insertRow`methods are called to update the database. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasNull](../java.sql/ResultSet.md))`()` <br /> Reports whether the last column read had a value of SQL`NULL`. Note that you must first call one of the getter methods on a column to try to read its value and then call the method`wasNull`to see if the value read was SQL`NULL`. <br /> | ||
| From class [Wrapper](../java.sql/Wrapper.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Public methods

### addRowSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addRowSetListener(listener: RowSetListener!): Unit
```

Registers the given listener so that it will be notified of events that occur on this`RowSet`object.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [RowSetListener](RowSetListener.md)!:a component that has implemented the`RowSetListener`interface and wants to be notified when events occur on this`RowSet`object |

**See Also**

- [#removeRowSetListener](RowSet.md)) 

### clearParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearParameters(): Unit
```

Clears the parameters set for this`RowSet`object's command.

In general, parameter values remain in force for repeated use of a`RowSet`object. Setting a parameter value automatically clears its previous value. However, in some cases it is useful to immediately release the resources used by the current parameter values, which can be done by calling the method`clearParameters`.

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun execute(): Unit
```

Fills this`RowSet`object with data.

The`execute`method may use the following properties to create a connection for reading data: url, data source name, user name, password, transaction isolation, and type map. The`execute`method may use the following properties to create a statement to execute a command: command, read only, maximum field size, maximum rows, escape processing, and query timeout.

If the required properties have not been set, an exception is thrown. If this method is successful, the current contents of the rowset are discarded and the rowset's metadata is also (re)set. If there are outstanding updates, they are ignored.

If this`RowSet`object does not maintain a continuous connection with its source of data, it may use a reader (a`RowSetReader`object) to fill itself with data. In this case, a reader will have been registered with this`RowSet`object, and the method`execute`will call on the reader's`readData`method as part of its implementation.

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or any of the properties necessary for making a connection and creating a statement have not been set |

### getCommand

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCommand(): String!
```

Retrieves this`RowSet`object's command property. The command property contains a command string, which must be an SQL query, that can be executed to fill the rowset with data. The default value is`null`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the command string; may be`null` |

**See Also**

- [#setCommand](RowSet.md)) 

### getDataSourceName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDataSourceName(): String!
```

Retrieves the logical name that identifies the data source for this`RowSet`object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a data source name |

**See Also**

- [#setDataSourceName](RowSet.md))
- [#setUrl](RowSet.md)) 

### getEscapeProcessing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEscapeProcessing(): Boolean
```

Retrieves whether escape processing is enabled for this`RowSet`object. If escape scanning is enabled, which is the default, the driver will do escape substitution before sending an SQL statement to the database.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if escape processing is enabled;`false`if it is disabled |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setEscapeProcessing](RowSet.md)) 

### getMaxFieldSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxFieldSize(): Int
```

Retrieves the maximum number of bytes that may be returned for certain column values. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARYBINARY`,`CHAR`,`VARCHAR`,`LONGVARCHAR`,`NCHAR`and`NVARCHAR`columns. If the limit is exceeded, the excess data is silently discarded.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current maximum column size limit; zero means that there is no limit |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setMaxFieldSize](RowSet.md)) 

### getMaxRows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMaxRows(): Int
```

Retrieves the maximum number of rows that this`RowSet`object can contain. If the limit is exceeded, the excess rows are silently dropped.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current maximum number of rows that this`RowSet`object can contain; zero means unlimited |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setMaxRows](RowSet.md)) 

### getPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPassword(): String!
```

Retrieves the password used to create a database connection. The password property is set at run time before calling the method`execute`. It is not usually part of the serialized state of a`RowSet`object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the password for making a database connection |

**See Also**

- [#setPassword](RowSet.md)) 

### getQueryTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getQueryTimeout(): Int
```

Retrieves the maximum number of seconds the driver will wait for a statement to execute. If this limit is exceeded, an`SQLException`is thrown.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current query timeout limit in seconds; zero means unlimited |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setQueryTimeout](RowSet.md)) 

### getTransactionIsolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTransactionIsolation(): Int
```

Retrieves the transaction isolation level set for this`RowSet`object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the transaction isolation level; one of`Connection.TRANSACTION_READ_UNCOMMITTED`,`Connection.TRANSACTION_READ_COMMITTED`,`Connection.TRANSACTION_REPEATABLE_READ`, or`Connection.TRANSACTION_SERIALIZABLE` |

**See Also**

- [#setTransactionIsolation](RowSet.md)) 

### getTypeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTypeMap(): MutableMap<String!, Class<*>!>!
```

Retrieves the`Map`object associated with this`RowSet`object, which specifies the custom mapping of SQL user-defined types, if any. The default is for the type map to be empty.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](../java.lang/Class.md)<*>!>! | a`java.util.Map`object containing the names of SQL user-defined types and the Java classes to which they are to be mapped |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setTypeMap](RowSet.md)) 

### getUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUrl(): String!
```

Retrieves the url property this`RowSet`object will use to create a connection if it uses the`DriverManager`instead of a`DataSource`object to establish the connection. The default value is`null`.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string url |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#setUrl](RowSet.md)) 

### getUsername

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUsername(): String!
```

Retrieves the username used to create a database connection for this`RowSet`object. The username property is set at run time before calling the method`execute`. It is not usually part of the serialized state of a`RowSet`object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the username property |

**See Also**

- [#setUsername](RowSet.md)) 

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(): Boolean
```

Retrieves whether this`RowSet`object is read-only. If updates are possible, the default is for a rowset to be updatable.

Attempts to update a read-only rowset will result in an`SQLException`being thrown.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`RowSet`object is read-only;`false`if it is updatable |

**See Also**

- [#setReadOnly](RowSet.md)) 

### removeRowSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeRowSetListener(listener: RowSetListener!): Unit
```

Removes the specified listener from the list of components that will be notified when an event occurs on this`RowSet`object.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [RowSetListener](RowSetListener.md)!:a component that has been registered as a listener for this`RowSet`object |

**See Also**

- [#addRowSetListener](RowSet.md)) 

### setArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setArray(
    i: Int, 
    x: Array!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`Array`value. The driver will convert this to the`ARRAY`value that the`Array`object represents before sending it to the database.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Array](../java.sql/Array.md)!:an object representing an SQL array |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterIndex: Int, 
    x: InputStream!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given input stream. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setAsciiStream`which takes a length parameter.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](../java.io/InputStream.md)!:the Java input stream that contains the ASCII parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.io.InputStream`value. It may be more practical to send a very large ASCII value via a`java.io.InputStream`rather than as a`LONGVARCHAR`parameter. The driver will read the data from the stream as needed until it reaches end-of-file.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](../java.io/InputStream.md)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterName: String!, 
    x: InputStream!
): Unit
```

Sets the designated parameter to the given input stream. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setAsciiStream`which takes a length parameter.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](../java.io/InputStream.md)!:the Java input stream that contains the ASCII parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterName: String!, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](../java.io/InputStream.md)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBigDecimal(
    parameterIndex: Int, 
    x: BigDecimal!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.math.BigDeciaml`value. The driver converts this to an SQL`NUMERIC`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [BigDecimal](../java.math/BigDecimal.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setBigDecimal

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBigDecimal(
    parameterName: String!, 
    x: BigDecimal!
): Unit
```

Sets the designated parameter to the given`java.math.BigDecimal`value. The driver converts this to an SQL`NUMERIC`value when it sends it to the database.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [BigDecimal](../java.math/BigDecimal.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterIndex: Int, 
    x: InputStream!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given input stream. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBinaryStream`which takes a length parameter.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](../java.io/InputStream.md)!:the java input stream which contains the binary parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.io.InputStream`value. It may be more practical to send a very large binary value via a`java.io.InputStream`rather than as a`LONGVARBINARY`parameter. The driver will read the data from the stream as needed until it reaches end-of-file.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](../java.io/InputStream.md)!:the java input stream which contains the binary parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterName: String!, 
    x: InputStream!
): Unit
```

Sets the designated parameter to the given input stream. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBinaryStream`which takes a length parameter.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](../java.io/InputStream.md)!:the java input stream which contains the binary parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterName: String!, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](../java.io/InputStream.md)!:the java input stream which contains the binary parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterIndex: Int, 
    inputStream: InputStream!
): Unit
```

Sets the designated parameter to a`InputStream`object. This method differs from the`setBinaryStream (int, InputStream)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARBINARY`or a`BLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBlob`which takes a length parameter.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `inputStream` | [InputStream](../java.io/InputStream.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed`PreparedStatement`or if parameterIndex does not correspond to a parameter marker in the SQL statement, |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterIndex: Int, 
    inputStream: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to a`InputStream`object. The inputstream must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setBinaryStream (int, InputStream, int)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARBINARY`or a`BLOB`

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `inputStream` | [InputStream](../java.io/InputStream.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed`PreparedStatement`, if parameterIndex does not correspond to a parameter marker in the SQL statement, if the length specified is less than zero or if the number of bytes in the inputstream does not match the specfied length. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    i: Int, 
    x: Blob!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`Blob`value. The driver will convert this to the`BLOB`value that the`Blob`object represents before sending it to the database.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Blob](../java.sql/Blob.md)!:an object representing a BLOB |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterName: String!, 
    inputStream: InputStream!
): Unit
```

Sets the designated parameter to a`InputStream`object. This method differs from the`setBinaryStream (int, InputStream)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be send to the server as a`LONGVARBINARY`or a`BLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBlob`which takes a length parameter.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `inputStream` | [InputStream](../java.io/InputStream.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterName: String!, 
    inputStream: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to a`InputStream`object. The`inputstream`must contain the number of characters specified by length, otherwise a`SQLException`will be generated when the`CallableStatement`is executed. This method differs from the`setBinaryStream (int, InputStream, int)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARBINARY`or a`BLOB`

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set the second is 2, ... |
| `inputStream` | [InputStream](../java.io/InputStream.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement, or if the length specified is less than zero; if the number of bytes in the inputstream does not match the specfied length; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterName: String!, 
    x: Blob!
): Unit
```

Sets the designated parameter to the given`java.sql.Blob`object. The driver converts this to an SQL`BLOB`value when it sends it to the database.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Blob](../java.sql/Blob.md)!:a`Blob`object that maps an SQL`BLOB`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBoolean(
    parameterIndex: Int, 
    x: Boolean
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`boolean`value. The driver converts this to an SQL`BIT`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setBoolean

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBoolean(
    parameterName: String!, 
    x: Boolean
): Unit
```

Sets the designated parameter to the given Java`boolean`value. The driver converts this to an SQL`BIT`or`BOOLEAN`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setByte(
    parameterIndex: Int, 
    x: Byte
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`byte`value. The driver converts this to an SQL`TINYINT`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setByte

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setByte(
    parameterName: String!, 
    x: Byte
): Unit
```

Sets the designated parameter to the given Java`byte`value. The driver converts this to an SQL`TINYINT`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBytes(
    parameterIndex: Int, 
    x: ByteArray!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java array of`byte`values. Before sending it to the database, the driver converts this to an SQL`VARBINARY`or`LONGVARBINARY`value, depending on the argument's size relative to the driver's limits on`VARBINARY`values.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setBytes

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBytes(
    parameterName: String!, 
    x: ByteArray!
): Unit
```

Sets the designated parameter to the given Java array of bytes. The driver converts this to an SQL`VARBINARY`or`LONGVARBINARY`(depending on the argument's size relative to the driver's limits on`VARBINARY`values) when it sends it to the database.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterIndex: Int, 
    reader: Reader!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`Reader`object. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setCharacterStream`which takes a length parameter.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:the`java.io.Reader`object that contains the Unicode data |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterIndex: Int, 
    reader: Reader!, 
    length: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.io.Reader`value. It may be more practical to send a very large UNICODE value via a`java.io.Reader`rather than as a`LONGVARCHAR`parameter. The driver will read the data from the stream as needed until it reaches end-of-file.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:the`Reader`object that contains the UNICODE data to be set |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in the stream |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterName: String!, 
    reader: Reader!
): Unit
```

Sets the designated parameter to the given`Reader`object. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setCharacterStream`which takes a length parameter.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `reader` | [Reader](../java.io/Reader.md)!:the`java.io.Reader`object that contains the Unicode data |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterName: String!, 
    reader: Reader!, 
    length: Int
): Unit
```

Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `reader` | [Reader](../java.io/Reader.md)!:the`java.io.Reader`object that contains the UNICODE data used as the designated parameter |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in the stream |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterIndex: Int, 
    reader: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARCHAR`or a`CLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setClob`which takes a length parameter.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed`PreparedStatement`or if parameterIndex does not correspond to a parameter marker in the SQL statement |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterIndex: Int, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The reader must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARCHAR`or a`CLOB`

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed`PreparedStatement`, if parameterIndex does not correspond to a parameter marker in the SQL statement, or if the length specified is less than zero. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    i: Int, 
    x: Clob!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`Clob`value. The driver will convert this to the`CLOB`value that the`Clob`object represents before sending it to the database.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Clob](../java.sql/Clob.md)!:an object representing a CLOB |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterName: String!, 
    reader: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be send to the server as a`LONGVARCHAR`or a`CLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setClob`which takes a length parameter.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterName: String!, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The`reader`must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`CallableStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be send to the server as a`LONGVARCHAR`or a`CLOB`

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the length specified is less than zero; a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterName: String!, 
    x: Clob!
): Unit
```

Sets the designated parameter to the given`java.sql.Clob`object. The driver converts this to an SQL`CLOB`value when it sends it to the database.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Clob](../java.sql/Clob.md)!:a`Clob`object that maps an SQL`CLOB`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setCommand

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCommand(cmd: String!): Unit
```

Sets this`RowSet`object's command property to the given SQL query. This property is optional when a rowset gets its data from a data source that does not support commands, such as a spreadsheet.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cmd` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the SQL query that will be used to get the data for this`RowSet`object; may be`null` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getCommand](RowSet.md)) 

### setConcurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setConcurrency(concurrency: Int): Unit
```

Sets the concurrency of this`RowSet`object to the given concurrency level. This method is used to change the concurrency level of a rowset, which is by default`ResultSet.CONCUR_READ_ONLY`

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `concurrency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the`ResultSet`constants specifying a concurrency level:`ResultSet.CONCUR_READ_ONLY`or`ResultSet.CONCUR_UPDATABLE` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.ResultSet#getConcurrency](../java.sql/ResultSet.md)) 

### setDataSourceName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDataSourceName(name: String!): Unit
```

Sets the data source name property for this`RowSet`object to the given`String`.

The value of the data source name property can be used to do a lookup of a`DataSource`object that has been registered with a naming service. After being retrieved, the`DataSource`object can be used to create a connection to the data source that it represents.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the logical name of the data source for this`RowSet`object; may be`null` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getDataSourceName](RowSet.md)) 

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterIndex: Int, 
    x: Date!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Date`value. The driver converts this to an SQL`DATE`value before sending it to the database, using the default`java.util.Calendar`to calculate the date.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Date](../java.sql/Date.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterIndex: Int, 
    x: Date!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Date`value. The driver will convert this to an SQL`DATE`value, using the given`java.util.Calendar`object to calculate the date.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Date](../java.sql/Date.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`java.util.Calendar`object to use for calculating the date |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setDate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterName: String!, 
    x: Date!
): Unit
```

Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. The driver converts this to an SQL`DATE`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Date](../java.sql/Date.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setDate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterName: String!, 
    x: Date!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`DATE`value, which the driver then sends to the database. With a a`Calendar`object, the driver can calculate the date taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Date](../java.sql/Date.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`Calendar`object the driver will use to construct the date |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDouble(
    parameterIndex: Int, 
    x: Double
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`double`value. The driver converts this to an SQL`DOUBLE`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setDouble

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDouble(
    parameterName: String!, 
    x: Double
): Unit
```

Sets the designated parameter to the given Java`double`value. The driver converts this to an SQL`DOUBLE`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setEscapeProcessing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEscapeProcessing(enable: Boolean): Unit
```

Sets escape processing for this`RowSet`object on or off. If escape scanning is on (the default), the driver will do escape substitution before sending an SQL statement to the database.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable escape processing;`false`to disable it |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getEscapeProcessing](RowSet.md)) 

### setFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFloat(
    parameterIndex: Int, 
    x: Float
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`float`value. The driver converts this to an SQL`REAL`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setFloat

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFloat(
    parameterName: String!, 
    x: Float
): Unit
```

Sets the designated parameter to the given Java`float`value. The driver converts this to an SQL`FLOAT`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInt(
    parameterIndex: Int, 
    x: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`int`value. The driver converts this to an SQL`INTEGER`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setInt

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInt(
    parameterName: String!, 
    x: Int
): Unit
```

Sets the designated parameter to the given Java`int`value. The driver converts this to an SQL`INTEGER`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLong(
    parameterIndex: Int, 
    x: Long
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`long`value. The driver converts this to an SQL`BIGINT`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setLong

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLong(
    parameterName: String!, 
    x: Long
): Unit
```

Sets the designated parameter to the given Java`long`value. The driver converts this to an SQL`BIGINT`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setMaxFieldSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMaxFieldSize(max: Int): Unit
```

Sets the maximum number of bytes that can be returned for a column value to the given number of bytes. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARYBINARY`,`CHAR`,`VARCHAR`,`LONGVARCHAR`,`NCHAR`and`NVARCHAR`columns. If the limit is exceeded, the excess data is silently discarded. For maximum portability, use values greater than 256.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new max column size limit in bytes; zero means unlimited |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getMaxFieldSize](RowSet.md)) 

### setMaxRows

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMaxRows(max: Int): Unit
```

Sets the maximum number of rows that this`RowSet`object can contain to the specified number. If the limit is exceeded, the excess rows are silently dropped.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new maximum number of rows; zero means unlimited |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getMaxRows](RowSet.md)) 

### setNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNCharacterStream(
    parameterIndex: Int, 
    value: Reader!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNCharacterStream`which takes a length parameter.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the first parameter is 1, the second is 2, ... |
| `value` | [Reader](../java.io/Reader.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur ; if a database access error occurs; or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNCharacterStream(
    parameterIndex: Int, 
    value: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the first parameter is 1, the second is 2, ... |
| `value` | [Reader](../java.io/Reader.md)!:the parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur ; or if a database access error occurs |

### setNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNCharacterStream(
    parameterName: String!, 
    value: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNCharacterStream`which takes a length parameter.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `value` | [Reader](../java.io/Reader.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur ; if a database access error occurs; or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNCharacterStream(
    parameterName: String!, 
    value: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the column to be set |
| `value` | [Reader](../java.io/Reader.md)!:the parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; or if a database access error occurs |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterIndex: Int, 
    reader: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGNVARCHAR`or a`NCLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNClob`which takes a length parameter.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterIndex: Int, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The reader must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGNVARCHAR`or a`NCLOB`

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the length specified is less than zero; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterIndex: Int, 
    value: NClob!
): Unit
```

Sets the designated parameter to a`java.sql.NClob`object. The driver converts this to a SQL`NCLOB`value when it sends it to the database.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the first parameter is 1, the second is 2, ... |
| `value` | [NClob](../java.sql/NClob.md)!:the parameter value |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur ; or if a database access error occurs |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterName: String!, 
    reader: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be send to the server as a`LONGNVARCHAR`or a`NCLOB`

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNClob`which takes a length parameter.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterName: String!, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to a`Reader`object. The`reader`must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`CallableStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be send to the server as a`LONGNVARCHAR`or a`NCLOB`

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set |
| `reader` | [Reader](../java.io/Reader.md)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |
| --- | --- |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the length specified is less than zero; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNClob(
    parameterName: String!, 
    value: NClob!
): Unit
```

Sets the designated parameter to a`java.sql.NClob`object. The object implements the`java.sql.NClob`interface. This`NClob`object maps to a SQL`NCLOB`.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the column to be set |
| `value` | [NClob](../java.sql/NClob.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; or if a database access error occurs |

### setNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNString(
    parameterIndex: Int, 
    value: String!
): Unit
```

Sets the designated paramter to the given`String`object. The driver converts this to a SQL`NCHAR`or`NVARCHAR`or`LONGNVARCHAR`value (depending on the argument's size relative to the driver's limits on`NVARCHAR`values) when it sends it to the database.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the first parameter is 1, the second is 2, ... |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur ; or if a database access error occurs |

### setNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNString(
    parameterName: String!, 
    value: String!
): Unit
```

Sets the designated paramter to the given`String`object. The driver converts this to a SQL`NCHAR`or`NVARCHAR`or`LONGNVARCHAR`

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the column to be set |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; or if a database access error occurs |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterIndex: Int, 
    sqlType: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's SQL command to SQL`NULL`.

**Note:**You must specify the parameter's SQL type.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a SQL type code defined by`java.sql.Types` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    paramIndex: Int, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Sets the designated parameter in this`RowSet`object's SQL command to SQL`NULL`. This version of the method`setNull`should be used for SQL user-defined types (UDTs) and`REF`type parameters. Examples of UDTs include:`STRUCT`,`DISTINCT`,`JAVA_OBJECT`, and named array types.

**Note:** To be portable, applications must give the SQL type code and the fully qualified SQL type name when specifying a NULL UDT or`REF`parameter. In the case of a UDT, the name is the type name of the parameter itself. For a`REF`parameter, the name is the type name of the referenced type. If a JDBC driver does not need the type code or type name information, it may ignore it. Although it is intended for UDT and`REF`parameters, this method may be used to set a null parameter of any JDBC type. If the parameter does not have a user-defined or`REF`type, the typeName parameter is ignored.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paramIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from`java.sql.Types` |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully qualified name of an SQL UDT or the type name of the SQL structured type being referenced by a`REF`type; ignored if the parameter is not a UDT or`REF`type |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setNull

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterName: String!, 
    sqlType: Int
): Unit
```

Sets the designated parameter to SQL`NULL`.

**Note:**You must specify the parameter's SQL type.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type code defined in`java.sql.Types` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNull

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterName: String!, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Sets the designated parameter to SQL`NULL`. This version of the method`setNull`should be used for user-defined types and REF type parameters. Examples of user-defined types include: STRUCT, DISTINCT, JAVA_OBJECT, and named array types.

**Note:**To be portable, applications must give the SQL type code and the fully-qualified SQL type name when specifying a NULL user-defined or REF parameter. In the case of a user-defined type the name is the type name of the parameter itself. For a REF parameter, the name is the type name of the referenced type. If a JDBC driver does not need the type code or type name information, it may ignore it. Although it is intended for user-defined and Ref parameters, this method may be used to set a null parameter of any JDBC type. If the parameter does not have a user-defined or REF type, the given typeName is ignored.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from`java.sql.Types` |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully-qualified name of an SQL user-defined type; ignored if the parameter is not a user-defined type or SQL`REF`value |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterIndex: Int, 
    x: Any!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with a Java`Object`. For integral values, the`java.lang`equivalent objects should be used.

The JDBC specification provides a standard mapping from Java Object types to SQL types. The driver will convert the given Java object to its standard SQL mapping before sending it to the database.

Note that this method may be used to pass datatabase-specific abstract data types by using a driver-specific Java type. If the object is of a class implementing`SQLData`, the rowset should call the method`SQLData.writeSQL`to write the object to an`SQLOutput`data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

<br />

An exception is thrown if there is an ambiguity, for example, if the object is of a class implementing more than one of these interfaces.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object containing the input parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterIndex: Int, 
    x: Any!, 
    targetSqlType: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command with a Java`Object`. For integral values, the`java.lang`equivalent objects should be used. This method is like`setObject`above, but the scale used is the scale of the second parameter. Scalar values have a scale of zero. Literal values have the scale present in the literal.

Even though it is supported, it is not recommended that this method be called with floating point input values.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in`java.sql.Types`) to be sent to the database |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterIndex: Int, 
    x: Any!, 
    targetSqlType: Int, 
    scaleOrLength: Int
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given Java`Object`. For integral values, the`java.lang`equivalent objects should be used (for example, an instance of the class`Integer`for an`int`). If the second argument is an`InputStream`then the stream must contain the number of bytes specified by scaleOrLength. If the second argument is a`Reader`then the reader must contain the number of characters specified \* by scaleOrLength. If these conditions are not true the driver will generate a`SQLException`when the prepared statement is executed.

The given Java object will be converted to the targetSqlType before being sent to the database.

If the object is of a class implementing`SQLData`, the rowset should call the method`SQLData.writeSQL`to write the object to an`SQLOutput`data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

<br />

Note that this method may be used to pass datatabase-specific abstract data types.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in`java.sql.Types`) to be sent to the database. The scale argument may further qualify this type. |
| --- | --- |
| `scaleOrLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for`java.sql.Types.DECIMAL`or`java.sql.Types.NUMERIC types`, this is the number of digits after the decimal point. For Java Object types`InputStream`and`Reader`, this is the length of the data in the stream or reader. For all other types, this value will be ignored. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Types](../java.sql/Types.md) 

### setObject

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterName: String!, 
    x: Any!
): Unit
```

Sets the value of the designated parameter with the given object. The second parameter must be of type`Object`; therefore, the`java.lang`equivalent objects should be used for built-in types.

The JDBC specification specifies a standard mapping from Java`Object`types to SQL types. The given argument will be converted to the corresponding SQL type before being sent to the database.

Note that this method may be used to pass datatabase- specific abstract data types, by using a driver-specific Java type. If the object is of a class implementing the interface`SQLData`, the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

This method throws an exception if there is an ambiguity, for example, if the object is of a class implementing more than one of the interfaces named above.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed`CallableStatement`or if the given`Object`parameter is ambiguous |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setObject

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterName: String!, 
    x: Any!, 
    targetSqlType: Int
): Unit
```

Sets the value of the designated parameter with the given object. This method is like the method`setObject`above, except that it assumes a scale of zero.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in java.sql.Types) to be sent to the database |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

### setObject

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterName: String!, 
    x: Any!, 
    targetSqlType: Int, 
    scale: Int
): Unit
```

Sets the value of the designated parameter with the given object. The second argument must be an object type; for integral values, the`java.lang`equivalent objects should be used.

The given Java object will be converted to the given targetSqlType before being sent to the database. If the object has a custom mapping (is of a class implementing the interface`SQLData`), the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

Note that this method may be used to pass datatabase- specific abstract data types.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in java.sql.Types) to be sent to the database. The scale argument may further qualify this type. |
| --- | --- |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for java.sql.Types.DECIMAL or java.sql.Types.NUMERIC types, this is the number of digits after the decimal point. For all other types, this value will be ignored. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](../java.sql/Types.md) 

### setPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPassword(password: String!): Unit
```

Sets the database password for this`RowSet`object to the given`String`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------|
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the password string |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getPassword](RowSet.md)) 

### setQueryTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setQueryTimeout(seconds: Int): Unit
```

Sets the maximum time the driver will wait for a statement to execute to the given number of seconds. If this limit is exceeded, an`SQLException`is thrown.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new query timeout limit in seconds; zero means that there is no limit |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getQueryTimeout](RowSet.md)) 

### setReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setReadOnly(value: Boolean): Unit
```

Sets whether this`RowSet`object is read-only to the given`boolean`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if read-only;`false`if updatable |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#isReadOnly](RowSet.md)) 

### setRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRef(
    i: Int, 
    x: Ref!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`Ref`value. The driver will convert this to the appropriate`REF(<structured-type>)`value.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Ref](../java.sql/Ref.md)!:an object representing data of an SQL`REF`type |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRowId(
    parameterIndex: Int, 
    x: RowId!
): Unit
```

Sets the designated parameter to the given`java.sql.RowId`object. The driver converts this to a SQL`ROWID`value when it sends it to the database

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [RowId](../java.sql/RowId.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRowId(
    parameterName: String!, 
    x: RowId!
): Unit
```

Sets the designated parameter to the given`java.sql.RowId`object. The driver converts this to a SQL`ROWID`when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [RowId](../java.sql/RowId.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSQLXML(
    parameterIndex: Int, 
    xmlObject: SQLXML!
): Unit
```

Sets the designated parameter to the given`java.sql.SQLXML`object. The driver converts this to an SQL`XML`value when it sends it to the database.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `xmlObject` | [SQLXML](../java.sql/SQLXML.md)!:a`SQLXML`object that maps an SQL`XML`value |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed result set, the`java.xml.transform.Result`,`Writer`or`OutputStream`has not been closed for the`SQLXML`object or if there is an error processing the XML value. The`getCause`method of the exception may provide a more detailed exception, for example, if the stream does not contain valid XML. |

### setSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSQLXML(
    parameterName: String!, 
    xmlObject: SQLXML!
): Unit
```

Sets the designated parameter to the given`java.sql.SQLXML`object. The driver converts this to an`SQL XML`value when it sends it to the database.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `xmlObject` | [SQLXML](../java.sql/SQLXML.md)!:a`SQLXML`object that maps an`SQL XML`value |

| Exceptions ||
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, this method is called on a closed result set, the`java.xml.transform.Result`,`Writer`or`OutputStream`has not been closed for the`SQLXML`object or if there is an error processing the XML value. The`getCause`method of the exception may provide a more detailed exception, for example, if the stream does not contain valid XML. |

### setShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShort(
    parameterIndex: Int, 
    x: Short
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`short`value. The driver converts this to an SQL`SMALLINT`value before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setShort

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShort(
    parameterName: String!, 
    x: Short
): Unit
```

Sets the designated parameter to the given Java`short`value. The driver converts this to an SQL`SMALLINT`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(
    parameterIndex: Int, 
    x: String!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given Java`String`value. Before sending it to the database, the driver converts this to an SQL`VARCHAR`or`LONGVARCHAR`value, depending on the argument's size relative to the driver's limits on`VARCHAR`values.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(
    parameterName: String!, 
    x: String!
): Unit
```

Sets the designated parameter to the given Java`String`value. The driver converts this to an SQL`VARCHAR`or`LONGVARCHAR`value (depending on the argument's size relative to the driver's limits on`VARCHAR`values) when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterIndex: Int, 
    x: Time!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Time`value. The driver converts this to an SQL`TIME`value before sending it to the database, using the default`java.util.Calendar`to calculate it.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Time](../java.sql/Time.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterIndex: Int, 
    x: Time!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Time`value. The driver will convert this to an SQL`TIME`value, using the given`java.util.Calendar`object to calculate it, before sending it to the database.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Time](../java.sql/Time.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`java.util.Calendar`object to use for calculating the time |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterName: String!, 
    x: Time!
): Unit
```

Sets the designated parameter to the given`java.sql.Time`value. The driver converts this to an SQL`TIME`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Time](../java.sql/Time.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterName: String!, 
    x: Time!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIME`value, which the driver then sends to the database. With a a`Calendar`object, the driver can calculate the time taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Time](../java.sql/Time.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`Calendar`object the driver will use to construct the time |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterIndex: Int, 
    x: Timestamp!
): Unit
```

Sets the designated parameter in this`RowSet`object's command to the given`java.sql.Timestamp`value. The driver converts this to an SQL`TIMESTAMP`value before sending it to the database, using the default`java.util.Calendar`to calculate it.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Timestamp](../java.sql/Timestamp.md)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterIndex: Int, 
    x: Timestamp!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter in this`RowSet`object's command with the given`java.sql.Timestamp`value. The driver will convert this to an SQL`TIMESTAMP`value, using the given`java.util.Calendar`object to calculate it, before sending it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Timestamp](../java.sql/Timestamp.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`java.util.Calendar`object to use for calculating the timestamp |
| --- | --- |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setTimestamp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterName: String!, 
    x: Timestamp!
): Unit
```

Sets the designated parameter to the given`java.sql.Timestamp`value. The driver converts this to an SQL`TIMESTAMP`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Timestamp](../java.sql/Timestamp.md)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTimestamp

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterName: String!, 
    x: Timestamp!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIMESTAMP`value, which the driver then sends to the database. With a a`Calendar`object, the driver can calculate the timestamp taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Timestamp](../java.sql/Timestamp.md)!:the parameter value |
| `cal` | [Calendar](../java.util/Calendar.md)!:the`Calendar`object the driver will use to construct the timestamp |
| --- | --- |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTransactionIsolation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTransactionIsolation(level: Int): Unit
```

Sets the transaction isolation level for this`RowSet`obejct.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the transaction isolation level; one of`Connection.TRANSACTION_READ_UNCOMMITTED`,`Connection.TRANSACTION_READ_COMMITTED`,`Connection.TRANSACTION_REPEATABLE_READ`, or`Connection.TRANSACTION_SERIALIZABLE` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getTransactionIsolation](RowSet.md)) 

### setType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setType(type: Int): Unit
```

Sets the type of this`RowSet`object to the given type. This method is used to change the type of a rowset, which is by default read-only and non-scrollable.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the`ResultSet`constants specifying a type:`ResultSet.TYPE_FORWARD_ONLY`,`ResultSet.TYPE_SCROLL_INSENSITIVE`, or`ResultSet.TYPE_SCROLL_SENSITIVE` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.ResultSet#getType](../java.sql/ResultSet.md)) 

### setTypeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTypeMap(map: MutableMap<String!, Class<*>!>!): Unit
```

Installs the given`java.util.Map`object as the default type map for this`RowSet`object. This type map will be used unless another type map is supplied as a method parameter.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](../java.lang/Class.md)\<\*\>!\>!:a`java.util.Map`object containing the names of SQL user-defined types and the Java classes to which they are to be mapped |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getTypeMap](RowSet.md)) 

### setURL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setURL(
    parameterIndex: Int, 
    x: URL!
): Unit
```

Sets the designated parameter to the given`java.net.URL`value. The driver converts this to an SQL`DATALINK`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [URL](../java.net/URL.md)!:the`java.net.URL`object to be set |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUrl(url: String!): Unit
```

Sets the URL this`RowSet`object will use when it uses the`DriverManager`to create a connection. Setting this property is optional. If a URL is used, a JDBC driver that accepts the URL must be loaded before the rowset is used to connect to a database. The rowset will use the URL internally to create a database connection when reading or writing data. Either a URL or a data source name is used to create a connection, whichever was set to non null value most recently.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string value; may be`null` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getUrl](RowSet.md)) 

### setUsername

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUsername(name: String!): Unit
```

Sets the username property for this`RowSet`object to the given`String`.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a user name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [#getUsername](RowSet.md))
