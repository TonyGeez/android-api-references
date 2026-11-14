Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeManager

```
class TimeManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.time.TimeManager](TimeManager.md) |

The system service through which system components can interact with time and time zone services.

## Summary

| Public methods ||
|---|---|
| [TimeZone](../java.util/TimeZone.md)? | getHomeTimeZone Returns the current home time zone. |

## Public methods

### getHomeTimeZone

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHomeTimeZone(): TimeZone?
```

Returns the current home time zone.

The returned value may be `null` if the home time zone is not set or if the home time zone is invalid. This API only supports Olson IDs (e.g. "Europe/London"). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_HOME_TIME_ZONE:kotlin.String`
