# SQLInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLInput

```
interface SQLInput
```

| [java.sql.SQLInput](../java/sql/SQLInput.md) |

An input stream that contains a stream of values representing an instance of an SQL structured type or an SQL distinct type. This interface, used only for custom mapping, is used by the driver behind the scenes, and a programmer never directly invokes`SQLInput`methods. The*reader* methods (`readLong`,`readBytes`, and so on) provide a way for an implementation of the`SQLData`interface to read the values in an`SQLInput`object. And as described in`SQLData`, calls to reader methods must be made in the order that their corresponding attributes appear in the SQL definition of the type. The method`wasNull`is used to determine whether the last value read was SQL`NULL`.

When the method`getObject`is called with an object of a class implementing the interface`SQLData`, the JDBC driver calls the method`SQLData.getSQLType`to determine the SQL type of the user-defined type (UDT) being custom mapped. The driver creates an instance of`SQLInput`, populating it with the attributes of the UDT. The driver then passes the input stream to the method`SQLData.readSQL`, which in turn calls the`SQLInput`reader methods in its implementation for reading the attributes from the input stream.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](../java/sql/Array.md)! | [readArray](../java/sql/SQLInput.md))`()` Reads an SQL`ARRAY`value from the stream and returns it as an`Array`object in the Java programming language. |
| abstract [InputStream](../java/io/InputStream.md)! | [readAsciiStream](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a stream of ASCII characters. |
| abstract [BigDecimal](../java/math/BigDecimal.md)! | [readBigDecimal](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`java.math.BigDecimal`object in the Java programming language. |
| --- | --- |
| abstract [InputStream](../java/io/InputStream.md)! | [readBinaryStream](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a stream of uninterpreted bytes. |
| abstract [Blob](../java/sql/Blob.md)! | [readBlob](../java/sql/SQLInput.md))`()` Reads an SQL`BLOB`value from the stream and returns it as a`Blob`object in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [readBoolean](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`boolean`in the Java programming language. |
| --- | --- |
| abstract [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [readByte](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`byte`in the Java programming language. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [readBytes](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as an array of bytes in the Java programming language. |
| abstract [Reader](../java/io/Reader.md)! | [readCharacterStream](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a stream of Unicode characters. |
| --- | --- |
| abstract [Clob](../java/sql/Clob.md)! | [readClob](../java/sql/SQLInput.md))`()` Reads an SQL`CLOB`value from the stream and returns it as a`Clob`object in the Java programming language. |
| abstract [Date](../java/sql/Date.md)! | [readDate](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`java.sql.Date`object. |
| abstract [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [readDouble](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`double`in the Java programming language. |
| --- | --- |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [readFloat](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`float`in the Java programming language. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readInt](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as an`int`in the Java programming language. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLong](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`long`in the Java programming language. |
| --- | --- |
| abstract [NClob](../java/sql/NClob.md)! | [readNClob](../java/sql/SQLInput.md))`()` Reads an SQL`NCLOB`value from the stream and returns it as a`NClob`object in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readNString](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`String`in the Java programming language. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readObject](../java/sql/SQLInput.md))`()` Reads the datum at the head of the stream and returns it as an`Object`in the Java programming language. |
| --- | --- |
| abstract [Ref](../java/sql/Ref.md)! | [readRef](../java/sql/SQLInput.md))`()` Reads an SQL`REF`value from the stream and returns it as a`Ref`object in the Java programming language. |
| abstract [RowId](../java/sql/RowId.md)! | [readRowId](../java/sql/SQLInput.md))`()` Reads an SQL`ROWID`value from the stream and returns it as a`RowId`object in the Java programming language. |
| abstract [SQLXML](../java/sql/SQLXML.md)! | [readSQLXML](../java/sql/SQLInput.md))`()` Reads an SQL`XML`value from the stream and returns it as a`SQLXML`object in the Java programming language. |
| --- | --- |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [readShort](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`short`in the Java programming language. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readString](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`String`in the Java programming language. |
| abstract [Time](../java/sql/Time.md)! | [readTime](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`java.sql.Time`object. |
| --- | --- |
| abstract [Timestamp](../java/sql/Timestamp.md)! | [readTimestamp](../java/sql/SQLInput.md))`()` Reads the next attribute in the stream and returns it as a`java.sql.Timestamp`object. |
| abstract [URL](../java/net/URL.md)! | [readURL](../java/sql/SQLInput.md))`()` Reads an SQL`DATALINK`value from the stream and returns it as a`java.net.URL`object in the Java programming language. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasNull](../java/sql/SQLInput.md))`()` Retrieves whether the last value read was SQL`NULL`. |
| --- | --- |

## Public methods

### readArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readArray(): Array!
```

Reads an SQL`ARRAY`value from the stream and returns it as an`Array`object in the Java programming language.

| Return ||
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Array](../java/sql/Array.md)! | an`Array`object representing data of the SQL`ARRAY`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [InputStream](../java/io/InputStream.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [BigDecimal](../java/math/BigDecimal.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [InputStream](../java/io/InputStream.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [Blob](../java/sql/Blob.md)! | a`Blob`object representing data of the SQL`BLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [Reader](../java/io/Reader.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [Clob](../java/sql/Clob.md)! | a`Clob`object representing data of the SQL`CLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [Date](../java/sql/Date.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [NClob](../java/sql/NClob.md)! | a`NClob`object representing data of the SQL`NCLOB`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [Ref](../java/sql/Ref.md)! | a`Ref`object representing the SQL`REF`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [RowId](../java/sql/RowId.md)! | a`RowId`object representing data of the SQL`ROWID`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [SQLXML](../java/sql/SQLXML.md)! | a`SQLXML`object representing data of the SQL`XML`value at the head of the stream;`null`if the value read is SQL`NULL` |

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
| [Time](../java/sql/Time.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [Timestamp](../java/sql/Timestamp.md)! | the attribute; if the value is SQL`NULL`, returns`null` |

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
| [URL](../java/net/URL.md)! | a`java.net.URL`object. |

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
