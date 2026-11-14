Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeUtils

Kotlin | [Java](../android/util/TimeUtils.md)
| --- | --- |

```
open class TimeUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.TimeUtils](../android/util/TimeUtils.md) |

A class containing utility methods related to time zones.

## Summary

| Public methods ||
|---|---|
| open static [TimeZone](../java/util/TimeZone.md)! | `https://developer.android.com/reference/kotlin/android/util/TimeUtils#getTimeZone(kotlin.Int,%20kotlin.Boolean,%20kotlin.Long,%20kotlin.String)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, country: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Tries to return a time zone that would have had the specified offset and DST value at the specified moment in the specified country. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/util/TimeUtils#getTimeZoneDatabaseVersion()()` Returns a String indicating the version of the time zone database currently in use. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/util/TimeUtils#getTimeZoneIdsForCountryCode(kotlin.String)(countryCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns time zone IDs for time zones known to be associated with a country. |
| --- | --- |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/util/TimeUtils#isTimeBetween(java.time.LocalTime,%20java.time.LocalTime,%20java.time.LocalTime)(reference: https://developer.android.com/reference/kotlin/java/time/LocalTime.html#, start: https://developer.android.com/reference/kotlin/java/time/LocalTime.html#, end: https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)` This method is used to find if a clock time is inclusively between two other clock times |

## Public methods

### getTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTimeZone(
    offset: Int, 
    dst: Boolean, 
    when: Long, 
    country: String!
): TimeZone!
```

Tries to return a time zone that would have had the specified offset and DST value at the specified moment in the specified country. Returns null if no suitable zone could be found.

### getTimeZoneDatabaseVersion

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTimeZoneDatabaseVersion(): String!
```

Returns a String indicating the version of the time zone database currently in use. The format of the string is dependent on the underlying time zone database implementation, but will typically contain the year in which the database was updated plus a letter from a to z indicating changes made within that year.

Time zone database updates should be expected to occur periodically due to political and legal changes that cannot be anticipated in advance. Therefore, when computing the time for a future event, applications should be aware that the results may differ following a time zone database update. This method allows applications to detect that a database change has occurred, and to recalculate any cached times accordingly.

The time zone database may be assumed to change only when the device runtime is restarted. Therefore, it is not necessary to re-query the database version during the lifetime of an activity.

### getTimeZoneIdsForCountryCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getTimeZoneIdsForCountryCode(countryCode: String): MutableList<String!>?
```

Returns time zone IDs for time zones known to be associated with a country.

The list returned may be different from other on-device sources like `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#getRegion(kotlin.String)` as it can be curated to avoid contentious or obsolete mappings.

| Parameters ||
|---|---|
| `countryCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the ISO 3166-1 alpha-2 code for the country as can be obtained using `https://developer.android.com/reference/kotlin/java/util/Locale.html#getCountry()` This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | IDs that can be passed to `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#getTimeZone(kotlin.String)` or similar methods, or `null` if the countryCode is unrecognized |

### isTimeBetween

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isTimeBetween(
    reference: LocalTime, 
    start: LocalTime, 
    end: LocalTime
): Boolean
```

This method is used to find if a clock time is inclusively between two other clock times

| Parameters ||
|---|---|
| `reference` | [LocalTime](../java/time/LocalTime.md): The time of the day we want check if it is between start and end. This value cannot be `null`. |
| `start` | [LocalTime](../java/time/LocalTime.md): The start time reference. This value cannot be `null`. |
| `end` | [LocalTime](../java/time/LocalTime.md): The end time. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the reference time is between the two clock times, and false otherwise. |
