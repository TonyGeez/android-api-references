Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsageStatsManager

```
class UsageStatsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.usage.UsageStatsManager](UsageStatsManager.md) |

Provides access to device usage history and statistics. Usage data is aggregated into time intervals: days, weeks, months, and years.

<br />

When requesting usage data since a particular time, the request might look something like this:

```kotlin
PAST                   REQUEST_TIME                    TODAY                   FUTURE
  ---||---¦---|
                         YEAR ||                           ¦                       |
  ---||---¦---|
   MONTH            |         ||                MONTH      ¦                       |
  ---|---||---¦---|
    |      WEEK     |     WEEK||    |     WEEK     |     WE¦EK     |      WEEK     |
  ---||---|---¦---|
                              ||           |DAY|DAY|DAY|DAY¦DAY|DAY|DAY|DAY|DAY|DAY|
  ---||---¦---|
  
```
A request for data in the middle of a time interval will include that interval.

<br />

**NOTE:** Most methods on this API require the permission android.permission.PACKAGE_USAGE_STATS. However, declaring the permission implies intention to use the API and the user of the device still needs to grant permission through the Settings application. See `https://developer.android.com/reference/kotlin/android/provider/Settings.html#ACTION_USAGE_ACCESS_SETTINGS:kotlin.String`. Methods which only return the information for the calling package do not require this permission. E.g. `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()` and `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEventsForSelf(kotlin.Long,%20kotlin.Long)`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#EXTRA_EVENT_ACTION:kotlin.String` A String extra, when used with `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#getExtras()`, that indicates the action of the user interaction associated with the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#EXTRA_EVENT_CATEGORY:kotlin.String` A String extra, when used with `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#getExtras()`, that indicates the category of the user interaction associated with the event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_BEST:kotlin.Int` An interval type that will use the best fit interval for the given time range. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_DAILY:kotlin.Int` An interval type that spans a day. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_MONTHLY:kotlin.Int` An interval type that spans a month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_WEEKLY:kotlin.Int` An interval type that spans a week. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_YEARLY:kotlin.Int` An interval type that spans a year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` The app was used very recently, currently in use or likely to be used very soon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_FREQUENT:kotlin.Int` The app was used in the last few days and/or likely to be used in the next few days. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_RARE:kotlin.Int` The app has not be used for several days and/or is unlikely to be used for several days. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_RESTRICTED:kotlin.Int` The app has not be used for several days, is unlikely to be used for several days, and has been misbehaving in some manner. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_WORKING_SET:kotlin.Int` The app was used recently and/or likely to be used in the next few hours. |
| --- | --- |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()()` Returns the current standby bucket of the calling app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#isAppInactive(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns whether the specified app is currently considered inactive. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [UsageStats](UsageStats.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryAndAggregateUsageStats(kotlin.Long,%20kotlin.Long)(beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` A convenience method that queries for all stats in the given range (using the best interval for that range), merges the resulting data, and keys it by package name. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppUsageDuration](../android/app/usage/AppUsageDuration.md)!\> | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryAppUsageDuration(android.app.usage.AppUsageDurationQuery)(query: https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDurationQuery)` Gets application usage stats for the given time range, aggregated by the specified interval. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ConfigurationStats](ConfigurationStats.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryConfigurations(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(intervalType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Gets the hardware configurations the device was in for the given time range, aggregated by the specified interval. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EventStats](EventStats.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEventStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(intervalType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Gets aggregated event stats for the given time range, aggregated by the specified interval. |
| --- | --- |
| [UsageEvents](UsageEvents.md)? | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(android.app.usage.UsageEventsQuery)(query: https://developer.android.com/reference/kotlin/android/app/usage/UsageEventsQuery)` Query for events with specific UsageEventsQuery object. |
| [UsageEvents](UsageEvents.md)! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(kotlin.Long,%20kotlin.Long)(beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Query for events in the given time range. |
| [UsageEvents](UsageEvents.md)! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEventsForSelf(kotlin.Long,%20kotlin.Long)(beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Like `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(kotlin.Long,%20kotlin.Long)`, but only returns events for the calling package. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UsageStats](UsageStats.md)!\>! | `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(intervalType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Gets application usage stats for the given time range, aggregated by the specified interval. |

## Constants

### EXTRA_EVENT_ACTION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EVENT_ACTION: String
```

A String extra, when used with `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#getExtras()`, that indicates the action of the user interaction associated with the event. The action cannot be more than 127 characters, longer value will be truncated to 127 characters.

 Value: "android.app.usage.extra.EVENT_ACTION"

### EXTRA_EVENT_CATEGORY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_EVENT_CATEGORY: String
```

A String extra, when used with `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#getExtras()`, that indicates the category of the user interaction associated with the event. The category cannot be more than 127 characters, longer value will be truncated to 127 characters.

 Value: "android.app.usage.extra.EVENT_CATEGORY"

### INTERVAL_BEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_BEST: Int
```

An interval type that will use the best fit interval for the given time range. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`.

 Value: 4

### INTERVAL_DAILY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_DAILY: Int
```

An interval type that spans a day. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`.

 Value: 0

### INTERVAL_MONTHLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_MONTHLY: Int
```

An interval type that spans a month. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`.

 Value: 2

### INTERVAL_WEEKLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_WEEKLY: Int
```

An interval type that spans a week. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`.

 Value: 1

### INTERVAL_YEARLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERVAL_YEARLY: Int
```

An interval type that spans a year. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`.

 Value: 3

### STANDBY_BUCKET_ACTIVE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDBY_BUCKET_ACTIVE: Int
```

The app was used very recently, currently in use or likely to be used very soon. Standby bucket values that are ≤ `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` will not be throttled by the system while they are in this bucket. Buckets \> `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` will most likely be restricted in some way. For instance, jobs and alarms may be deferred.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()`

### STANDBY_BUCKET_FREQUENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDBY_BUCKET_FREQUENT: Int
```

The app was used in the last few days and/or likely to be used in the next few days. Restrictions will apply to these apps, such as deferral of jobs and alarms. The delays may be greater than for apps in higher buckets (lower bucket value). Bucket values \> `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_FREQUENT:kotlin.Int` may additionally have network access limited.

 Value: 30

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()`

### STANDBY_BUCKET_RARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDBY_BUCKET_RARE: Int
```

The app has not be used for several days and/or is unlikely to be used for several days. Apps in this bucket will have more restrictions, including network restrictions, except during certain short periods (at a minimum, once a day) when they are allowed to execute jobs, access the network, etc.

 Value: 40

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()`

### STANDBY_BUCKET_RESTRICTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDBY_BUCKET_RESTRICTED: Int
```

The app has not be used for several days, is unlikely to be used for several days, and has been misbehaving in some manner. Apps in this bucket will have the most restrictions, including network restrictions and additional restrictions on jobs.

Note: this bucket is not enabled in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.

 Value: 45

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()`

### STANDBY_BUCKET_WORKING_SET

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDBY_BUCKET_WORKING_SET: Int
```

The app was used recently and/or likely to be used in the next few hours. Restrictions will apply to these apps, such as deferral of jobs and alarms.

 Value: 20

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#getAppStandbyBucket()`

## Public methods

### getAppStandbyBucket

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppStandbyBucket(): Int
```

Returns the current standby bucket of the calling app. The system determines the standby state of the app based on app usage patterns. Standby buckets determine how much an app will be restricted from running background tasks such as jobs and alarms.

Restrictions increase progressively from `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_RESTRICTED:kotlin.Int`, with `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` being the least restrictive. The battery level of the device might also affect the restrictions.

Apps in buckets ≤ `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` have no standby restrictions imposed. Apps in buckets \> `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_FREQUENT:kotlin.Int` may have network access restricted when running in the background.

The standby state of an app can change at any time either due to a user interaction or a system interaction or some algorithm determining that the app can be restricted for a period of time before the user has a need for it.

You can also query the recent history of standby bucket changes by calling `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEventsForSelf(kotlin.Long,%20kotlin.Long)` and searching for `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#STANDBY_BUCKET_CHANGED:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current standby bucket of the calling app. One of STANDBY_BUCKET_\* constants. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_ACTIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_WORKING_SET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_FREQUENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_RARE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#STANDBY_BUCKET_RESTRICTED:kotlin.Int` |

### isAppInactive

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAppInactive(packageName: String!): Boolean
```

Returns whether the specified app is currently considered inactive. This will be true if the app hasn't been used directly or indirectly for a period of time defined by the system. This could be of the order of several hours or days. Apps are not considered inactive when the device is charging.

The caller must have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String` to query the inactive state of other apps

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package name of the app to query |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether the app is currently considered inactive or false if querying another app without `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String` |

### queryAndAggregateUsageStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryAndAggregateUsageStats(
    beginTime: Long, 
    endTime: Long
): MutableMap<String!, UsageStats!>!
```

A convenience method that queries for all stats in the given range (using the best interval for that range), merges the resulting data, and keys it by package name. See `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/android/app/usage/UsageStats!>!` | A `https://developer.android.com/reference/kotlin/java/util/Map.html#` keyed by package name |

### queryAppUsageDuration

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryAppUsageDuration(query: AppUsageDurationQuery): MutableList<AppUsageDuration!>
```

Gets application usage stats for the given time range, aggregated by the specified interval.

The usage statistics are pre-aggregated internally into calendar-aligned boundaries (e.g., for `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_DAILY:kotlin.Int`, a day is defined as midnight to midnight local time). The returned list will only contain apps that have been used in this time range.

The returned list will contain one or more `https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDuration` objects for each package, with usage data aggregated within each interval bucket that falls within the time range between `https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDurationQuery#getStartTimeMillis()` and `https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDurationQuery#getEndTimeMillis()`, which may include the expanded interval periods as described above.

Data can only be queried for the past 30 days. Queries for longer time ranges will return an empty list. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_APP_USAGE:kotlin.String`

| Parameters ||
|---|---|
| `query` | [AppUsageDurationQuery](../android/app/usage/AppUsageDurationQuery.md): the `https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDurationQuery` used to specify the query parameters. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDuration!>` | a list of `https://developer.android.com/reference/kotlin/android/app/usage/AppUsageDuration` for each app used for the given time interval. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the caller doesn't hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_APP_USAGE:kotlin.String` permission |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_DAILY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_WEEKLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_MONTHLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_YEARLY:kotlin.Int`

### queryConfigurations

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryConfigurations(
    intervalType: Int, 
    beginTime: Long, 
    endTime: Long
): MutableList<ConfigurationStats!>!
```

Gets the hardware configurations the device was in for the given time range, aggregated by the specified interval. The results are ordered as in `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryUsageStats(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`. *Note: Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.* . 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `intervalType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time interval by which the stats are aggregated. |
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats!>!` | A list of `https://developer.android.com/reference/kotlin/android/app/usage/ConfigurationStats` |

### queryEventStats

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryEventStats(
    intervalType: Int, 
    beginTime: Long, 
    endTime: Long
): MutableList<EventStats!>!
```

Gets aggregated event stats for the given time range, aggregated by the specified interval.

The returned list will contain a `https://developer.android.com/reference/kotlin/android/app/usage/EventStats` object for each event type that is being aggregated and has data for an interval that is a subset of the time range given.

The current event types that will be aggregated here are:

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#SCREEN_INTERACTIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#SCREEN_NON_INTERACTIVE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#KEYGUARD_SHOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event#KEYGUARD_HIDDEN:kotlin.Int`

*Note: Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.* . 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `intervalType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time interval by which the stats are aggregated. |
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/usage/EventStats!>!` | A list of `https://developer.android.com/reference/kotlin/android/app/usage/EventStats` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_DAILY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_WEEKLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_MONTHLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_YEARLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_BEST:kotlin.Int`

### queryEvents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryEvents(query: UsageEventsQuery): UsageEvents?
```

Query for events with specific UsageEventsQuery object. *Note: if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.* . 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `query` | [UsageEventsQuery](UsageEventsQuery.md): The query object used to specify the query parameters. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents?` | A `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents` which contains the events matching the query parameters. |

### queryEvents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryEvents(
    beginTime: Long, 
    endTime: Long
): UsageEvents!
```

Query for events in the given time range. Events are only kept by the system for a few days. *Note: Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.* . 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents!` | A `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents`. |

### queryEventsForSelf

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryEventsForSelf(
    beginTime: Long, 
    endTime: Long
): UsageEvents!
```

Like `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(kotlin.Long,%20kotlin.Long)`, but only returns events for the calling package. *Note: Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.*

| Parameters ||
|---|---|
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents!` | A `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents` object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#queryEvents(kotlin.Long,%20kotlin.Long)`

### queryUsageStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun queryUsageStats(
    intervalType: Int, 
    beginTime: Long, 
    endTime: Long
): MutableList<UsageStats!>!
```

Gets application usage stats for the given time range, aggregated by the specified interval.

The returned list will contain one or more `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats` objects for each package, with usage data that covers at least the given time range. Note: The begin and end times of the time range may be expanded to the nearest whole interval period.
*Note: Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, if the user's device is not in an unlocked state (as defined by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#isUserUnlocked()`), then `null` will be returned.* . 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PACKAGE_USAGE_STATS:kotlin.String`

| Parameters ||
|---|---|
| `intervalType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time interval by which the stats are aggregated. |
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of stats to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/usage/UsageStats!>!` | A list of `https://developer.android.com/reference/kotlin/android/app/usage/UsageStats` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_DAILY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_WEEKLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_MONTHLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_YEARLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager#INTERVAL_BEST:kotlin.Int`
