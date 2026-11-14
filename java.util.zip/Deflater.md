# Deflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Deflater

```
open class Deflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.zip.Deflater](../java/util/zip/Deflater.md) |

This class provides support for general purpose compression using the popular ZLIB compression library. The ZLIB compression library was initially developed as part of the PNG graphics standard and is not protected by patents. It is fully described in the specifications at the [java.util.zip package description](../java/util/zip/_package.md).

This class deflates sequences of bytes into ZLIB compressed data format. The input byte sequence is provided in either byte array or byte buffer, via one of the `setInput()` methods. The output byte sequence is written to the output byte array or byte buffer passed to the `deflate()` methods.

The following code fragment demonstrates a trivial compression and decompression of a string using `Deflater` and `Inflater`. 

```kotlin
try {
      // Encode a String into bytes
      String inputString = "blahblahblah";
      byte[] input = inputString.getBytes("UTF-8");
 
      // Compress the bytes
      byte[] output = new byte[100];
      Deflater compresser = new Deflater();
      compresser.setInput(input);
      compresser.finish();
      int compressedDataLength = compresser.deflate(output);
      compresser.end();
 
      // Decompress the bytes
      Inflater decompresser = new Inflater();
      decompresser.setInput(output, 0, compressedDataLength);
      byte[] result = new byte[100];
      int resultLength = decompresser.inflate(result);
      decompresser.end();
 
      // Decode the bytes into a String
      String outputString = new String(result, 0, resultLength, "UTF-8");
  } catch (java.io.UnsupportedEncodingException ex) {
      // handle
  } catch (java.util.zip.DataFormatException ex) {
      // handle
  }
  
```

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEST_COMPRESSION](../java/util/zip/Deflater.md) Compression level for best compression. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BEST_SPEED](../java/util/zip/Deflater.md) Compression level for fastest compression. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_COMPRESSION](../java/util/zip/Deflater.md) Default compression level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_STRATEGY](../java/util/zip/Deflater.md) Default compression strategy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFLATED](../java/util/zip/Deflater.md) Compression method for the deflate algorithm (the only one currently supported). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FILTERED](../java/util/zip/Deflater.md) Compression strategy best used for data consisting mostly of small values with a somewhat random distribution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL_FLUSH](../java/util/zip/Deflater.md) Compression flush mode used to flush out all pending output and reset the deflater. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HUFFMAN_ONLY](../java/util/zip/Deflater.md) Compression strategy for Huffman coding only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_COMPRESSION](../java/util/zip/Deflater.md) Compression level for no compression. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_FLUSH](../java/util/zip/Deflater.md) Compression flush mode used to achieve best compression result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_FLUSH](../java/util/zip/Deflater.md) Compression flush mode used to flush out all pending output; may degrade compression for some compression algorithms. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Deflater](../java/util/zip/Deflater.md))`()` Creates a new compressor with the default compression level. |
| [Deflater](../java/util/zip/Deflater.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new compressor using the specified compression level. |
| [Deflater](../java/util/zip/Deflater.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nowrap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new compressor using the specified compression level. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [deflate](../java/util/zip/Deflater.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Compresses the input data and fills specified buffer with compressed data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [deflate](../java/util/zip/Deflater.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compresses the input data and fills specified buffer with compressed data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [deflate](../java/util/zip/Deflater.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flush:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compresses the input data and fills the specified buffer with compressed data. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [deflate](../java/util/zip/Deflater.md))`(`output:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Compresses the input data and fills specified buffer with compressed data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [deflate](../java/util/zip/Deflater.md))`(`output:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`, `flush:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compresses the input data and fills the specified buffer with compressed data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../java/util/zip/Deflater.md))`()` Closes the compressor and discards any unprocessed input. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](../java/util/zip/Deflater.md))`()` When called, indicates that compression should end with the current contents of the input buffer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [finished](../java/util/zip/Deflater.md))`()` Returns true if the end of the compressed data output stream has been reached. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdler](../java/util/zip/Deflater.md))`()` Returns the ADLER-32 value of the uncompressed data. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBytesRead](../java/util/zip/Deflater.md))`()` Returns the total number of uncompressed bytes input so far. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBytesWritten](../java/util/zip/Deflater.md))`()` Returns the total number of compressed bytes output so far. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTotalIn](../java/util/zip/Deflater.md))`()` Returns the total number of uncompressed bytes input so far. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTotalOut](../java/util/zip/Deflater.md))`()` Returns the total number of compressed bytes output so far. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [needsInput](../java/util/zip/Deflater.md))`()` Returns true if no data remains in the input buffer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../java/util/zip/Deflater.md))`()` Resets deflater so that a new set of input data can be processed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](../java/util/zip/Deflater.md))`(`dictionary:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets preset dictionary for compression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](../java/util/zip/Deflater.md))`(`dictionary:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets preset dictionary for compression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDictionary](../java/util/zip/Deflater.md))`(`dictionary:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Sets preset dictionary for compression. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](../java/util/zip/Deflater.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Sets input data for compression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](../java/util/zip/Deflater.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets input data for compression. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](../java/util/zip/Deflater.md))`(`input:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Sets input data for compression. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLevel](../java/util/zip/Deflater.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the compression level to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrategy](../java/util/zip/Deflater.md))`(`strategy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the compression strategy to the specified value. |

## Constants

### BEST_COMPRESSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEST_COMPRESSION: Int
```

Compression level for best compression. 

 Value: 9

### BEST_SPEED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEST_SPEED: Int
```

Compression level for fastest compression. 

 Value: 1

### DEFAULT_COMPRESSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_COMPRESSION: Int
```

Default compression level. 

 Value: -1

### DEFAULT_STRATEGY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_STRATEGY: Int
```

Default compression strategy. 

 Value: 0

### DEFLATED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFLATED: Int
```

Compression method for the deflate algorithm (the only one currently supported). 

 Value: 8

### FILTERED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTERED: Int
```

Compression strategy best used for data consisting mostly of small values with a somewhat random distribution. Forces more Huffman coding and less string matching. 

 Value: 1

### FULL_FLUSH

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FULL_FLUSH: Int
```

Compression flush mode used to flush out all pending output and reset the deflater. Using this mode too often can seriously degrade compression. 

 Value: 3

**See Also**

- [java.util.zip.Deflater#deflate(byte[], int, int, int)](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#deflate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### HUFFMAN_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HUFFMAN_ONLY: Int
```

Compression strategy for Huffman coding only. 

 Value: 2

### NO_COMPRESSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_COMPRESSION: Int
```

Compression level for no compression. 

 Value: 0

### NO_FLUSH

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_FLUSH: Int
```

Compression flush mode used to achieve best compression result. 

 Value: 0

**See Also**

- [java.util.zip.Deflater#deflate(byte[], int, int, int)](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#deflate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### SYNC_FLUSH

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_FLUSH: Int
```

Compression flush mode used to flush out all pending output; may degrade compression for some compression algorithms. 

 Value: 2

**See Also**

- [java.util.zip.Deflater#deflate(byte[], int, int, int)](https://developer.android.com/reference/kotlin/java/util/zip/Deflater#deflate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))

## Public constructors

### Deflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Deflater()
```

Creates a new compressor with the default compression level. Compressed data will be generated in ZLIB format. 

### Deflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Deflater(level: Int)
```

Creates a new compressor using the specified compression level. Compressed data will be generated in ZLIB format.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the compression level (0-9) |

### Deflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Deflater(
    level: Int, 
    nowrap: Boolean)
```

Creates a new compressor using the specified compression level. If 'nowrap' is true then the ZLIB header and checksum fields will not be used in order to support the compression format used in both GZIP and PKZIP.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the compression level (0-9) |
| `nowrap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then use GZIP compatible compression |

## Public methods

### deflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deflate(output: ByteArray!): Int
```

Compresses the input data and fills specified buffer with compressed data. Returns actual number of bytes of compressed data. A return value of 0 indicates that [needsInput](../java/util/zip/Deflater.md)) should be called in order to determine if more input data is required.

This method uses [NO_FLUSH](../java/util/zip/Deflater.md) as its compression flush mode. An invocation of this method of the form `deflater.deflate(b)` yields the same result as the invocation of `deflater.deflate(b, 0, b.length, Deflater.NO_FLUSH)`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer for the compressed data |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes of compressed data written to the output buffer |

### deflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deflate(
    output: ByteArray!, 
    off: Int, 
    len: Int
): Int
```

Compresses the input data and fills specified buffer with compressed data. Returns actual number of bytes of compressed data. A return value of 0 indicates that [needsInput](../java/util/zip/Deflater.md)) should be called in order to determine if more input data is required.

This method uses [NO_FLUSH](../java/util/zip/Deflater.md) as its compression flush mode. An invocation of this method of the form `deflater.deflate(b, off, len)` yields the same result as the invocation of `deflater.deflate(b, off, len, Deflater.NO_FLUSH)`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer for the compressed data |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes of compressed data |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes of compressed data written to the output buffer |

### deflate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deflate(
    output: ByteArray!, 
    off: Int, 
    len: Int, 
    flush: Int
): Int
```

Compresses the input data and fills the specified buffer with compressed data. Returns actual number of bytes of data compressed.

Compression flush mode is one of the following three modes:

- [NO_FLUSH](../java/util/zip/Deflater.md): allows the deflater to decide how much data to accumulate, before producing output, in order to achieve the best compression (should be used in normal use scenario). A return value of 0 in this flush mode indicates that [needsInput()](../java/util/zip/Deflater.md)) should be called in order to determine if more input data is required.
- [SYNC_FLUSH](../java/util/zip/Deflater.md): all pending output in the deflater is flushed, to the specified output buffer, so that an inflater that works on compressed data can get all input data available so far (In particular the [needsInput()](../java/util/zip/Deflater.md)) returns `true` after this invocation if enough output space is provided). Flushing with [SYNC_FLUSH](../java/util/zip/Deflater.md) may degrade compression for some compression algorithms and so it should be used only when necessary.
- [FULL_FLUSH](../java/util/zip/Deflater.md): all pending output is flushed out as with [SYNC_FLUSH](../java/util/zip/Deflater.md). The compression state is reset so that the inflater that works on the compressed output data can restart from this point if previous compressed data has been damaged or if random access is desired. Using [FULL_FLUSH](../java/util/zip/Deflater.md) too often can seriously degrade compression.

In the case of [FULL_FLUSH](../java/util/zip/Deflater.md) or [SYNC_FLUSH](../java/util/zip/Deflater.md), if the return value is `len`, the space available in output buffer `b`, this method should be invoked again with the same `flush` parameter and more output space. Make sure that `len` is greater than 6 to avoid flush marker (5 bytes) being repeatedly output to the output buffer every time this method is invoked.

If the [setInput(java.nio.ByteBuffer)](../java/util/zip/Deflater.md)) method was called to provide a buffer for input, the input buffer's position will be advanced by the number of bytes consumed by this operation.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the buffer for the compressed data |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of bytes of compressed data |
| --- | --- |
| `flush` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the compression flush mode |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes of compressed data written to the output buffer |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the flush mode is invalid |

### deflate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deflate(output: ByteBuffer!): Int
```

Compresses the input data and fills specified buffer with compressed data. Returns actual number of bytes of compressed data. A return value of 0 indicates that [needsInput](../java/util/zip/Deflater.md)) should be called in order to determine if more input data is required.

This method uses [NO_FLUSH](../java/util/zip/Deflater.md) as its compression flush mode. An invocation of this method of the form `deflater.deflate(output)` yields the same result as the invocation of `deflater.deflate(output, Deflater.NO_FLUSH)`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteBuffer](../java/nio/ByteBuffer.md)!: the buffer for the compressed data |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes of compressed data written to the output buffer |

### deflate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deflate(
    output: ByteBuffer!, 
    flush: Int
): Int
```

Compresses the input data and fills the specified buffer with compressed data. Returns actual number of bytes of data compressed.

Compression flush mode is one of the following three modes:

- [NO_FLUSH](../java/util/zip/Deflater.md): allows the deflater to decide how much data to accumulate, before producing output, in order to achieve the best compression (should be used in normal use scenario). A return value of 0 in this flush mode indicates that [needsInput()](../java/util/zip/Deflater.md)) should be called in order to determine if more input data is required.
- [SYNC_FLUSH](../java/util/zip/Deflater.md): all pending output in the deflater is flushed, to the specified output buffer, so that an inflater that works on compressed data can get all input data available so far (In particular the [needsInput()](../java/util/zip/Deflater.md)) returns `true` after this invocation if enough output space is provided). Flushing with [SYNC_FLUSH](../java/util/zip/Deflater.md) may degrade compression for some compression algorithms and so it should be used only when necessary.
- [FULL_FLUSH](../java/util/zip/Deflater.md): all pending output is flushed out as with [SYNC_FLUSH](../java/util/zip/Deflater.md). The compression state is reset so that the inflater that works on the compressed output data can restart from this point if previous compressed data has been damaged or if random access is desired. Using [FULL_FLUSH](../java/util/zip/Deflater.md) too often can seriously degrade compression.

In the case of [FULL_FLUSH](../java/util/zip/Deflater.md) or [SYNC_FLUSH](../java/util/zip/Deflater.md), if the return value is equal to the [remaining space](../java/nio/Buffer.md)) of the buffer, this method should be invoked again with the same `flush` parameter and more output space. Make sure that the buffer has at least 6 bytes of remaining space to avoid the flush marker (5 bytes) being repeatedly output to the output buffer every time this method is invoked.

On success, the position of the given `output` byte buffer will be advanced by as many bytes as were produced by the operation, which is equal to the number returned by this method.

If the [setInput(java.nio.ByteBuffer)](../java/util/zip/Deflater.md)) method was called to provide a buffer for input, the input buffer's position will be advanced by the number of bytes consumed by this operation.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteBuffer](../java/nio/ByteBuffer.md)!: the buffer for the compressed data |
| `flush` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the compression flush mode |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the actual number of bytes of compressed data written to the output buffer |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the flush mode is invalid |

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun end(): Unit
```

Closes the compressor and discards any unprocessed input. This method should be called when the compressor is no longer being used. Once this method is called, the behavior of the Deflater object is undefined. 

### finish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finish(): Unit
```

When called, indicates that compression should end with the current contents of the input buffer. 

### finished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finished(): Boolean
```

Returns true if the end of the compressed data output stream has been reached.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the end of the compressed data output stream has been reached |

### getAdler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAdler(): Int
```

Returns the ADLER-32 value of the uncompressed data.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ADLER-32 value of the uncompressed data |

### getBytesRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBytesRead(): Long
```

Returns the total number of uncompressed bytes input so far.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total (non-negative) number of uncompressed bytes input so far |

### getBytesWritten

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBytesWritten(): Long
```

Returns the total number of compressed bytes output so far.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total (non-negative) number of compressed bytes output so far |

### getTotalIn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalIn(): Int
```

Returns the total number of uncompressed bytes input so far.

Since the number of bytes may be greater than Integer.MAX_VALUE, the [getBytesRead()](../java/util/zip/Deflater.md)) method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of uncompressed bytes input so far |

### getTotalOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalOut(): Int
```

Returns the total number of compressed bytes output so far.

Since the number of bytes may be greater than Integer.MAX_VALUE, the [getBytesWritten()](../java/util/zip/Deflater.md)) method is now the preferred means of obtaining this information.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the total number of compressed bytes output so far |

### needsInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun needsInput(): Boolean
```

Returns true if no data remains in the input buffer. This can be used to determine if one of the `setInput()` methods should be called in order to provide more input.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the input data buffer is empty and setInput() should be called in order to provide more input |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets deflater so that a new set of input data can be processed. Keeps current compression level and strategy settings. 

### setDictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(dictionary: ByteArray!): Unit
```

Sets preset dictionary for compression. A preset dictionary is used when the history buffer can be predetermined. When the data is later uncompressed with Inflater.inflate(), Inflater.getAdler() can be called in order to get the Adler-32 value of the dictionary required for decompression.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the dictionary data bytes |

**See Also**

- [java.util.zip.Inflater#getAdler](../java/util/zip/Inflater.md)) 

### setDictionary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(
    dictionary: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Sets preset dictionary for compression. A preset dictionary is used when the history buffer can be predetermined. When the data is later uncompressed with Inflater.inflate(), Inflater.getAdler() can be called in order to get the Adler-32 value of the dictionary required for decompression.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the dictionary data bytes |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the data |
| --- | --- |

**See Also**

- [java.util.zip.Inflater#getAdler](../java/util/zip/Inflater.md)) 

### setDictionary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDictionary(dictionary: ByteBuffer!): Unit
```

Sets preset dictionary for compression. A preset dictionary is used when the history buffer can be predetermined. When the data is later uncompressed with Inflater.inflate(), Inflater.getAdler() can be called in order to get the Adler-32 value of the dictionary required for decompression.

The bytes in given byte buffer will be fully consumed by this method. On return, its position will equal its limit.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `dictionary` | [ByteBuffer](../java/nio/ByteBuffer.md)!: the dictionary data bytes |

**See Also**

- [java.util.zip.Inflater#getAdler](../java/util/zip/Inflater.md)) 

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(input: ByteArray!): Unit
```

Sets input data for compression.

One of the `setInput()` methods should be called whenever `needsInput()` returns true indicating that more input data is required.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the input data bytes |

**See Also**

- [java.util.zip.Deflater#needsInput](../java/util/zip/Deflater.md)) 

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(
    input: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Sets input data for compression.

One of the `setInput()` methods should be called whenever `needsInput()` returns true indicating that more input data is required.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the input data bytes |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start offset of the data |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the data |
| --- | --- |

**See Also**

- [java.util.zip.Deflater#needsInput](../java/util/zip/Deflater.md)) 

### setInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInput(input: ByteBuffer!): Unit
```

Sets input data for compression.

One of the `setInput()` methods should be called whenever `needsInput()` returns true indicating that more input data is required.

The given buffer's position will be advanced as deflate operations are performed, up to the buffer's limit. The input buffer may be modified (refilled) between deflate operations; doing so is equivalent to creating a new buffer and setting it with this method.

Modifying the input buffer's contents, position, or limit concurrently with an deflate operation will result in undefined behavior, which may include incorrect operation results or operation failure.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](../java/nio/ByteBuffer.md)!: the input data bytes |

**See Also**

- [java.util.zip.Deflater#needsInput](../java/util/zip/Deflater.md)) 

### setLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLevel(level: Int): Unit
```

Sets the compression level to the specified value.

If the compression level is changed, the next invocation of `deflate` will compress the input available so far with the old level (and may be flushed); the new level will take effect only after that invocation.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new compression level (0-9) |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if the compression level is invalid |

### setStrategy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrategy(strategy: Int): Unit
```

Sets the compression strategy to the specified value.

If the compression strategy is changed, the next invocation of `deflate` will compress the input available so far with the old strategy (and may be flushed); the new strategy will take effect only after that invocation.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------|
| `strategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new compression strategy |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if the compression strategy is invalid |
