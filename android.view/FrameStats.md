# FrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrameStats

Kotlin| [Java](FrameStats.md) 
| --- | --- |

```
abstract class FrameStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.FrameStats](FrameStats.md) |

| Known Direct Subclasses [WindowAnimationFrameStats](WindowAnimationFrameStats.md), [WindowContentFrameStats](WindowContentFrameStats.md) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [WindowAnimationFrameStats](WindowAnimationFrameStats.md) | This class contains window animation frame statistics. | | [WindowContentFrameStats](WindowContentFrameStats.md) | This class contains window content frame statistics. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This is the base class for frame statistics.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UNDEFINED_TIME_NANO](FrameStats.md) Undefined time. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [FrameStats](FrameStats.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndTimeNano](FrameStats.md))`()` Gets the end time of the interval for which these statistics apply. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrameCount](FrameStats.md))`()` Gets the number of frames for which there is data. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFramePresentedTimeNano](FrameStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time a frame at a given index was presented. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRefreshPeriodNano](FrameStats.md))`()` Gets the refresh period of the display hosting the window(s) for which these statistics apply. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeNano](FrameStats.md))`()` Gets the start time of the interval for which these statistics apply. |

## Constants

### UNDEFINED_TIME_NANO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDEFINED_TIME_NANO: Long
```

Undefined time. 

 Value: -1L

## Public constructors

### FrameStats

```
FrameStats()
```

## Public methods

### getEndTimeNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTimeNano(): Long
```

Gets the end time of the interval for which these statistics apply. The end interval is the time when the last frame was presented.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The end time in nanoseconds or [UNDEFINED_TIME_NANO](FrameStats.md) if there is no frame data. |

### getFrameCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrameCount(): Int
```

Gets the number of frames for which there is data.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of frames. |

### getFramePresentedTimeNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFramePresentedTimeNano(index: Int): Long
```

Get the time a frame at a given index was presented.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The frame index. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The presented time in nanoseconds or [UNDEFINED_TIME_NANO](FrameStats.md) if the frame is not presented yet. |

### getRefreshPeriodNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRefreshPeriodNano(): Long
```

Gets the refresh period of the display hosting the window(s) for which these statistics apply.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The refresh period in nanoseconds. |

### getStartTimeNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTimeNano(): Long
```

Gets the start time of the interval for which these statistics apply. The start interval is the time when the first frame was presented.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The start time in nanoseconds or [UNDEFINED_TIME_NANO](FrameStats.md) if there is no frame data. |
