# TimeRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeRangeFilter

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/TimeRangeFilter "View this page in Java") 

```
interface TimeRangeFilter
```

| [android.health.connect.TimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter#) |

| Known Direct Subclasses [LocalTimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/LocalTimeRangeFilter), [TimeInstantRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [LocalTimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/LocalTimeRangeFilter) | Specification of local time range for health connect requests. | | [TimeInstantRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter) | Specification of time range for read and delete requests. | |

A Base class to represent a request for time range for read and delete requests. Internally represents a SQLLite \* argument that specifies start and end time to put in as SQLLite parameters.

## Summary
