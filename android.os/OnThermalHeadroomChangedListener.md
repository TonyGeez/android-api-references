Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnThermalHeadroomChangedListener

Kotlin | [Java](https://developer.android.com/reference/android/os/PowerManager.OnThermalHeadroomChangedListener "View this page in Java")
| --- | --- |

```
interface OnThermalHeadroomChangedListener
```

| [android.os.PowerManager.OnThermalHeadroomChangedListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener#) |

Listener passed to android.os.PowerManager#addThermalHeadroomListener and `https://developer.android.com/reference/kotlin/android/os/PowerManager#removeThermalHeadroomListener(android.os.PowerManager.OnThermalHeadroomChangedListener)` to notify caller of Thermal headroom or thresholds changes.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener#onThermalHeadroomChanged(kotlin.Float,%20kotlin.Float,%20kotlin.Int,%20kotlin.collections.MutableMap)(headroom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, forecastHeadroom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, forecastSeconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, thresholds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html!>)` Called when overall thermal headroom or headroom thresholds have significantly changed that requires action. |

## Public methods

### onThermalHeadroomChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onThermalHeadroomChanged(
    headroom: Float, 
    forecastHeadroom: Float, 
    forecastSeconds: Int, 
    thresholds: MutableMap<Int!, Float!>
): Unit
```

Called when overall thermal headroom or headroom thresholds have significantly changed that requires action.

This may not be used to fully replace the `https://developer.android.com/reference/kotlin/android/os/PowerManager#getThermalHeadroom(kotlin.Int)` API as it will only notify on one of the conditions below that will significantly change one or both values of current headroom and headroom thresholds since previous callback: 1. thermal throttling events: when the skin temperature has cross any of the thresholds and there isn't a previous callback in a short time ago with similar values. 2. skin temperature threshold change events: note that if the absolute °C threshold values change in a way that does not significantly change the current headroom nor headroom thresholds, it will not trigger any callback. The client should not need to take action in such case since the difference from temperature vs threshold hasn't changed.

By API version 36, it provides a forecast in the same call for developer's convenience based on a `forecastSeconds` defined by the device, which can be static or dynamic varied by OEM. Be aware that it will not notify on forecast temperature change but the events mentioned above. So periodically polling against `https://developer.android.com/reference/kotlin/android/os/PowerManager#getThermalHeadroom(kotlin.Int)` API should still be used to actively monitor temperature forecast in advance.

This serves as a more advanced option compared to thermal status listener, where the latter will only notify on thermal throttling events with status update.

| Parameters ||
|---|---|
| `headroom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): current headroom. Value is 0.0f or greater |
| `forecastHeadroom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): forecasted headroom in future. Value is 0.0f or greater |
| `forecastSeconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): how many seconds in the future used in forecast. Value is 0 or greater |
| --- | --- |
| `thresholds` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>: new headroom thresholds, see `https://developer.android.com/reference/kotlin/android/os/PowerManager#getThermalHeadroomThresholds()` This value cannot be `null`. |
