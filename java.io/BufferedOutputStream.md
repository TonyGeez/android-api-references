# BufferedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BufferedOutputStream

```
open class BufferedOutputStream : FilterOutputStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.io.OutputStream](../java/io/OutputStream.md) |||
| | ↳ | [java.io.FilterOutputStream](../java/io/FilterOutputStream.md) ||
| | | ↳ | [java.io.BufferedOutputStream](../java/io/BufferedOutputStream.md) |
| --- | --- | --- | --- |

The class implements a buffered output stream. By setting up such an output stream, an application can write bytes to the underlying output stream without necessarily causing a call to the underlying system for each byte written.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BufferedOutputStream](../java/io/BufferedOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`)` Creates a new buffered output stream to write data to the specified underlying output stream. |
| [BufferedOutputStream](../java/io/BufferedOutputStream.md))`(`out:` ` [OutputStream](../java/io/OutputStream.md)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new buffered output stream to write data to the specified underlying output stream with the specified buffer size. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../java/io/BufferedOutputStream.md))`()` Flushes this buffered output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/BufferedOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes`len`bytes from the specified byte array starting at offset`off`to this buffered output stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/BufferedOutputStream.md))`(`b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes the specified byte to this buffered output stream. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [FilterOutputStream](../java/io/FilterOutputStream.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/FilterOutputStream.md))`()` <br /> Closes this output stream and releases any system resources associated with the stream. When not already closed, the`close`method of`FilterOutputStream`calls its`flush`method, and then calls the`close`method of its underlying output stream. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../java/io/FilterOutputStream.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Writes`b.length`bytes to this output stream. The`write`method of`FilterOutputStream`calls its`write`method of three arguments with the arguments`b`,`0`, and`b.length`. Note that this method does not call the one-argument`write`method of its underlying output stream with the single argument`b`. <br /> | ||
| From class [OutputStream](../java/io/OutputStream.md) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java/io/OutputStream.md)! | [nullOutputStream](../java/io/OutputStream.md))`()` <br /> Returns a new`OutputStream`which discards all bytes. The returned stream is initially open. The stream is closed by calling the`close()`method. Subsequent calls to`close()`have no effect. While the stream is open, the`write(int)`,`write(byte[])`, and`write(byte[], int, int)`methods do nothing. After the stream has been closed, these methods all throw`IOException`. The`flush()`method does nothing. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [buf](../java/io/BufferedOutputStream.md) The internal buffer where data is stored. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](../java/io/BufferedOutputStream.md) The number of valid bytes in the buffer. |

| Inherited properties ||
|---|---|
| From class [FilterOutputStream](../java/io/FilterOutputStream.md) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [OutputStream](../java/io/OutputStream.md)! | [out](../java/io/FilterOutputStream.md) <br /> The underlying output stream to be filtered. <br /> | ||

## Public constructors

### BufferedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedOutputStream(out: OutputStream!)
```

Creates a new buffered output stream to write data to the specified underlying output stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:the underlying output stream. |

### BufferedOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BufferedOutputStream(
    out: OutputStream!, 
    size: Int)
```

Creates a new buffered output stream to write data to the specified underlying output stream with the specified buffer size.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java/io/OutputStream.md)!:the underlying output stream. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the buffer size. |

| Exceptions ||
|--------------------------------------|----------------|
| `java.lang.IllegalArgumentException` | if size \<= 0. |

## Public methods

### flush

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Flushes this buffered output stream. This forces any buffered output bytes to be written out to the underlying output stream.

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- [java.io.FilterOutputStream#out](../java/io/FilterOutputStream.md) 

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Writes`len`bytes from the specified byte array starting at offset`off`to this buffered output stream.

Ordinarily this method stores bytes from the given array into this stream's buffer, flushing the buffer to the underlying output stream as needed. If the requested length is at least as large as this stream's buffer, however, then this method will flush the buffer and write the bytes directly to the underlying output stream. Thus redundant`BufferedOutputStream`s will not copy data unnecessarily.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start offset in the data. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to write. |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun write(b: Int): Unit
```

Writes the specified byte to this buffered output stream.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the byte to be written. |

| Exceptions ||
|-----------------------|-------------------------|
| `java.io.IOException` | if an I/O error occurs. |

## Properties

### buf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var buf: ByteArray!
```

The internal buffer where data is stored. 

### count

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var count: Int
```

The number of valid bytes in the buffer. This value is always in the range`0`through`buf.length`; elements`buf[0]`through`buf[count-1]`contain valid byte data.
