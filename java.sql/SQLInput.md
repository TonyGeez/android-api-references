# SQLInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLInput

```
interface SQLInput
```

| [java.sql.SQLInput](https://developer.android.com/reference/kotlin/java/sql/SQLInput#) |

An input stream that contains a stream of values representing an instance of an SQL structured type or an SQL distinct type. This interface, used only for custom mapping, is used by the driver behind the scenes, and a programmer never directly invokes`SQLInput`methods. The*reader* methods (`readLong`,`readBytes`, and so on) provide a way for an implementation of the`SQLData`interface to read the values in an`SQLInput`object. And as described in`SQLData`, calls to reader methods must be made in the order that their corresponding attributes appear in the SQL definition of the type. The method`wasNull`is used to determine whether the last value read was SQL`NULL`.

When the method`getObject`is called with an object of a class implementing the interface`SQLData`, the JDBC driver calls the method`SQLData.getSQLType`to determine the SQL type of the user-defined type (UDT) being custom mapped. The driver creates an instance of`SQLInput`, populating it with the attributes of the UDT. The driver then passes the input stream to the method`SQLData.readSQL`, which in turn calls the`SQLInput`reader methods in its implementation for reading the attributes from the input stream.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | [readArray](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readArray())`()` Reads an SQL`ARRAY`value from the stream and returns it as an`Array`object in the Java programming language. |
| abstract [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [readAsciiStream](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readAsciiStream())`()` Reads the next attribute in the stream and returns it as a stream of ASCII characters. |
| abstract [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | [readBigDecimal](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readBigDecimal())`()` Reads the next attribute in the stream and returns it as a`java.math.BigDecimal`object in the Java programming language. |
| abstract [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [readBinaryStream](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readBinaryStream())`()` Reads the next attribute in the stream and returns it as a stream of uninterpreted bytes. |
| abstract [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | [readBlob](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readBlob())`()` Reads an SQL`BLOB`value from the stream and returns it as a`Blob`object in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [readBoolean](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readBoolean())`()` Reads the next attribute in the stream and returns it as a`boolean`in the Java programming language. |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [readByte](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readByte())`()` Reads the next attribute in the stream and returns it as a`byte`in the Java programming language. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readBytes](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readBytes())`()` Reads the next attribute in the stream and returns it as an array of bytes in the Java programming language. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [readCharacterStream](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readCharacterStream())`()` Reads the next attribute in the stream and returns it as a stream of Unicode characters. |
| abstract [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | [readClob](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readClob())`()` Reads an SQL`CLOB`value from the stream and returns it as a`Clob`object in the Java programming language. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | [readDate](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readDate())`()` Reads the next attribute in the stream and returns it as a`java.sql.Date`object. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [readDouble](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readDouble())`()` Reads the next attribute in the stream and returns it as a`double`in the Java programming language. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [readFloat](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readFloat())`()` Reads the next attribute in the stream and returns it as a`float`in the Java programming language. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readInt](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readInt())`()` Reads the next attribute in the stream and returns it as an`int`in the Java programming language. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLong](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readLong())`()` Reads the next attribute in the stream and returns it as a`long`in the Java programming language. |
| abstract [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | [readNClob](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readNClob())`()` Reads an SQL`NCLOB`value from the stream and returns it as a`NClob`object in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readNString](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readNString())`()` Reads the next attribute in the stream and returns it as a`String`in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readObject](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readObject())`()` Reads the datum at the head of the stream and returns it as an`Object`in the Java programming language. |
| abstract [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | [readRef](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readRef())`()` Reads an SQL`REF`value from the stream and returns it as a`Ref`object in the Java programming language. |
| abstract [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | [readRowId](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readRowId())`()` Reads an SQL`ROWID`value from the stream and returns it as a`RowId`object in the Java programming language. |
| abstract [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | [readSQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readSQLXML())`()` Reads an SQL`XML`value from the stream and returns it as a`SQLXML`object in the Java programming language. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [readShort](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readShort())`()` Reads the next attribute in the stream and returns it as a`short`in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readString](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readString())`()` Reads the next attribute in the stream and returns it as a`String`in the Java programming language. |
| abstract [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | [readTime](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readTime())`()` Reads the next attribute in the stream and returns it as a`java.sql.Time`object. |
| abstract [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | [readTimestamp](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readTimestamp())`()` Reads the next attribute in the stream and returns it as a`java.sql.Timestamp`object. |
| abstract [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | [readURL](https://developer.android.com/reference/kotlin/java/sql/SQLInput#readURL())`()` Reads an SQL`DATALINK`value from the stream and returns it as a`java.net.URL`object in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasNull](https://developer.android.com/reference/kotlin/java/sql/SQLInput#wasNull())`()` Retrieves whether the last value read was SQL`NULL`. |

## Public methods

### readArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readArray(): Array!
```

Reads an SQL`ARRAY`value from the stream and returns it as an`Array`object in the Java programming language.

| Return ||
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Array](https://developer.android.com/reference/kotlin/java/sql/Array)! | an`Array`object representing data of the SQL`ARRAY`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAsciiStream(): InputStream!
```

Reads the next attribute in the stream and returns it as a stream of ASCII characters.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBigDecimal(): BigDecimal!
```

Reads the next attribute in the stream and returns it as a`java.math.BigDecimal`object in the Java programming language.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBinaryStream(): InputStream!
```

Reads the next attribute in the stream and returns it as a stream of uninterpreted bytes.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBlob(): Blob!
```

Reads an SQL`BLOB`value from the stream and returns it as a`Blob`object in the Java programming language.

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Blob](https://developer.android.com/reference/kotlin/java/sql/Blob)! | a`Blob`object representing data of the SQL`BLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBoolean(): Boolean
```

Reads the next attribute in the stream and returns it as a`boolean`in the Java programming language.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the attribute; if the value is SQL`NULL`, returns`false` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readByte(): Byte
```

Reads the next attribute in the stream and returns it as a`byte`in the Java programming language.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readBytes(): ByteArray!
```

Reads the next attribute in the stream and returns it as an array of bytes in the Java programming language.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readCharacterStream(): Reader!
```

Reads the next attribute in the stream and returns it as a stream of Unicode characters.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readClob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readClob(): Clob!
```

Reads an SQL`CLOB`value from the stream and returns it as a`Clob`object in the Java programming language.

| Return ||
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob)! | a`Clob`object representing data of the SQL`CLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readDate(): Date!
```

Reads the next attribute in the stream and returns it as a`java.sql.Date`object.

| Return ||
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/sql/Date)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readDouble(): Double
```

Reads the next attribute in the stream and returns it as a`double`in the Java programming language.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readFloat(): Float
```

Reads the next attribute in the stream and returns it as a`float`in the Java programming language.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readInt(): Int
```

Reads the next attribute in the stream and returns it as an`int`in the Java programming language.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readLong(): Long
```

Reads the next attribute in the stream and returns it as a`long`in the Java programming language.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readNClob

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readNClob(): NClob!
```

Reads an SQL`NCLOB`value from the stream and returns it as a`NClob`object in the Java programming language.

| Return ||
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob)! | a`NClob`object representing data of the SQL`NCLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readNString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readNString(): String!
```

Reads the next attribute in the stream and returns it as a`String`in the Java programming language. It is intended for use when accessing`NCHAR`,`NVARCHAR`and`LONGNVARCHAR`columns.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readObject(): Any!
```

Reads the datum at the head of the stream and returns it as an`Object`in the Java programming language. The actual type of the object returned is determined by the default type mapping, and any customizations present in this stream's type map.

A type map is registered with the stream by the JDBC driver before the stream is passed to the application.

When the datum at the head of the stream is an SQL`NULL`, the method returns`null`. If the datum is an SQL structured or distinct type, it determines the SQL type of the datum at the head of the stream. If the stream's type map has an entry for that SQL type, the driver constructs an object of the appropriate class and calls the method`SQLData.readSQL`on that object, which reads additional data from the stream, using the protocol described for that method.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the datum at the head of the stream as an`Object`in the Java programming language;`null`if the datum is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readRef(): Ref!
```

Reads an SQL`REF`value from the stream and returns it as a`Ref`object in the Java programming language.

| Return ||
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Ref](https://developer.android.com/reference/kotlin/java/sql/Ref)! | a`Ref`object representing the SQL`REF`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readRowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readRowId(): RowId!
```

Reads an SQL`ROWID`value from the stream and returns it as a`RowId`object in the Java programming language.

| Return ||
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [RowId](https://developer.android.com/reference/kotlin/java/sql/RowId)! | a`RowId`object representing data of the SQL`ROWID`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readSQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readSQLXML(): SQLXML!
```

Reads an SQL`XML`value from the stream and returns it as a`SQLXML`object in the Java programming language.

| Return ||
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML)! | a`SQLXML`object representing data of the SQL`XML`value at the head of the stream;`null`if the value read is SQL`NULL` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readShort(): Short
```

Reads the next attribute in the stream and returns it as a`short`in the Java programming language.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the attribute; if the value is SQL`NULL`, returns`0` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readString(): String!
```

Reads the next attribute in the stream and returns it as a`String`in the Java programming language.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readTime(): Time!
```

Reads the next attribute in the stream and returns it as a`java.sql.Time`object.

| Return ||
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readTimestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readTimestamp(): Timestamp!
```

Reads the next attribute in the stream and returns it as a`java.sql.Timestamp`object.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp)! | the attribute; if the value is SQL`NULL`, returns`null` |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### readURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readURL(): URL!
```

Reads an SQL`DATALINK`value from the stream and returns it as a`java.net.URL`object in the Java programming language.

| Return ||
|---------------------------------------------------------------------------|------------------------|
| [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)! | a`java.net.URL`object. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs, or if a URL is malformed |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### wasNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun wasNull(): Boolean
```

Retrieves whether the last value read was SQL`NULL`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the most recently read SQL value was SQL`NULL`;`false`otherwise |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
