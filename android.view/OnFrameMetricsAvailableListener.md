# Window.OnFrameMetricsAvailableListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFrameMetricsAvailableListener

Kotlin | [Java](../android/view/Window.OnFrameMetricsAvailableListener.md) 
| --- | --- |

```
interface OnFrameMetricsAvailableListener
```

| [android.view.Window.OnFrameMetricsAvailableListener](../android/view/Window.OnFrameMetricsAvailableListener.md) |

Callback for clients that want frame timing information for each frame rendered by the Window.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFrameMetricsAvailable](../android/view/Window.OnFrameMetricsAvailableListener.md))`(`window:` ` [Window](Window.md)!`, `frameMetrics:` ` [FrameMetrics](FrameMetrics.md)!`, `dropCountSinceLastInvocation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when information is available for the previously rendered frame. |

## Public methods

### onFrameMetricsAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFrameMetricsAvailable(
    window: Window!, 
    frameMetrics: FrameMetrics!, 
    dropCountSinceLastInvocation: Int
): Unit
```

Called when information is available for the previously rendered frame. Reports can be dropped if this callback takes too long to execute, as the report producer cannot wait for the consumer to complete. It is highly recommended that clients copy the passed in FrameMetrics via [FrameMetrics.FrameMetrics(FrameMetrics)](FrameMetrics.md)) within this method and defer additional computation or storage to another thread to avoid unnecessarily dropping reports.

| Parameters ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `window` | [Window](Window.md)!: The [Window](Window.md) on which the frame was displayed. |
| `frameMetrics` | [FrameMetrics](FrameMetrics.md)!: the available metrics. This object is reused on every call and thus **this reference is not valid outside the scope of this method**. |
| `dropCountSinceLastInvocation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of reports dropped since the last time this callback was invoked. |
| --- | --- |
