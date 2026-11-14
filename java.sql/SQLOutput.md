# SQLOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLOutput

```
interface SQLOutput
```

| [java.sql.SQLOutput](../java/sql/SQLOutput.md) |

The output stream for writing the attributes of a user-defined type back to the database. This interface, used only for custom mapping, is used by the driver, and its methods are never directly invoked by a programmer.

When an object of a class implementing the interface`SQLData`is passed as an argument to an SQL statement, the JDBC driver calls the method`SQLData.getSQLType`to determine the kind of SQL datum being passed to the database. The driver then creates an instance of`SQLOutput`and passes it to the method`SQLData.writeSQL`. The method`writeSQL`in turn calls the appropriate`SQLOutput`*writer* methods`writeBoolean`,`writeCharacterStream`, and so on) to write data from the`SQLData`object to the`SQLOutput`output stream as the representation of an SQL user-defined type.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeArray](../java/sql/SQLOutput.md))`(`x:` ` [Array](../java/sql/Array.md)!`)` Writes an SQL`ARRAY`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeAsciiStream](../java/sql/SQLOutput.md))`(`x:` ` [InputStream](../java/io/InputStream.md)!`)` Writes the next attribute to the stream as a stream of ASCII characters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBigDecimal](../java/sql/SQLOutput.md))`(`x:` ` [BigDecimal](../java/math/BigDecimal.md)!`)` Writes the next attribute to the stream as a java. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBinaryStream](../java/sql/SQLOutput.md))`(`x:` ` [InputStream](../java/io/InputStream.md)!`)` Writes the next attribute to the stream as a stream of uninterpreted bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBlob](../java/sql/SQLOutput.md))`(`x:` ` [Blob](../java/sql/Blob.md)!`)` Writes an SQL`BLOB`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBoolean](../java/sql/SQLOutput.md))`(`x:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Writes the next attribute to the stream as a Java boolean. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeByte](../java/sql/SQLOutput.md))`(`x:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Writes the next attribute to the stream as a Java byte. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeBytes](../java/sql/SQLOutput.md))`(`x:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes the next attribute to the stream as an array of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeCharacterStream](../java/sql/SQLOutput.md))`(`x:` ` [Reader](../java/io/Reader.md)!`)` Writes the next attribute to the stream as a stream of Unicode characters. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeClob](../java/sql/SQLOutput.md))`(`x:` ` [Clob](../java/sql/Clob.md)!`)` Writes an SQL`CLOB`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDate](../java/sql/SQLOutput.md))`(`x:` ` [Date](../java/sql/Date.md)!`)` Writes the next attribute to the stream as a java. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDouble](../java/sql/SQLOutput.md))`(`x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Writes the next attribute to the stream as a Java double. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeFloat](../java/sql/SQLOutput.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Writes the next attribute to the stream as a Java float. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeInt](../java/sql/SQLOutput.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the next attribute to the stream as a Java int. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeLong](../java/sql/SQLOutput.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Writes the next attribute to the stream as a Java long. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNClob](../java/sql/SQLOutput.md))`(`x:` ` [NClob](../java/sql/NClob.md)!`)` Writes an SQL`NCLOB`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeNString](../java/sql/SQLOutput.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes the next attribute to the stream as a`String`in the Java programming language. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeObject](../java/sql/SQLOutput.md))`(`x:` ` [SQLData](../java/sql/SQLData.md)!`)` Writes to the stream the data contained in the given`SQLData`object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeRef](../java/sql/SQLOutput.md))`(`x:` ` [Ref](../java/sql/Ref.md)!`)` Writes an SQL`REF`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeRowId](../java/sql/SQLOutput.md))`(`x:` ` [RowId](../java/sql/RowId.md)!`)` Writes an SQL`ROWID`value to the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeSQLXML](../java/sql/SQLOutput.md))`(`x:` ` [SQLXML](../java/sql/SQLXML.md)!`)` Writes an SQL`XML`value to the stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeShort](../java/sql/SQLOutput.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Writes the next attribute to the stream as a Java short. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeString](../java/sql/SQLOutput.md))`(`x:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes the next attribute to the stream as a`String`in the Java programming language. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeStruct](../java/sql/SQLOutput.md))`(`x:` ` [Struct](../java/sql/Struct.md)!`)` Writes an SQL structured type value to the stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTime](../java/sql/SQLOutput.md))`(`x:` ` [Time](../java/sql/Time.md)!`)` Writes the next attribute to the stream as a java. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeTimestamp](../java/sql/SQLOutput.md))`(`x:` ` [Timestamp](../java/sql/Timestamp.md)!`)` Writes the next attribute to the stream as a java. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeURL](../java/sql/SQLOutput.md))`(`x:` ` [URL](../java/net/URL.md)!`)` Writes a SQL`DATALINK`value to the stream. |
| --- | --- |

## Public methods

### writeArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeArray(x: Array!): Unit
```

Writes an SQL`ARRAY`value to the stream.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Array](../java/sql/Array.md)!:an`Array`object representing data of an SQL`ARRAY`type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeAsciiStream(x: InputStream!): Unit
```

Writes the next attribute to the stream as a stream of ASCII characters.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [InputStream](../java/io/InputStream.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBigDecimal(x: BigDecimal!): Unit
```

Writes the next attribute to the stream as a java.math.BigDecimal object. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [BigDecimal](../java/math/BigDecimal.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBinaryStream(x: InputStream!): Unit
```

Writes the next attribute to the stream as a stream of uninterpreted bytes.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [InputStream](../java/io/InputStream.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBlob(x: Blob!): Unit
```

Writes an SQL`BLOB`value to the stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [Blob](../java/sql/Blob.md)!:a`Blob`object representing data of an SQL`BLOB`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBoolean(x: Boolean): Unit
```

Writes the next attribute to the stream as a Java boolean. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------|
| `x` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeByte(x: Byte): Unit
```

Writes the next attribute to the stream as a Java byte. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `x` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeBytes(x: ByteArray!): Unit
```

Writes the next attribute to the stream as an array of bytes. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeCharacterStream(x: Reader!): Unit
```

Writes the next attribute to the stream as a stream of Unicode characters.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `x` | [Reader](../java/io/Reader.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeClob(x: Clob!): Unit
```

Writes an SQL`CLOB`value to the stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `x` | [Clob](../java/sql/Clob.md)!:a`Clob`object representing data of an SQL`CLOB`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeDate(x: Date!): Unit
```

Writes the next attribute to the stream as a java.sql.Date object. Writes the next attribute to the stream as a`java.sql.Date`object in the Java programming language.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Date](../java/sql/Date.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeDouble(x: Double): Unit
```

Writes the next attribute to the stream as a Java double. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeFloat(x: Float): Unit
```

Writes the next attribute to the stream as a Java float. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeInt(x: Int): Unit
```

Writes the next attribute to the stream as a Java int. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeLong(x: Long): Unit
```

Writes the next attribute to the stream as a Java long. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeNClob(x: NClob!): Unit
```

Writes an SQL`NCLOB`value to the stream.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `x` | [NClob](../java/sql/NClob.md)!:a`NClob`object representing data of an SQL`NCLOB`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeNString(x: String!): Unit
```

Writes the next attribute to the stream as a`String`in the Java programming language. The driver converts this to a SQL`NCHAR`or`NVARCHAR`or`LONGNVARCHAR`value (depending on the argument's size relative to the driver's limits on`NVARCHAR`values) when it sends it to the stream.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeObject(x: SQLData!): Unit
```

Writes to the stream the data contained in the given`SQLData`object. When the`SQLData`object is`null`, this method writes an SQL`NULL`to the stream. Otherwise, it calls the`SQLData.writeSQL`method of the given object, which writes the object's attributes to the stream. The implementation of the method`SQLData.writeSQ`calls the appropriate`SQLOutput`writer method(s) for writing each of the object's attributes in order. The attributes must be read from an`SQLInput`input stream and written to an`SQLOutput`output stream in the same order in which they were listed in the SQL definition of the user-defined type.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [SQLData](../java/sql/SQLData.md)!:the object representing data of an SQL structured or distinct type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeRef(x: Ref!): Unit
```

Writes an SQL`REF`value to the stream.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------|
| `x` | [Ref](../java/sql/Ref.md)!:a`Ref`object representing data of an SQL`REF`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeRowId(x: RowId!): Unit
```

Writes an SQL`ROWID`value to the stream.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `x` | [RowId](../java/sql/RowId.md)!:a`RowId`object representing data of an SQL`ROWID`value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeSQLXML(x: SQLXML!): Unit
```

Writes an SQL`XML`value to the stream.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `x` | [SQLXML](../java/sql/SQLXML.md)!:a`SQLXML`object representing data of an SQL`XML`value |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, the`java.xml.transform.Result`,`Writer`or`OutputStream`has not been closed for the`SQLXML`object or if there is an error processing the XML value. The`getCause`method of the exception may provide a more detailed exception, for example, if the stream does not contain valid XML. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeShort(x: Short): Unit
```

Writes the next attribute to the stream as a Java short. Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `x` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeString(x: String!): Unit
```

Writes the next attribute to the stream as a`String`in the Java programming language.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `x` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeStruct

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeStruct(x: Struct!): Unit
```

Writes an SQL structured type value to the stream.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Struct](../java/sql/Struct.md)!:a`Struct`object representing data of an SQL structured type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeTime(x: Time!): Unit
```

Writes the next attribute to the stream as a java.sql.Time object. Writes the next attribute to the stream as a`java.sql.Date`object in the Java programming language.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Time](../java/sql/Time.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeTimestamp(x: Timestamp!): Unit
```

Writes the next attribute to the stream as a java.sql.Timestamp object. Writes the next attribute to the stream as a`java.sql.Date`object in the Java programming language.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------|
| `x` | [Timestamp](../java/sql/Timestamp.md)!:the value to pass to the database |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### writeURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeURL(x: URL!): Unit
```

Writes a SQL`DATALINK`value to the stream.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [URL](../java/net/URL.md)!:a`java.net.URL`object representing the data of SQL DATALINK type |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
