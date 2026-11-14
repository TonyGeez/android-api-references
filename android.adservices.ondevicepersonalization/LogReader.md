Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LogReader

```
open class LogReader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.LogReader](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/LogReader#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

An interface to a read logs from REQUESTS and EVENTS Used as a Data Access Object for the REQUESTS and EVENTS table.

## Summary

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord)!\> | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/LogReader#getJoinedEvents(java.time.Instant,%20java.time.Instant)(startTime: https://developer.android.com/reference/kotlin/java/time/Instant.html#, endTime: https://developer.android.com/reference/kotlin/java/time/Instant.html#)` Retrieves a List of EventLogRecord with its corresponding RequestLogRecord written by this IsolatedService within the specified time range. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)!\> | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/LogReader#getRequests(java.time.Instant,%20java.time.Instant)(startTime: https://developer.android.com/reference/kotlin/java/time/Instant.html#, endTime: https://developer.android.com/reference/kotlin/java/time/Instant.html#)` Retrieves a List of RequestLogRecords written by this IsolatedService within the specified time range. |

## Public methods

### getJoinedEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getJoinedEvents(
    startTime: Instant, 
    endTime: Instant
): MutableList<EventLogRecord!>
```

**Deprecated:** *Deprecated in Java.*

Retrieves a List of EventLogRecord with its corresponding RequestLogRecord written by this IsolatedService within the specified time range. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `startTime` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#): This value cannot be `null`. |
| `endTime` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord!>` | This value cannot be `null`. |

### getRequests

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequests(
    startTime: Instant, 
    endTime: Instant
): MutableList<RequestLogRecord!>
```

**Deprecated:** *Deprecated in Java.*

Retrieves a List of RequestLogRecords written by this IsolatedService within the specified time range. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `startTime` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#): This value cannot be `null`. |
| `endTime` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord!>` | This value cannot be `null`. |
