# DateUtils

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateUtils

Kotlin| [Java](https://developer.android.com/reference/android/text/format/DateUtils "View this page in Java") 

```
open class DateUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.format.DateUtils](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#) |

This class contains various date-related utilities for creating text for things like elapsed time and date ranges, strings for days of the week and months, and AM/PM text etc.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBREV_MONTH_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#ABBREV_MONTH_FORMAT:kotlin.String) This is not actually a useful month name in all locales. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ABBREV_WEEKDAY_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#ABBREV_WEEKDAY_FORMAT:kotlin.String) <br /> |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DAY_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#DAY_IN_MILLIS:kotlin.Long) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_12HOUR](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_12HOUR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_24HOUR](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_24HOUR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_ABBREV_ALL](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_ALL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_ABBREV_MONTH](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_MONTH:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_ABBREV_RELATIVE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_RELATIVE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_ABBREV_TIME](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_TIME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_ABBREV_WEEKDAY](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_WEEKDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_CAP_AMPM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_CAP_AMPM:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_CAP_MIDNIGHT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_CAP_MIDNIGHT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_CAP_NOON](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_CAP_NOON:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_CAP_NOON_MIDNIGHT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_CAP_NOON_MIDNIGHT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NO_MIDNIGHT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NO_MIDNIGHT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NO_MONTH_DAY](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NO_MONTH_DAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NO_NOON](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NO_NOON:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NO_NOON_MIDNIGHT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NO_NOON_MIDNIGHT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NO_YEAR](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NO_YEAR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NUMERIC_DATE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NUMERIC_DATE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SHOW_DATE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_SHOW_DATE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SHOW_TIME](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_SHOW_TIME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SHOW_WEEKDAY](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_SHOW_WEEKDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_SHOW_YEAR](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_SHOW_YEAR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_UTC](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_UTC:kotlin.Int) <br /> |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [HOUR_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#HOUR_IN_MILLIS:kotlin.Long) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HOUR_MINUTE_24](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#HOUR_MINUTE_24:kotlin.String) This is not actually the preferred 24-hour date format in all locales. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_LONG:kotlin.Int) Request the full spelled-out name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int) Request an abbreviated version of the name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORT:kotlin.Int) Request a shorter abbreviated version of the name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_SHORTER](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORTER:kotlin.Int) Request an even shorter abbreviated version of the name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LENGTH_SHORTEST](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORTEST:kotlin.Int) Request an even shorter abbreviated version of the name. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [MINUTE_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#MINUTE_IN_MILLIS:kotlin.Long) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MONTH_DAY_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#MONTH_DAY_FORMAT:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MONTH_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#MONTH_FORMAT:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMERIC_MONTH_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#NUMERIC_MONTH_FORMAT:kotlin.String) <br /> |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [SECOND_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#SECOND_IN_MILLIS:kotlin.Long) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [WEEKDAY_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#WEEKDAY_FORMAT:kotlin.String) <br /> |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [WEEK_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#WEEK_IN_MILLIS:kotlin.Long) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_FORMAT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#YEAR_FORMAT:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [YEAR_FORMAT_TWO_DIGITS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#YEAR_FORMAT_TWO_DIGITS:kotlin.String) <br /> |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [YEAR_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#YEAR_IN_MILLIS:kotlin.Long) <br /> |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [DateUtils](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#DateUtils())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)! | [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `formatter:` ` [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)!`, `startMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a date or a time range according to the local conventions. |
| openstatic [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)! | [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `formatter:` ` [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)!`, `startMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeZone:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Formats a date or a time range according to the local conventions. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `startMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a date or a time range according to the local conventions. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatDateTime](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateTime(android.content.Context,%20kotlin.Long,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a date or a time according to the local conventions. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatElapsedTime](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatElapsedTime(java.lang.StringBuilder,%20kotlin.Long))`(`recycle:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `elapsedSeconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Formats an elapsed time in a format like "MM:SS" or "H:MM:SS" (using a form suited to the current locale), similar to that used on the call-in-progress screen. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatElapsedTime](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatElapsedTime(kotlin.Long))`(`elapsedSeconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Formats an elapsed time in the form "MM:SS" or "H:MM:SS" for display on the call-in-progress screen. |
| static [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [formatSameDayTime](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatSameDayTime(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int))`(`then:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `now:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Format a date / time such that if the then is on the same day as now, it shows just the time and if it's a different day, it shows just the date. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAMPMString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getAMPMString(kotlin.Int))`(`ampm:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized string for AM or PM. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDayOfWeekString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getDayOfWeekString(kotlin.Int,%20kotlin.Int))`(`dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `abbrev:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a string for the day of the week. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMonthString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getMonthString(kotlin.Int,%20kotlin.Int))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `abbrev:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized string for the month of the year. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeDateTimeString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeDateTimeString(android.content.Context,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int))`(`c:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minResolution:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transitionResolution:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return string describing the elapsed time since startTime formatted like "\[relative time/date\], \[time\]". |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeTimeSpanString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(android.content.Context,%20kotlin.Long))`(`c:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Convenience function to return relative time string without preposition. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeTimeSpanString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(android.content.Context,%20kotlin.Long,%20kotlin.Boolean))`(`c:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `withPreposition:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeTimeSpanString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(kotlin.Long))`(`startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string describing the elapsed time since startTime. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeTimeSpanString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `now:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minResolution:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns a string describing 'time' as a time relative to 'now'. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getRelativeTimeSpanString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `now:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minResolution:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string describing 'time' as a time relative to 'now'. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isToday](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#isToday(kotlin.Long))`(`when:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [sameMonthTable](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#sameMonthTable:kotlin.IntArray) <br /> |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [sameYearTable](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#sameYearTable:kotlin.IntArray) <br /> |

## Constants

### ABBREV_MONTH_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ABBREV_MONTH_FORMAT: String
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

This is not actually a useful month name in all locales. 

 Value: "%b"

### ABBREV_WEEKDAY_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ABBREV_WEEKDAY_FORMAT: String
```  

 Value: "%a"

### DAY_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY_IN_MILLIS: Long
```  

 Value: 86400000L

### FORMAT_12HOUR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_12HOUR: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 64

### FORMAT_24HOUR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_24HOUR: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 128

### FORMAT_ABBREV_ALL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ABBREV_ALL: Int
```  

 Value: 524288

### FORMAT_ABBREV_MONTH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ABBREV_MONTH: Int
```  

 Value: 65536

### FORMAT_ABBREV_RELATIVE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ABBREV_RELATIVE: Int
```  

 Value: 262144

### FORMAT_ABBREV_TIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ABBREV_TIME: Int
```  

 Value: 16384

### FORMAT_ABBREV_WEEKDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_ABBREV_WEEKDAY: Int
```  

 Value: 32768

### FORMAT_CAP_AMPM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_CAP_AMPM: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 256

### FORMAT_CAP_MIDNIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_CAP_MIDNIGHT: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 4096

### FORMAT_CAP_NOON

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_CAP_NOON: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 1024

### FORMAT_CAP_NOON_MIDNIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_CAP_NOON_MIDNIGHT: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 5120

### FORMAT_NO_MIDNIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NO_MIDNIGHT: Int
```  

 Value: 2048

### FORMAT_NO_MONTH_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NO_MONTH_DAY: Int
```  

 Value: 32

### FORMAT_NO_NOON

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NO_NOON: Int
```  

 Value: 512

### FORMAT_NO_NOON_MIDNIGHT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NO_NOON_MIDNIGHT: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 2560

### FORMAT_NO_YEAR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NO_YEAR: Int
```  

 Value: 8

### FORMAT_NUMERIC_DATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NUMERIC_DATE: Int
```  

 Value: 131072

### FORMAT_SHOW_DATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SHOW_DATE: Int
```  

 Value: 16

### FORMAT_SHOW_TIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SHOW_TIME: Int
```  

 Value: 1

### FORMAT_SHOW_WEEKDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SHOW_WEEKDAY: Int
```  

 Value: 2

### FORMAT_SHOW_YEAR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_SHOW_YEAR: Int
```  

 Value: 4

### FORMAT_UTC

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_UTC: Int
```

**Deprecated:** *Use [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String))and pass in [Time.TIMEZONE_UTC](https://developer.android.com/reference/kotlin/android/text/format/Time#TIMEZONE_UTC:kotlin.String) for the timeZone instead.* 

 Value: 8192

### HOUR_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR_IN_MILLIS: Long
```  

 Value: 3600000L

### HOUR_MINUTE_24

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HOUR_MINUTE_24: String
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

This is not actually the preferred 24-hour date format in all locales. 

 Value: "%H:%M"

### LENGTH_LONG

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_LONG: Int
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Request the full spelled-out name. For use with the 'abbrev' parameter of [getDayOfWeekString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getDayOfWeekString(kotlin.Int,%20kotlin.Int))and [getMonthString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getMonthString(kotlin.Int,%20kotlin.Int)). 

 Value: 10

### LENGTH_MEDIUM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_MEDIUM: Int
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Request an abbreviated version of the name. For use with the 'abbrev' parameter of [getDayOfWeekString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getDayOfWeekString(kotlin.Int,%20kotlin.Int))and [getMonthString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getMonthString(kotlin.Int,%20kotlin.Int)). 

 Value: 20

### LENGTH_SHORT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_SHORT: Int
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Request a shorter abbreviated version of the name. For use with the 'abbrev' parameter of [getDayOfWeekString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getDayOfWeekString(kotlin.Int,%20kotlin.Int))and [getMonthString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getMonthString(kotlin.Int,%20kotlin.Int)). 

 Value: 30

### LENGTH_SHORTER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_SHORTER: Int
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Request an even shorter abbreviated version of the name. Do not use this. Currently this will always return the same result as [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORT:kotlin.Int). 

 Value: 40

### LENGTH_SHORTEST

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LENGTH_SHORTEST: Int
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Request an even shorter abbreviated version of the name. For use with the 'abbrev' parameter of [getDayOfWeekString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getDayOfWeekString(kotlin.Int,%20kotlin.Int))and [getMonthString](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getMonthString(kotlin.Int,%20kotlin.Int)). 

 Value: 50

### MINUTE_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTE_IN_MILLIS: Long
```  

 Value: 60000L

### MONTH_DAY_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONTH_DAY_FORMAT: String
```  

 Value: "%-d"

### MONTH_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONTH_FORMAT: String
```  

 Value: "%B"

### NUMERIC_MONTH_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC_MONTH_FORMAT: String
```  

 Value: "%m"

### SECOND_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECOND_IN_MILLIS: Long
```  

 Value: 1000L

### WEEKDAY_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEEKDAY_FORMAT: String
```  

 Value: "%A"

### WEEK_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEEK_IN_MILLIS: Long
```  

 Value: 604800000L

### YEAR_FORMAT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YEAR_FORMAT: String
```  

 Value: "%Y"

### YEAR_FORMAT_TWO_DIGITS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YEAR_FORMAT_TWO_DIGITS: String
```  

 Value: "%g"

### YEAR_IN_MILLIS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YEAR_IN_MILLIS: Long
```

**Deprecated:** *Not all years have the same number of days, and this constant is actually the length of 364 days. Please use other date/time constructs such as [java.util.concurrent.TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#), [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) or [java.time.Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) instead.* 

 Value: 31449600000L

## Public constructors

### DateUtils

```
DateUtils()
```

## Public methods

### formatDateRange

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatDateRange(
    context: Context!, 
    formatter: Formatter!, 
    startMillis: Long, 
    endMillis: Long, 
    flags: Int
): Formatter!
```

Formats a date or a time range according to the local conventions.

Note that this is a convenience method for formatting the date or time range in the local time zone. If you want to specify the time zone please use [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context is required only if the time is shown |
| `formatter` | [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)!:the Formatter used for formatting the date range. Note: be sure to call setLength(0) on StringBuilder passed to the Formatter constructor unless you want the results to accumulate. |
| `startMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time in UTC milliseconds |
| `endMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the end time in UTC milliseconds |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit mask of options See [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String)) |

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)! | a string containing the formatted date/time range. |

### formatDateRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatDateRange(
    context: Context!, 
    formatter: Formatter!, 
    startMillis: Long, 
    endMillis: Long, 
    flags: Int, 
    timeZone: String!
): Formatter!
```

Formats a date or a time range according to the local conventions.

Example output strings (date formats in these examples are shown using the US date format convention but that may change depending on the local settings):

- 10:15am
- 3:00pm - 4:00pm
- 3pm - 4pm
- 3PM - 4PM
- 08:00 - 17:00
- Oct 9
- Tue, Oct 9
- October 9, 2007
- Oct 9 - 10
- Oct 9 - 10, 2007
- Oct 28 - Nov 3, 2007
- Dec 31, 2007 - Jan 1, 2008
- Oct 9, 8:00am - Oct 10, 5:00pm
- 12/31/2007 - 01/01/2008

The flags argument is a bitmask of options from the following list:

- FORMAT_SHOW_TIME
- FORMAT_SHOW_WEEKDAY
- FORMAT_SHOW_YEAR
- FORMAT_SHOW_DATE
- FORMAT_NO_MONTH_DAY
- FORMAT_12HOUR
- FORMAT_24HOUR
- FORMAT_CAP_AMPM
- FORMAT_NO_NOON
- FORMAT_CAP_NOON
- FORMAT_NO_MIDNIGHT
- FORMAT_CAP_MIDNIGHT
- FORMAT_UTC
- FORMAT_ABBREV_TIME
- FORMAT_ABBREV_WEEKDAY
- FORMAT_ABBREV_MONTH
- FORMAT_ABBREV_ALL
- FORMAT_NUMERIC_DATE

If FORMAT_SHOW_TIME is set, the time is shown as part of the date range. If the start and end time are the same, then just the start time is shown.

If FORMAT_SHOW_WEEKDAY is set, then the weekday is shown.

If FORMAT_SHOW_YEAR is set, then the year is always shown. If FORMAT_SHOW_YEAR is not set, then the year is shown only if it is different from the current year, or if the start and end dates fall on different years.

Normally the date is shown unless the start and end day are the same. If FORMAT_SHOW_DATE is set, then the date is always shown, even for same day ranges.

If FORMAT_NO_MONTH_DAY is set, then if the date is shown, just the month name will be shown, not the day of the month. For example, "January, 2008" instead of "January 6 - 12, 2008".

If FORMAT_CAP_AMPM is set and 12-hour time is used, then the "AM" and "PM" are capitalized. You should not use this flag because in some locales these terms cannot be capitalized, and in many others it doesn't make sense to do so even though it is possible.

If FORMAT_NO_NOON is set and 12-hour time is used, then "12pm" is shown instead of "noon".

If FORMAT_CAP_NOON is set and 12-hour time is used, then "Noon" is shown instead of "noon". You should probably not use this flag because in many locales it will not make sense to capitalize the term.

If FORMAT_NO_MIDNIGHT is set and 12-hour time is used, then "12am" is shown instead of "midnight".

If FORMAT_CAP_MIDNIGHT is set and 12-hour time is used, then "Midnight" is shown instead of "midnight". You should probably not use this flag because in many locales it will not make sense to capitalize the term.

If FORMAT_12HOUR is set and the time is shown, then the time is shown in the 12-hour time format. You should not normally set this. Instead, let the time format be chosen automatically according to the system settings. If both FORMAT_12HOUR and FORMAT_24HOUR are set, then FORMAT_24HOUR takes precedence.

If FORMAT_24HOUR is set and the time is shown, then the time is shown in the 24-hour time format. You should not normally set this. Instead, let the time format be chosen automatically according to the system settings. If both FORMAT_12HOUR and FORMAT_24HOUR are set, then FORMAT_24HOUR takes precedence.

If FORMAT_UTC is set, then the UTC time zone is used for the start and end milliseconds unless a time zone is specified. If a time zone is specified it will be used regardless of the FORMAT_UTC flag.

If FORMAT_ABBREV_TIME is set and 12-hour time format is used, then the start and end times (if shown) are abbreviated by not showing the minutes if they are zero. For example, instead of "3:00pm" the time would be abbreviated to "3pm".

If FORMAT_ABBREV_WEEKDAY is set, then the weekday (if shown) is abbreviated to a 3-letter string.

If FORMAT_ABBREV_MONTH is set, then the month (if shown) is abbreviated to a 3-letter string.

If FORMAT_ABBREV_ALL is set, then the weekday and the month (if shown) are abbreviated to 3-letter strings.

If FORMAT_NUMERIC_DATE is set, then the date is shown in numeric format instead of using the name of the month. For example, "12/31/2008" instead of "December 31, 2008".

If the end date ends at 12:00am at the beginning of a day, it is formatted as the end of the previous day in two scenarios:

- For single day events. This results in "8pm - midnight" instead of "Nov 10, 8pm - Nov 11, 12am".
- When the time is not displayed. This results in "Nov 10 - 11" for an event with a start date of Nov 10 and an end date of Nov 12 at 00:00.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context is required only if the time is shown |
| `formatter` | [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)!:the Formatter used for formatting the date range. Note: be sure to call setLength(0) on StringBuilder passed to the Formatter constructor unless you want the results to accumulate. |
| `startMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time in UTC milliseconds |
| `endMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the end time in UTC milliseconds |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit mask of options |
| `timeZone` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the time zone to compute the string in. Use null for local or if the FORMAT_UTC flag is being used. |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#)! | the formatter with the formatted date/time range appended to the string buffer. |

### formatDateRange

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatDateRange(
    context: Context!, 
    startMillis: Long, 
    endMillis: Long, 
    flags: Int
): String!
```

Formats a date or a time range according to the local conventions.

Note that this is a convenience method. Using it involves creating an internal [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#) instance on-the-fly, which is somewhat costly in terms of memory and time. This is probably acceptable if you use the method only rarely, but if you rely on it for formatting a large number of dates, consider creating and reusing your own [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#) instance and use the version of [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int))that takes a [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context is required only if the time is shown |
| `startMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time in UTC milliseconds |
| `endMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the end time in UTC milliseconds |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit mask of options See [formatDateRange](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#formatDateRange(android.content.Context,%20java.util.Formatter,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String)) |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string containing the formatted date/time range. |

### formatDateTime

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatDateTime(
    context: Context!, 
    millis: Long, 
    flags: Int
): String!
```

Formats a date or a time according to the local conventions. There are lots of options that allow the caller to control, for example, if the time is shown, if the day of the week is shown, if the month name is abbreviated, if noon is shown instead of 12pm, and so on. For the complete list of options, see the documentation for #formatDateRange.

Example output strings (date formats in these examples are shown using the US date format convention but that may change depending on the local settings):

- 10:15am
- 3:00pm
- 3pm
- 3PM
- 08:00
- 17:00
- noon
- Noon
- midnight
- Midnight
- Oct 31
- Oct 31, 2007
- October 31, 2007
- 10am, Oct 31
- 17:00, Oct 31
- Wed
- Wednesday
- 10am, Wed, Oct 31
- Wed, Oct 31
- Wednesday, Oct 31
- Wed, Oct 31, 2007
- Wed, October 31
- 10/31/2007

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context is required only if the time is shown |
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a point in time in UTC milliseconds |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit mask of formatting options |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string containing the formatted date/time. |

### formatElapsedTime

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatElapsedTime(
    recycle: StringBuilder!, 
    elapsedSeconds: Long
): String!
```

Formats an elapsed time in a format like "MM:SS" or "H:MM:SS" (using a form suited to the current locale), similar to that used on the call-in-progress screen.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recycle` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!: [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#) to recycle, or null to use a temporary one. |
| `elapsedSeconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the elapsed time in seconds. |

### formatElapsedTime

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatElapsedTime(elapsedSeconds: Long): String!
```

Formats an elapsed time in the form "MM:SS" or "H:MM:SS" for display on the call-in-progress screen.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------|
| `elapsedSeconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the elapsed time in seconds. |

### formatSameDayTime

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun formatSameDayTime(
    then: Long, 
    now: Long, 
    dateStyle: Int, 
    timeStyle: Int
): CharSequence!
```

Format a date / time such that if the then is on the same day as now, it shows just the time and if it's a different day, it shows just the date.

The parameters dateFormat and timeFormat should each be one of [java.text.DateFormat#DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#DEFAULT:kotlin.Int), [java.text.DateFormat#FULL](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#FULL:kotlin.Int), [java.text.DateFormat#LONG](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#LONG:kotlin.Int), [java.text.DateFormat#MEDIUM](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#MEDIUM:kotlin.Int) or [java.text.DateFormat#SHORT](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#SHORT:kotlin.Int)

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `then` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the date to format |
| `now` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the base time |
| `dateStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):how to format the date portion. |
| `timeStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):how to format the time portion. |

### getAMPMString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAMPMString(ampm: Int): String!
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Return a localized string for AM or PM.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ampm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Either [Calendar.AM](https://developer.android.com/reference/kotlin/java/util/Calendar.html#AM:kotlin.Int) or [Calendar.PM](https://developer.android.com/reference/kotlin/java/util/Calendar.html#PM:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Localized version of "AM" or "PM". |

| Exceptions ||
|---------------------------------------|-------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the ampm is out of bounds. |

### getDayOfWeekString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDayOfWeekString(
    dayOfWeek: Int, 
    abbrev: Int
): String!
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Return a string for the day of the week.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [Calendar.SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar.html#SUNDAY:kotlin.Int), [Calendar.MONDAY](https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONDAY:kotlin.Int), etc. |
| `abbrev` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_LONG:kotlin.Int), [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORT:kotlin.Int), [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int), or [LENGTH_SHORTEST](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORTEST:kotlin.Int). Note that in most languages, [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORT:kotlin.Int) will return the same as [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int). Undefined lengths will return [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int) but may return something different in the future. |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the dayOfWeek is out of bounds. |

### getMonthString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMonthString(
    month: Int, 
    abbrev: Int
): String!
```

**Deprecated:** *Use [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#) instead.*

Return a localized string for the month of the year.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [Calendar.JANUARY](https://developer.android.com/reference/kotlin/java/util/Calendar.html#JANUARY:kotlin.Int), [Calendar.FEBRUARY](https://developer.android.com/reference/kotlin/java/util/Calendar.html#FEBRUARY:kotlin.Int), etc. |
| `abbrev` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [LENGTH_LONG](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_LONG:kotlin.Int), [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int), or [LENGTH_SHORTEST](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_SHORTEST:kotlin.Int). Undefined lengths will return [LENGTH_MEDIUM](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#LENGTH_MEDIUM:kotlin.Int) but may return something different in the future. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Localized month of the year. |

### getRelativeDateTimeString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeDateTimeString(
    c: Context!, 
    time: Long, 
    minResolution: Long, 
    transitionResolution: Long, 
    flags: Int
): CharSequence!
```

Return string describing the elapsed time since startTime formatted like "\[relative time/date\], \[time\]".

Example output strings for the US date format.

- 3 min. ago, 10:15 AM
- Yesterday, 12:20 PM
- Dec 12, 4:12 AM
- 11/14/2007, 8:20 AM

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):some time in the past. |
| `minResolution` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum elapsed time (in milliseconds) to report when showing relative times. For example, a time 3 seconds in the past will be reported as "0 minutes ago" if this is set to [MINUTE_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#MINUTE_IN_MILLIS:kotlin.Long). |
| `transitionResolution` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the elapsed time (in milliseconds) at which to stop reporting relative measurements. Elapsed times greater than this resolution will default to normal date formatting. For example, will transition from "7 days ago" to "Dec 12" when using [WEEK_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#WEEK_IN_MILLIS:kotlin.Long). |

### getRelativeTimeSpanString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeTimeSpanString(
    c: Context!, 
    millis: Long
): CharSequence!
```

Convenience function to return relative time string without preposition.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `c` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:context for resources |
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time in milliseconds |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) containing relative time. |

**See Also**

- [#getRelativeTimeSpanString(Context, long, boolean)](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(android.content.Context,%20kotlin.Long,%20kotlin.Boolean)) 

### getRelativeTimeSpanString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeTimeSpanString(
    c: Context!, 
    millis: Long, 
    withPreposition: Boolean
): CharSequence!
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `withPreposition` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, the string returned will include the correct preposition ("at 9:20am", "on 10/12/2008" or "on May 29"). |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a relative time string to display the time expressed by millis. Times are counted starting at midnight, which means that assuming that the current time is March 31st, 0:30: - "millis=0:10 today" will be displayed as "0:10" - "millis=11:30pm the day before" will be displayed as "Mar 30" If the given millis is in a different year, then the full date is returned in numeric format (e.g., "10/12/2008"). |

### getRelativeTimeSpanString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeTimeSpanString(startTime: Long): CharSequence!
```

Returns a string describing the elapsed time since startTime.

The minimum timespan to report is set to [MINUTE_IN_MILLIS](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#MINUTE_IN_MILLIS:kotlin.Long).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------|
| `startTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):some time in the past. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a String object containing the elapsed time. |

**See Also**

- [#getRelativeTimeSpanString(long, long, long)](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#getRelativeTimeSpanString(kotlin.Long,%20kotlin.Long,%20kotlin.Long)) 

### getRelativeTimeSpanString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeTimeSpanString(
    time: Long, 
    now: Long, 
    minResolution: Long
): CharSequence!
```

Returns a string describing 'time' as a time relative to 'now'.

Time spans in the past are formatted like "42 minutes ago". Time spans in the future are formatted like "In 42 minutes".

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to describe, in milliseconds |
| `now` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the current time in milliseconds |
| `minResolution` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum timespan to report. For example, a time 3 seconds in the past will be reported as "0 minutes ago" if this is set to MINUTE_IN_MILLIS. Pass one of 0, MINUTE_IN_MILLIS, HOUR_IN_MILLIS, DAY_IN_MILLIS, WEEK_IN_MILLIS |

### getRelativeTimeSpanString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRelativeTimeSpanString(
    time: Long, 
    now: Long, 
    minResolution: Long, 
    flags: Int
): CharSequence!
```

Returns a string describing 'time' as a time relative to 'now'.

Time spans in the past are formatted like "42 minutes ago". Time spans in the future are formatted like "In 42 minutes".

Can use [FORMAT_ABBREV_RELATIVE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_RELATIVE:kotlin.Int) flag to use abbreviated relative times, like "42 mins ago".

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to describe, in milliseconds |
| `now` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the current time in milliseconds |
| `minResolution` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum timespan to report. For example, a time 3 seconds in the past will be reported as "0 minutes ago" if this is set to MINUTE_IN_MILLIS. Pass one of 0, MINUTE_IN_MILLIS, HOUR_IN_MILLIS, DAY_IN_MILLIS, WEEK_IN_MILLIS |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit mask of formatting options, such as [FORMAT_NUMERIC_DATE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_NUMERIC_DATE:kotlin.Int) or [FORMAT_ABBREV_RELATIVE](https://developer.android.com/reference/kotlin/android/text/format/DateUtils#FORMAT_ABBREV_RELATIVE:kotlin.Int) |

### isToday

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isToday(when: Long): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the supplied when is today else false |

## Properties

### sameMonthTable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sameMonthTable: IntArray!
```

**Deprecated:** *Do not use.* 

### sameYearTable

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val sameYearTable: IntArray!
```

**Deprecated:** *Do not use.*
