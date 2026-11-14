# PreparedStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreparedStatement

```
interface PreparedStatement : Statement
```

| [java.sql.PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#) |

| Known Direct Subclasses [CallableStatement](https://developer.android.com/reference/kotlin/java/sql/CallableStatement) |------------------------------------------------------------------------------------------------|------------------------------------------------------| | [CallableStatement](https://developer.android.com/reference/kotlin/java/sql/CallableStatement) | The interface used to execute SQL stored procedures. | |

An object that represents a precompiled SQL statement.

A SQL statement is precompiled and stored in a`PreparedStatement`object. This object can then be used to efficiently execute this statement multiple times.

**Note:** The setter methods (`setShort`,`setString`, and so on) for setting IN parameter values must specify types that are compatible with the defined SQL type of the input parameter. For instance, if the IN parameter has SQL type`INTEGER`, then the method`setInt`should be used.

If arbitrary parameter type conversions are required, the method`setObject`should be used with a target SQL type.

In the following example of setting a parameter,`con`represents an active connection: 

```kotlin
PreparedStatement pstmt = con.prepareStatement("UPDATE EMPLOYEES
                                      SET SALARY = ? WHERE ID = ?");
    pstmt.setBigDecimal(1, 153833.00)
    pstmt.setInt(2, 110592)
  
```

## Summary

| Inherited constants ||
|---|---|
| From class [Statement](https://developer.android.com/reference/kotlin/java/sql/Statement) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_ALL_RESULTS](https://developer.android.com/reference/kotlin/java/sql/Statement#CLOSE_ALL_RESULTS:kotlin.Int) <br /> The constant indicating that all`ResultSet`objects that have previously been kept open should be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_CURRENT_RESULT](https://developer.android.com/reference/kotlin/java/sql/Statement#CLOSE_CURRENT_RESULT:kotlin.Int) <br /> The constant indicating that the current`ResultSet`object should be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXECUTE_FAILED](https://developer.android.com/reference/kotlin/java/sql/Statement#EXECUTE_FAILED:kotlin.Int) <br /> The constant indicating that an error occured while executing a batch statement. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEEP_CURRENT_RESULT](https://developer.android.com/reference/kotlin/java/sql/Statement#KEEP_CURRENT_RESULT:kotlin.Int) <br /> The constant indicating that the current`ResultSet`object should not be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_GENERATED_KEYS](https://developer.android.com/reference/kotlin/java/sql/Statement#NO_GENERATED_KEYS:kotlin.Int) <br /> The constant indicating that generated keys should not be made available for retrieval. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETURN_GENERATED_KEYS](https://developer.android.com/reference/kotlin/java/sql/Statement#RETURN_GENERATED_KEYS:kotlin.Int) <br /> The constant indicating that generated keys should be made available for retrieval. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS_NO_INFO](https://developer.android.com/reference/kotlin/java/sql/Statement#SUCCESS_NO_INFO:kotlin.Int) <br /> The constant indicating that a batch statement executed successfully but that no count of the number of rows it affected is available. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#addBatch())`()` Adds a set of parameters to this`PreparedStatement`object's batch of commands. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearParameters](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#clearParameters())`()` Clears the current parameter values immediately. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#execute())`()` Executes the SQL statement in this`PreparedStatement`object, which may be any kind of SQL statement. |
| abstract [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [executeQuery](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#executeQuery())`()` Executes the SQL query in this`PreparedStatement`object and returns the`ResultSet`object generated by the query. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#executeUpdate())`()` Executes the SQL statement in this`PreparedStatement`object, which must be an SQL Data Manipulation Language (DML) statement, such as`INSERT`,`UPDATE`or`DELETE`; or an SQL statement that returns nothing, such as a DDL statement. |
| abstract [ResultSetMetaData](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData)! | [getMetaData](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#getMetaData())`()` Retrieves a`ResultSetMetaData`object that contains information about the columns of the`ResultSet`object that will be returned when this`PreparedStatement`object is executed. |
| abstract [ParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/ParameterMetaData)! | [getParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#getParameterMetaData())`()` Retrieves the number, types and properties of this`PreparedStatement`object's parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArray](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setArray(kotlin.Int,%20java.sql.Array))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Array](https://developer.android.com/reference/kotlin/java/sql/Array)!`)` Sets the designated parameter to the given`java.sql.Array`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBigDecimal](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBigDecimal(kotlin.Int,%20java.math.BigDecimal))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Sets the designated parameter to the given`java.math.BigDecimal`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.sql.Blob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)!`)` Sets the designated parameter to the given`java.sql.Blob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBoolean(kotlin.Int,%20kotlin.Boolean))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the designated parameter to the given Java`boolean`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setByte(kotlin.Int,%20kotlin.Byte))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the designated parameter to the given Java`byte`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBytes](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBytes(kotlin.Int,%20kotlin.ByteArray))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the designated parameter to the given Java array of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to the given`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given`Reader`object, which is the given number of characters long. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given`Reader`object, which is the given number of characters long. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.sql.Clob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)!`)` Sets the designated parameter to the given`java.sql.Clob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDate(kotlin.Int,%20java.sql.Date))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`)` Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDate(kotlin.Int,%20java.sql.Date,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDouble(kotlin.Int,%20kotlin.Double))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the designated parameter to the given Java`double`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setFloat(kotlin.Int,%20kotlin.Float))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the designated parameter to the given Java`float`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setInt(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given Java`int`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setLong(kotlin.Int,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given Java`long`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNCharacterStream(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.sql.NClob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)!`)` Sets the designated parameter to a`java.sql.NClob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNString](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNString(kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated paramter to the given`String`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNull(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNull(kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of the designated parameter using the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scaleOrLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRef](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setRef(kotlin.Int,%20java.sql.Ref))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)!`)` Sets the designated parameter to the given`REF(<structured-type>)`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowId](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setRowId(kotlin.Int,%20java.sql.RowId))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)!`)` Sets the designated parameter to the given`java.sql.RowId`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSQLXML](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setSQLXML(kotlin.Int,%20java.sql.SQLXML))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xmlObject:` ` [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)!`)` Sets the designated parameter to the given`java.sql.SQLXML`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setShort(kotlin.Int,%20kotlin.Short))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the designated parameter to the given Java`short`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setString(kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to the given Java`String`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTime(kotlin.Int,%20java.sql.Time))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`)` Sets the designated parameter to the given`java.sql.Time`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTime(kotlin.Int,%20java.sql.Time,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTimestamp(kotlin.Int,%20java.sql.Timestamp))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTimestamp(kotlin.Int,%20java.sql.Timestamp,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setURL(kotlin.Int,%20java.net.URL))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`)` Sets the designated parameter to the given`java.net.URL`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUnicodeStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setUnicodeStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |

| Inherited functions ||
|---|---|
| From class [Statement](https://developer.android.com/reference/kotlin/java/sql/Statement) |----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#addBatch(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Adds the given SQL command to the current list of commmands for this`Statement`object. The commands in this list can be executed as a batch by calling the method`executeBatch`. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/sql/Statement#cancel())`()` <br /> Cancels this`Statement`object if both the DBMS and driver support aborting an SQL statement. This method can be used by one thread to cancel a statement that is being executed by another thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#clearBatch())`()` <br /> Empties this`Statement`object's current list of SQL commands. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearWarnings](https://developer.android.com/reference/kotlin/java/sql/Statement#clearWarnings())`()` <br /> Clears all the warnings reported on this`Statement`object. After a call to this method, the method`getWarnings`will return`null`until a new warning is reported for this`Statement`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/sql/Statement#close())`()` <br /> Releases this`Statement`object's database and JDBC resources immediately instead of waiting for this to happen when it is automatically closed. It is generally good practice to release resources as soon as you are finished with them to avoid tying up database resources. Calling the method`close`on a`Statement`object that is already closed has no effect. **Note:** When a`Statement`object is closed, its current`ResultSet`object, if one exists, is also closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which may return multiple results. In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.Int))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `autoGeneratedKeys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that any auto-generated keys should be made available for retrieval. The driver will ignore this signal if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.IntArray))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnIndexes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the indexes of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). Under some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.Array))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the names of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [executeBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#executeBatch())`()` <br /> Submits a batch of commands to the database for execution and if all commands execute successfully, returns an array of update counts. The`int`elements of the array that is returned are ordered to correspond to the commands in the batch, which are ordered according to the order in which they were added to the batch. The elements in the array returned by the method`executeBatch`may be one of the following: 1. A number greater than or equal to zero -- indicates that the command was processed successfully and is an update count giving the number of rows in the database that were affected by the command's execution 2. A value of`SUCCESS_NO_INFO`-- indicates that the command was processed successfully but that the number of rows affected is unknown If one of the commands in a batch update fails to execute properly, this method throws a`BatchUpdateException`, and a JDBC driver may or may not continue to process the remaining commands in the batch. However, the driver's behavior must be consistent with a particular DBMS, either always continuing to process commands or never continuing to process commands. If the driver continues processing after a failure, the array returned by the method`BatchUpdateException.getUpdateCounts`will contain as many elements as there are commands in the batch, and at least one of the elements will be the following: <br /> 3. A value of`EXECUTE_FAILED`-- indicates that the command failed to execute successfully and occurs only if a driver continues to process commands after a command fails <br /> The possible implementations and return values have been modified in the Java 2 SDK, Standard Edition, version 1.3 to accommodate the option of continuing to proccess commands in a batch update after a`BatchUpdateException`obejct has been thrown. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [executeQuery](https://developer.android.com/reference/kotlin/java/sql/Statement#executeQuery(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which returns a single`ResultSet`object. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which may be an`INSERT`,`UPDATE`, or`DELETE`statement or an SQL statement that returns nothing, such as an SQL DDL statement. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.Int))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `autoGeneratedKeys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Executes the given SQL statement and signals the driver with the given flag about whether the auto-generated keys produced by this`Statement`object should be made available for retrieval. The driver will ignore the flag if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.IntArray))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnIndexes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Executes the given SQL statement and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the indexes of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.Array))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Executes the given SQL statement and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the names of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/Statement#getConnection())`()` <br /> Retrieves the`Connection`object that produced this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchDirection](https://developer.android.com/reference/kotlin/java/sql/Statement#getFetchDirection())`()` <br /> Retrieves the direction for fetching rows from database tables that is the default for result sets generated from this`Statement`object. If this`Statement`object has not set a fetch direction by calling the method`setFetchDirection`, the return value is implementation-specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchSize](https://developer.android.com/reference/kotlin/java/sql/Statement#getFetchSize())`()` <br /> Retrieves the number of result set rows that is the default fetch size for`ResultSet`objects generated from this`Statement`object. If this`Statement`object has not set a fetch size by calling the method`setFetchSize`, the return value is implementation-specific. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getGeneratedKeys](https://developer.android.com/reference/kotlin/java/sql/Statement#getGeneratedKeys())`()` <br /> Retrieves any auto-generated keys created as a result of executing this`Statement`object. If this`Statement`object did not generate any keys, an empty`ResultSet`object is returned. **Note:**If the columns which represent the auto-generated keys were not specified, the JDBC driver implementation will determine the columns which best represent the auto-generated keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxFieldSize](https://developer.android.com/reference/kotlin/java/sql/Statement#getMaxFieldSize())`()` <br /> Retrieves the maximum number of bytes that can be returned for character and binary column values in a`ResultSet`object produced by this`Statement`object. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARY`,`CHAR`,`VARCHAR`,`NCHAR`,`NVARCHAR`,`LONGNVARCHAR`and`LONGVARCHAR`columns. If the limit is exceeded, the excess data is silently discarded. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxRows](https://developer.android.com/reference/kotlin/java/sql/Statement#getMaxRows())`()` <br /> Retrieves the maximum number of rows that a`ResultSet`object produced by this`Statement`object can contain. If this limit is exceeded, the excess rows are silently dropped. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMoreResults](https://developer.android.com/reference/kotlin/java/sql/Statement#getMoreResults())`()` <br /> Moves to this`Statement`object's next result, returns`true`if it is a`ResultSet`object, and implicitly closes any current`ResultSet`object(s) obtained with the method`getResultSet`. There are no more results when the following is true: ```kotlin // stmt is a Statement object ((stmt.getMoreResults() == false) && (stmt.getUpdateCount() == -1)) ``` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMoreResults](https://developer.android.com/reference/kotlin/java/sql/Statement#getMoreResults(kotlin.Int))`(`current:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Moves to this`Statement`object's next result, deals with any current`ResultSet`object(s) according to the instructions specified by the given flag, and returns`true`if the next result is a`ResultSet`object. There are no more results when the following is true: ```kotlin // stmt is a Statement object ((stmt.getMoreResults(current) == false) && (stmt.getUpdateCount() == -1)) ``` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueryTimeout](https://developer.android.com/reference/kotlin/java/sql/Statement#getQueryTimeout())`()` <br /> Retrieves the number of seconds the driver will wait for a`Statement`object to execute. If the limit is exceeded, a`SQLException`is thrown. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getResultSet](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSet())`()` <br /> Retrieves the current result as a`ResultSet`object. This method should be called only once per result. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetConcurrency](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetConcurrency())`()` <br /> Retrieves the result set concurrency for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetHoldability](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetHoldability())`()` <br /> Retrieves the result set holdability for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetType](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetType())`()` <br /> Retrieves the result set type for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUpdateCount](https://developer.android.com/reference/kotlin/java/sql/Statement#getUpdateCount())`()` <br /> Retrieves the current result as an update count; if the result is a`ResultSet`object or there are no more results, -1 is returned. This method should be called only once per result. <br /> | | [SQLWarning](https://developer.android.com/reference/kotlin/java/sql/SQLWarning)! | [getWarnings](https://developer.android.com/reference/kotlin/java/sql/Statement#getWarnings())`()` <br /> Retrieves the first warning reported by calls on this`Statement`object. Subsequent`Statement`object warnings will be chained to this`SQLWarning`object. The warning chain is automatically cleared each time a statement is (re)executed. This method may not be called on a closed`Statement`object; doing so will cause an`SQLException`to be thrown. **Note:** If you are processing a`ResultSet`object, any warnings associated with reads on that`ResultSet`object will be chained on it rather than on the`Statement`object that produced it. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/java/sql/Statement#isClosed())`()` <br /> Retrieves whether this`Statement`object has been closed. A`Statement`is closed if the method close has been called on it, or if it is automatically closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPoolable](https://developer.android.com/reference/kotlin/java/sql/Statement#isPoolable())`()` <br /> Returns a value indicating whether the`Statement`is poolable or not. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursorName](https://developer.android.com/reference/kotlin/java/sql/Statement#setCursorName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the SQL cursor name to the given`String`, which will be used by subsequent`Statement`object`execute`methods. This name can then be used in SQL positioned update or delete statements to identify the current row in the`ResultSet`object generated by this statement. If the database does not support positioned update/delete, this method is a noop. To insure that a cursor has the proper isolation level to support updates, the cursor's`SELECT`statement should have the form`SELECT FOR UPDATE`. If`FOR UPDATE`is not present, positioned updates may fail. **Note:** By definition, the execution of positioned updates and deletes must be done by a different`Statement`object than the one that generated the`ResultSet`object being used for positioning. Also, cursor names must be unique within a connection. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEscapeProcessing](https://developer.android.com/reference/kotlin/java/sql/Statement#setEscapeProcessing(kotlin.Boolean))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets escape processing on or off. If escape scanning is on (the default), the driver will do escape substitution before sending the SQL statement to the database. Note: Since prepared statements have usually been parsed prior to making this call, disabling escape processing for`PreparedStatements`objects will have no effect. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchDirection](https://developer.android.com/reference/kotlin/java/sql/Statement#setFetchDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives the driver a hint as to the direction in which rows will be processed in`ResultSet`objects created using this`Statement`object. The default value is`ResultSet.FETCH_FORWARD`. Note that this method sets the default fetch direction for result sets generated by this`Statement`object. Each result set has its own methods for getting and setting its own fetch direction. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchSize](https://developer.android.com/reference/kotlin/java/sql/Statement#setFetchSize(kotlin.Int))`(`rows:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives the JDBC driver a hint as to the number of rows that should be fetched from the database when more rows are needed for`ResultSet`objects genrated by this`Statement`. If the value specified is zero, then the hint is ignored. The default value is zero. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxFieldSize](https://developer.android.com/reference/kotlin/java/sql/Statement#setMaxFieldSize(kotlin.Int))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the limit for the maximum number of bytes that can be returned for character and binary column values in a`ResultSet`object produced by this`Statement`object. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARY`,`CHAR`,`VARCHAR`,`NCHAR`,`NVARCHAR`,`LONGNVARCHAR`and`LONGVARCHAR`fields. If the limit is exceeded, the excess data is silently discarded. For maximum portability, use values greater than 256. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxRows](https://developer.android.com/reference/kotlin/java/sql/Statement#setMaxRows(kotlin.Int))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the limit for the maximum number of rows that any`ResultSet`object generated by this`Statement`object can contain to the given number. If the limit is exceeded, the excess rows are silently dropped. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPoolable](https://developer.android.com/reference/kotlin/java/sql/Statement#setPoolable(kotlin.Boolean))`(`poolable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Requests that a`Statement`be pooled or not pooled. The value specified is a hint to the statement pool implementation indicating whether the applicaiton wants the statement to be pooled. It is up to the statement pool manager as to whether the hint is used. The poolable value of a statement is applicable to both internal statement caches implemented by the driver and external statement caches implemented by application servers and other applications. By default, a`Statement`is not poolable when created, and a`PreparedStatement`and`CallableStatement`are poolable when created. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQueryTimeout](https://developer.android.com/reference/kotlin/java/sql/Statement#setQueryTimeout(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of seconds the driver will wait for a`Statement`object to execute to the given number of seconds. By default there is no limit on the amount of time allowed for a running statement to complete. If the limit is exceeded, an`SQLTimeoutException`is thrown. A JDBC driver must apply this limit to the`execute`,`executeQuery`and`executeUpdate`methods. **Note:** JDBC driver implementations may also apply this limit to`ResultSet`methods (consult your driver vendor documentation for details). **Note:** In the case of`Statement`batching, it is implementation defined as to whether the time-out is applied to individual SQL commands added via the`addBatch`method or to the entire batch of SQL commands invoked by the`executeBatch`method (consult your driver vendor documentation for details). <br /> | ||
| From class [Wrapper](https://developer.android.com/reference/kotlin/java/sql/Wrapper) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](https://developer.android.com/reference/kotlin/java/sql/Wrapper#isWrapperFor(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](https://developer.android.com/reference/kotlin/java/sql/Wrapper#unwrap(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Public methods

### addBatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addBatch(): Unit
```

Adds a set of parameters to this`PreparedStatement`object's batch of commands.

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

**See Also**

- [java.sql.Statement#addBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#addBatch(kotlin.String)) 

### clearParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearParameters(): Unit
```

Clears the current parameter values immediately.

In general, parameter values remain in force for repeated use of a statement. Setting a parameter value automatically clears its previous value. However, in some cases it is useful to immediately release the resources used by the current parameter values; this can be done by calling the method`clearParameters`.

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun execute(): Boolean
```

Executes the SQL statement in this`PreparedStatement`object, which may be any kind of SQL statement. Some prepared statements return multiple results; the`execute`method handles these complex statements as well as the simpler form of statements handled by the methods`executeQuery`and`executeUpdate`.

The`execute`method returns a`boolean`to indicate the form of the first result. You must call either the method`getResultSet`or`getUpdateCount`to retrieve the result; you must call`getMoreResults`to move to any subsequent result(s).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the first result is a`ResultSet`object;`false`if the first result is an update count or there is no result |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLTimeoutException` | when the driver has determined that the timeout value that was specified by the`setQueryTimeout`method has been exceeded and has at least attempted to cancel the currently running`Statement` |
| `java.sql.SQLException` | if a database access error occurs; this method is called on a closed`PreparedStatement`or an argument is supplied to this method |

**See Also**

- [java.sql.Statement#getResultSet](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSet())
- [java.sql.Statement#getUpdateCount](https://developer.android.com/reference/kotlin/java/sql/Statement#getUpdateCount()) 

### executeQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun executeQuery(): ResultSet!
```

Executes the SQL query in this`PreparedStatement`object and returns the`ResultSet`object generated by the query.

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | a`ResultSet`object that contains the data produced by the query; never`null` |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLTimeoutException` | when the driver has determined that the timeout value that was specified by the`setQueryTimeout`method has been exceeded and has at least attempted to cancel the currently running`Statement` |
| `java.sql.SQLException` | if a database access error occurs; this method is called on a closed`PreparedStatement`or the SQL statement does not return a`ResultSet`object |

### executeUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun executeUpdate(): Int
```

Executes the SQL statement in this`PreparedStatement`object, which must be an SQL Data Manipulation Language (DML) statement, such as`INSERT`,`UPDATE`or`DELETE`; or an SQL statement that returns nothing, such as a DDL statement.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | either (1) the row count for SQL Data Manipulation Language (DML) statements or (2) 0 for SQL statements that return nothing |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLTimeoutException` | when the driver has determined that the timeout value that was specified by the`setQueryTimeout`method has been exceeded and has at least attempted to cancel the currently running`Statement` |
| `java.sql.SQLException` | if a database access error occurs; this method is called on a closed`PreparedStatement`or the SQL statement returns a`ResultSet`object |

### getMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMetaData(): ResultSetMetaData!
```

Retrieves a`ResultSetMetaData`object that contains information about the columns of the`ResultSet`object that will be returned when this`PreparedStatement`object is executed.

Because a`PreparedStatement`object is precompiled, it is possible to know about the`ResultSet`object that it will return without having to execute it. Consequently, it is possible to invoke the method`getMetaData`on a`PreparedStatement`object rather than waiting to execute it and then invoking the`ResultSet.getMetaData`method on the`ResultSet`object that is returned.

**NOTE:**Using this method may be expensive for some drivers due to the lack of underlying DBMS support.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [ResultSetMetaData](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData)! | the description of a`ResultSet`object's columns or`null`if the driver cannot return a`ResultSetMetaData`object |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getParameterMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParameterMetaData(): ParameterMetaData!
```

Retrieves the number, types and properties of this`PreparedStatement`object's parameters.

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/ParameterMetaData)! | a`ParameterMetaData`object that contains information about the number, types and properties for each parameter marker of this`PreparedStatement`object |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`PreparedStatement` |

**See Also**

- [java.sql.ParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/ParameterMetaData) 

### setArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setArray(
    parameterIndex: Int, 
    x: Array!
): Unit
```

Sets the designated parameter to the given`java.sql.Array`object. The driver converts this to an SQL`ARRAY`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Array](https://developer.android.com/reference/kotlin/java/sql/Array)!:an`Array`object that maps an SQL`ARRAY`value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterIndex: Int, 
    x: InputStream!
): Unit
```

Sets the designated parameter to the given input stream. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setAsciiStream`which takes a length parameter.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBigDecimal(
    parameterIndex: Int, 
    x: BigDecimal!
): Unit
```

Sets the designated parameter to the given`java.math.BigDecimal`value. The driver converts this to an SQL`NUMERIC`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterIndex: Int, 
    x: InputStream!
): Unit
```

Sets the designated parameter to the given input stream. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBinaryStream`which takes a length parameter.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Int
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

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
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or if parameterIndex does not correspond to a parameter marker in the SQL statement, |
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
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the parameter data. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`; if the length specified is less than zero or if the number of bytes in the inputstream does not match the specfied length. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBlob(
    parameterIndex: Int, 
    x: Blob!
): Unit
```

Sets the designated parameter to the given`java.sql.Blob`object. The driver converts this to an SQL`BLOB`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)!:a`Blob`object that maps an SQL`BLOB`value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBoolean(
    parameterIndex: Int, 
    x: Boolean
): Unit
```

Sets the designated parameter to the given Java`boolean`value. The driver converts this to an SQL`BIT`or`BOOLEAN`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setByte(
    parameterIndex: Int, 
    x: Byte
): Unit
```

Sets the designated parameter to the given Java`byte`value. The driver converts this to an SQL`TINYINT`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBytes(
    parameterIndex: Int, 
    x: ByteArray!
): Unit
```

Sets the designated parameter to the given Java array of bytes. The driver converts this to an SQL`VARBINARY`or`LONGVARBINARY`(depending on the argument's size relative to the driver's limits on`VARBINARY`values) when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterIndex: Int, 
    reader: Reader!
): Unit
```

Sets the designated parameter to the given`Reader`object. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setCharacterStream`which takes a length parameter.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the Unicode data |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterIndex: Int, 
    reader: Reader!, 
    length: Int
): Unit
```

Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the Unicode data |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterIndex: Int, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the Unicode data |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the stream |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or if parameterIndex does not correspond to a parameter marker in the SQL statement |
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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or if the length specified is less than zero. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setClob(
    parameterIndex: Int, 
    x: Clob!
): Unit
```

Sets the designated parameter to the given`java.sql.Clob`object. The driver converts this to an SQL`CLOB`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)!:a`Clob`object that maps an SQL`CLOB`value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterIndex: Int, 
    x: Date!
): Unit
```

Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. The driver converts this to an SQL`DATE`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDate(
    parameterIndex: Int, 
    x: Date!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`DATE`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the date taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the date |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDouble(
    parameterIndex: Int, 
    x: Double
): Unit
```

Sets the designated parameter to the given Java`double`value. The driver converts this to an SQL`DOUBLE`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFloat(
    parameterIndex: Int, 
    x: Float
): Unit
```

Sets the designated parameter to the given Java`float`value. The driver converts this to an SQL`REAL`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInt(
    parameterIndex: Int, 
    x: Int
): Unit
```

Sets the designated parameter to the given Java`int`value. The driver converts this to an SQL`INTEGER`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setLong(
    parameterIndex: Int, 
    x: Long
): Unit
```

Sets the designated parameter to the given Java`long`value. The driver converts this to an SQL`BIGINT`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNCharacterStream(
    parameterIndex: Int, 
    value: Reader!
): Unit
```

Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

**Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNCharacterStream`which takes a length parameter.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the first parameter is 1, the second is 2, ... |
| `value` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the parameter value |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs; or this method is called on a closed`PreparedStatement` |
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
| `value` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs; or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

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
| `value` | [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)!:the parameter value |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs; or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs; or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterIndex: Int, 
    sqlType: Int
): Unit
```

Sets the designated parameter to SQL`NULL`.

**Note:**You must specify the parameter's SQL type.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type code defined in`java.sql.Types` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterIndex: Int, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Sets the designated parameter to SQL`NULL`. This version of the method`setNull`should be used for user-defined types and REF type parameters. Examples of user-defined types include: STRUCT, DISTINCT, JAVA_OBJECT, and named array types.

**Note:**To be portable, applications must give the SQL type code and the fully-qualified SQL type name when specifying a NULL user-defined or REF parameter. In the case of a user-defined type the name is the type name of the parameter itself. For a REF parameter, the name is the type name of the referenced type. If a JDBC driver does not need the type code or type name information, it may ignore it. Although it is intended for user-defined and Ref parameters, this method may be used to set a null parameter of any JDBC type. If the parameter does not have a user-defined or REF type, the given typeName is ignored.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from`java.sql.Types` |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully-qualified name of an SQL user-defined type; ignored if the parameter is not a user-defined type or REF |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type or if the JDBC driver does not support this method |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterIndex: Int, 
    x: Any!
): Unit
```

Sets the value of the designated parameter using the given object. The second parameter must be of type`Object`; therefore, the`java.lang`equivalent objects should be used for built-in types.

The JDBC specification specifies a standard mapping from Java`Object`types to SQL types. The given argument will be converted to the corresponding SQL type before being sent to the database.

Note that this method may be used to pass datatabase- specific abstract data types, by using a driver-specific Java type. If the object is of a class implementing the interface`SQLData`, the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`,`RowId`,`SQLXML`or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

**Note:** Not all databases allow for a non-typed Null to be sent to the backend. For maximum portability, the`setNull`or the`setObject(int parameterIndex, Object x, int sqlType)`method should be used instead of`setObject(int parameterIndex, Object x)`.

**Note:**This method throws an exception if there is an ambiguity, for example, if the object is of a class implementing more than one of the interfaces named above.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or the type of the given object is ambiguous |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setObject(
    parameterIndex: Int, 
    x: Any!, 
    targetSqlType: Int
): Unit
```

Sets the value of the designated parameter with the given object. This method is like the method`setObject`above, except that it assumes a scale of zero.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in java.sql.Types) to be sent to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

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

Sets the value of the designated parameter with the given object. The second argument must be an object type; for integral values, the`java.lang`equivalent objects should be used. If the second argument is an`InputStream`then the stream must contain the number of bytes specified by scaleOrLength. If the second argument is a`Reader`then the reader must contain the number of characters specified by scaleOrLength. If these conditions are not true the driver will generate a`SQLException`when the prepared statement is executed.

The given Java object will be converted to the given targetSqlType before being sent to the database. If the object has a custom mapping (is of a class implementing the interface`SQLData`), the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type.

Note that this method may be used to pass database-specific abstract data types.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |
| `targetSqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type (as defined in java.sql.Types) to be sent to the database. The scale argument may further qualify this type. |
| `scaleOrLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for`java.sql.Types.DECIMAL`or`java.sql.Types.NUMERIC types`, this is the number of digits after the decimal point. For Java Object types`InputStream`and`Reader`, this is the length of the data in the stream or reader. For all other types, this value will be ignored. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or if the Java Object specified by x is an InputStream or Reader object and the value of the scale parameter is less than zero |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### setRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRef(
    parameterIndex: Int, 
    x: Ref!
): Unit
```

Sets the designated parameter to the given`REF(<structured-type>)`value. The driver converts this to an SQL`REF`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)!:an SQL`REF`value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

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
| `x` | [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)!:the parameter value |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSQLXML(
    parameterIndex: Int, 
    xmlObject: SQLXML!
): Unit
```

Sets the designated parameter to the given`java.sql.SQLXML`object. The driver converts this to an SQL`XML`value when it sends it to the database.

<br />

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |
| `xmlObject` | [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)!:a`SQLXML`object that maps an SQL`XML`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs; this method is called on a closed`PreparedStatement`or the`java.xml.transform.Result`,`Writer`or`OutputStream`has not been closed for the`SQLXML`object |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShort(
    parameterIndex: Int, 
    x: Short
): Unit
```

Sets the designated parameter to the given Java`short`value. The driver converts this to an SQL`SMALLINT`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(
    parameterIndex: Int, 
    x: String!
): Unit
```

Sets the designated parameter to the given Java`String`value. The driver converts this to an SQL`VARCHAR`or`LONGVARCHAR`value (depending on the argument's size relative to the driver's limits on`VARCHAR`values) when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterIndex: Int, 
    x: Time!
): Unit
```

Sets the designated parameter to the given`java.sql.Time`value. The driver converts this to an SQL`TIME`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTime(
    parameterIndex: Int, 
    x: Time!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIME`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the time taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the time |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterIndex: Int, 
    x: Timestamp!
): Unit
```

Sets the designated parameter to the given`java.sql.Timestamp`value. The driver converts this to an SQL`TIMESTAMP`value when it sends it to the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!:the parameter value |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTimestamp(
    parameterIndex: Int, 
    x: Timestamp!, 
    cal: Calendar!
): Unit
```

Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIMESTAMP`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the timestamp taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the timestamp |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!:the`java.net.URL`object to be set |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |

### setUnicodeStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUnicodeStream(
    parameterIndex: Int, 
    x: InputStream!, 
    length: Int
): Unit
```

**Deprecated:** *Use setCharacterStream*

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large Unicode value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from Unicode to the database char format. The byte format of the Unicode stream must be a Java UTF-8, as defined in the Java Virtual Machine Specification.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:a`java.io.InputStream`object that contains the Unicode parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterIndex does not correspond to a parameter marker in the SQL statement; if a database access error occurs or this method is called on a closed`PreparedStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
