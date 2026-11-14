# MediaParser.InputReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputReader

Kotlin| [Java](../android/media/MediaParser.InputReader.md) 
| --- | --- |

```
interface InputReader
```

| [android.media.MediaParser.InputReader](../android/media/MediaParser.InputReader.md) |

| Known Direct Subclasses [MediaParser.SeekableInputReader](../android/media/MediaParser.SeekableInputReader.md) |---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------| | [MediaParser.SeekableInputReader](../android/media/MediaParser.SeekableInputReader.md) | [InputReader](../android/media/MediaParser.InputReader.md) that allows setting the read position. | |
| --- | --- | --- | --- | --- | --- | --- |

Provides input data to [MediaParser](MediaParser.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLength](../android/media/MediaParser.InputReader.md))`()` Returns the length of the input in bytes, or -1 if the length is unknown. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPosition](../android/media/MediaParser.InputReader.md))`()` Returns the current read position (byte offset) in the stream. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../android/media/MediaParser.InputReader.md))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to`readLength`bytes of data and stores them into`buffer`, starting at index`offset`. |
| --- | --- |

## Public methods

### getLength

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Long
```

Returns the length of the input in bytes, or -1 if the length is unknown. 

### getPosition

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPosition(): Long
```

Returns the current read position (byte offset) in the stream. 

### read

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    buffer: ByteArray, 
    offset: Int, 
    readLength: Int
): Int
```

Reads up to`readLength`bytes of data and stores them into`buffer`, starting at index`offset`.

This method blocks until at least one byte is read, the end of input is detected, or an exception is thrown. The read position advances to the first unread byte.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The buffer into which the read data should be stored. This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The start offset into`buffer`at which data should be written. |
| `readLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of bytes to read. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The non-zero number of bytes read, or -1 if no data is available because the end of the input has been reached. |

| Exceptions ||
|-----------------------|---------------------------------------------|
| `java.io.IOException` | If an error occurs reading from the source. |
