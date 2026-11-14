# FrameMetrics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FrameMetrics

Kotlin| [Java](https://developer.android.com/reference/android/view/FrameMetrics "View this page in Java") 

```
class FrameMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.FrameMetrics](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#) |

Class containing timing data for various milestones in a frame lifecycle reported by the rendering subsystem.

Supported metrics can be queried via their corresponding identifier.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ANIMATION_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#ANIMATION_DURATION:kotlin.Int) Metric identifier for animation callback duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMMAND_ISSUE_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#COMMAND_ISSUE_DURATION:kotlin.Int) Metric identifier for command issue duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEADLINE](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#DEADLINE:kotlin.Int) Metric identifier for the total duration that was available to the app to produce a frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRAW_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#DRAW_DURATION:kotlin.Int) Metric identifier for draw duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST_DRAW_FRAME](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#FIRST_DRAW_FRAME:kotlin.Int) Metric identifier for a boolean value determining whether this frame was the first to draw in a new Window layout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_TIMELINE_VSYNC_ID](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#FRAME_TIMELINE_VSYNC_ID:kotlin.Int) Metric identifier for the frame's VSync identifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GPU_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#GPU_DURATION:kotlin.Int) Metric identifier for GPU duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_HANDLING_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#INPUT_HANDLING_DURATION:kotlin.Int) Metric identifier for input handling duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTENDED_VSYNC_TIMESTAMP](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#INTENDED_VSYNC_TIMESTAMP:kotlin.Int) Metric identifier for the timestamp of the intended vsync for this frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LAYOUT_MEASURE_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#LAYOUT_MEASURE_DURATION:kotlin.Int) Metric identifier for layout/measure duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SWAP_BUFFERS_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#SWAP_BUFFERS_DURATION:kotlin.Int) Metric identifier for swap buffers duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#SYNC_DURATION:kotlin.Int) Metric identifier for sync duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOTAL_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#TOTAL_DURATION:kotlin.Int) Metric identifier for total frame duration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_DELAY_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#UNKNOWN_DELAY_DURATION:kotlin.Int) Metric identifier for unknown delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VSYNC_TIMESTAMP](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#VSYNC_TIMESTAMP:kotlin.Int) Metric identifier for the timestamp of the actual vsync for this frame. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FrameMetrics](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#FrameMetrics(android.view.FrameMetrics))`(`other:` ` [FrameMetrics](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#)!`)` Constructs a FrameMetrics object as a copy. |

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMetric](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#getMetric(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the value associated with Metric identifier`id`for this frame. |

## Constants

### ANIMATION_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ANIMATION_DURATION: Int
```

Metric identifier for animation callback duration.

Represents the number of nanoseconds elapsed issuing animation callbacks. 

 Value: 2

### COMMAND_ISSUE_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMMAND_ISSUE_DURATION: Int
```

Metric identifier for command issue duration.

Represents the number of nanoseconds elapsed issuing draw commands to the GPU. 

 Value: 6

### DEADLINE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEADLINE: Int
```

Metric identifier for the total duration that was available to the app to produce a frame.

Represents the total time in nanoseconds the system allocated for the app to produce its frame. If FrameMetrics.TOTAL_DURATION \< FrameMetrics.DEADLINE, the app hit its intended deadline and there was no jank visible to the user. 

 Value: 13

### DRAW_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRAW_DURATION: Int
```

Metric identifier for draw duration.

Represents the number of nanoseconds elapsed computing DisplayLists for transformations applied to the view hierarchy. 

 Value: 4

### FIRST_DRAW_FRAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIRST_DRAW_FRAME: Int
```

Metric identifier for a boolean value determining whether this frame was the first to draw in a new Window layout.

[getMetric(int)](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#getMetric(kotlin.Int))will return 0 for false, 1 for true.

First draw frames are expected to be slow and should usually be exempt from display jank calculations as they do not cause skips in animations and are usually hidden by window animations or other tricks. 

 Value: 9

### FRAME_TIMELINE_VSYNC_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_TIMELINE_VSYNC_ID: Int
```

Metric identifier for the frame's VSync identifier.

The id that corresponds to the chosen frame timeline, used to correlate a frame produced by HWUI with the timeline data from the compositor. 

 Value: 14

### GPU_DURATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPU_DURATION: Int
```

Metric identifier for GPU duration.

Represents the total time in nanoseconds this frame took to complete on the GPU. 

 Value: 12

### INPUT_HANDLING_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_HANDLING_DURATION: Int
```

Metric identifier for input handling duration.

Represents the number of nanoseconds elapsed issuing input handling callbacks. 

 Value: 1

### INTENDED_VSYNC_TIMESTAMP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENDED_VSYNC_TIMESTAMP: Int
```

Metric identifier for the timestamp of the intended vsync for this frame.

The intended start point for the frame. If this value is different from [VSYNC_TIMESTAMP](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#VSYNC_TIMESTAMP:kotlin.Int), there was work occurring on the UI thread that prevented it from responding to the vsync signal in a timely fashion. 

 Value: 10

### LAYOUT_MEASURE_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAYOUT_MEASURE_DURATION: Int
```

Metric identifier for layout/measure duration.

Represents the number of nanoseconds elapsed measuring and laying out the invalidated pieces of the view hierarchy. 

 Value: 3

### SWAP_BUFFERS_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWAP_BUFFERS_DURATION: Int
```

Metric identifier for swap buffers duration.

Represents the number of nanoseconds elapsed issuing the frame buffer for this frame to the display subsystem. 

 Value: 7

### SYNC_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DURATION: Int
```

Metric identifier for sync duration.

Represents the number of nanoseconds elapsed synchronizing the computed display lists with the render thread. 

 Value: 5

### TOTAL_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOTAL_DURATION: Int
```

Metric identifier for total frame duration.

Represents the total time in nanoseconds this frame took to render and be issued to the display subsystem.

The total duration is the difference in time between when the frame began and when it ended. This value may not be exactly equal to the sum of the values of all other time-valued metric identifiers because some stages may happen concurrently. 

 Value: 8

### UNKNOWN_DELAY_DURATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_DELAY_DURATION: Int
```

Metric identifier for unknown delay.

Represents the number of nanoseconds elapsed waiting for the UI thread to become responsive and process the frame. This should be 0 most of the time. 

 Value: 0

### VSYNC_TIMESTAMP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VSYNC_TIMESTAMP: Int
```

Metric identifier for the timestamp of the actual vsync for this frame.

The time value that was used in all the vsync listeners and drawing for the frame (Choreographer frame callbacks, animations, [View.getDrawingTime()](https://developer.android.com/reference/kotlin/android/view/View#getDrawingTime()), etc.) 

 Value: 11

## Public constructors

### FrameMetrics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FrameMetrics(other: FrameMetrics!)
```

Constructs a FrameMetrics object as a copy.

Use this method to copy out metrics reported by [Window.OnFrameMetricsAvailableListener.onFrameMetricsAvailable(](https://developer.android.com/reference/kotlin/android/view/Window.OnFrameMetricsAvailableListener#onFrameMetricsAvailable(android.view.Window,%20android.view.FrameMetrics,%20kotlin.Int))

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `other` | [FrameMetrics](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#)!:the FrameMetrics object to copy. |

## Public methods

### getMetric

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetric(id: Int): Long
```

Retrieves the value associated with Metric identifier`id`for this frame.

Boolean metrics are represented in \[0,1\], with 0 corresponding to false, and 1 corresponding to true.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the metric to retrieve Value is [android.view.FrameMetrics#UNKNOWN_DELAY_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#UNKNOWN_DELAY_DURATION:kotlin.Int), [android.view.FrameMetrics#INPUT_HANDLING_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#INPUT_HANDLING_DURATION:kotlin.Int), [android.view.FrameMetrics#ANIMATION_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#ANIMATION_DURATION:kotlin.Int), [android.view.FrameMetrics#LAYOUT_MEASURE_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#LAYOUT_MEASURE_DURATION:kotlin.Int), [android.view.FrameMetrics#DRAW_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#DRAW_DURATION:kotlin.Int), [android.view.FrameMetrics#SYNC_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#SYNC_DURATION:kotlin.Int), [android.view.FrameMetrics#COMMAND_ISSUE_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#COMMAND_ISSUE_DURATION:kotlin.Int), [android.view.FrameMetrics#SWAP_BUFFERS_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#SWAP_BUFFERS_DURATION:kotlin.Int), [android.view.FrameMetrics#TOTAL_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#TOTAL_DURATION:kotlin.Int), [android.view.FrameMetrics#FIRST_DRAW_FRAME](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#FIRST_DRAW_FRAME:kotlin.Int), [android.view.FrameMetrics#INTENDED_VSYNC_TIMESTAMP](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#INTENDED_VSYNC_TIMESTAMP:kotlin.Int), [android.view.FrameMetrics#VSYNC_TIMESTAMP](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#VSYNC_TIMESTAMP:kotlin.Int), [android.view.FrameMetrics#GPU_DURATION](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#GPU_DURATION:kotlin.Int), or [android.view.FrameMetrics#DEADLINE](https://developer.android.com/reference/kotlin/android/view/FrameMetrics#DEADLINE:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of the metric or -1 if it is not available. |
