# TimeZoneNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeZoneNames

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/TimeZoneNames "View this page in Java") 
| --- | --- |

```
abstract class TimeZoneNames : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#) |

`TimeZoneNames`is an abstract class representing the time zone display name data model defined by [UTS#35 Unicode Locale Data Markup Language (LDML)](http://www.unicode.org/reports/tr35/). The model defines meta zone, which is used for storing a set of display names. A meta zone can be shared by multiple time zones. Also a time zone may have multiple meta zone historic mappings.

For example, people in the United States refer the zone used by the east part of North America as "Eastern Time". The tz database contains multiple time zones "America/New_York", "America/Detroit", "America/Montreal" and some others that belong to "Eastern Time". However, assigning different display names to these time zones does not make much sense for most of people.

In [CLDR](http://cldr.unicode.org/)(which uses LDML for representing locale data), the display name "Eastern Time" is stored as long generic display name of a meta zone identified by the ID "America_Eastern". Then, there is another table maintaining the historic mapping to meta zones for each time zone. The time zones in the above example ("America/New_York", "America/Detroit"...) are mapped to the meta zone "America_Eastern".

Sometimes, a time zone is mapped to a different time zone in the past. For example, "America/Indiana/Knox" had been moving "Eastern Time" and "Central Time" back and forth. Therefore, it is necessary that time zone to meta zones mapping data are stored by date range.

**Note:**

[TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat) assumes an instance of`TimeZoneNames`is immutable. If you want to provide your own`TimeZoneNames`implementation and use it with [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat), you must follow the contract.

The methods in this class assume that time zone IDs are already canonicalized. For example, you may not get proper result returned by a method with time zone ID "America/Indiana/Indianapolis", because it's not a canonical time zone ID (the canonical time zone ID for the time zone is "America/Indianapolis". See [TimeZone.getCanonicalID(String)](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#getCanonicalID(kotlin.String))about ICU canonical time zone IDs.

In CLDR, most of time zone display names except location names are provided through meta zones. But a time zone may have a specific name that is not shared with other time zones. For example, time zone "Europe/London" has English long name for standard time "Greenwich Mean Time", which is also shared with other time zones. However, the long name for daylight saving time is "British Summer Time", which is only used for "Europe/London".

[getTimeZoneDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getTimeZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType))is designed for accessing a name only used by a single time zone. But is not necessarily mean that a subclass implementation use the same model with CLDR. A subclass implementation may provide time zone names only through [getTimeZoneDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getTimeZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType)), or only through [getMetaZoneDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType)), or both.

The default`TimeZoneNames`implementation returned by [getInstance(android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getInstance(android.icu.util.ULocale))uses the locale data imported from CLDR. In CLDR, set of meta zone IDs and mappings between zone IDs and meta zone IDs are shared by all locales. Therefore, the behavior of [getAvailableMetaZoneIDs()](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getAvailableMetaZoneIDs()), [getAvailableMetaZoneIDs(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getAvailableMetaZoneIDs(kotlin.String)), [getMetaZoneID(java.lang.String,long)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneID(kotlin.String,%20kotlin.Long)), and [getReferenceZoneID(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getReferenceZoneID(kotlin.String,%20kotlin.String))won't be changed no matter what locale is used for getting an instance of`TimeZoneNames`.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------|
| | [NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType) Time zone display name types |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableMetaZoneIDs](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getAvailableMetaZoneIDs())`()` Returns an immutable set of all available meta zone IDs. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableMetaZoneIDs](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getAvailableMetaZoneIDs(kotlin.String))`(`tzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns an immutable set of all available meta zone IDs used by the given time zone. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType,%20kotlin.Long))`(`tzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!`, `date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the display name of the time zone at the given date. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExemplarLocationName](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getExemplarLocationName(kotlin.String))`(`tzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the exemplar location name for the given time zone. |
| openstatic [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns an instance of`TimeZoneNames`for the specified locale. |
| openstatic [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns an instance of`TimeZoneNames`for the specified [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMetaZoneDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType))`(`mzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!`)` Returns the display name of the meta zone. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMetaZoneID](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneID(kotlin.String,%20kotlin.Long))`(`tzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the meta zone ID for the given canonical time zone ID at the given date. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReferenceZoneID](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getReferenceZoneID(kotlin.String,%20kotlin.String))`(`mzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `region:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the reference zone ID for the given meta zone ID for the region. |
| --- | --- |
| openstatic [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#)! | [getTZDBInstance](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getTZDBInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns an instance of`TimeZoneNames`containing only short specific zone names ([NameType.SHORT_STANDARD](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType) and [NameType.SHORT_DAYLIGHT](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)), compatible with the IANA tz database's zone abbreviations (not localized). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTimeZoneDisplayName](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getTimeZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType))`(`tzID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!`)` Returns the display name of the time zone. |

## Public methods

### getAvailableMetaZoneIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAvailableMetaZoneIDs(): MutableSet<String!>!
```

Returns an immutable set of all available meta zone IDs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An immutable set of all available meta zone IDs. |

### getAvailableMetaZoneIDs

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAvailableMetaZoneIDs(tzID: String!): MutableSet<String!>!
```

Returns an immutable set of all available meta zone IDs used by the given time zone.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `tzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The canonical time zone ID. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An immutable set of all available meta zone IDs used by the given time zone. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(
    tzID: String!, 
    type: TimeZoneNames.NameType!, 
    date: Long
): String!
```

Returns the display name of the time zone at the given date.

**Note:** This method calls the subclass's [getTimeZoneDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getTimeZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType))first. When the result is null, this method calls [getMetaZoneID(java.lang.String,long)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneID(kotlin.String,%20kotlin.Long))to get the meta zone ID mapped from the time zone, then calls [getMetaZoneDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getMetaZoneDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The canonical time zone ID. |
| `type` | [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!:The display name type. See [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType). |
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The date |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name for the time zone at the given date. When this object does not have a localized display name for the time zone with the specified type and date, null is returned. |

### getExemplarLocationName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExemplarLocationName(tzID: String!): String!
```

Returns the exemplar location name for the given time zone. When this object does not have a localized location name, the default implementation may still returns a programmatically generated name with the logic described below.

1. Check if the ID contains "/". If not, return null.
2. Check if the ID does not start with "Etc/" or "SystemV/". If it does, return null.
3. Extract a substring after the last occurrence of "/".
4. Replace "_" with " ".

For example, "New York" is returned for the time zone ID "America/New_York" when this object does not have the localized location name.

<br />

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `tzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The canonical time zone ID |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The exemplar location name for the given time zone, or null when a localized location name is not available and the fallback logic described above cannot extract location from the ID. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): TimeZoneNames!
```

Returns an instance of`TimeZoneNames`for the specified locale.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------|
| [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#)! | An instance of`TimeZoneNames` |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): TimeZoneNames!
```

Returns an instance of`TimeZoneNames`for the specified [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------|
| [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#)! | An instance of`TimeZoneDisplayNames` |

### getMetaZoneDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMetaZoneDisplayName(
    mzID: String!, 
    type: TimeZoneNames.NameType!
): String!
```

Returns the display name of the meta zone.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The meta zone ID. |
| `type` | [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!:The display name type. See [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name of the meta zone. When this object does not have a localized display name for the given meta zone with the specified type or the implementation does not provide any display names associated with meta zones, null is returned. |

### getMetaZoneID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMetaZoneID(
    tzID: String!, 
    date: Long
): String!
```

Returns the meta zone ID for the given canonical time zone ID at the given date.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `tzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The canonical time zone ID. |
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The date. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The meta zone ID for the given time zone ID at the given date. If the time zone does not have a corresponding meta zone at the given date or the implementation does not support meta zones, null is returned. |

### getReferenceZoneID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getReferenceZoneID(
    mzID: String!, 
    region: String!
): String!
```

Returns the reference zone ID for the given meta zone ID for the region. Note: Each meta zone must have a reference zone associated with a special region "001" (world). Some meta zones may have region specific reference zone IDs other than the special region "001". When a meta zone does not have any region specific reference zone IDs, this method return the reference zone ID for the special region "001" (world).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `mzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The meta zone ID. |
| `region` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The region. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The reference zone ID ("golden zone" in the LDML specification) for the given time zone ID for the region. If the meta zone is unknown or the implementation does not support meta zones, null is returned. |

### getTZDBInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTZDBInstance(locale: ULocale!): TimeZoneNames!
```

Returns an instance of`TimeZoneNames`containing only short specific zone names ([NameType.SHORT_STANDARD](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType) and [NameType.SHORT_DAYLIGHT](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)), compatible with the IANA tz database's zone abbreviations (not localized). 
Note: The input locale is used for resolving ambiguous names (e.g. "IST" is parsed as Israel Standard Time for Israel, while it is parsed as India Standard Time for all other regions). The zone names returned by this instance are not localized. 

### getTimeZoneDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTimeZoneDisplayName(
    tzID: String!, 
    type: TimeZoneNames.NameType!
): String!
```

Returns the display name of the time zone. Unlike [getDisplayName(java.lang.String,android.icu.text.TimeZoneNames.NameType,long)](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames#getDisplayName(kotlin.String,%20android.icu.text.TimeZoneNames.NameType,%20kotlin.Long)), this method does not get a name from a meta zone used by the time zone.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tzID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The canonical time zone ID. |
| `type` | [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType)!:The display name type. See [TimeZoneNames.NameType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames.NameType). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name for the time zone. When this object does not have a localized display name for the given time zone with the specified type, null is returned. |
