# FrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrameStats

Kotlin| [Java](https://developer.android.com/reference/android/view/FrameStats "View this page in Java") 

```
abstract class FrameStats
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.FrameStats](https://developer.android.com/reference/kotlin/android/view/FrameStats#) |

| Known Direct Subclasses [WindowAnimationFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowAnimationFrameStats), [WindowContentFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowContentFrameStats) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [WindowAnimationFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowAnimationFrameStats) | This class contains window animation frame statistics. | | [WindowContentFrameStats](https://developer.android.com/reference/kotlin/android/view/WindowContentFrameStats) | This class contains window content frame statistics. | |

This is the base class for frame statistics.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UNDEFINED_TIME_NANO](https://developer.android.com/reference/kotlin/android/view/FrameStats#UNDEFINED_TIME_NANO:kotlin.Long) Undefined time. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [FrameStats](https://developer.android.com/reference/kotlin/android/view/FrameStats#FrameStats())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndTimeNano](https://developer.android.com/reference/kotlin/android/view/FrameStats#getEndTimeNano())`()` Gets the end time of the interval for which these statistics apply. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrameCount](https://developer.android.com/reference/kotlin/android/view/FrameStats#getFrameCount())`()` Gets the number of frames for which there is data. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFramePresentedTimeNano](https://developer.android.com/reference/kotlin/android/view/FrameStats#getFramePresentedTimeNano(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time a frame at a given index was presented. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRefreshPeriodNano](https://developer.android.com/reference/kotlin/android/view/FrameStats#getRefreshPeriodNano())`()` Gets the refresh period of the display hosting the window(s) for which these statistics apply. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeNano](https://developer.android.com/reference/kotlin/android/view/FrameStats#getStartTimeNano())`()` Gets the start time of the interval for which these statistics apply. |

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The end time in nanoseconds or [UNDEFINED_TIME_NANO](https://developer.android.com/reference/kotlin/android/view/FrameStats#UNDEFINED_TIME_NANO:kotlin.Long) if there is no frame data. |

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The presented time in nanoseconds or [UNDEFINED_TIME_NANO](https://developer.android.com/reference/kotlin/android/view/FrameStats#UNDEFINED_TIME_NANO:kotlin.Long) if the frame is not presented yet. |

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The start time in nanoseconds or [UNDEFINED_TIME_NANO](https://developer.android.com/reference/kotlin/android/view/FrameStats#UNDEFINED_TIME_NANO:kotlin.Long) if there is no frame data. |
