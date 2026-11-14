# Time

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Time

```
open class Time : Date
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) ||
| | ↳ | [java.sql.Time](https://developer.android.com/reference/kotlin/java/sql/Time#) |

A thin wrapper around the`java.util.Date`class that allows the JDBC API to identify this as an SQL`TIME`value. The`Time`class adds formatting and parsing operations to support the JDBC escape syntax for time values.

The date components should be set to the "zero epoch" value of January 1, 1970 and should not be accessed.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time#Time(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`Time`object initialized with the given values for the hour, minute, and second. |
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time#Time(kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a`Time`object using a milliseconds time value. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDate](https://developer.android.com/reference/kotlin/java/sql/Time#getDate())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDay](https://developer.android.com/reference/kotlin/java/sql/Time#getDay())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonth](https://developer.android.com/reference/kotlin/java/sql/Time#getMonth())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYear](https://developer.android.com/reference/kotlin/java/sql/Time#getYear())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/sql/Time#setDate(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonth](https://developer.android.com/reference/kotlin/java/sql/Time#setMonth(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/Time#setTime(kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets a`Time`object using a milliseconds time value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYear](https://developer.android.com/reference/kotlin/java/sql/Time#setYear(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/sql/Time#toString())`()` Formats a time in JDBC time escape format. |
| --- | --- |
| openstatic [Time](https://developer.android.com/reference/kotlin/java/sql/Time#)! | [valueOf](https://developer.android.com/reference/kotlin/java/sql/Time#valueOf(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a string in JDBC time escape format to a`Time`value. |

| Inherited functions ||
|---|---|
| From class [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UTC](https://developer.android.com/reference/kotlin/java/util/Date.html#UTC(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hrs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `min:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines the date and time based on the arguments. The arguments are interpreted as a year, month, day of the month, hour of the day, minute within the hour, and second within the minute, exactly as for the`Date`constructor with six arguments, except that the arguments are interpreted relative to UTC rather than to the local time zone. The time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](https://developer.android.com/reference/kotlin/java/util/Date.html#after(java.util.Date))`(`when:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Tests if this date is after the specified date. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](https://developer.android.com/reference/kotlin/java/util/Date.html#before(java.util.Date))`(`when:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Tests if this date is before the specified date. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/Date.html#clone())`()` <br /> Return a copy of this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/util/Date.html#compareTo(java.util.Date))`(`other:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Compares two Dates for ordering. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/Date.html#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares two dates for equality. The result is`true`if and only if the argument is not`null`and is a`Date`object that represents the same point in time, to the millisecond, as this object. Thus, two`Date`objects are equal if and only if the`getTime`method returns the same`long`value for both. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [from](https://developer.android.com/reference/kotlin/java/util/Date.html#from(java.time.Instant))`(`instant:` ` [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!`)` <br /> Obtains an instance of`Date`from an`Instant`object. `Instant`uses a precision of nanoseconds, whereas`Date`uses a precision of milliseconds. The conversion will truncate any excess precision information as though the amount in nanoseconds was subject to integer division by one million. `Instant`can store points on the time-line further in the future and further in the past than`Date`. In this scenario, this method will throw an exception. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHours](https://developer.android.com/reference/kotlin/java/util/Date.html#getHours())`()` <br /> Returns the hour represented by this`Date`object. The returned value is a number (`0`through`23`) representing the hour within the day that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinutes](https://developer.android.com/reference/kotlin/java/util/Date.html#getMinutes())`()` <br /> Returns the number of minutes past the hour represented by this date, as interpreted in the local time zone. The value returned is between`0`and`59`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSeconds](https://developer.android.com/reference/kotlin/java/util/Date.html#getSeconds())`()` <br /> Returns the number of seconds past the minute represented by this date. The value returned is between`0`and`61`. The values`60`and`61`can only occur on those Java Virtual Machines that take leap seconds into account. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTime](https://developer.android.com/reference/kotlin/java/util/Date.html#getTime())`()` <br /> Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT represented by this`Date`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimezoneOffset](https://developer.android.com/reference/kotlin/java/util/Date.html#getTimezoneOffset())`()` <br /> Returns the offset, measured in minutes, for the local time zone relative to UTC that is appropriate for the time represented by this`Date`object. For example, in Massachusetts, five time zones west of Greenwich: ```kotlin new Date(96, 1, 14).getTimezoneOffset() returns 300 ``` because on February 14, 1996, standard time (Eastern Standard Time) is in use, which is offset five hours from UTC; but: ```kotlin new Date(96, 5, 1).getTimezoneOffset() returns 240 ``` because on June 1, 1996, daylight saving time (Eastern Daylight Time) is in use, which is offset only four hours from UTC. This method produces the same result as if it computed: ```kotlin (this.getTime() - UTC(this.getYear(), this.getMonth(), this.getDate(), this.getHours(), this.getMinutes(), this.getSeconds())) / (60 * 1000) ``` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/Date.html#hashCode())`()` <br /> Returns a hash code value for this object. The result is the exclusive OR of the two halves of the primitive`long`value returned by the [Date.getTime](https://developer.android.com/reference/kotlin/java/util/Date.html#getTime())method. That is, the hash code is the value of the expression: ```kotlin <code>(int)(this.getTime()^(this.getTime() &gt;&gt;&gt; 32)) </code> ``` <br /> <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parse](https://developer.android.com/reference/kotlin/java/util/Date.html#parse(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to interpret the string`s`as a representation of a date and time. If the attempt is successful, the time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). If the attempt fails, an`IllegalArgumentException`is thrown. It accepts many syntaxes; in particular, it recognizes the IETF standard date syntax: "Sat, 12 Aug 1995 13:30:00 GMT". It also understands the continental U.S. time-zone abbreviations, but for general use, a time-zone offset should be used: "Sat, 12 Aug 1995 13:30:00 GMT+0430" (4 hours, 30 minutes west of the Greenwich meridian). If no time zone is specified, the local time zone is assumed. GMT and UTC are considered equivalent. The string`s`is processed from left to right, looking for data of interest. Any material in`s`that is within the ASCII parenthesis characters`(`and`)`is ignored. Parentheses may be nested. Otherwise, the only characters permitted within`s`are these ASCII characters: ```kotlin abcdefghijklmnopqrstuvwxyz ABCDEFGHIJKLMNOPQRSTUVWXYZ 0123456789,+-:/ ``` and whitespace characters. A consecutive sequence of decimal digits is treated as a decimal number: - If a number is preceded by`+`or`-`and a year has already been recognized, then the number is a time-zone offset. If the number is less than 24, it is an offset measured in hours. Otherwise, it is regarded as an offset in minutes, expressed in 24-hour time format without punctuation. A preceding`-`means a westward offset. Time zone offsets are always relative to UTC (Greenwich). Thus, for example,`-5`occurring in the string would mean "five hours west of Greenwich" and`+0430`would mean "four hours and thirty minutes east of Greenwich." It is permitted for the string to specify`GMT`,`UT`, or`UTC`redundantly-for example,`GMT-5`or`utc+0430`. - The number is regarded as a year number if one of the following conditions is true: - The number is equal to or greater than 70 and followed by a space, comma, slash, or end of string - The number is less than 70, and both a month and a day of the month have already been recognized If the recognized year number is less than 100, it is interpreted as an abbreviated year relative to a century of which dates are within 80 years before and 19 years after the time when the Date class is initialized. After adjusting the year number, 1900 is subtracted from it. For example, if the current year is 1999 then years in the range 19 to 99 are assumed to mean 1919 to 1999, while years from 0 to 18 are assumed to mean 2000 to 2018. Note that this is slightly different from the interpretation of years less than 100 that is used in [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#). - If the number is followed by a colon, it is regarded as an hour, unless an hour has already been recognized, in which case it is regarded as a minute. - If the number is followed by a slash, it is regarded as a month (it is decreased by 1 to produce a number in the range`0`to`11`), unless a month has already been recognized, in which case it is regarded as a day of the month. - If the number is followed by whitespace, a comma, a hyphen, or end of string, then if an hour has been recognized but not a minute, it is regarded as a minute; otherwise, if a minute has been recognized but not a second, it is regarded as a second; otherwise, it is regarded as a day of the month. A consecutive sequence of letters is regarded as a word and treated as follows: - A word that matches`AM`, ignoring case, is ignored (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - A word that matches`PM`, ignoring case, adds`12`to the hour (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - Any word that matches any prefix of`SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY`, or`SATURDAY`, ignoring case, is ignored. For example,`sat, Friday, TUE`, and`Thurs`are ignored. - Otherwise, any word that matches any prefix of`JANUARY, FEBRUARY, MARCH, APRIL, MAY, JUNE, JULY, AUGUST, SEPTEMBER, OCTOBER, NOVEMBER`, or`DECEMBER`, ignoring case, and considering them in the order given here, is recognized as specifying a month and is converted to a number (`0`to`11`). For example,`aug, Sept, april`, and`NOV`are recognized as months. So is`Ma`, which is recognized as`MARCH`, not`MAY`. - Any word that matches`GMT, UT`, or`UTC`, ignoring case, is treated as referring to UTC. - Any word that matches`EST, CST, MST`, or`PST`, ignoring case, is recognized as referring to the time zone in North America that is five, six, seven, or eight hours west of Greenwich, respectively. Any word that matches`EDT, CDT, MDT`, or`PDT`, ignoring case, is recognized as referring to the same time zone, respectively, during daylight saving time. Once the entire string s has been scanned, it is converted to a time result in one of two ways. If a time zone or time-zone offset has been recognized, then the year, month, day of month, hour, minute, and second are interpreted in UTC and then the time-zone offset is applied. Otherwise, the year, month, day of month, hour, minute, and second are interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHours](https://developer.android.com/reference/kotlin/java/util/Date.html#setHours(kotlin.Int))`(`hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the hour of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified hour of the day, with the year, month, date, minute, and second the same as before, as interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinutes](https://developer.android.com/reference/kotlin/java/util/Date.html#setMinutes(kotlin.Int))`(`minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the minutes of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified minute of the hour, with the year, month, date, hour, and second the same as before, as interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSeconds](https://developer.android.com/reference/kotlin/java/util/Date.html#setSeconds(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the seconds of this`Date`to the specified value. This`Date`object is modified so that it represents a point in time within the specified second of the minute, with the year, month, date, hour, and minute the same as before, as interpreted in the local time zone. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toGMTString](https://developer.android.com/reference/kotlin/java/util/Date.html#toGMTString())`()` <br /> Creates a string representation of this`Date`object of the form: ```kotlin d mon yyyy hh:mm:ss GMT ``` where: - *d* is the day of the month (`1`through`31`), as one or two decimal digits. - *mon* is the month (`Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec`). - *yyyy*is the year, as four decimal digits. - *hh* is the hour of the day (`00`through`23`), as two decimal digits. - *mm* is the minute within the hour (`00`through`59`), as two decimal digits. - *ss* is the second within the minute (`00`through`61`), as two decimal digits. - *GMT* is exactly the ASCII letters "`GMT`" to indicate Greenwich Mean Time. <br /> The result does not depend on the local time zone. <br /> | | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)! | [toInstant](https://developer.android.com/reference/kotlin/java/util/Date.html#toInstant())`()` <br /> Converts this`Date`object to an`Instant`. The conversion creates an`Instant`that represents the same point on the time-line as this`Date`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocaleString](https://developer.android.com/reference/kotlin/java/util/Date.html#toLocaleString())`()` <br /> Creates a string representation of this`Date`object in an implementation-dependent form. The intent is that the form should be familiar to the user of the Java application, wherever it may happen to be running. The intent is comparable to that of the "`%c`" format supported by the`strftime()`function of ISO C. <br /> | ||

## Public constructors

### Time

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Time(
    hour: Int, 
    minute: Int, 
    second: Int)
```

**Deprecated:** *Use the constructor that takes a milliseconds value in place of this constructor*

Constructs a`Time`object initialized with the given values for the hour, minute, and second. The driver sets the date components to January 1, 1970. Any method that attempts to access the date components of a`Time`object will throw a`java.lang.IllegalArgumentException`.

The result is undefined if a given argument is out of bounds.

| Parameters ||
|----------|------------------------------------------------------------------------------------|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 59 |
| --- | --- |

### Time

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Time(time: Long)
```

Constructs a`Time`object using a milliseconds time value.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):milliseconds since January 1, 1970, 00:00:00 GMT; a negative number is milliseconds before January 1, 1970, 00:00:00 GMT |

## Public methods

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDate(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a date component.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day of the month represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setDate](https://developer.android.com/reference/kotlin/java/sql/Time#setDate(kotlin.Int)) 

### getDay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDay(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a day component.*

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day of the week represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

### getMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonth(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a month component.*

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the month represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setMonth](https://developer.android.com/reference/kotlin/java/sql/Time#setMonth(kotlin.Int)) 

### getYear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYear(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a year component.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the year represented by this date, minus 1900. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setYear](https://developer.android.com/reference/kotlin/java/sql/Time#setYear(kotlin.Int)) 

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDate(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a date component.*

| Parameters ||
|--------|------------------------------------------|
| `date` | the day of the month value between 1-31. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getDate](https://developer.android.com/reference/kotlin/java/sql/Time#getDate()) 

### setMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonth(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a month component.*

| Parameters ||
|---------|-------------------------------|
| `month` | the month value between 0-11. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getMonth](https://developer.android.com/reference/kotlin/java/sql/Time#getMonth()) 

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(time: Long): Unit
```

Sets a`Time`object using a milliseconds time value.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):milliseconds since January 1, 1970, 00:00:00 GMT; a negative number is milliseconds before January 1, 1970, 00:00:00 GMT |

### setYear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setYear(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL`TIME`values do not have a year component.*

| Parameters ||
|--------|-----------------|
| `year` | the year value. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getYear](https://developer.android.com/reference/kotlin/java/sql/Time#getYear()) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Formats a time in JDBC time escape format.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`in hh:mm:ss format |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(s: String!): Time!
```

Converts a string in JDBC time escape format to a`Time`value.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:time in format "hh:mm:ss" |

| Return ||
|------------------------------------------------------------------------|-----------------------------|
| [Time](https://developer.android.com/reference/kotlin/java/sql/Time#)! | a corresponding`Time`object |
