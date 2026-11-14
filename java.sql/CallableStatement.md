# CallableStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallableStatement

```
interface CallableStatement : PreparedStatement
```

| [java.sql.CallableStatement](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#) |

The interface used to execute SQL stored procedures. The JDBC API provides a stored procedure SQL escape syntax that allows stored procedures to be called in a standard way for all RDBMSs. This escape syntax has one form that includes a result parameter and one that does not. If used, the result parameter must be registered as an OUT parameter. The other parameters can be used for input, output or both. Parameters are referred to sequentially, by number, with the first parameter being 1. 

```kotlin
{?= call <procedure-name>[(<arg1>,<arg2>, ...)]}
    {call <procedure-name>[(<arg1>,<arg2>, ...)]}
  
```

<br />

IN parameter values are set using the`set`methods inherited from [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement). The type of all OUT parameters must be registered prior to executing the stored procedure; their values are retrieved after execution via the`get`methods provided here.

A`CallableStatement`can return one [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet) object or multiple`ResultSet`objects. Multiple`ResultSet`objects are handled using operations inherited from [Statement](https://developer.android.com/reference/kotlin/java/sql/Statement).

For maximum portability, a call's`ResultSet`objects and update counts should be processed prior to getting the values of output parameters.

<br />

## Summary

| Inherited constants ||
|---|---|
| From class [Statement](https://developer.android.com/reference/kotlin/java/sql/Statement) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_ALL_RESULTS](https://developer.android.com/reference/kotlin/java/sql/Statement#CLOSE_ALL_RESULTS:kotlin.Int) <br /> The constant indicating that all`ResultSet`objects that have previously been kept open should be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_CURRENT_RESULT](https://developer.android.com/reference/kotlin/java/sql/Statement#CLOSE_CURRENT_RESULT:kotlin.Int) <br /> The constant indicating that the current`ResultSet`object should be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXECUTE_FAILED](https://developer.android.com/reference/kotlin/java/sql/Statement#EXECUTE_FAILED:kotlin.Int) <br /> The constant indicating that an error occured while executing a batch statement. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEEP_CURRENT_RESULT](https://developer.android.com/reference/kotlin/java/sql/Statement#KEEP_CURRENT_RESULT:kotlin.Int) <br /> The constant indicating that the current`ResultSet`object should not be closed when calling`getMoreResults`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_GENERATED_KEYS](https://developer.android.com/reference/kotlin/java/sql/Statement#NO_GENERATED_KEYS:kotlin.Int) <br /> The constant indicating that generated keys should not be made available for retrieval. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RETURN_GENERATED_KEYS](https://developer.android.com/reference/kotlin/java/sql/Statement#RETURN_GENERATED_KEYS:kotlin.Int) <br /> The constant indicating that generated keys should be made available for retrieval. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS_NO_INFO](https://developer.android.com/reference/kotlin/java/sql/Statement#SUCCESS_NO_INFO:kotlin.Int) <br /> The constant indicating that a batch statement executed successfully but that no count of the number of rows it affected is available. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | [getArray](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getArray(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`ARRAY`parameter as an [java.sql.Array](https://developer.android.com/reference/kotlin/java/sql/Array) object in the Java programming language. |
| abstract [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | [getArray](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getArray(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`ARRAY`parameter as an [java.sql.Array](https://developer.android.com/reference/kotlin/java/sql/Array) object in the Java programming language. |
| abstract [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | [getBigDecimal](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBigDecimal(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with as many digits to the right of the decimal point as the value contains. |
| abstract [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | [getBigDecimal](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBigDecimal(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with*scale*digits to the right of the decimal point. |
| abstract [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | [getBigDecimal](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBigDecimal(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with as many digits to the right of the decimal point as the value contains. |
| abstract [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | [getBlob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBlob(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`BLOB`parameter as a [java.sql.Blob](https://developer.android.com/reference/kotlin/java/sql/Blob) object in the Java programming language. |
| abstract [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | [getBlob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBlob(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`BLOB`parameter as a [java.sql.Blob](https://developer.android.com/reference/kotlin/java/sql/Blob) object in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBoolean(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`BIT`or`BOOLEAN`parameter as a`boolean`in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBoolean(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`BIT`or`BOOLEAN`parameter as a`boolean`in the Java programming language. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getByte(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`TINYINT`parameter as a`byte`in the Java programming language. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getByte(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`TINYINT`parameter as a`byte`in the Java programming language. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBytes(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`BINARY`or`VARBINARY`parameter as an array of`byte`values in the Java programming language. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getBytes(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`BINARY`or`VARBINARY`parameter as an array of`byte`values in the Java programming language. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getCharacterStream(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getCharacterStream(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. |
| abstract [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | [getClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getClob(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`CLOB`parameter as a`java.sql.Clob`object in the Java programming language. |
| abstract [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | [getClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getClob(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`CLOB`parameter as a`java.sql.Clob`object in the Java programming language. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | [getDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDate(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`DATE`parameter as a`java.sql.Date`object. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | [getDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDate(kotlin.Int,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of the designated JDBC`DATE`parameter as a`java.sql.Date`object, using the given`Calendar`object to construct the date. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | [getDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDate(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`DATE`parameter as a`java.sql.Date`object. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | [getDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDate(kotlin.String,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of a JDBC`DATE`parameter as a`java.sql.Date`object, using the given`Calendar`object to construct the date. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDouble(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`DOUBLE`parameter as a`double`in the Java programming language. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getDouble(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`DOUBLE`parameter as a`double`in the Java programming language. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getFloat(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`FLOAT`parameter as a`float`in the Java programming language. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getFloat(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`FLOAT`parameter as a`float`in the Java programming language. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getInt(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`INTEGER`parameter as an`int`in the Java programming language. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getInt(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`INTEGER`parameter as an`int`in the Java programming language. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getLong(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`BIGINT`parameter as a`long`in the Java programming language. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getLong(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`BIGINT`parameter as a`long`in the Java programming language. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNCharacterStream(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNCharacterStream(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. |
| abstract [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | [getNClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNClob(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`NCLOB`parameter as a`java.sql.NClob`object in the Java programming language. |
| abstract [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | [getNClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNClob(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`NCLOB`parameter as a`java.sql.NClob`object in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNString(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`parameter as a`String`in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getNString(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of the designated`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`parameter as a`String`in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getObject(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated parameter as an`Object`in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getObject(kotlin.Int,%20kotlin.collections.MutableMap))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!>!`)` Returns an object representing the value of OUT parameter`parameterIndex`and uses`map`for the custom mapping of the parameter value. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getObject(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a parameter as an`Object`in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getObject(kotlin.String,%20kotlin.collections.MutableMap))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!>!`)` Returns an object representing the value of OUT parameter`parameterName`and uses`map`for the custom mapping of the parameter value. |
| abstract [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | [getRef](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getRef(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`REF(<structured-type>)`parameter as a [java.sql.Ref](https://developer.android.com/reference/kotlin/java/sql/Ref) object in the Java programming language. |
| abstract [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | [getRef](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getRef(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`REF(<structured-type>)`parameter as a [java.sql.Ref](https://developer.android.com/reference/kotlin/java/sql/Ref) object in the Java programming language. |
| abstract [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | [getRowId](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getRowId(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`ROWID`parameter as a`java.sql.RowId`object. |
| abstract [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | [getRowId](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getRowId(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of the designated JDBC`ROWID`parameter as a`java.sql.RowId`object. |
| abstract [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | [getSQLXML](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getSQLXML(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated`SQL XML`parameter as a`java.sql.SQLXML`object in the Java programming language. |
| abstract [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | [getSQLXML](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getSQLXML(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of the designated`SQL XML`parameter as a`java.sql.SQLXML`object in the Java programming language. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getShort(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`SMALLINT`parameter as a`short`in the Java programming language. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getShort(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`SMALLINT`parameter as a`short`in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getString(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`CHAR`,`VARCHAR`, or`LONGVARCHAR`parameter as a`String`in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getString(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`CHAR`,`VARCHAR`, or`LONGVARCHAR`parameter as a`String`in the Java programming language. |
| abstract [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | [getTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTime(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`TIME`parameter as a`java.sql.Time`object. |
| abstract [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | [getTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTime(kotlin.Int,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of the designated JDBC`TIME`parameter as a`java.sql.Time`object, using the given`Calendar`object to construct the time. |
| abstract [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | [getTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTime(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`TIME`parameter as a`java.sql.Time`object. |
| abstract [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | [getTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTime(kotlin.String,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of a JDBC`TIME`parameter as a`java.sql.Time`object, using the given`Calendar`object to construct the time. |
| abstract [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | [getTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTimestamp(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object. |
| abstract [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | [getTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTimestamp(kotlin.Int,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of the designated JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object, using the given`Calendar`object to construct the`Timestamp`object. |
| abstract [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | [getTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTimestamp(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object. |
| abstract [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | [getTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getTimestamp(kotlin.String,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Retrieves the value of a JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object, using the given`Calendar`object to construct the`Timestamp`object. |
| abstract [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | [getURL](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getURL(kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value of the designated JDBC`DATALINK`parameter as a`java.net.URL`object. |
| abstract [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | [getURL](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#getURL(kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the value of a JDBC`DATALINK`parameter as a`java.net.URL`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers the OUT parameter in ordinal position`parameterIndex`to the JDBC type`sqlType`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers the parameter in ordinal position`parameterIndex`to be of JDBC type`sqlType`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Registers the designated output parameter. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.String,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers the OUT parameter named`parameterName`to the JDBC type`sqlType`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers the parameter named`parameterName`to be of JDBC type`sqlType`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerOutParameter](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#registerOutParameter(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Registers the designated output parameter. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setAsciiStream(kotlin.String,%20java.io.InputStream))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setAsciiStream(kotlin.String,%20java.io.InputStream,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setAsciiStream(kotlin.String,%20java.io.InputStream,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBigDecimal](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBigDecimal(kotlin.String,%20java.math.BigDecimal))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Sets the designated parameter to the given`java.math.BigDecimal`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBinaryStream(kotlin.String,%20java.io.InputStream))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to the given input stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBinaryStream(kotlin.String,%20java.io.InputStream,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBinaryStream(kotlin.String,%20java.io.InputStream,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given input stream, which will have the specified number of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBlob(kotlin.String,%20java.io.InputStream))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBlob(kotlin.String,%20java.io.InputStream,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`InputStream`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBlob(kotlin.String,%20java.sql.Blob))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)!`)` Sets the designated parameter to the given`java.sql.Blob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBoolean(kotlin.String,%20kotlin.Boolean))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the designated parameter to the given Java`boolean`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setByte(kotlin.String,%20kotlin.Byte))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the designated parameter to the given Java`byte`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBytes](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setBytes(kotlin.String,%20kotlin.ByteArray))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets the designated parameter to the given Java array of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setCharacterStream(kotlin.String,%20java.io.Reader))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to the given`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setCharacterStream(kotlin.String,%20java.io.Reader,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given`Reader`object, which is the given number of characters long. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setCharacterStream(kotlin.String,%20java.io.Reader,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given`Reader`object, which is the given number of characters long. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setClob(kotlin.String,%20java.io.Reader))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setClob(kotlin.String,%20java.io.Reader,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setClob(kotlin.String,%20java.sql.Clob))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)!`)` Sets the designated parameter to the given`java.sql.Clob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setDate(kotlin.String,%20java.sql.Date))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`)` Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setDate(kotlin.String,%20java.sql.Date,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setDouble(kotlin.String,%20kotlin.Double))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the designated parameter to the given Java`double`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setFloat(kotlin.String,%20kotlin.Float))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the designated parameter to the given Java`float`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setInt(kotlin.String,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to the given Java`int`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setLong(kotlin.String,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to the given Java`long`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNCharacterStream(kotlin.String,%20java.io.Reader))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNCharacterStream(kotlin.String,%20java.io.Reader,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNClob(kotlin.String,%20java.io.Reader))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNClob(kotlin.String,%20java.io.Reader,%20kotlin.Long))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the designated parameter to a`Reader`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNClob(kotlin.String,%20java.sql.NClob))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)!`)` Sets the designated parameter to a`java.sql.NClob`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNString(kotlin.String,%20kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to the given`String`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNull(kotlin.String,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setNull(kotlin.String,%20kotlin.Int,%20kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to SQL`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setObject(kotlin.String,%20kotlin.Any))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setObject(kotlin.String,%20kotlin.Any,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setObject(kotlin.String,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the designated parameter with the given object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowId](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setRowId(kotlin.String,%20java.sql.RowId))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)!`)` Sets the designated parameter to the given`java.sql.RowId`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSQLXML](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setSQLXML(kotlin.String,%20java.sql.SQLXML))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `xmlObject:` ` [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)!`)` Sets the designated parameter to the given`java.sql.SQLXML`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setShort(kotlin.String,%20kotlin.Short))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the designated parameter to the given Java`short`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setString(kotlin.String,%20kotlin.String))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated parameter to the given Java`String`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setTime(kotlin.String,%20java.sql.Time))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`)` Sets the designated parameter to the given`java.sql.Time`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setTime(kotlin.String,%20java.sql.Time,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setTimestamp(kotlin.String,%20java.sql.Timestamp))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setTimestamp(kotlin.String,%20java.sql.Timestamp,%20java.util.Calendar))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#setURL(kotlin.String,%20java.net.URL))`(`parameterName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `val:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`)` Sets the designated parameter to the given`java.net.URL`object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasNull](https://developer.android.com/reference/kotlin/java/sql/CallableStatement#wasNull())`()` Retrieves whether the last OUT parameter read had the value of SQL`NULL`. |

| Inherited functions ||
|---|---|
| From class [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#addBatch())`()` <br /> Adds a set of parameters to this`PreparedStatement`object's batch of commands. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearParameters](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#clearParameters())`()` <br /> Clears the current parameter values immediately. In general, parameter values remain in force for repeated use of a statement. Setting a parameter value automatically clears its previous value. However, in some cases it is useful to immediately release the resources used by the current parameter values; this can be done by calling the method`clearParameters`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#execute())`()` <br /> Executes the SQL statement in this`PreparedStatement`object, which may be any kind of SQL statement. Some prepared statements return multiple results; the`execute`method handles these complex statements as well as the simpler form of statements handled by the methods`executeQuery`and`executeUpdate`. The`execute`method returns a`boolean`to indicate the form of the first result. You must call either the method`getResultSet`or`getUpdateCount`to retrieve the result; you must call`getMoreResults`to move to any subsequent result(s). <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [executeQuery](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#executeQuery())`()` <br /> Executes the SQL query in this`PreparedStatement`object and returns the`ResultSet`object generated by the query. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#executeUpdate())`()` <br /> Executes the SQL statement in this`PreparedStatement`object, which must be an SQL Data Manipulation Language (DML) statement, such as`INSERT`,`UPDATE`or`DELETE`; or an SQL statement that returns nothing, such as a DDL statement. <br /> | | [ResultSetMetaData](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData)! | [getMetaData](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#getMetaData())`()` <br /> Retrieves a`ResultSetMetaData`object that contains information about the columns of the`ResultSet`object that will be returned when this`PreparedStatement`object is executed. Because a`PreparedStatement`object is precompiled, it is possible to know about the`ResultSet`object that it will return without having to execute it. Consequently, it is possible to invoke the method`getMetaData`on a`PreparedStatement`object rather than waiting to execute it and then invoking the`ResultSet.getMetaData`method on the`ResultSet`object that is returned. **NOTE:**Using this method may be expensive for some drivers due to the lack of underlying DBMS support. <br /> | | [ParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/ParameterMetaData)! | [getParameterMetaData](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#getParameterMetaData())`()` <br /> Retrieves the number, types and properties of this`PreparedStatement`object's parameters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArray](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setArray(kotlin.Int,%20java.sql.Array))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Array](https://developer.android.com/reference/kotlin/java/sql/Array)!`)` <br /> Sets the designated parameter to the given`java.sql.Array`object. The driver converts this to an SQL`ARRAY`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` <br /> Sets the designated parameter to the given input stream. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setAsciiStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setAsciiStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBigDecimal](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBigDecimal(kotlin.Int,%20java.math.BigDecimal))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` <br /> Sets the designated parameter to the given`java.math.BigDecimal`value. The driver converts this to an SQL`NUMERIC`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` <br /> Sets the designated parameter to the given input stream. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBinaryStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBinaryStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.io.InputStream))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` <br /> Sets the designated parameter to a`InputStream`object. This method differs from the`setBinaryStream (int, InputStream)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARBINARY`or a`BLOB` **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setBlob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.io.InputStream,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to a`InputStream`object. The inputstream must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setBinaryStream (int, InputStream, int)`method because it informs the driver that the parameter value should be sent to the server as a`BLOB`. When the`setBinaryStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARBINARY`or a`BLOB` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBlob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBlob(kotlin.Int,%20java.sql.Blob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)!`)` <br /> Sets the designated parameter to the given`java.sql.Blob`object. The driver converts this to an SQL`BLOB`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBoolean(kotlin.Int,%20kotlin.Boolean))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the designated parameter to the given Java`boolean`value. The driver converts this to an SQL`BIT`or`BOOLEAN`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setByte(kotlin.Int,%20kotlin.Byte))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Sets the designated parameter to the given Java`byte`value. The driver converts this to an SQL`TINYINT`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBytes](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setBytes(kotlin.Int,%20kotlin.ByteArray))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Sets the designated parameter to the given Java array of bytes. The driver converts this to an SQL`VARBINARY`or`LONGVARBINARY`(depending on the argument's size relative to the driver's limits on`VARBINARY`values) when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` <br /> Sets the designated parameter to the given`Reader`object. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` <br /> Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARCHAR`or a`CLOB` **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to a`Reader`object. The reader must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`CLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGVARCHAR`or a`CLOB` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setClob(kotlin.Int,%20java.sql.Clob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)!`)` <br /> Sets the designated parameter to the given`java.sql.Clob`object. The driver converts this to an SQL`CLOB`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDate(kotlin.Int,%20java.sql.Date))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`)` <br /> Sets the designated parameter to the given`java.sql.Date`value using the default time zone of the virtual machine that is running the application. The driver converts this to an SQL`DATE`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDate(kotlin.Int,%20java.sql.Date,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` <br /> Sets the designated parameter to the given`java.sql.Date`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`DATE`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the date taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setDouble(kotlin.Int,%20kotlin.Double))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Sets the designated parameter to the given Java`double`value. The driver converts this to an SQL`DOUBLE`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setFloat(kotlin.Int,%20kotlin.Float))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Sets the designated parameter to the given Java`float`value. The driver converts this to an SQL`REAL`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setInt(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to the given Java`int`value. The driver converts this to an SQL`INTEGER`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setLong(kotlin.Int,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to the given Java`long`value. The driver converts this to an SQL`BIGINT`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNCharacterStream(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` <br /> Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNCharacterStream`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNCharacterStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNCharacterStream(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to a`Reader`object. The`Reader`reads the data till end-of-file is reached. The driver does the necessary conversion from Java character format to the national character set in the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.io.Reader))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` <br /> Sets the designated parameter to a`Reader`object. This method differs from the`setCharacterStream (int, Reader)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGNVARCHAR`or a`NCLOB` **Note:** Consult your JDBC driver documentation to determine if it might be more efficient to use a version of`setNClob`which takes a length parameter. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.io.Reader,%20kotlin.Long))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reader:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the designated parameter to a`Reader`object. The reader must contain the number of characters specified by length otherwise a`SQLException`will be generated when the`PreparedStatement`is executed. This method differs from the`setCharacterStream (int, Reader, int)`method because it informs the driver that the parameter value should be sent to the server as a`NCLOB`. When the`setCharacterStream`method is used, the driver may have to do extra work to determine whether the parameter data should be sent to the server as a`LONGNVARCHAR`or a`NCLOB` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNClob](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNClob(kotlin.Int,%20java.sql.NClob))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)!`)` <br /> Sets the designated parameter to a`java.sql.NClob`object. The driver converts this to a SQL`NCLOB`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNString](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNString(kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the designated paramter to the given`String`object. The driver converts this to a SQL`NCHAR`or`NVARCHAR`or`LONGNVARCHAR`value (depending on the argument's size relative to the driver's limits on`NVARCHAR`values) when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNull(kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to SQL`NULL`. **Note:**You must specify the parameter's SQL type. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNull](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setNull(kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the designated parameter to SQL`NULL`. This version of the method`setNull`should be used for user-defined types and REF type parameters. Examples of user-defined types include: STRUCT, DISTINCT, JAVA_OBJECT, and named array types. **Note:**To be portable, applications must give the SQL type code and the fully-qualified SQL type name when specifying a NULL user-defined or REF parameter. In the case of a user-defined type the name is the type name of the parameter itself. For a REF parameter, the name is the type name of the referenced type. If a JDBC driver does not need the type code or type name information, it may ignore it. Although it is intended for user-defined and Ref parameters, this method may be used to set a null parameter of any JDBC type. If the parameter does not have a user-defined or REF type, the given typeName is ignored. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the value of the designated parameter using the given object. The second parameter must be of type`Object`; therefore, the`java.lang`equivalent objects should be used for built-in types. The JDBC specification specifies a standard mapping from Java`Object`types to SQL types. The given argument will be converted to the corresponding SQL type before being sent to the database. Note that this method may be used to pass datatabase- specific abstract data types, by using a driver-specific Java type. If the object is of a class implementing the interface`SQLData`, the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`,`RowId`,`SQLXML`or`Array`, the driver should pass it to the database as a value of the corresponding SQL type. **Note:** Not all databases allow for a non-typed Null to be sent to the backend. For maximum portability, the`setNull`or the`setObject(int parameterIndex, Object x, int sqlType)`method should be used instead of`setObject(int parameterIndex, Object x)`. **Note:**This method throws an exception if there is an ambiguity, for example, if the object is of a class implementing more than one of the interfaces named above. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the value of the designated parameter with the given object. This method is like the method`setObject`above, except that it assumes a scale of zero. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObject](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setObject(kotlin.Int,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `targetSqlType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scaleOrLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the value of the designated parameter with the given object. The second argument must be an object type; for integral values, the`java.lang`equivalent objects should be used. If the second argument is an`InputStream`then the stream must contain the number of bytes specified by scaleOrLength. If the second argument is a`Reader`then the reader must contain the number of characters specified by scaleOrLength. If these conditions are not true the driver will generate a`SQLException`when the prepared statement is executed. The given Java object will be converted to the given targetSqlType before being sent to the database. If the object has a custom mapping (is of a class implementing the interface`SQLData`), the JDBC driver should call the method`SQLData.writeSQL`to write it to the SQL data stream. If, on the other hand, the object is of a class implementing`Ref`,`Blob`,`Clob`,`NClob`,`Struct`,`java.net.URL`, or`Array`, the driver should pass it to the database as a value of the corresponding SQL type. Note that this method may be used to pass database-specific abstract data types. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRef](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setRef(kotlin.Int,%20java.sql.Ref))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)!`)` <br /> Sets the designated parameter to the given`REF(<structured-type>)`value. The driver converts this to an SQL`REF`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowId](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setRowId(kotlin.Int,%20java.sql.RowId))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)!`)` <br /> Sets the designated parameter to the given`java.sql.RowId`object. The driver converts this to a SQL`ROWID`value when it sends it to the database <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSQLXML](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setSQLXML(kotlin.Int,%20java.sql.SQLXML))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xmlObject:` ` [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)!`)` <br /> Sets the designated parameter to the given`java.sql.SQLXML`object. The driver converts this to an SQL`XML`value when it sends it to the database. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setShort(kotlin.Int,%20kotlin.Short))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> Sets the designated parameter to the given Java`short`value. The driver converts this to an SQL`SMALLINT`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setString(kotlin.Int,%20kotlin.String))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the designated parameter to the given Java`String`value. The driver converts this to an SQL`VARCHAR`or`LONGVARCHAR`value (depending on the argument's size relative to the driver's limits on`VARCHAR`values) when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTime(kotlin.Int,%20java.sql.Time))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`)` <br /> Sets the designated parameter to the given`java.sql.Time`value. The driver converts this to an SQL`TIME`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTime(kotlin.Int,%20java.sql.Time,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` <br /> Sets the designated parameter to the given`java.sql.Time`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIME`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the time taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTimestamp(kotlin.Int,%20java.sql.Timestamp))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`)` <br /> Sets the designated parameter to the given`java.sql.Timestamp`value. The driver converts this to an SQL`TIMESTAMP`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimestamp](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setTimestamp(kotlin.Int,%20java.sql.Timestamp,%20java.util.Calendar))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!`, `cal:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` <br /> Sets the designated parameter to the given`java.sql.Timestamp`value, using the given`Calendar`object. The driver uses the`Calendar`object to construct an SQL`TIMESTAMP`value, which the driver then sends to the database. With a`Calendar`object, the driver can calculate the timestamp taking into account a custom timezone. If no`Calendar`object is specified, the driver uses the default timezone, which is that of the virtual machine running the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setURL(kotlin.Int,%20java.net.URL))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!`)` <br /> Sets the designated parameter to the given`java.net.URL`value. The driver converts this to an SQL`DATALINK`value when it sends it to the database. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUnicodeStream](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement#setUnicodeStream(kotlin.Int,%20java.io.InputStream,%20kotlin.Int))`(`parameterIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large Unicode value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from Unicode to the database char format. The byte format of the Unicode stream must be a Java UTF-8, as defined in the Java Virtual Machine Specification. **Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface. <br /> | ||
| From class [Statement](https://developer.android.com/reference/kotlin/java/sql/Statement) |----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#addBatch(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Adds the given SQL command to the current list of commmands for this`Statement`object. The commands in this list can be executed as a batch by calling the method`executeBatch`. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/sql/Statement#cancel())`()` <br /> Cancels this`Statement`object if both the DBMS and driver support aborting an SQL statement. This method can be used by one thread to cancel a statement that is being executed by another thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#clearBatch())`()` <br /> Empties this`Statement`object's current list of SQL commands. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearWarnings](https://developer.android.com/reference/kotlin/java/sql/Statement#clearWarnings())`()` <br /> Clears all the warnings reported on this`Statement`object. After a call to this method, the method`getWarnings`will return`null`until a new warning is reported for this`Statement`object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/sql/Statement#close())`()` <br /> Releases this`Statement`object's database and JDBC resources immediately instead of waiting for this to happen when it is automatically closed. It is generally good practice to release resources as soon as you are finished with them to avoid tying up database resources. Calling the method`close`on a`Statement`object that is already closed has no effect. **Note:** When a`Statement`object is closed, its current`ResultSet`object, if one exists, is also closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which may return multiple results. In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.Int))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `autoGeneratedKeys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that any auto-generated keys should be made available for retrieval. The driver will ignore this signal if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.IntArray))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnIndexes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the indexes of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). Under some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execute](https://developer.android.com/reference/kotlin/java/sql/Statement#execute(kotlin.String,%20kotlin.Array))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Executes the given SQL statement, which may return multiple results, and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the names of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). In some (uncommon) situations, a single SQL statement may return multiple result sets and/or update counts. Normally you can ignore this unless you are (1) executing a stored procedure that you know may return multiple results or (2) you are dynamically executing an unknown SQL string. The`execute`method executes an SQL statement and indicates the form of the first result. You must then use the methods`getResultSet`or`getUpdateCount`to retrieve the result, and`getMoreResults`to move to any subsequent result(s). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [executeBatch](https://developer.android.com/reference/kotlin/java/sql/Statement#executeBatch())`()` <br /> Submits a batch of commands to the database for execution and if all commands execute successfully, returns an array of update counts. The`int`elements of the array that is returned are ordered to correspond to the commands in the batch, which are ordered according to the order in which they were added to the batch. The elements in the array returned by the method`executeBatch`may be one of the following: 1. A number greater than or equal to zero -- indicates that the command was processed successfully and is an update count giving the number of rows in the database that were affected by the command's execution 2. A value of`SUCCESS_NO_INFO`-- indicates that the command was processed successfully but that the number of rows affected is unknown If one of the commands in a batch update fails to execute properly, this method throws a`BatchUpdateException`, and a JDBC driver may or may not continue to process the remaining commands in the batch. However, the driver's behavior must be consistent with a particular DBMS, either always continuing to process commands or never continuing to process commands. If the driver continues processing after a failure, the array returned by the method`BatchUpdateException.getUpdateCounts`will contain as many elements as there are commands in the batch, and at least one of the elements will be the following: <br /> 3. A value of`EXECUTE_FAILED`-- indicates that the command failed to execute successfully and occurs only if a driver continues to process commands after a command fails <br /> The possible implementations and return values have been modified in the Java 2 SDK, Standard Edition, version 1.3 to accommodate the option of continuing to proccess commands in a batch update after a`BatchUpdateException`obejct has been thrown. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [executeQuery](https://developer.android.com/reference/kotlin/java/sql/Statement#executeQuery(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which returns a single`ResultSet`object. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Executes the given SQL statement, which may be an`INSERT`,`UPDATE`, or`DELETE`statement or an SQL statement that returns nothing, such as an SQL DDL statement. **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.Int))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `autoGeneratedKeys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Executes the given SQL statement and signals the driver with the given flag about whether the auto-generated keys produced by this`Statement`object should be made available for retrieval. The driver will ignore the flag if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.IntArray))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnIndexes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Executes the given SQL statement and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the indexes of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdate](https://developer.android.com/reference/kotlin/java/sql/Statement#executeUpdate(kotlin.String,%20kotlin.Array))`(`sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `columnNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Executes the given SQL statement and signals the driver that the auto-generated keys indicated in the given array should be made available for retrieval. This array contains the names of the columns in the target table that contain the auto-generated keys that should be made available. The driver will ignore the array if the SQL statement is not an`INSERT`statement, or an SQL statement able to return auto-generated keys (the list of such statements is vendor-specific). **Note:** This method cannot be called on a`PreparedStatement`or`CallableStatement`. <br /> | | [Connection](https://developer.android.com/reference/kotlin/java/sql/Connection)! | [getConnection](https://developer.android.com/reference/kotlin/java/sql/Statement#getConnection())`()` <br /> Retrieves the`Connection`object that produced this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchDirection](https://developer.android.com/reference/kotlin/java/sql/Statement#getFetchDirection())`()` <br /> Retrieves the direction for fetching rows from database tables that is the default for result sets generated from this`Statement`object. If this`Statement`object has not set a fetch direction by calling the method`setFetchDirection`, the return value is implementation-specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFetchSize](https://developer.android.com/reference/kotlin/java/sql/Statement#getFetchSize())`()` <br /> Retrieves the number of result set rows that is the default fetch size for`ResultSet`objects generated from this`Statement`object. If this`Statement`object has not set a fetch size by calling the method`setFetchSize`, the return value is implementation-specific. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getGeneratedKeys](https://developer.android.com/reference/kotlin/java/sql/Statement#getGeneratedKeys())`()` <br /> Retrieves any auto-generated keys created as a result of executing this`Statement`object. If this`Statement`object did not generate any keys, an empty`ResultSet`object is returned. **Note:**If the columns which represent the auto-generated keys were not specified, the JDBC driver implementation will determine the columns which best represent the auto-generated keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxFieldSize](https://developer.android.com/reference/kotlin/java/sql/Statement#getMaxFieldSize())`()` <br /> Retrieves the maximum number of bytes that can be returned for character and binary column values in a`ResultSet`object produced by this`Statement`object. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARY`,`CHAR`,`VARCHAR`,`NCHAR`,`NVARCHAR`,`LONGNVARCHAR`and`LONGVARCHAR`columns. If the limit is exceeded, the excess data is silently discarded. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxRows](https://developer.android.com/reference/kotlin/java/sql/Statement#getMaxRows())`()` <br /> Retrieves the maximum number of rows that a`ResultSet`object produced by this`Statement`object can contain. If this limit is exceeded, the excess rows are silently dropped. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMoreResults](https://developer.android.com/reference/kotlin/java/sql/Statement#getMoreResults())`()` <br /> Moves to this`Statement`object's next result, returns`true`if it is a`ResultSet`object, and implicitly closes any current`ResultSet`object(s) obtained with the method`getResultSet`. There are no more results when the following is true: ```kotlin // stmt is a Statement object ((stmt.getMoreResults() == false) && (stmt.getUpdateCount() == -1)) ``` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMoreResults](https://developer.android.com/reference/kotlin/java/sql/Statement#getMoreResults(kotlin.Int))`(`current:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Moves to this`Statement`object's next result, deals with any current`ResultSet`object(s) according to the instructions specified by the given flag, and returns`true`if the next result is a`ResultSet`object. There are no more results when the following is true: ```kotlin // stmt is a Statement object ((stmt.getMoreResults(current) == false) && (stmt.getUpdateCount() == -1)) ``` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueryTimeout](https://developer.android.com/reference/kotlin/java/sql/Statement#getQueryTimeout())`()` <br /> Retrieves the number of seconds the driver will wait for a`Statement`object to execute. If the limit is exceeded, a`SQLException`is thrown. <br /> | | [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet)! | [getResultSet](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSet())`()` <br /> Retrieves the current result as a`ResultSet`object. This method should be called only once per result. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetConcurrency](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetConcurrency())`()` <br /> Retrieves the result set concurrency for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetHoldability](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetHoldability())`()` <br /> Retrieves the result set holdability for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultSetType](https://developer.android.com/reference/kotlin/java/sql/Statement#getResultSetType())`()` <br /> Retrieves the result set type for`ResultSet`objects generated by this`Statement`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUpdateCount](https://developer.android.com/reference/kotlin/java/sql/Statement#getUpdateCount())`()` <br /> Retrieves the current result as an update count; if the result is a`ResultSet`object or there are no more results, -1 is returned. This method should be called only once per result. <br /> | | [SQLWarning](https://developer.android.com/reference/kotlin/java/sql/SQLWarning)! | [getWarnings](https://developer.android.com/reference/kotlin/java/sql/Statement#getWarnings())`()` <br /> Retrieves the first warning reported by calls on this`Statement`object. Subsequent`Statement`object warnings will be chained to this`SQLWarning`object. The warning chain is automatically cleared each time a statement is (re)executed. This method may not be called on a closed`Statement`object; doing so will cause an`SQLException`to be thrown. **Note:** If you are processing a`ResultSet`object, any warnings associated with reads on that`ResultSet`object will be chained on it rather than on the`Statement`object that produced it. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/java/sql/Statement#isClosed())`()` <br /> Retrieves whether this`Statement`object has been closed. A`Statement`is closed if the method close has been called on it, or if it is automatically closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPoolable](https://developer.android.com/reference/kotlin/java/sql/Statement#isPoolable())`()` <br /> Returns a value indicating whether the`Statement`is poolable or not. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursorName](https://developer.android.com/reference/kotlin/java/sql/Statement#setCursorName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the SQL cursor name to the given`String`, which will be used by subsequent`Statement`object`execute`methods. This name can then be used in SQL positioned update or delete statements to identify the current row in the`ResultSet`object generated by this statement. If the database does not support positioned update/delete, this method is a noop. To insure that a cursor has the proper isolation level to support updates, the cursor's`SELECT`statement should have the form`SELECT FOR UPDATE`. If`FOR UPDATE`is not present, positioned updates may fail. **Note:** By definition, the execution of positioned updates and deletes must be done by a different`Statement`object than the one that generated the`ResultSet`object being used for positioning. Also, cursor names must be unique within a connection. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEscapeProcessing](https://developer.android.com/reference/kotlin/java/sql/Statement#setEscapeProcessing(kotlin.Boolean))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets escape processing on or off. If escape scanning is on (the default), the driver will do escape substitution before sending the SQL statement to the database. Note: Since prepared statements have usually been parsed prior to making this call, disabling escape processing for`PreparedStatements`objects will have no effect. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchDirection](https://developer.android.com/reference/kotlin/java/sql/Statement#setFetchDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives the driver a hint as to the direction in which rows will be processed in`ResultSet`objects created using this`Statement`object. The default value is`ResultSet.FETCH_FORWARD`. Note that this method sets the default fetch direction for result sets generated by this`Statement`object. Each result set has its own methods for getting and setting its own fetch direction. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFetchSize](https://developer.android.com/reference/kotlin/java/sql/Statement#setFetchSize(kotlin.Int))`(`rows:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gives the JDBC driver a hint as to the number of rows that should be fetched from the database when more rows are needed for`ResultSet`objects genrated by this`Statement`. If the value specified is zero, then the hint is ignored. The default value is zero. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxFieldSize](https://developer.android.com/reference/kotlin/java/sql/Statement#setMaxFieldSize(kotlin.Int))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the limit for the maximum number of bytes that can be returned for character and binary column values in a`ResultSet`object produced by this`Statement`object. This limit applies only to`BINARY`,`VARBINARY`,`LONGVARBINARY`,`CHAR`,`VARCHAR`,`NCHAR`,`NVARCHAR`,`LONGNVARCHAR`and`LONGVARCHAR`fields. If the limit is exceeded, the excess data is silently discarded. For maximum portability, use values greater than 256. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxRows](https://developer.android.com/reference/kotlin/java/sql/Statement#setMaxRows(kotlin.Int))`(`max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the limit for the maximum number of rows that any`ResultSet`object generated by this`Statement`object can contain to the given number. If the limit is exceeded, the excess rows are silently dropped. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPoolable](https://developer.android.com/reference/kotlin/java/sql/Statement#setPoolable(kotlin.Boolean))`(`poolable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Requests that a`Statement`be pooled or not pooled. The value specified is a hint to the statement pool implementation indicating whether the applicaiton wants the statement to be pooled. It is up to the statement pool manager as to whether the hint is used. The poolable value of a statement is applicable to both internal statement caches implemented by the driver and external statement caches implemented by application servers and other applications. By default, a`Statement`is not poolable when created, and a`PreparedStatement`and`CallableStatement`are poolable when created. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQueryTimeout](https://developer.android.com/reference/kotlin/java/sql/Statement#setQueryTimeout(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of seconds the driver will wait for a`Statement`object to execute to the given number of seconds. By default there is no limit on the amount of time allowed for a running statement to complete. If the limit is exceeded, an`SQLTimeoutException`is thrown. A JDBC driver must apply this limit to the`execute`,`executeQuery`and`executeUpdate`methods. **Note:** JDBC driver implementations may also apply this limit to`ResultSet`methods (consult your driver vendor documentation for details). **Note:** In the case of`Statement`batching, it is implementation defined as to whether the time-out is applied to individual SQL commands added via the`addBatch`method or to the entire batch of SQL commands invoked by the`executeBatch`method (consult your driver vendor documentation for details). <br /> | ||
| From class [Wrapper](https://developer.android.com/reference/kotlin/java/sql/Wrapper) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](https://developer.android.com/reference/kotlin/java/sql/Wrapper#isWrapperFor(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](https://developer.android.com/reference/kotlin/java/sql/Wrapper#unwrap(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Public methods

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(parameterIndex: Int): Array!
```

Retrieves the value of the designated JDBC`ARRAY`parameter as an [java.sql.Array](https://developer.android.com/reference/kotlin/java/sql/Array) object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | the parameter value as an`Array`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getArray(parameterName: String!): Array!
```

Retrieves the value of a JDBC`ARRAY`parameter as an [java.sql.Array](https://developer.android.com/reference/kotlin/java/sql/Array) object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | the parameter value as an`Array`object in Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBigDecimal(parameterIndex: Int): BigDecimal!
```

Retrieves the value of the designated JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with as many digits to the right of the decimal point as the value contains.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | the parameter value in full precision. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBigDecimal(
    parameterIndex: Int, 
    scale: Int
): BigDecimal!
```

**Deprecated:** *use`getBigDecimal(int parameterIndex)`or`getBigDecimal(String parameterName)`*

Retrieves the value of the designated JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with*scale*digits to the right of the decimal point.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of digits to the right of the decimal point |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBigDecimal(parameterName: String!): BigDecimal!
```

Retrieves the value of a JDBC`NUMERIC`parameter as a`java.math.BigDecimal`object with as many digits to the right of the decimal point as the value contains.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | the parameter value in full precision. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `SQLExceptionif` | parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlob(parameterIndex: Int): Blob!
```

Retrieves the value of the designated JDBC`BLOB`parameter as a [java.sql.Blob](https://developer.android.com/reference/kotlin/java/sql/Blob) object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | the parameter value as a`Blob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBlob(parameterName: String!): Blob!
```

Retrieves the value of a JDBC`BLOB`parameter as a [java.sql.Blob](https://developer.android.com/reference/kotlin/java/sql/Blob) object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | the parameter value as a`Blob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBoolean(parameterIndex: Int): Boolean
```

Retrieves the value of the designated JDBC`BIT`or`BOOLEAN`parameter as a`boolean`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the parameter value. If the value is SQL`NULL`, the result is`false`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBoolean(parameterName: String!): Boolean
```

Retrieves the value of a JDBC`BIT`or`BOOLEAN`parameter as a`boolean`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the parameter value. If the value is SQL`NULL`, the result is`false`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getByte(parameterIndex: Int): Byte
```

Retrieves the value of the designated JDBC`TINYINT`parameter as a`byte`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getByte(parameterName: String!): Byte
```

Retrieves the value of a JDBC`TINYINT`parameter as a`byte`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBytes(parameterIndex: Int): ByteArray!
```

Retrieves the value of the designated JDBC`BINARY`or`VARBINARY`parameter as an array of`byte`values in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBytes(parameterName: String!): ByteArray!
```

Retrieves the value of a JDBC`BINARY`or`VARBINARY`parameter as an array of`byte`values in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(parameterIndex: Int): Reader!
```

Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a`java.io.Reader`object that contains the parameter value; if the value is SQL`NULL`, the value returned is`null`in the Java programming language. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

### getCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(parameterName: String!): Reader!
```

Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a`java.io.Reader`object that contains the parameter value; if the value is SQL`NULL`, the value returned is`null`in the Java programming language |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClob(parameterIndex: Int): Clob!
```

Retrieves the value of the designated JDBC`CLOB`parameter as a`java.sql.Clob`object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | the parameter value as a`Clob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getClob(parameterName: String!): Clob!
```

Retrieves the value of a JDBC`CLOB`parameter as a`java.sql.Clob`object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | the parameter value as a`Clob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDate(parameterIndex: Int): Date!
```

Retrieves the value of the designated JDBC`DATE`parameter as a`java.sql.Date`object.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDate(
    parameterIndex: Int, 
    cal: Calendar!
): Date!
```

Retrieves the value of the designated JDBC`DATE`parameter as a`java.sql.Date`object, using the given`Calendar`object to construct the date. With a`Calendar`object, the driver can calculate the date taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the date |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDate(parameterName: String!): Date!
```

Retrieves the value of a JDBC`DATE`parameter as a`java.sql.Date`object.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDate(
    parameterName: String!, 
    cal: Calendar!
): Date!
```

Retrieves the value of a JDBC`DATE`parameter as a`java.sql.Date`object, using the given`Calendar`object to construct the date. With a`Calendar`object, the driver can calculate the date taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the date |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDouble(parameterIndex: Int): Double
```

Retrieves the value of the designated JDBC`DOUBLE`parameter as a`double`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDouble(parameterName: String!): Double
```

Retrieves the value of a JDBC`DOUBLE`parameter as a`double`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFloat(parameterIndex: Int): Float
```

Retrieves the value of the designated JDBC`FLOAT`parameter as a`float`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFloat(parameterName: String!): Float
```

Retrieves the value of a JDBC`FLOAT`parameter as a`float`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInt(parameterIndex: Int): Int
```

Retrieves the value of the designated JDBC`INTEGER`parameter as an`int`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInt(parameterName: String!): Int
```

Retrieves the value of a JDBC`INTEGER`parameter as an`int`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLong(parameterIndex: Int): Long
```

Retrieves the value of the designated JDBC`BIGINT`parameter as a`long`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLong(parameterName: String!): Long
```

Retrieves the value of a JDBC`BIGINT`parameter as a`long`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNCharacterStream(parameterIndex: Int): Reader!
```

Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`parameters.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, ... |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a`java.io.Reader`object that contains the parameter value; if the value is SQL`NULL`, the value returned is`null`in the Java programming language. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getNCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNCharacterStream(parameterName: String!): Reader!
```

Retrieves the value of the designated parameter as a`java.io.Reader`object in the Java programming language. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`parameters.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a`java.io.Reader`object that contains the parameter value; if the value is SQL`NULL`, the value returned is`null`in the Java programming language |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNClob(parameterIndex: Int): NClob!
```

Retrieves the value of the designated JDBC`NCLOB`parameter as a`java.sql.NClob`object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | the parameter value as a`NClob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNClob(parameterName: String!): NClob!
```

Retrieves the value of a JDBC`NCLOB`parameter as a`java.sql.NClob`object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | the parameter value as a`NClob`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNString(parameterIndex: Int): String!
```

Retrieves the value of the designated`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`parameter as a`String`in the Java programming language.

For the fixed-length type JDBC`NCHAR`, the`String`object returned has exactly the same value the SQL`NCHAR`value had in the database, including any padding added by the database.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`object that maps an`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNString(parameterName: String!): String!
```

Retrieves the value of the designated`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`parameter as a`String`in the Java programming language.

For the fixed-length type JDBC`NCHAR`, the`String`object returned has exactly the same value the SQL`NCHAR`value had in the database, including any padding added by the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`object that maps an`NCHAR`,`NVARCHAR`or`LONGNVARCHAR`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(parameterIndex: Int): Any!
```

Retrieves the value of the designated parameter as an`Object`in the Java programming language. If the value is an SQL`NULL`, the driver returns a Java`null`.

This method returns a Java object whose type corresponds to the JDBC type that was registered for this parameter using the method`registerOutParameter`. By registering the target JDBC type as`java.sql.Types.OTHER`, this method can be used to read database-specific abstract data types.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | A`java.lang.Object`holding the OUT parameter value |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(
    parameterIndex: Int, 
    map: MutableMap<String!, Class<*>!>!
): Any!
```

Returns an object representing the value of OUT parameter`parameterIndex`and uses`map`for the custom mapping of the parameter value.

This method returns a Java object whose type corresponds to the JDBC type that was registered for this parameter using the method`registerOutParameter`. By registering the target JDBC type as`java.sql.Types.OTHER`, this method can be used to read database-specific abstract data types.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!\>!:the mapping from SQL type names to Java classes |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a`java.lang.Object`holding the OUT parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(parameterName: String!): Any!
```

Retrieves the value of a parameter as an`Object`in the Java programming language. If the value is an SQL`NULL`, the driver returns a Java`null`.

This method returns a Java object whose type corresponds to the JDBC type that was registered for this parameter using the method`registerOutParameter`. By registering the target JDBC type as`java.sql.Types.OTHER`, this method can be used to read database-specific abstract data types.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | A`java.lang.Object`holding the OUT parameter value. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getObject(
    parameterName: String!, 
    map: MutableMap<String!, Class<*>!>!
): Any!
```

Returns an object representing the value of OUT parameter`parameterName`and uses`map`for the custom mapping of the parameter value.

This method returns a Java object whose type corresponds to the JDBC type that was registered for this parameter using the method`registerOutParameter`. By registering the target JDBC type as`java.sql.Types.OTHER`, this method can be used to read database-specific abstract data types.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!\>!:the mapping from SQL type names to Java classes |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a`java.lang.Object`holding the OUT parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRef(parameterIndex: Int): Ref!
```

Retrieves the value of the designated JDBC`REF(<structured-type>)`parameter as a [java.sql.Ref](https://developer.android.com/reference/kotlin/java/sql/Ref) object in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | the parameter value as a`Ref`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRef(parameterName: String!): Ref!
```

Retrieves the value of a JDBC`REF(<structured-type>)`parameter as a [java.sql.Ref](https://developer.android.com/reference/kotlin/java/sql/Ref) object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | the parameter value as a`Ref`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRowId(parameterIndex: Int): RowId!
```

Retrieves the value of the designated JDBC`ROWID`parameter as a`java.sql.RowId`object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2,... |

| Return ||
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | a`RowId`object that represents the JDBC`ROWID`value is used as the designated parameter. If the parameter contains a SQL`NULL`, then a`null`value is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRowId(parameterName: String!): RowId!
```

Retrieves the value of the designated JDBC`ROWID`parameter as a`java.sql.RowId`object.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | a`RowId`object that represents the JDBC`ROWID`value is used as the designated parameter. If the parameter contains a SQL`NULL`, then a`null`value is returned. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSQLXML(parameterIndex: Int): SQLXML!
```

Retrieves the value of the designated`SQL XML`parameter as a`java.sql.SQLXML`object in the Java programming language.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first parameter is 1, the second is 2, ... |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | a`SQLXML`object that maps an`SQL XML`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSQLXML(parameterName: String!): SQLXML!
```

Retrieves the value of the designated`SQL XML`parameter as a`java.sql.SQLXML`object in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | a`SQLXML`object that maps an`SQL XML`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShort(parameterIndex: Int): Short
```

Retrieves the value of the designated JDBC`SMALLINT`parameter as a`short`in the Java programming language.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getShort(parameterName: String!): Short
```

Retrieves the value of a JDBC`SMALLINT`parameter as a`short`in the Java programming language.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the parameter value. If the value is SQL`NULL`, the result is`0`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getString(parameterIndex: Int): String!
```

Retrieves the value of the designated JDBC`CHAR`,`VARCHAR`, or`LONGVARCHAR`parameter as a`String`in the Java programming language.

For the fixed-length type JDBC`CHAR`, the`String`object returned has exactly the same value the SQL`CHAR`value had in the database, including any padding added by the database.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getString(parameterName: String!): String!
```

Retrieves the value of a JDBC`CHAR`,`VARCHAR`, or`LONGVARCHAR`parameter as a`String`in the Java programming language.

For the fixed-length type JDBC`CHAR`, the`String`object returned has exactly the same value the SQL`CHAR`value had in the database, including any padding added by the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTime(parameterIndex: Int): Time!
```

Retrieves the value of the designated JDBC`TIME`parameter as a`java.sql.Time`object.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTime(
    parameterIndex: Int, 
    cal: Calendar!
): Time!
```

Retrieves the value of the designated JDBC`TIME`parameter as a`java.sql.Time`object, using the given`Calendar`object to construct the time. With a`Calendar`object, the driver can calculate the time taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the time |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | the parameter value; if the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTime(parameterName: String!): Time!
```

Retrieves the value of a JDBC`TIME`parameter as a`java.sql.Time`object.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTime(
    parameterName: String!, 
    cal: Calendar!
): Time!
```

Retrieves the value of a JDBC`TIME`parameter as a`java.sql.Time`object, using the given`Calendar`object to construct the time. With a`Calendar`object, the driver can calculate the time taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the time |

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | the parameter value; if the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(parameterIndex: Int): Timestamp!
```

Retrieves the value of the designated JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(
    parameterIndex: Int, 
    cal: Calendar!
): Timestamp!
```

Retrieves the value of the designated JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object, using the given`Calendar`object to construct the`Timestamp`object. With a`Calendar`object, the driver can calculate the timestamp taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the timestamp |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |

**See Also**

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(parameterName: String!): Timestamp!
```

Retrieves the value of a JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimestamp(
    parameterName: String!, 
    cal: Calendar!
): Timestamp!
```

Retrieves the value of a JDBC`TIMESTAMP`parameter as a`java.sql.Timestamp`object, using the given`Calendar`object to construct the`Timestamp`object. With a`Calendar`object, the driver can calculate the timestamp taking into account a custom timezone and locale. If no`Calendar`object is specified, the driver uses the default timezone and locale.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the timestamp |

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | the parameter value. If the value is SQL`NULL`, the result is`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURL(parameterIndex: Int): URL!
```

Retrieves the value of the designated JDBC`DATALINK`parameter as a`java.net.URL`object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2,... |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | a`java.net.URL`object that represents the JDBC`DATALINK`value used as the designated parameter |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs, this method is called on a closed`CallableStatement`, or if the URL being returned is not a valid URL on the Java platform |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### getURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURL(parameterName: String!): URL!
```

Retrieves the value of a JDBC`DATALINK`parameter as a`java.net.URL`object.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | the parameter value as a`java.net.URL`object in the Java programming language. If the value was SQL`NULL`, the value`null`is returned. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs, this method is called on a closed`CallableStatement`, or if there is a problem with the URL |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterIndex: Int, 
    sqlType: Int
): Unit
```

Registers the OUT parameter in ordinal position`parameterIndex`to the JDBC type`sqlType`. All OUT parameters must be registered before a stored procedure is executed.

The JDBC type specified by`sqlType`for an OUT parameter determines the Java type that must be used in the`get`method to read the value of that parameter.

If the JDBC type expected to be returned to this output parameter is specific to this particular database,`sqlType`should be`java.sql.Types.OTHER`. The method #getObject retrieves the value.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the JDBC type code defined by`java.sql.Types`. If the parameter is of JDBC type`NUMERIC`or`DECIMAL`, the version of`registerOutParameter`that accepts a scale value should be used. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterIndex: Int, 
    sqlType: Int, 
    scale: Int
): Unit
```

Registers the parameter in ordinal position`parameterIndex`to be of JDBC type`sqlType`. All OUT parameters must be registered before a stored procedure is executed.

The JDBC type specified by`sqlType`for an OUT parameter determines the Java type that must be used in the`get`method to read the value of that parameter.

This version of`registerOutParameter`should be used when the parameter is of JDBC type`NUMERIC`or`DECIMAL`.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2, and so on |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the SQL type code defined by`java.sql.Types`. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the desired number of digits to the right of the decimal point. It must be greater than or equal to zero. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterIndex: Int, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Registers the designated output parameter. This version of the method`registerOutParameter`should be used for a user-defined or`REF`output parameter. Examples of user-defined types include:`STRUCT`,`DISTINCT`,`JAVA_OBJECT`, and named array types.

All OUT parameters must be registered before a stored procedure is executed.

For a user-defined parameter, the fully-qualified SQL type name of the parameter should also be given, while a`REF`parameter requires that the fully-qualified type name of the referenced type be given. A JDBC driver that does not need the type code and type name information may ignore it. To be portable, however, applications should always provide these values for user-defined and`REF`parameters. Although it is intended for user-defined and`REF`parameters, this method may be used to register a parameter of any JDBC type. If the parameter does not have a user-defined or`REF`type, the*typeName*parameter is ignored.

**Note:**When reading the value of an out parameter, you must use the getter method whose Java type corresponds to the parameter's registered SQL type.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first parameter is 1, the second is 2,... |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully-qualified name of an SQL structured type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if the parameterIndex is not valid; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterName: String!, 
    sqlType: Int
): Unit
```

Registers the OUT parameter named`parameterName`to the JDBC type`sqlType`. All OUT parameters must be registered before a stored procedure is executed.

The JDBC type specified by`sqlType`for an OUT parameter determines the Java type that must be used in the`get`method to read the value of that parameter.

If the JDBC type expected to be returned to this output parameter is specific to this particular database,`sqlType`should be`java.sql.Types.OTHER`. The method #getObject retrieves the value.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the JDBC type code defined by`java.sql.Types`. If the parameter is of JDBC type`NUMERIC`or`DECIMAL`, the version of`registerOutParameter`that accepts a scale value should be used. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type or if the JDBC driver does not support this method |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterName: String!, 
    sqlType: Int, 
    scale: Int
): Unit
```

Registers the parameter named`parameterName`to be of JDBC type`sqlType`. All OUT parameters must be registered before a stored procedure is executed.

The JDBC type specified by`sqlType`for an OUT parameter determines the Java type that must be used in the`get`method to read the value of that parameter.

This version of`registerOutParameter`should be used when the parameter is of JDBC type`NUMERIC`or`DECIMAL`.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):SQL type code defined by`java.sql.Types`. |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the desired number of digits to the right of the decimal point. It must be greater than or equal to zero. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type or if the JDBC driver does not support this method |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### registerOutParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun registerOutParameter(
    parameterName: String!, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Registers the designated output parameter. This version of the method`registerOutParameter`should be used for a user-named or REF output parameter. Examples of user-named types include: STRUCT, DISTINCT, JAVA_OBJECT, and named array types.

All OUT parameters must be registered before a stored procedure is executed.

For a user-named parameter the fully-qualified SQL type name of the parameter should also be given, while a REF parameter requires that the fully-qualified type name of the referenced type be given. A JDBC driver that does not need the type code and type name information may ignore it. To be portable, however, applications should always provide these values for user-named and REF parameters. Although it is intended for user-named and REF parameters, this method may be used to register a parameter of any JDBC type. If the parameter does not have a user-named or REF type, the typeName parameter is ignored.

**Note:** When reading the value of an out parameter, you must use the`getXXX`method whose Java type XXX corresponds to the parameter's registered SQL type.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully-qualified name of an SQL structured type |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`sqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type or if the JDBC driver does not support this method |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

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
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |

### setAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setAsciiStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(
    parameterName: String!, 
    x: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large ASCII value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.InputStream`. Data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from ASCII to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the Java input stream that contains the ASCII parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

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
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |

### setBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(
    parameterName: String!, 
    x: InputStream!, 
    length: Long
): Unit
```

Sets the designated parameter to the given input stream, which will have the specified number of bytes. When a very large binary value is input to a`LONGVARBINARY`parameter, it may be more practical to send it via a`java.io.InputStream`object. The data will be read from the stream as needed until end-of-file is reached.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the java input stream which contains the binary parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
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
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of bytes in the parameter data. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the length specified is less than zero; if the number of bytes in the inputstream does not match the specfied length; if a database access error occurs or this method is called on a closed`CallableStatement` |
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
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)!:a`Blob`object that maps an SQL`BLOB`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the Unicode data |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |

### setCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the UNICODE data used as the designated parameter |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(
    parameterName: String!, 
    reader: Reader!, 
    length: Long
): Unit
```

Sets the designated parameter to the given`Reader`object, which is the given number of characters long. When a very large UNICODE value is input to a`LONGVARCHAR`parameter, it may be more practical to send it via a`java.io.Reader`object. The data will be read from the stream as needed until end-of-file is reached. The JDBC driver will do any necessary conversion from UNICODE to the database char format.

**Note:**This stream object can either be a standard Java stream object or your own subclass that implements the standard interface.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the`java.io.Reader`object that contains the UNICODE data used as the designated parameter |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the stream |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the length specified is less than zero; a database access error occurs or this method is called on a closed`CallableStatement` |
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
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)!:a`Clob`object that maps an SQL`CLOB`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Date](https://developer.android.com/reference/kotlin/java/sql/Date)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the date |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

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
| `value` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the parameter value |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs; or this method is called on a closed`CallableStatement` |
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
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set |
| `value` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:the parameter value |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
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
| `reader` | [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!:An object that contains the data to set the parameter value to. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of characters in the parameter data. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the length specified is less than zero; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
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
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set |
| `value` | [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)!:the parameter value |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNString(
    parameterName: String!, 
    value: String!
): Unit
```

Sets the designated parameter to the given`String`object. The driver converts this to a SQL`NCHAR`or`NVARCHAR`or`LONGNVARCHAR`

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter to be set |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the parameter value |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if the driver does not support national character sets; if the driver can detect that a data conversion error could occur; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNull(
    parameterName: String!, 
    sqlType: Int, 
    typeName: String!
): Unit
```

Sets the designated parameter to SQL`NULL`. This version of the method`setNull`should be used for user-defined types and REF type parameters. Examples of user-defined types include: STRUCT, DISTINCT, JAVA_OBJECT, and named array types.

**Note:**To be portable, applications must give the SQL type code and the fully-qualified SQL type name when specifying a NULL user-defined or REF parameter. In the case of a user-defined type the name is the type name of the parameter itself. For a REF parameter, the name is the type name of the referenced type.

Although it is intended for user-defined and Ref parameters, this method may be used to set a null parameter of any JDBC type. If the parameter does not have a user-defined or REF type, the given typeName is ignored.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `sqlType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a value from`java.sql.Types` |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the fully-qualified name of an SQL user-defined type; ignored if the parameter is not a user-defined type or SQL`REF`value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

**Note:** Not all databases allow for a non-typed Null to be sent to the backend. For maximum portability, the`setNull`or the`setObject(String parameterName, Object x, int sqlType)`method should be used instead of`setObject(String parameterName, Object x)`.

<br />

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `x` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the object containing the input parameter value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs, this method is called on a closed`CallableStatement`or if the given`Object`parameter is ambiguous |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

### setObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):for java.sql.Types.DECIMAL or java.sql.Types.NUMERIC types, this is the number of digits after the decimal point. For all other types, this value will be ignored. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if`targetSqlType`is a`ARRAY`,`BLOB`,`CLOB`,`DATALINK`,`JAVA_OBJECT`,`NCHAR`,`NCLOB`,`NVARCHAR`,`LONGNVARCHAR`,`REF`,`ROWID`,`SQLXML`or`STRUCT`data type and the JDBC driver does not support this data type |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

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
| `x` | [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

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
|-----------------|----------------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `xmlObject` | [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)!:a`SQLXML`object that maps an`SQL XML`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs; this method is called on a closed`CallableStatement`or the`java.xml.transform.Result`,`Writer`or`OutputStream`has not been closed for the`SQLXML`object |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Time](https://developer.android.com/reference/kotlin/java/sql/Time)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the time |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!:the parameter value |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `x` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)!:the parameter value |
| `cal` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:the`Calendar`object the driver will use to construct the timestamp |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs or this method is called on a closed`CallableStatement` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setURL(
    parameterName: String!, 
    val: URL!
): Unit
```

Sets the designated parameter to the given`java.net.URL`object. The driver converts this to an SQL`DATALINK`value when it sends it to the database.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the parameter |
| `val` | [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)!:the parameter value |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if parameterName does not correspond to a named parameter; if a database access error occurs; this method is called on a closed`CallableStatement`or if a URL is malformed |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### wasNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun wasNull(): Boolean
```

Retrieves whether the last OUT parameter read had the value of SQL`NULL`. Note that this method should be called only after calling a getter method; otherwise, there is no value to use in determining whether it is`null`or not.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the last parameter read was SQL`NULL`;`false`otherwise |

| Exceptions ||
|-------------------------|-------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called on a closed`CallableStatement` |
