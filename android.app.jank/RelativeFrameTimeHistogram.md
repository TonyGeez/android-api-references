# RelativeFrameTimeHistogram

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RelativeFrameTimeHistogram

Kotlin| [Java](../android/app/jank/RelativeFrameTimeHistogram.md) 
| --- | --- |

```
open class RelativeFrameTimeHistogram
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.jank.RelativeFrameTimeHistogram](../android/app/jank/RelativeFrameTimeHistogram.md) |

A histogram of frame times relative to their deadline. This class aids in reporting [AppJankStats](../android/app/jank/AppJankStats.md) to the system and is designed for use by library widgets. It facilitates the recording of frame times in relation to the frame deadline. The class records the distribution of time remaining until a frame is considered janky or how janky the frame was.

A frame's relative frame time value indicates whether it was delivered early, on time, or late. A negative relative frame time value indicates the frame was delivered early, a value of zero indicates the frame was delivered on time and a positive value indicates the frame was delivered late. The values of the endpoints indicate how early or late a frame was delivered.

The relative frame times are recorded as a histogram: values are [added](../android/app/jank/RelativeFrameTimeHistogram.md))to a bucket by increasing the bucket's counter. The count of frames with a relative frame time between [bucket endpoints](../android/app/jank/RelativeFrameTimeHistogram.md))`i`and`i+1`can be obtained through index`i`of [getBucketCounters](../android/app/jank/RelativeFrameTimeHistogram.md)).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RelativeFrameTimeHistogram](../android/app/jank/RelativeFrameTimeHistogram.md))`()` Create a new instance of RelativeFrameTimeHistogram. |

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addRelativeFrameTimeMillis](../android/app/jank/RelativeFrameTimeHistogram.md))`(`frameTimeMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increases the count by one for the bucket representing the relative frame time. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getBucketCounters](../android/app/jank/RelativeFrameTimeHistogram.md))`()` Returns the counts for the all the relative frame time buckets. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getBucketEndpointsMillis](../android/app/jank/RelativeFrameTimeHistogram.md))`()` Returns the relative frame time endpoints for the histogram. |
| --- | --- |

## Public constructors

### RelativeFrameTimeHistogram

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RelativeFrameTimeHistogram()
```

Create a new instance of RelativeFrameTimeHistogram.

## Public methods

### addRelativeFrameTimeMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addRelativeFrameTimeMillis(frameTimeMillis: Int): Unit
```

Increases the count by one for the bucket representing the relative frame time.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameTimeMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):relative frame time in millis, relative frame time is the difference between a frames deadline and when it was rendered. |

### getBucketCounters

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBucketCounters(): IntArray
```

Returns the counts for the all the relative frame time buckets.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | an array of integers representing the counts of relative frame times. This value cannot be null. |

### getBucketEndpointsMillis

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBucketEndpointsMillis(): IntArray
```

Returns the relative frame time endpoints for the histogram.

Index`i`of [getBucketCounters](../android/app/jank/RelativeFrameTimeHistogram.md))contains the count of frames that had a relative frame time between`endpoints[i]`(inclusive) and`endpoints[i+1]`(exclusive).

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | array of integers representing the endpoints for the predefined histogram count buckets. This value cannot be null. |
