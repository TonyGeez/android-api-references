# Date

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Date

```
open class Date : Date
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Date](../java/util/Date.md) ||
| | ↳ | [java.sql.Date](../java/sql/Date.md) |

A thin wrapper around a millisecond value that allows JDBC to identify this as an SQL`DATE`value. A milliseconds value represents the number of milliseconds that have passed since January 1, 1970 00:00:00.000 GMT.

To conform with the definition of SQL`DATE`, the millisecond values wrapped by a`java.sql.Date`instance must be 'normalized' by setting the hours, minutes, seconds, and milliseconds to zero in the particular time zone with which the instance is associated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Date](../java/sql/Date.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`Date`object initialized with the given year, month, and day. |
| [Date](../java/sql/Date.md))`(`date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a`Date`object using the given milliseconds time value. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHours](../java/sql/Date.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinutes](../java/sql/Date.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSeconds](../java/sql/Date.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHours](../java/sql/Date.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinutes](../java/sql/Date.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSeconds](../java/sql/Date.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](../java/sql/Date.md))`(`date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets an existing`Date`object using the given milliseconds time value. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/sql/Date.md))`()` Formats a date in the date escape format yyyy-mm-dd. |
| openstatic [Date](../java/sql/Date.md)! | [valueOf](../java/sql/Date.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a string in JDBC date escape format to a`Date`value. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Date](../java/util/Date.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UTC](../java/util/Date.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hrs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `min:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines the date and time based on the arguments. The arguments are interpreted as a year, month, day of the month, hour of the day, minute within the hour, and second within the minute, exactly as for the`Date`constructor with six arguments, except that the arguments are interpreted relative to UTC rather than to the local time zone. The time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](../java/util/Date.md))`(`when:` ` [Date](../java/util/Date.md)!`)` <br /> Tests if this date is after the specified date. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](../java/util/Date.md))`(`when:` ` [Date](../java/util/Date.md)!`)` <br /> Tests if this date is before the specified date. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/Date.md))`()` <br /> Return a copy of this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../java/util/Date.md))`(`other:` ` [Date](../java/util/Date.md)!`)` <br /> Compares two Dates for ordering. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/Date.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares two dates for equality. The result is`true`if and only if the argument is not`null`and is a`Date`object that represents the same point in time, to the millisecond, as this object. Thus, two`Date`objects are equal if and only if the`getTime`method returns the same`long`value for both. <br /> | | [Date](../java/util/Date.md)! | [from](../java/util/Date.md))`(`instant:` ` [Instant](../java/time/Instant.md)!`)` <br /> Obtains an instance of`Date`from an`Instant`object. `Instant`uses a precision of nanoseconds, whereas`Date`uses a precision of milliseconds. The conversion will truncate any excess precision information as though the amount in nanoseconds was subject to integer division by one million. `Instant`can store points on the time-line further in the future and further in the past than`Date`. In this scenario, this method will throw an exception. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDate](../java/util/Date.md))`()` <br /> Returns the day of the month represented by this`Date`object. The value returned is between`1`and`31`representing the day of the month that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDay](../java/util/Date.md))`()` <br /> Returns the day of the week represented by this date. The returned value (`0`= Sunday,`1`= Monday,`2`= Tuesday,`3`= Wednesday,`4`= Thursday,`5`= Friday,`6`= Saturday) represents the day of the week that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonth](../java/util/Date.md))`()` <br /> Returns a number representing the month that contains or begins with the instant in time represented by this`Date`object. The value returned is between`0`and`11`, with the value`0`representing January. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTime](../java/util/Date.md))`()` <br /> Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT represented by this`Date`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimezoneOffset](../java/util/Date.md))`()` <br /> Returns the offset, measured in minutes, for the local time zone relative to UTC that is appropriate for the time represented by this`Date`object. For example, in Massachusetts, five time zones west of Greenwich: ```kotlin new Date(96, 1, 14).getTimezoneOffset() returns 300 ``` because on February 14, 1996, standard time (Eastern Standard Time) is in use, which is offset five hours from UTC; but: ```kotlin new Date(96, 5, 1).getTimezoneOffset() returns 240 ``` because on June 1, 1996, daylight saving time (Eastern Daylight Time) is in use, which is offset only four hours from UTC. This method produces the same result as if it computed: ```kotlin (this.getTime() - UTC(this.getYear(), this.getMonth(), this.getDate(), this.getHours(), this.getMinutes(), this.getSeconds())) / (60 * 1000) ``` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYear](../java/util/Date.md))`()` <br /> Returns a value that is the result of subtracting 1900 from the year that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/Date.md))`()` <br /> Returns a hash code value for this object. The result is the exclusive OR of the two halves of the primitive`long`value returned by the [Date.getTime](../java/util/Date.md))method. That is, the hash code is the value of the expression: ```kotlin <code>(int)(this.getTime()^(this.getTime() &gt;&gt;&gt; 32)) </code> ``` <br /> <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parse](../java/util/Date.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to interpret the string`s`as a representation of a date and time. If the attempt is successful, the time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). If the attempt fails, an`IllegalArgumentException`is thrown. It accepts many syntaxes; in particular, it recognizes the IETF standard date syntax: "Sat, 12 Aug 1995 13:30:00 GMT". It also understands the continental U.S. time-zone abbreviations, but for general use, a time-zone offset should be used: "Sat, 12 Aug 1995 13:30:00 GMT+0430" (4 hours, 30 minutes west of the Greenwich meridian). If no time zone is specified, the local time zone is assumed. GMT and UTC are considered equivalent. The string`s`is processed from left to right, looking for data of interest. Any material in`s`that is within the ASCII parenthesis characters`(`and`)`is ignored. Parentheses may be nested. Otherwise, the only characters permitted within`s`are these ASCII characters: ```kotlin abcdefghijklmnopqrstuvwxyz ABCDEFGHIJKLMNOPQRSTUVWXYZ 0123456789,+-:/ ``` and whitespace characters. A consecutive sequence of decimal digits is treated as a decimal number: - If a number is preceded by`+`or`-`and a year has already been recognized, then the number is a time-zone offset. If the number is less than 24, it is an offset measured in hours. Otherwise, it is regarded as an offset in minutes, expressed in 24-hour time format without punctuation. A preceding`-`means a westward offset. Time zone offsets are always relative to UTC (Greenwich). Thus, for example,`-5`occurring in the string would mean "five hours west of Greenwich" and`+0430`would mean "four hours and thirty minutes east of Greenwich." It is permitted for the string to specify`GMT`,`UT`, or`UTC`redundantly-for example,`GMT-5`or`utc+0430`. - The number is regarded as a year number if one of the following conditions is true: - The number is equal to or greater than 70 and followed by a space, comma, slash, or end of string - The number is less than 70, and both a month and a day of the month have already been recognized If the recognized year number is less than 100, it is interpreted as an abbreviated year relative to a century of which dates are within 80 years before and 19 years after the time when the Date class is initialized. After adjusting the year number, 1900 is subtracted from it. For example, if the current year is 1999 then years in the range 19 to 99 are assumed to mean 1919 to 1999, while years from 0 to 18 are assumed to mean 2000 to 2018. Note that this is slightly different from the interpretation of years less than 100 that is used in [java.text.SimpleDateFormat](../java/text/SimpleDateFormat.md). - If the number is followed by a colon, it is regarded as an hour, unless an hour has already been recognized, in which case it is regarded as a minute. - If the number is followed by a slash, it is regarded as a month (it is decreased by 1 to produce a number in the range`0`to`11`), unless a month has already been recognized, in which case it is regarded as a day of the month. - If the number is followed by whitespace, a comma, a hyphen, or end of string, then if an hour has been recognized but not a minute, it is regarded as a minute; otherwise, if a minute has been recognized but not a second, it is regarded as a second; otherwise, it is regarded as a day of the month. A consecutive sequence of letters is regarded as a word and treated as follows: - A word that matches`AM`, ignoring case, is ignored (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - A word that matches`PM`, ignoring case, adds`12`to the hour (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - Any word that matches any prefix of`SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY`, or`SATURDAY`, ignoring case, is ignored. For example,`sat, Friday, TUE`, and`Thurs`are ignored. - Otherwise, any word that matches any prefix of`JANUARY, FEBRUARY, MARCH, APRIL, MAY, JUNE, JULY, AUGUST, SEPTEMBER, OCTOBER, NOVEMBER`, or`DECEMBER`, ignoring case, and considering them in the order given here, is recognized as specifying a month and is converted to a number (`0`to`11`). For example,`aug, Sept, april`, and`NOV`are recognized as months. So is`Ma`, which is recognized as`MARCH`, not`MAY`. - Any word that matches`GMT, UT`, or`UTC`, ignoring case, is treated as referring to UTC. - Any word that matches`EST, CST, MST`, or`PST`, ignoring case, is recognized as referring to the time zone in North America that is five, six, seven, or eight hours west of Greenwich, respectively. Any word that matches`EDT, CDT, MDT`, or`PDT`, ignoring case, is recognized as referring to the same time zone, respectively, during daylight saving time. Once the entire string s has been scanned, it is converted to a time result in one of two ways. If a time zone or time-zone offset has been recognized, then the year, month, day of month, hour, minute, and second are interpreted in UTC and then the time-zone offset is applied. Otherwise, the year, month, day of month, hour, minute, and second are interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](../java/util/Date.md))`(`date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the day of the month of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified day of the month, with the year, month, hour, minute, and second the same as before, as interpreted in the local time zone. If the date was April 30, for example, and the date is set to 31, then it will be treated as if it were on May 1, because April has only 30 days. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonth](../java/util/Date.md))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the month of this date to the specified value. This`Date`object is modified so that it represents a point in time within the specified month, with the year, date, hour, minute, and second the same as before, as interpreted in the local time zone. If the date was October 31, for example, and the month is set to June, then the new date will be treated as if it were on July 1, because June has only 30 days. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYear](../java/util/Date.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the year of this`Date`object to be the specified value plus 1900. This`Date`object is modified so that it represents a point in time within the specified year, with the month, date, hour, minute, and second the same as before, as interpreted in the local time zone. (Of course, if the date was February 29, for example, and the year is set to a non-leap year, then the new date will be treated as if it were on March 1.) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toGMTString](../java/util/Date.md))`()` <br /> Creates a string representation of this`Date`object of the form: ```kotlin d mon yyyy hh:mm:ss GMT ``` where: - *d* is the day of the month (`1`through`31`), as one or two decimal digits. - *mon* is the month (`Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec`). - *yyyy*is the year, as four decimal digits. - *hh* is the hour of the day (`00`through`23`), as two decimal digits. - *mm* is the minute within the hour (`00`through`59`), as two decimal digits. - *ss* is the second within the minute (`00`through`61`), as two decimal digits. - *GMT* is exactly the ASCII letters "`GMT`" to indicate Greenwich Mean Time. <br /> The result does not depend on the local time zone. <br /> | | [Instant](../java/time/Instant.md)! | [toInstant](../java/util/Date.md))`()` <br /> Converts this`Date`object to an`Instant`. The conversion creates an`Instant`that represents the same point on the time-line as this`Date`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocaleString](../java/util/Date.md))`()` <br /> Creates a string representation of this`Date`object in an implementation-dependent form. The intent is that the form should be familiar to the user of the Java application, wherever it may happen to be running. The intent is comparable to that of the "`%c`" format supported by the`strftime()`function of ISO C. <br /> | ||

## Public constructors

### Date

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Date(
    year: Int, 
    month: Int, 
    day: Int)
```

**Deprecated:** *instead use the constructor`Date(long date)`*

Constructs a`Date`object initialized with the given year, month, and day.

The result is undefined if a given argument is out of bounds.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year minus 1900; must be 0 to 8099. (Note that 8099 is 9999 minus 1900.) |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 11 |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):1 to 31 |
| --- | --- |

### Date

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Date(date: Long)
```

Constructs a`Date`object using the given milliseconds time value. If the given milliseconds value contains time information, the driver will set the time components to the time in the default time zone (the time zone of the Java virtual machine running the application) that corresponds to zero GMT.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):milliseconds since January 1, 1970, 00:00:00 GMT not to exceed the milliseconds representation for the year 8099. A negative number indicates the number of milliseconds before January 1, 1970, 00:00:00 GMT. |

## Public methods

### getHours

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHours(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hour represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setHours](../java/sql/Date.md)) 

### getMinutes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinutes(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of minutes past the hour represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setMinutes](../java/sql/Date.md)) 

### getSeconds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSeconds(): Int
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of seconds past the minute represented by this date. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#setSeconds](../java/sql/Date.md)) 

### setHours

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHours(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Parameters ||
|---------|-----------------|
| `hours` | the hour value. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getHours](../java/sql/Date.md)) 

### setMinutes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinutes(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Parameters ||
|-----------|---------------------------|
| `minutes` | the value of the minutes. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getMinutes](../java/sql/Date.md)) 

### setSeconds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSeconds(i: Int): Unit
```

**Deprecated:** *This method is deprecated and should not be used because SQL Date values do not have a time component.*

| Parameters ||
|-----------|--------------------|
| `seconds` | the seconds value. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if this method is invoked |

**See Also**

- [#getSeconds](../java/sql/Date.md)) 

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(date: Long): Unit
```

Sets an existing`Date`object using the given milliseconds time value. If the given milliseconds value contains time information, the driver will set the time components to the time in the default time zone (the time zone of the Java virtual machine running the application) that corresponds to zero GMT.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | the number of milliseconds. |
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):milliseconds since January 1, 1970, 00:00:00 GMT not to exceed the milliseconds representation for the year 8099. A negative number indicates the number of milliseconds before January 1, 1970, 00:00:00 GMT. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Formats a date in the date escape format yyyy-mm-dd.

<br />

| Return ||
|----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a String in yyyy-mm-dd format |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(s: String!): Date!
```

Converts a string in JDBC date escape format to a`Date`value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`object representing a date in in the format "yyyy-\[m\]m-\[d\]d". The leading zero for`mm`and`dd`may also be omitted. |

| Return ||
|------------------------------------------------------------------------|----------------------------------------------------|
| [Date](../java/sql/Date.md)! | a`java.sql.Date`object representing the given date |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the date given is not in the JDBC date escape format (yyyy-\[m\]m-\[d\]d) |
