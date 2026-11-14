# Blob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Blob

```
interface Blob
```

| [java.sql.Blob](Blob.md) |

The representation (mapping) in the JavaTM programming language of an SQL`BLOB`value. An SQL`BLOB`is a built-in type that stores a Binary Large Object as a column value in a row of a database table. By default drivers implement`Blob`using an SQL`locator(BLOB)`, which means that a`Blob`object contains a logical pointer to the SQL`BLOB`data rather than the data itself. A`Blob`object is valid for the duration of the transaction in which is was created.

Methods in the interfaces [ResultSet](ResultSet.md), [CallableStatement](CallableStatement.md), and [PreparedStatement](PreparedStatement.md), such as`getBlob`and`setBlob`allow a programmer to access an SQL`BLOB`value. The`Blob`interface provides methods for getting the length of an SQL`BLOB`(Binary Large Object) value, for materializing a`BLOB`value on the client, and for determining the position of a pattern of bytes within a`BLOB`value. In addition, this interface has methods for updating a`BLOB`value.

All methods on the`Blob`interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [free](Blob.md))`()` This method frees the`Blob`object and releases the resources that it holds. |
| abstract [InputStream](../java.io/InputStream.md)! | [getBinaryStream](Blob.md))`()` Retrieves the`BLOB`value designated by this`Blob`instance as a stream. |
| abstract [InputStream](../java.io/InputStream.md)! | [getBinaryStream](Blob.md))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an`InputStream`object that contains a partial`Blob`value, starting with the byte specified by pos, which is length bytes in length. |
| --- | --- |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](Blob.md))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves all or part of the`BLOB`value that this`Blob`object represents, as an array of bytes. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [length](Blob.md))`()` Returns the number of bytes in the`BLOB`value designated by this`Blob`object. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](Blob.md))`(`pattern:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `start:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves the byte position at which the specified byte array`pattern`begins within the`BLOB`value that this`Blob`object represents. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [position](Blob.md))`(`pattern:` ` [Blob](Blob.md)!`, `start:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves the byte position in the`BLOB`value designated by this`Blob`object at which`pattern`begins. |
| abstract [OutputStream](../java.io/OutputStream.md)! | [setBinaryStream](Blob.md))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Retrieves a stream that can be used to write to the`BLOB`value that this`Blob`object represents. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setBytes](Blob.md))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Writes the given array of bytes to the`BLOB`value that this`Blob`object represents, starting at position`pos`, and returns the number of bytes written. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setBytes](Blob.md))`(`pos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes all or part of the given`byte`array to the`BLOB`value that this`Blob`object represents and returns the number of bytes written. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [truncate](Blob.md))`(`len:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Truncates the`BLOB`value that this`Blob`object represents to be`len`bytes in length. |

## Public methods

### free

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun free(): Unit
```

This method frees the`Blob`object and releases the resources that it holds. The object is invalid once the`free`method is called.

After`free`has been called, any attempt to invoke a method other than`free`will result in a`SQLException`being thrown. If`free`is called multiple times, the subsequent calls to`free`are treated as a no-op.

<br />

| Exceptions ||
|--------------------------------------------|---------------------------------------------------|
| `java.sql.SQLException` | if an error occurs releasing the Blob's resources |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBinaryStream(): InputStream!
```

Retrieves the`BLOB`value designated by this`Blob`instance as a stream.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------|
| [InputStream](../java.io/InputStream.md)! | a stream containing the`BLOB`data |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#setBinaryStream](Blob.md)) 

### getBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBinaryStream(
    pos: Long, 
    length: Long
): InputStream!
```

Returns an`InputStream`object that contains a partial`Blob`value, starting with the byte specified by pos, which is length bytes in length.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset to the first byte of the partial value to be retrieved. The first byte in the`Blob`is at position 1 |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the partial value to be retrieved |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | `InputStream`through which the partial`Blob`value can be read. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if pos is less than 1 or if pos is greater than the number of bytes in the`Blob`or if pos + length is greater than the number of bytes in the`Blob` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBytes(
    pos: Long, 
    length: Int
): ByteArray!
```

Retrieves all or part of the`BLOB`value that this`Blob`object represents, as an array of bytes. This`byte`array contains up to`length`consecutive bytes starting at position`pos`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the ordinal position of the first byte in the`BLOB`value to be extracted; the first byte is at position 1 |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of consecutive bytes to be copied; the value for length must be 0 or greater |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing up to`length`consecutive bytes from the`BLOB`value designated by this`Blob`object, starting with the byte at position`pos` |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value; if pos is less than 1 or length is less than 0 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun length(): Long
```

Returns the number of bytes in the`BLOB`value designated by this`Blob`object.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | length of the`BLOB`in bytes |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the length of the`BLOB` |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(
    pattern: ByteArray!, 
    start: Long
): Long
```

Retrieves the byte position at which the specified byte array`pattern`begins within the`BLOB`value that this`Blob`object represents. The search for`pattern`begins at position`start`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array for which to search |
| `start` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position at which to begin searching; the first position is 1 |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the position at which the pattern appears, else -1 |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`or if start is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### position

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun position(
    pattern: Blob!, 
    start: Long
): Long
```

Retrieves the byte position in the`BLOB`value designated by this`Blob`object at which`pattern`begins. The search begins at position`start`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [Blob](Blob.md)!:the`Blob`object designating the`BLOB`value for which to search |
| `start` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position in the`BLOB`value at which to begin searching; the first position is 1 |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the position at which the pattern begins, else -1 |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value or if start is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBinaryStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(pos: Long): OutputStream!
```

Retrieves a stream that can be used to write to the`BLOB`value that this`Blob`object represents. The stream begins at position`pos`. The bytes written to the stream will overwrite the existing bytes in the`Blob`object starting at the position`pos`. If the end of the`Blob`value is reached while writing to the stream, then the length of the`Blob`value will be increased to accomodate the extra bytes.

**Note:** If the value specified for`pos`is greater then the length+1 of the`BLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position in the`BLOB`value at which to start writing; the first position is 1 |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [OutputStream](../java.io/OutputStream.md)! | a`java.io.OutputStream`object to which data can be written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

### setBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBytes(
    pos: Long, 
    bytes: ByteArray!
): Int
```

Writes the given array of bytes to the`BLOB`value that this`Blob`object represents, starting at position`pos`, and returns the number of bytes written. The array of bytes will overwrite the existing bytes in the`Blob`object starting at the position`pos`. If the end of the`Blob`value is reached while writing the array of bytes, then the length of the`Blob`value will be increased to accomodate the extra bytes.

**Note:** If the value specified for`pos`is greater then the length+1 of the`BLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position in the`BLOB`object at which to start writing; the first position is 1 |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to be written to the`BLOB`value that this`Blob`object represents |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#getBytes](Blob.md)) 

### setBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBytes(
    pos: Long, 
    bytes: ByteArray!, 
    offset: Int, 
    len: Int
): Int
```

Writes all or part of the given`byte`array to the`BLOB`value that this`Blob`object represents and returns the number of bytes written. Writing starts at position`pos`in the`BLOB`value;`len`bytes from the given byte array are written. The array of bytes will overwrite the existing bytes in the`Blob`object starting at the position`pos`. If the end of the`Blob`value is reached while writing the array of bytes, then the length of the`Blob`value will be increased to accomodate the extra bytes.

**Note:** If the value specified for`pos`is greater then the length+1 of the`BLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position in the`BLOB`object at which to start writing; the first position is 1 |
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to be written to this`BLOB`object |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the array`bytes`at which to start reading the bytes to be set |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to be written to the`BLOB`value from the array of bytes`bytes` |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes written |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value or if pos is less than 1 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

**See Also**

- [#getBytes](Blob.md)) 

### truncate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun truncate(len: Long): Unit
```

Truncates the`BLOB`value that this`Blob`object represents to be`len`bytes in length.

**Note:** If the value specified for`pos`is greater then the length+1 of the`BLOB`value then the behavior is undefined. Some JDBC drivers may throw a`SQLException`while other drivers may support this operation.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `len` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length, in bytes, to which the`BLOB`value that this`Blob`object represents should be truncated |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error accessing the`BLOB`value or if len is less than 0 |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |
