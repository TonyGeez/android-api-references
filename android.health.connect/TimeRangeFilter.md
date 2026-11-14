# TimeRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeRangeFilter

Kotlin| [Java](TimeRangeFilter.md) 
| --- | --- |

```
interface TimeRangeFilter
```

| [android.health.connect.TimeRangeFilter](TimeRangeFilter.md) |

| Known Direct Subclasses [LocalTimeRangeFilter](LocalTimeRangeFilter.md), [TimeInstantRangeFilter](TimeInstantRangeFilter.md) |------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [LocalTimeRangeFilter](LocalTimeRangeFilter.md) | Specification of local time range for health connect requests. | | [TimeInstantRangeFilter](TimeInstantRangeFilter.md) | Specification of time range for read and delete requests. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Base class to represent a request for time range for read and delete requests. Internally represents a SQLLite \* argument that specifies start and end time to put in as SQLLite parameters.

## Summary
