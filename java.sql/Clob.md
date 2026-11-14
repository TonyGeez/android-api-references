# Clob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Clob

```
interface Clob
```

| [java.sql.Clob](https://developer.android.com/reference/kotlin/java/sql/Clob#) |

| Known Direct Subclasses [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob) |------------------------------------------------------------------------|------------------------------------------------------------------------| | [NClob](https://developer.android.com/reference/kotlin/java/sql/NClob) | The mapping in the JavaTM programming language for the SQL`NCLOB`type. | |

The mapping in the JavaTM programming language for the SQL`CLOB`type. An SQL`CLOB`is a built-in type that stores a Character Large Object as a column value in a row of a database table. By default drivers implement a`Clob`object using an SQL`locator(CLOB)`, which means that a`Clob`object contains a logical pointer to the SQL`CLOB`data rather than the data itself. A`Clob`object is valid for the duration of the transaction in which it was created.

The`Clob`interface provides methods for getting the length of an SQL`CLOB`(Character Large Object) value, for materializing a`CLOB`value on the client, and for searching for a substring or`CLOB`object within a`CLOB`value. Methods in the interfaces [ResultSet](https://developer.android.com/reference/kotlin/java/sql/ResultSet), [CallableStatement](https://developer.android.com/reference/kotlin/java/sql/CallableStatement), and [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement), such as`getClob`and`setClob`allow a programmer to access an SQL`CLOB`value. In addition, this interface has methods for updating a`CLOB`value.

All methods on the`Clob`interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [free](https://developer.android.com/reference/kotlin/java/sql/Clob#free())`()` This method frees the`Clob`object and releases the resources the resources that it holds. |
| abstract [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getAsciiStream](https://developer.android.com/reference/kotlin/java/sql/Clob#getAsciiStream())`()` Retrieves the`CLOB`value designated by this`Clob`object as an ascii stream. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/java/sql/Clob#getCharacterStream())`()` Retrieves the`CLOB`value designated by this`Clob`object as a`java.io.Reader`object (or as a stream of characters). |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/java/sql/Clob#getCharacterStream(kotlin.Long,%20kotlin.Long))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a`Reader`object that contains a partial`Clob`value, starting with the character specified by pos, which is length characters in length. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubString](https://developer.android.com/reference/kotlin/java/sql/Clob#getSubString(kotlin.Long,%20kotlin.Int))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves a copy of the specified substring in the`CLOB`value designated by this`Clob`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [length](https://developer.android.com/reference/kotlin/java/sql/Clob#length())`()` Retrieves the number of characters in the`CLOB`value designated by this`Clob`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](https://developer.android.com/reference/kotlin/java/sql/Clob#position(kotlin.String,%20kotlin.Long))`(`searchstr:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves the character position at which the specified substring`searchstr`appears in the SQL`CLOB`value represented by this`Clob`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](https://developer.android.com/reference/kotlin/java/sql/Clob#position(java.sql.Clob,%20kotlin.Long))`(`searchstr:` ` [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob#)!`, `start:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves the character position at which the specified`Clob`object`searchstr`appears in this`Clob`object. |
| abstract [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/Clob#setAsciiStream(kotlin.Long))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves a stream to be used to write Ascii characters to the`CLOB`value that this`Clob`object represents, starting at position`pos`. |
| abstract [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/Clob#setCharacterStream(kotlin.Long))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves a stream to be used to write a stream of Unicode characters to the`CLOB`value that this`Clob`object represents, at position`pos`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/Clob#setString(kotlin.Long,%20kotlin.String))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Writes the given Java`String`to the`CLOB`value that this`Clob`object designates at the position`pos`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/Clob#setString(kotlin.Long,%20kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`characters of`str`, starting at character`offset`, to the`CLOB`value that this`Clob`represents. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [truncate](https://developer.android.com/reference/kotlin/java/sql/Clob#truncate(kotlin.Long))`(`len:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Truncates the`CLOB`value that this`Clob`designates to have a length of`len`characters. |

## Public methods

### free

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun free(): Unit
```

This method frees the`Clob`object and releases the resources the resources that it holds. The object is invalid once the`free`method is called.

After`free`has been called, any attempt to invoke a method other than`free`will result in a`SQLException`being thrown. If`free`is called multiple times, the subsequent calls to`free`are treated as a no-op.

<br />

| Exceptions ||
|--------------------------------------------|---------------------------------------------------|
| `java.sql.SQLException` | if an error occurs releasing the Clob's resources |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAsciiStream(): InputStream!
```

Retrieves the`CLOB`value designated by this`Clob`object as an ascii stream.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | a`java.io.InputStream`object containing the`CLOB`data |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setAsciiStream](https://developer.android.com/reference/kotlin/java/sql/Clob#setAsciiStream(kotlin.Long)) 

### getCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(): Reader!
```

Retrieves the`CLOB`value designated by this`Clob`object as a`java.io.Reader`object (or as a stream of characters).

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a`java.io.Reader`object containing the`CLOB`data |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/Clob#setCharacterStream(kotlin.Long)) 

### getCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(
    pos: Long, 
    length: Long
): Reader!
```

Returns a`Reader`object that contains a partial`Clob`value, starting with the character specified by pos, which is length characters in length.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset to the first character of the partial value to be retrieved. The first character in the Clob is at position 1. |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in characters of the partial value to be retrieved. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | `Reader`through which the partial`Clob`value can be read. |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if pos is less than 1 or if pos is greater than the number of characters in the`Clob`or if pos + length is greater than the number of characters in the`Clob` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getSubString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSubString(
    pos: Long, 
    length: Int
): String!
```

Retrieves a copy of the specified substring in the`CLOB`value designated by this`Clob`object. The substring begins at position`pos`and has up to`length`consecutive characters.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the first character of the substring to be extracted. The first character is at position 1. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of consecutive characters to be copied; the value for length must be 0 or greater |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`that is the specified substring in the`CLOB`value designated by this`Clob`object |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value; if pos is less than 1 or length is less than 0 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun length(): Long
```

Retrieves the number of characters in the`CLOB`value designated by this`Clob`object.

| Return ||
|------------------------------------------------------------------------------|----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | length of the`CLOB`in characters |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the length of the`CLOB`value |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(
    searchstr: String!, 
    start: Long
): Long
```

Retrieves the character position at which the specified substring`searchstr`appears in the SQL`CLOB`value represented by this`Clob`object. The search begins at position`start`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `searchstr` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the substring for which to search |
| `start` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to begin searching; the first position is 1 |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the position at which the substring appears or -1 if it is not present; the first position is 1 |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(
    searchstr: Clob!, 
    start: Long
): Long
```

Retrieves the character position at which the specified`Clob`object`searchstr`appears in this`Clob`object. The search begins at position`start`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `searchstr` | [Clob](https://developer.android.com/reference/kotlin/java/sql/Clob#)!:the`Clob`object for which to search |
| `start` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to begin searching; the first position is 1 |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the position at which the`Clob`object appears or -1 if it is not present; the first position is 1 |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if start is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setAsciiStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAsciiStream(pos: Long): OutputStream!
```

Retrieves a stream to be used to write Ascii characters to the`CLOB`value that this`Clob`object represents, starting at position`pos`. Characters written to the stream will overwrite the existing characters in the`Clob`object starting at the position`pos`. If the end of the`Clob`value is reached while writing characters to the stream, then the length of the`Clob`value will be increased to accomodate the extra characters.

**Note:** If the value specified for`pos`is greater then the length+1 of the`CLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to start writing to this`CLOB`object; The first position is 1 |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | the stream to which ASCII encoded characters can be written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#getAsciiStream](https://developer.android.com/reference/kotlin/java/sql/Clob#getAsciiStream()) 

### setCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(pos: Long): Writer!
```

Retrieves a stream to be used to write a stream of Unicode characters to the`CLOB`value that this`Clob`object represents, at position`pos`. Characters written to the stream will overwrite the existing characters in the`Clob`object starting at the position`pos`. If the end of the`Clob`value is reached while writing characters to the stream, then the length of the`Clob`value will be increased to accomodate the extra characters.

**Note:** If the value specified for`pos`is greater then the length+1 of the`CLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to start writing to the`CLOB`value; The first position is 1 |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | a stream to which Unicode encoded characters can be written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(
    pos: Long, 
    str: String!
): Int
```

Writes the given Java`String`to the`CLOB`value that this`Clob`object designates at the position`pos`. The string will overwrite the existing characters in the`Clob`object starting at the position`pos`. If the end of the`Clob`value is reached while writing the given string, then the length of the`Clob`value will be increased to accomodate the extra characters.

**Note:** If the value specified for`pos`is greater then the length+1 of the`CLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to start writing to the`CLOB`value that this`Clob`object represents; The first position is 1 |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be written to the`CLOB`value that this`Clob`designates |

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of characters written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(
    pos: Long, 
    str: String!, 
    offset: Int, 
    len: Int
): Int
```

Writes`len`characters of`str`, starting at character`offset`, to the`CLOB`value that this`Clob`represents. The string will overwrite the existing characters in the`Clob`object starting at the position`pos`. If the end of the`Clob`value is reached while writing the given string, then the length of the`Clob`value will be increased to accomodate the extra characters.

**Note:** If the value specified for`pos`is greater then the length+1 of the`CLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to start writing to this`CLOB`object; The first position is 1 |
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be written to the`CLOB`value that this`Clob`object represents |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into`str`to start reading the characters to be written |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of characters to be written |

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of characters written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### truncate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun truncate(len: Long): Unit
```

Truncates the`CLOB`value that this`Clob`designates to have a length of`len`characters.

**Note:** If the value specified for`pos`is greater then the length+1 of the`CLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `len` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length, in characters, to which the`CLOB`value should be truncated |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`CLOB`value or if len is less than 0 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
