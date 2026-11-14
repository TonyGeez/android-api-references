# MediaParser.SeekableInputReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SeekableInputReader

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaParser.SeekableInputReader "View this page in Java") 
| --- | --- |

```
interface SeekableInputReader : MediaParser.InputReader
```

| [android.media.MediaParser.SeekableInputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader#) |

[InputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader) that allows setting the read position.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekToPosition](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader#seekToPosition(kotlin.Long))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the read position at the given `position`. |

| Inherited functions ||
|---|---|
| From class [InputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader#getLength())`()` Returns the length of the input in bytes, or -1 if the length is unknown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader#getPosition())`()` Returns the current read position (byte offset) in the stream. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader#read(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to `readLength` bytes of data and stores them into `buffer`, starting at index `offset`. This method blocks until at least one byte is read, the end of input is detected, or an exception is thrown. The read position advances to the first unread byte. <br /> | ||

## Public methods

### seekToPosition

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun seekToPosition(position: Long): Unit
```

Sets the read position at the given `position`.

[advance](https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)) will immediately return after calling this method.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The position to seek to, in bytes. |
