# MediaParser.SeekableInputReader

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SeekableInputReader

Kotlin | [Java](../android/media/MediaParser.SeekableInputReader.md) 
| --- | --- |

```
interface SeekableInputReader : MediaParser.InputReader
```

| [android.media.MediaParser.SeekableInputReader](../android/media/MediaParser.SeekableInputReader.md) |

[InputReader](../android/media/MediaParser.InputReader.md) that allows setting the read position.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekToPosition](../android/media/MediaParser.SeekableInputReader.md))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the read position at the given `position`. |

| Inherited functions ||
|---|---|
| From class [InputReader](../android/media/MediaParser.InputReader.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLength](../android/media/MediaParser.InputReader.md))`()` Returns the length of the input in bytes, or -1 if the length is unknown. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPosition](../android/media/MediaParser.InputReader.md))`()` Returns the current read position (byte offset) in the stream. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](../android/media/MediaParser.InputReader.md))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads up to `readLength` bytes of data and stores them into `buffer`, starting at index `offset`. This method blocks until at least one byte is read, the end of input is detected, or an exception is thrown. The read position advances to the first unread byte. <br /> | ||

## Public methods

### seekToPosition

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun seekToPosition(position: Long): Unit
```

Sets the read position at the given `position`.

[advance](MediaParser.md)) will immediately return after calling this method.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The position to seek to, in bytes. |
