# TimedMetaData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimedMetaData

Kotlin| [Java](../android/media/TimedMetaData.md) 
| --- | --- |

```
class TimedMetaData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.TimedMetaData](../android/media/TimedMetaData.md) |

Class that embodies one timed metadata access unit, including

- a time stamp, and
- raw uninterpreted byte-array extracted directly from the container.

<br />

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TimedMetaData](../android/media/TimedMetaData.md))`(`timestampUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `metaData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getMetaData](../android/media/TimedMetaData.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestamp](../android/media/TimedMetaData.md))`()` <br /> |

## Public constructors

### TimedMetaData

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TimedMetaData(
    timestampUs: Long, 
    metaData: ByteArray)
```

Constructor.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timestampUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the timestamp in microsecond for the timed metadata |
| `metaData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the metadata array for the timed metadata. No data copying is made. It should not be null. |

## Public methods

### getMetaData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetaData(): ByteArray!
```

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | raw, uninterpreted content of this metadata access unit; for ID3 tags this includes everything starting from the 3 byte signature "ID3". |

### getTimestamp

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestamp(): Long
```

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the timestamp associated with this metadata access unit in microseconds; 0 denotes playback start. |
