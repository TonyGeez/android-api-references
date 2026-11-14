Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangingResultCallback

Kotlin | [Java](RangingResultCallback.md)
| --- | --- |

```
abstract class RangingResultCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.RangingResultCallback](RangingResultCallback.md) |

Base class for ranging result callbacks. Should be extended by applications and set when calling startRanging. If the ranging operation fails in whole (not attempted) then onRangingFailure will be called with a failure code. If the ranging operation is performed for each of the requested peers then the onRangingResults will be called with the set of results (@link RangingResult, each of which has its own success/failure code getStatus.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResultCallback#STATUS_CODE_FAIL:kotlin.Int` A failure code for the whole ranging request operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResultCallback#STATUS_CODE_FAIL_RTT_NOT_AVAILABLE:kotlin.Int` A failure code for the whole ranging request operation. |

| Public constructors ||
|---|---|
| RangingResultCallback <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRangingFailure Called when a ranging operation failed in whole - i. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRangingResults Called when a ranging operation was executed. |

## Constants

### STATUS_CODE_FAIL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_CODE_FAIL: Int
```

A failure code for the whole ranging request operation. Indicates a failure.

 Value: 1

### STATUS_CODE_FAIL_RTT_NOT_AVAILABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATUS_CODE_FAIL_RTT_NOT_AVAILABLE: Int
```

A failure code for the whole ranging request operation. Indicates that the request failed due to RTT not being available - e.g. Wi-Fi was disabled. Use the isAvailable and `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager#ACTION_WIFI_RTT_STATE_CHANGED:kotlin.String` to track RTT availability.

 Value: 2

## Public constructors

### RangingResultCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RangingResultCallback()
```

## Public methods

### onRangingFailure

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onRangingFailure(code: Int): Unit
```

Called when a ranging operation failed in whole - i.e. no ranging operation to any of the devices specified in the request was attempted.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A status code indicating the type of failure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResultCallback#STATUS_CODE_FAIL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/RangingResultCallback#STATUS_CODE_FAIL_RTT_NOT_AVAILABLE:kotlin.Int` |

### onRangingResults

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onRangingResults(results: MutableList<RangingResult!>): Unit
```

Called when a ranging operation was executed. The list of results corresponds to devices specified in the ranging request.

| Parameters ||
|---|---|
| `results` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RangingResult](RangingResult.md)!\>: List of range measurements, one per requested device. This value cannot be `null`. |
