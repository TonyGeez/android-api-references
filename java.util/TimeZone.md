# TimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeZone

```
abstract class TimeZone : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.TimeZone](../java/util/TimeZone.md) |

| Known Direct Subclasses [SimpleTimeZone](../java/util/SimpleTimeZone.md) |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [SimpleTimeZone](../java/util/SimpleTimeZone.md) | `SimpleTimeZone`is a concrete subclass of`TimeZone`that represents a time zone for use with a Gregorian calendar. | |
| --- | --- | --- | --- | --- | --- | --- |

represents a time zone offset, and also figures out daylight savings.

Typically, you get a`TimeZone`using`getDefault`which creates a`TimeZone`based on the time zone where the program is running. For example, for a program running in Japan,`getDefault`creates a`TimeZone`object based on Japanese Standard Time.

You can also get a`TimeZone`using`getTimeZone`along with a time zone ID. For instance, the time zone ID for the U.S. Pacific Time zone is "America/Los_Angeles". So, you can get a U.S. Pacific Time`TimeZone`object with:
{@snippet lang=java : \* TimeZone tz = TimeZone.getTimeZone("America/Los_Angeles"); \* } You can use the`getAvailableIDs`method to iterate through all the supported time zone IDs. You can then choose a supported ID to get a`TimeZone`. If the time zone you want is not represented by one of the supported IDs, then a custom time zone ID can be specified to produce a TimeZone. The syntax of a custom time zone ID is: 

```kotlin
<a id="CustomID"><i>CustomID:</i></a><code>GMT</code><i>Sign</i><i>Hours</i><code>:</code><i>Minutes</i><code>:</code><i>Seconds</i><code>GMT</code><i>Sign</i><i>Hours</i><code>:</code><i>Minutes</i><code>GMT</code><i>Sign</i><i>Hours</i><i>Minutes</i><code>GMT</code><i>Sign</i><i>Hours</i><i>Sign:</i>one of
          <code>+ -</code><i>Hours:</i><i>Digit</i><i>Digit</i><i>Digit</i><i>Minutes:</i><i>Digit</i><i>Digit</i><i>Seconds:</i><i>Digit</i><i>Digit</i><i>Digit:</i>one of
          <code>0 1 2 3 4 5 6 7 8 9</code>
```
*Hours* must be between 0 to 23 and*Minutes* /*Seconds* must be between 00 to 59. For example, "GMT+10" and "GMT+0010" mean ten hours and ten minutes ahead of GMT, respectively.

The format is locale independent and digits must be taken from the Basic Latin block of the Unicode standard. No daylight saving time transition schedule can be specified with a custom time zone ID. If the specified string doesn't match the syntax,`"GMT"`is used.

When creating a`TimeZone`, the specified custom time zone ID is normalized in the following syntax: 

```kotlin
<a id="NormalizedCustomID"><i>NormalizedCustomID:</i></a><code>GMT</code><i>Sign</i><i>TwoDigitHours</i><code>:</code><i>Minutes</i>[<i>ColonSeconds</i>]
  <i>Sign:</i>one of
          <code>+ -</code><i>TwoDigitHours:</i><i>Digit</i><i>Digit</i><i>Minutes:</i><i>Digit</i><i>Digit</i><i>ColonSeconds:</i><code>:</code><i>Digit</i><i>Digit</i><i>Digit:</i>one of
          <code>0 1 2 3 4 5 6 7 8 9</code>
```
For example, TimeZone.getTimeZone("GMT-8").getID() returns "GMT-08:00".*ColonSeconds* part only appears if the seconds value is non-zero.

## Three-letter time zone IDs

For compatibility with JDK 1.1.x, some other three-letter time zone IDs (such as "PST", "CTT", "AST") are also supported. However,**their use is deprecated** because the same abbreviation is often used for multiple time zones (for example, "CST" could be U.S. "Central Standard Time" and "China Standard Time"), and the Java platform can then only recognize one of them.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](../java/util/TimeZone.md) A style specifier for`getDisplayName()`indicating a long name, such as "Pacific Standard Time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](../java/util/TimeZone.md) A style specifier for`getDisplayName()`indicating a short name, such as "PST. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [TimeZone](../java/util/TimeZone.md))`()` Sole constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/TimeZone.md))`()` Creates a copy of this`TimeZone`. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableIDs](../java/util/TimeZone.md))`()` Gets all the available IDs supported. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableIDs](../java/util/TimeZone.md))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the available IDs according to the given time zone offset in milliseconds. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDSTSavings](../java/util/TimeZone.md))`()` Returns the amount of time to be added to local standard time to get local wall clock time. |
| openstatic [TimeZone](../java/util/TimeZone.md)! | [getDefault](../java/util/TimeZone.md))`()` Gets the default`TimeZone`for this host. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/util/TimeZone.md))`()` Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the default locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/util/TimeZone.md))`(`daylight:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a name in the specified`style`of this`TimeZone`suitable for presentation to the user in the default locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/util/TimeZone.md))`(`daylightTime:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Returns the [short](../java/util/TimeZone.md) or [long](../java/util/TimeZone.md) name of this time zone with either standard or daylight time, as written in`locale`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../java/util/TimeZone.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the specified`locale`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getID](../java/util/TimeZone.md))`()` Gets the ID of this time zone. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](../java/util/TimeZone.md))`(`era:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `milliseconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the time zone offset, for current date, modified in case of daylight savings. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](../java/util/TimeZone.md))`(`date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the offset of this time zone from UTC at the specified date. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRawOffset](../java/util/TimeZone.md))`()` Returns the amount of time in milliseconds to add to UTC to get standard time in this time zone. |
| openstatic [TimeZone](../java/util/TimeZone.md)! | [getTimeZone](../java/util/TimeZone.md))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the`TimeZone`for the given ID. |
| openstatic [TimeZone](../java/util/TimeZone.md)! | [getTimeZone](../java/util/TimeZone.md))`(`zoneId:` ` [ZoneId](../java/time/ZoneId.md)!`)` Gets the`TimeZone`for the given`zoneId`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSameRules](../java/util/TimeZone.md))`(`other:` ` [TimeZone](../java/util/TimeZone.md)!`)` Returns true if this zone has the same rule and offset as another zone. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inDaylightTime](../java/util/TimeZone.md))`(`date:` ` [Date](../java/util/Date.md)!`)` Queries if the given`date`is in Daylight Saving Time in this time zone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [observesDaylightTime](../java/util/TimeZone.md))`()` Returns`true`if this`TimeZone`is currently in Daylight Saving Time, or if a transition from Standard Time to Daylight Saving Time occurs at any future time. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](../java/util/TimeZone.md))`(`timeZone:` ` [TimeZone](../java/util/TimeZone.md)!`)` Sets the`TimeZone`that is returned by the`getDefault`method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setID](../java/util/TimeZone.md))`(`ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the time zone ID. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRawOffset](../java/util/TimeZone.md))`(`offsetMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the base time zone offset to GMT. |
| --- | --- |
| open [ZoneId](../java/time/ZoneId.md)! | [toZoneId](../java/util/TimeZone.md))`()` Converts this`TimeZone`object to a`ZoneId`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [useDaylightTime](../java/util/TimeZone.md))`()` Queries if this`TimeZone`uses Daylight Saving Time. |

## Constants

### LONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LONG: Int
```

A style specifier for`getDisplayName()`indicating a long name, such as "Pacific Standard Time." 

 Value: 1

**See Also**

- [#SHORT](../java/util/TimeZone.md) 

### SHORT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHORT: Int
```

A style specifier for`getDisplayName()`indicating a short name, such as "PST." 

 Value: 0

**See Also**

- [#LONG](../java/util/TimeZone.md)

## Public constructors

### TimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TimeZone()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates a copy of this`TimeZone`.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this`TimeZone` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getAvailableIDs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableIDs(): Array<String!>!
```

Gets all the available IDs supported.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of IDs. |

### getAvailableIDs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableIDs(rawOffset: Int): Array<String!>!
```

Gets the available IDs according to the given time zone offset in milliseconds.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given time zone GMT offset in milliseconds. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of IDs, where the time zone for that ID has the specified GMT offset. For example, "America/Phoenix" and "America/Denver" both have GMT-07:00, but differ in daylight saving behavior. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/TimeZone#getRawOffset()> 

### getDSTSavings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDSTSavings(): Int
```

Returns the amount of time to be added to local standard time to get local wall clock time.

The default implementation returns 3600000 milliseconds (i.e., one hour) if a call to [useDaylightTime()](../java/util/TimeZone.md))returns`true`. Otherwise, 0 (zero) is returned.

If an underlying`TimeZone`implementation subclass supports historical and future Daylight Saving Time schedule changes, this method returns the amount of saving time of the last known Daylight Saving Time rule that can be a future prediction.

If the amount of saving time at any given time stamp is required, construct a [Calendar](../java/util/Calendar.md) with this`TimeZone`and the time stamp, and call [Calendar.get](../java/util/Calendar.md))`(` [Calendar.DST_OFFSET](../java/util/Calendar.md)`)`.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of saving time in milliseconds |

**See Also**

- [#inDaylightTime(Date)](../java/util/TimeZone.md))
- [#getOffset(long)](../java/util/TimeZone.md))
- [#getOffset(int,int,int,int,int,int)](../java/util/TimeZone.md))
- [java.util.Calendar#ZONE_OFFSET](../java/util/Calendar.md) 

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): TimeZone!
```

Gets the default`TimeZone`for this host. The source of the default`TimeZone`may vary with implementation.

| Return ||
|---------------------------------------------------------------------------------|----------------------|
| [TimeZone](../java/util/TimeZone.md)! | a default`TimeZone`. |

**See Also**

- [#setDefault(TimeZone)](../java/util/TimeZone.md)) 

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): String!
```

Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the default locale.

This method is equivalent to:
{@snippet lang=java : \* // @link substring="LONG" target="#LONG" : \* getDisplayName(false, LONG, \* // @link substring="Locale.Category.DISPLAY" target="Locale.Category#DISPLAY" : \* Locale.getDefault(Locale.Category.DISPLAY)); \* }

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the human-readable name of this time zone in the default locale. |

**See Also**

- [#getDisplayName(boolean, int, Locale)](../java/util/TimeZone.md))
- [java.util.Locale#getDefault(Locale.Category)](../java/util/Locale.md))
- [java.util.Locale.Category](../java/util/Locale.Category.md) 

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(
    daylight: Boolean, 
    style: Int
): String!
```

Returns a name in the specified`style`of this`TimeZone`suitable for presentation to the user in the default locale. If the specified`daylight`is`true`, a Daylight Saving Time name is returned (even if this`TimeZone`doesn't observe Daylight Saving Time). Otherwise, a Standard Time name is returned.

This method is equivalent to:
{@snippet lang=java : \* getDisplayName(daylight, style, \* // @link substring="Locale.Category.DISPLAY" target="Locale.Category#DISPLAY" : \* Locale.getDefault(Locale.Category.DISPLAY)); \* }

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `daylight` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`specifying a Daylight Saving Time name, or`false`specifying a Standard Time name |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [LONG](../java/util/TimeZone.md) or [SHORT](../java/util/TimeZone.md) |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the human-readable name of this time zone in the default locale. |

| Exceptions ||
|--------------------------------------|----------------------|
| `java.lang.IllegalArgumentException` | if`style`is invalid. |

**See Also**

- [#getDisplayName(boolean, int, Locale)](../java/util/TimeZone.md))
- [java.util.Locale#getDefault(Locale.Category)](../java/util/Locale.md))
- [java.util.Locale.Category](../java/util/Locale.Category.md)
- [java.text.DateFormatSymbols#getZoneStrings()](../java/text/DateFormatSymbols.md)) 

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(
    daylightTime: Boolean, 
    style: Int, 
    locale: Locale!
): String!
```

Returns the [short](../java/util/TimeZone.md) or [long](../java/util/TimeZone.md) name of this time zone with either standard or daylight time, as written in`locale`. If the name is not available, the result is in the format`GMT[+-]hh:mm`.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `daylightTime` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`specifying a Daylight Saving Time name, or`false`specifying a Standard Time name |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [LONG](../java/util/TimeZone.md) or [SHORT](../java/util/TimeZone.md) |
| `locale` | [Locale](../java/util/Locale.md)!:the locale in which to supply the display name. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the human-readable name of this time zone in the given locale. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | This method may throw an`IllegalArgumentException`if`style`is invalid. |
| `java.lang.NullPointerException` | This method may throw a`NullPointerException`if`ID`is`null` |

**See Also**

- [java.text.DateFormatSymbols#getZoneStrings()](../java/text/DateFormatSymbols.md)) 

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(locale: Locale!): String!
```

Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the specified`locale`.

This method is equivalent to:
{@snippet lang=java : \* // @link substring="LONG" target="#LONG" : \* getDisplayName(false, LONG, locale); \* }

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale in which to supply the display name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the human-readable name of this time zone in the given locale. |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`locale`is`null`. |

**See Also**

- [#getDisplayName(boolean, int, Locale)](../java/util/TimeZone.md)) 

### getID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getID(): String!
```

Gets the ID of this time zone.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ID of this time zone. |

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOffset(
    era: Int, 
    year: Int, 
    month: Int, 
    day: Int, 
    dayOfWeek: Int, 
    milliseconds: Int
): Int
```

Gets the time zone offset, for current date, modified in case of daylight savings. This is the offset to add to UTC to get local time.

This method returns a historically correct offset if an underlying`TimeZone`implementation subclass supports historical Daylight Saving Time schedule and GMT offset changes.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `era` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the era of the given date. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year in the given date. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the month in the given date. Month is 0-based. e.g., 0 for January. |
| --- | --- |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day-in-month of the given date. |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day-of-week of the given date. |
| `milliseconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the milliseconds in day in*standard*local time. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset in milliseconds to add to GMT to get local time. |

**See Also**

- [java.util.Calendar#ZONE_OFFSET](../java/util/Calendar.md)
- [java.util.Calendar#DST_OFFSET](../java/util/Calendar.md) 

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffset(date: Long): Int
```

Returns the offset of this time zone from UTC at the specified date. If Daylight Saving Time is in effect at the specified date, the offset value is adjusted with the amount of daylight saving.

This method returns a historically correct offset value if an underlying TimeZone implementation subclass supports historical Daylight Saving Time schedule and GMT offset changes.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the date represented in milliseconds since January 1, 1970 00:00:00 GMT |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of time in milliseconds to add to UTC to get local time. |

**See Also**

- [java.util.Calendar#ZONE_OFFSET](../java/util/Calendar.md)
- [java.util.Calendar#DST_OFFSET](../java/util/Calendar.md) 

### getRawOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRawOffset(): Int
```

Returns the amount of time in milliseconds to add to UTC to get standard time in this time zone. Because this value is not affected by daylight saving time, it is called*raw offset*.

If an underlying`TimeZone`implementation subclass supports historical GMT offset changes, the method returns the raw offset value of the current date. In Honolulu, for example, its raw offset changed from GMT-10:30 to GMT-10:00 in 1947, and this method always returns -36000000 milliseconds (i.e., -10 hours).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of raw offset time in milliseconds to add to UTC. |

**See Also**

- [java.util.Calendar#ZONE_OFFSET](../java/util/Calendar.md) 

### getTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTimeZone(id: String!): TimeZone!
```

Gets the`TimeZone`for the given ID.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ID for a`TimeZone`, either an abbreviation such as "PST", a full name such as "America/Los_Angeles", or a custom ID such as "GMT-8:00". Note that the support of abbreviations is for JDK 1.1.x compatibility only and full names should be used. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [TimeZone](../java/util/TimeZone.md)! | the specified`TimeZone`, or the GMT zone if the given ID cannot be understood. |

| Exceptions ||
|----------------------------------|----------------|
| `java.lang.NullPointerException` | if`ID`is`null` |

### getTimeZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTimeZone(zoneId: ZoneId!): TimeZone!
```

Gets the`TimeZone`for the given`zoneId`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `zoneId` | [ZoneId](../java/time/ZoneId.md)!:a [ZoneId](../java/time/ZoneId.md) from which the time zone ID is obtained |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [TimeZone](../java/util/TimeZone.md)! | the specified`TimeZone`, or the GMT zone if the given ID cannot be understood. |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`zoneId`is`null` |

### hasSameRules

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSameRules(other: TimeZone!): Boolean
```

Returns true if this zone has the same rule and offset as another zone. That is, if this zone differs only in ID, if at all. Returns false if the other zone is null.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `other` | [TimeZone](../java/util/TimeZone.md)!:the`TimeZone`object to be compared with |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the other zone is not null and is the same as this one, with the possible exception of the ID |

### inDaylightTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun inDaylightTime(date: Date!): Boolean
```

Queries if the given`date`is in Daylight Saving Time in this time zone.

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `date` | [Date](../java/util/Date.md)!:the given Date. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given date is in Daylight Saving Time,`false`, otherwise. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------|
| `java.lang.NullPointerException` | This method may throw a`NullPointerException`if`date`is`null` |

### observesDaylightTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun observesDaylightTime(): Boolean
```

Returns`true`if this`TimeZone`is currently in Daylight Saving Time, or if a transition from Standard Time to Daylight Saving Time occurs at any future time.

The default implementation returns`true`if`useDaylightTime()`or`inDaylightTime(new Date())`returns`true`.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`TimeZone`is currently in Daylight Saving Time, or if a transition from Standard Time to Daylight Saving Time occurs at any future time;`false`otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/TimeZone#useDaylightTime()>
- [#inDaylightTime(Date)](../java/util/TimeZone.md))
- [java.util.Calendar#DST_OFFSET](../java/util/Calendar.md) 

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(timeZone: TimeZone!): Unit
```

Sets the`TimeZone`that is returned by the`getDefault`method.`zone`is cached. If`zone`is null, the cached default`TimeZone`is cleared. This method doesn't change the value of the`user.timezone`property.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `timeZone` | [TimeZone](../java/util/TimeZone.md)!:the new default`TimeZone`, or null |

**See Also**

- [#getDefault](../java/util/TimeZone.md)) 

### setID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setID(ID: String!): Unit
```

Sets the time zone ID. This does not change any other data in the time zone object.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new time zone ID. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | This method may throw a`NullPointerException`if`ID`is`null` |

### setRawOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRawOffset(offsetMillis: Int): Unit
```

Sets the base time zone offset to GMT. This is the offset to add to UTC to get local time.

If an underlying`TimeZone`implementation subclass supports historical GMT offset changes, the specified GMT offset is set as the latest GMT offset and the difference from the known latest GMT offset value is used to adjust all historical GMT offset values.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------|
| `offsetMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given base time zone offset to GMT. |

### toZoneId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toZoneId(): ZoneId!
```

Converts this`TimeZone`object to a`ZoneId`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [ZoneId](../java/time/ZoneId.md)! | a`ZoneId`representing the same time zone as this`TimeZone` |

### useDaylightTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun useDaylightTime(): Boolean
```

Queries if this`TimeZone`uses Daylight Saving Time.

If an underlying`TimeZone`implementation subclass supports historical and future Daylight Saving Time schedule changes, this method refers to the last known Daylight Saving Time rule that can be a future prediction and may not be the same as the current rule. Consider calling [observesDaylightTime()](../java/util/TimeZone.md))if the current rule should also be taken into account.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`TimeZone`uses Daylight Saving Time,`false`, otherwise. |

**See Also**

- [#inDaylightTime(Date)](../java/util/TimeZone.md))
- [java.util.Calendar#DST_OFFSET](../java/util/Calendar.md)
