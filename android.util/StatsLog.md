# StatsLog

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatsLog

Kotlin| [Java](StatsLog.md) 
| --- | --- |

```
class StatsLog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.StatsLog](StatsLog.md) |

StatsLog provides an API for developers to send events to statsd. The events can be used to define custom metrics inside statsd.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [logBinaryPushStateChanged](StatsLog.md))`(`trainName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `trainVersionCode:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `experimentIds:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`)` Logs an event for binary push for module updates. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [logEvent](StatsLog.md))`(`label:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Logs an event that does not represent a start or stop boundary. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [logStart](StatsLog.md))`(`label:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Logs a start event. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [logStop](StatsLog.md))`(`label:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Logs a stop event. |

## Public methods

### logBinaryPushStateChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun logBinaryPushStateChanged(
    trainName: String, 
    trainVersionCode: Long, 
    options: Int, 
    state: Int, 
    experimentIds: LongArray
): Boolean
```

Logs an event for binary push for module updates. 
Requires [android.Manifest.permission#DUMP](../android/Manifest.permission.md) and [android.Manifest.permission#PACKAGE_USAGE_STATS](../android/Manifest.permission.md)

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trainName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of install train. This value cannot be`null`. |
| `trainVersionCode` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):version code of the train. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):optional flags about this install. The last 3 bits indicate options: 0x01: FLAG_REQUIRE_STAGING 0x02: FLAG_ROLLBACK_ENABLED 0x04: FLAG_REQUIRE_LOW_LATENCY_MONITOR |
| --- | --- |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):current install state. Defined as State enums in BinaryPushStateChanged atom in frameworks/proto_logging/stats/atoms.proto |
| `experimentIds` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):experiment ids. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the log request was sent to statsd. |

### logEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun logEvent(label: Int): Boolean
```

Logs an event that does not represent a start or stop boundary.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `label` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):developer-chosen label. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the log request was sent to statsd. |

### logStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun logStart(label: Int): Boolean
```

Logs a start event.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `label` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):developer-chosen label. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the log request was sent to statsd. |

### logStop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun logStop(label: Int): Boolean
```

Logs a stop event.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `label` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):developer-chosen label. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the log request was sent to statsd. |
