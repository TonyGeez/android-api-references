Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DigestOutputStream

```
open class DigestOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java/io/OutputStream.md) |||
| | ↳ | [java.io.FilterOutputStream](../java/io/FilterOutputStream.md) ||
| | | ↳ | [java.security.DigestOutputStream](../java/security/DigestOutputStream.md) |
| --- | --- | --- | --- |

A transparent stream that updates the associated message digest using the bits going through the stream.

To complete the message digest computation, call one of the `digest` methods on the associated message digest after your calls to one of this digest output stream's #write(int) methods.

It is possible to turn this stream on or off (see `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#on(kotlin.Boolean)`). When it is on, a call to one of the `write` methods results in an update on the message digest. But when it is off, the message digest is not updated. The default is for the stream to be on.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#DigestOutputStream(java.io.OutputStream,%20java.security.MessageDigest)(stream: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!, digest: https://developer.android.com/reference/kotlin/java/security/MessageDigest!)` Creates a digest output stream, using the specified output stream and message digest. |

| Public methods ||
|---|---|
| open [MessageDigest](../java/security/MessageDigest.md)! | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#getMessageDigest()()` Returns the message digest associated with this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#on(kotlin.Boolean)(on: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Turns the digest function on or off. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#setMessageDigest(java.security.MessageDigest)(digest: https://developer.android.com/reference/kotlin/java/security/MessageDigest!)` Associates the specified message digest with this stream. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#toString()()` Prints a string representation of this digest output stream and its associated message digest object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#write(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, off: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Updates the message digest (if the digest function is on) using the specified subarray, and in any case writes the subarray to the output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#write(kotlin.Int)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Updates the message digest (if the digest function is on) using the specified byte, and in any case writes the byte to the output stream. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#close()()` Closes this output stream and releases any system resources associated with the stream. When not already closed, the `close` method of `FilterOutputStream` calls its `flush` method, and then calls the `close` method of its underlying output stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#flush()()` Flushes this output stream and forces any buffered output bytes to be written out to the stream. The `flush` method of `FilterOutputStream` calls the `flush` method of its underlying output stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#write(kotlin.ByteArray)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Writes `b.length` bytes to this output stream. The `write` method of `FilterOutputStream` calls its `write` method of three arguments with the arguments `b`, `0`, and `b.length`. Note that this method does not call the one-argument `write` method of its underlying output stream with the single argument `b`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#nullOutputStream()()` Returns a new `OutputStream` which discards all bytes. The returned stream is initially open. The stream is closed by calling the `close()` method. Subsequent calls to `close()` have no effect. While the stream is open, the `write(int)`, `write(byte[])`, and `write(byte[], int, int)` methods do nothing. After the stream has been closed, these methods all throw `IOException`. The `flush()` method does nothing. <br /> | ||

| Properties ||
|---|---|
| [MessageDigest](../java/security/MessageDigest.md)! | `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#digest:java.security.MessageDigest` The message digest associated with this stream. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | `https://developer.android.com/reference/kotlin/java/io/FilterOutputStream.html#out:java.io.OutputStream` The underlying output stream to be filtered. <br /> | ||

## Public constructors

### DigestOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DigestOutputStream(
    stream: OutputStream!, 
    digest: MessageDigest!)
```

Creates a digest output stream, using the specified output stream and message digest.

| Parameters ||
|---|---|
| `stream` | [OutputStream](../java/io/OutputStream.md)!: the output stream. |
| `digest` | [MessageDigest](../java/security/MessageDigest.md)!: the message digest to associate with this stream. |

## Public methods

### getMessageDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMessageDigest(): MessageDigest!
```

Returns the message digest associated with this stream.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/MessageDigest!` | the message digest associated with this stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#setMessageDigest(java.security.MessageDigest)`

### on

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun on(on: Boolean): Unit
```

Turns the digest function on or off. The default is on. When it is on, a call to one of the `write` methods results in an update on the message digest. But when it is off, the message digest is not updated.

| Parameters ||
|---|---|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to turn the digest function on, false to turn it off. |

### setMessageDigest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMessageDigest(digest: MessageDigest!): Unit
```

Associates the specified message digest with this stream.

| Parameters ||
|---|---|
| `digest` | [MessageDigest](../java/security/MessageDigest.md)!: the message digest to be associated with this stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#getMessageDigest()`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Prints a string representation of this digest output stream and its associated message digest object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the message digest (if the digest function is on) using the specified subarray, and in any case writes the subarray to the output stream. That is, if the digest function is on (see `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#on(kotlin.Boolean)`), this method calls `update` on the message digest associated with this stream, passing it the subarray specifications. This method then writes the subarray bytes to the output stream, blocking until the bytes are actually written.

| Parameters ||
|---|---|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the array containing the subarray to be used for updating and writing to the output stream. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset into `b` of the first byte to be updated and written. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes of data to be updated and written from `b`, starting at offset `off`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/MessageDigest#update(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun write(b: Int): Unit
```

Updates the message digest (if the digest function is on) using the specified byte, and in any case writes the byte to the output stream. That is, if the digest function is on (see `https://developer.android.com/reference/kotlin/java/security/DigestOutputStream#on(kotlin.Boolean)`), this method calls `update` on the message digest associated with this stream, passing it the byte `b`. This method then writes the byte to the output stream, blocking until the byte is actually written.

| Parameters ||
|---|---|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the byte to be used for updating and writing to the output stream. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/MessageDigest#update(kotlin.Byte)`

## Properties

### digest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var digest: MessageDigest!
```

The message digest associated with this stream.
