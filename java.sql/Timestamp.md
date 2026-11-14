# Timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Timestamp

```
open class Timestamp : Date
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) ||
| | ↳ | [java.sql.Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#) |

A thin wrapper around`java.util.Date`that allows the JDBC API to identify this as an SQL`TIMESTAMP`value. It adds the ability to hold the SQL`TIMESTAMP`fractional seconds value, by allowing the specification of fractional seconds to a precision of nanoseconds. A Timestamp also provides formatting and parsing operations to support the JDBC escape syntax for timestamp values.

The precision of a Timestamp object is calculated to be either:

- `19 `, which is the number of characters in yyyy-mm-dd hh:mm:ss
- ` 20 + s `, which is the number of characters in the yyyy-mm-dd hh:mm:ss.\[fff...\] and`s`represents the scale of the given Timestamp, its fractional seconds precision.

**Note:** This type is a composite of a`java.util.Date`and a separate nanoseconds value. Only integral seconds are stored in the`java.util.Date`component. The fractional seconds - the nanos - are separate. The`Timestamp.equals(Object)`method never returns`true`when passed an object that isn't an instance of`java.sql.Timestamp`, because the nanos component of a date is unknown. As a result, the`Timestamp.equals(Object)`method is not symmetric with respect to the`java.util.Date.equals(Object)`method. Also, the`hashCode`method uses the underlying`java.util.Date`implementation and therefore does not include nanos in its computation.

Due to the differences between the`Timestamp`class and the`java.util.Date`class mentioned above, it is recommended that code not view`Timestamp`values generically as an instance of`java.util.Date`. The inheritance relationship between`Timestamp`and`java.util.Date`really denotes implementation inheritance, and not type inheritance.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#Timestamp(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nano:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`Timestamp`object initialized with the given values. |
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#Timestamp(kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a`Timestamp`object using a milliseconds time value. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](https://developer.android.com/reference/kotlin/java/sql/Timestamp#after(java.sql.Timestamp))`(`ts:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!`)` Indicates whether this`Timestamp`object is later than the given`Timestamp`object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](https://developer.android.com/reference/kotlin/java/sql/Timestamp#before(java.sql.Timestamp))`(`ts:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!`)` Indicates whether this`Timestamp`object is earlier than the given`Timestamp`object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/sql/Timestamp#compareTo(java.sql.Timestamp))`(`ts:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!`)` Compares this`Timestamp`object to the given`Timestamp`object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/sql/Timestamp#compareTo(java.util.Date))`(`other:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Compares this`Timestamp`object to the given`Date`object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/sql/Timestamp#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests to see if this`Timestamp`object is equal to the given object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/sql/Timestamp#equals(java.sql.Timestamp))`(`ts:` ` [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!`)` Tests to see if this`Timestamp`object is equal to the given`Timestamp`object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNanos](https://developer.android.com/reference/kotlin/java/sql/Timestamp#getNanos())`()` Gets this`Timestamp`object's`nanos`value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTime](https://developer.android.com/reference/kotlin/java/sql/Timestamp#getTime())`()` Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT represented by this`Timestamp`object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/sql/Timestamp#hashCode())`()` Returns a hash code value for this object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNanos](https://developer.android.com/reference/kotlin/java/sql/Timestamp#setNanos(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this`Timestamp`object's`nanos`field to the given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/sql/Timestamp#setTime(kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets this`Timestamp`object to represent a point in time that is time milliseconds after January 1, 1970 00:00:00 GMT. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/sql/Timestamp#toString())`()` Formats a timestamp in JDBC timestamp escape format. |
| --- | --- |
| openstatic [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)! | [valueOf](https://developer.android.com/reference/kotlin/java/sql/Timestamp#valueOf(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a`String`object in JDBC timestamp escape format to a`Timestamp`value. |

| Inherited functions ||
|---|---|
| From class [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UTC](https://developer.android.com/reference/kotlin/java/util/Date.html#UTC(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hrs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `min:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines the date and time based on the arguments. The arguments are interpreted as a year, month, day of the month, hour of the day, minute within the hour, and second within the minute, exactly as for the`Date`constructor with six arguments, except that the arguments are interpreted relative to UTC rather than to the local time zone. The time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](https://developer.android.com/reference/kotlin/java/util/Date.html#after(java.util.Date))`(`when:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Tests if this date is after the specified date. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](https://developer.android.com/reference/kotlin/java/util/Date.html#before(java.util.Date))`(`when:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` <br /> Tests if this date is before the specified date. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/Date.html#clone())`()` <br /> Return a copy of this object. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [from](https://developer.android.com/reference/kotlin/java/util/Date.html#from(java.time.Instant))`(`instant:` ` [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!`)` <br /> Obtains an instance of`Date`from an`Instant`object. `Instant`uses a precision of nanoseconds, whereas`Date`uses a precision of milliseconds. The conversion will truncate any excess precision information as though the amount in nanoseconds was subject to integer division by one million. `Instant`can store points on the time-line further in the future and further in the past than`Date`. In this scenario, this method will throw an exception. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDate](https://developer.android.com/reference/kotlin/java/util/Date.html#getDate())`()` <br /> Returns the day of the month represented by this`Date`object. The value returned is between`1`and`31`representing the day of the month that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDay](https://developer.android.com/reference/kotlin/java/util/Date.html#getDay())`()` <br /> Returns the day of the week represented by this date. The returned value (`0`= Sunday,`1`= Monday,`2`= Tuesday,`3`= Wednesday,`4`= Thursday,`5`= Friday,`6`= Saturday) represents the day of the week that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHours](https://developer.android.com/reference/kotlin/java/util/Date.html#getHours())`()` <br /> Returns the hour represented by this`Date`object. The returned value is a number (`0`through`23`) representing the hour within the day that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinutes](https://developer.android.com/reference/kotlin/java/util/Date.html#getMinutes())`()` <br /> Returns the number of minutes past the hour represented by this date, as interpreted in the local time zone. The value returned is between`0`and`59`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonth](https://developer.android.com/reference/kotlin/java/util/Date.html#getMonth())`()` <br /> Returns a number representing the month that contains or begins with the instant in time represented by this`Date`object. The value returned is between`0`and`11`, with the value`0`representing January. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSeconds](https://developer.android.com/reference/kotlin/java/util/Date.html#getSeconds())`()` <br /> Returns the number of seconds past the minute represented by this date. The value returned is between`0`and`61`. The values`60`and`61`can only occur on those Java Virtual Machines that take leap seconds into account. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimezoneOffset](https://developer.android.com/reference/kotlin/java/util/Date.html#getTimezoneOffset())`()` <br /> Returns the offset, measured in minutes, for the local time zone relative to UTC that is appropriate for the time represented by this`Date`object. For example, in Massachusetts, five time zones west of Greenwich: ```kotlin new Date(96, 1, 14).getTimezoneOffset() returns 300 ``` because on February 14, 1996, standard time (Eastern Standard Time) is in use, which is offset five hours from UTC; but: ```kotlin new Date(96, 5, 1).getTimezoneOffset() returns 240 ``` because on June 1, 1996, daylight saving time (Eastern Daylight Time) is in use, which is offset only four hours from UTC. This method produces the same result as if it computed: ```kotlin (this.getTime() - UTC(this.getYear(), this.getMonth(), this.getDate(), this.getHours(), this.getMinutes(), this.getSeconds())) / (60 * 1000) ``` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYear](https://developer.android.com/reference/kotlin/java/util/Date.html#getYear())`()` <br /> Returns a value that is the result of subtracting 1900 from the year that contains or begins with the instant in time represented by this`Date`object, as interpreted in the local time zone. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [parse](https://developer.android.com/reference/kotlin/java/util/Date.html#parse(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to interpret the string`s`as a representation of a date and time. If the attempt is successful, the time indicated is returned represented as the distance, measured in milliseconds, of that time from the epoch (00:00:00 GMT on January 1, 1970). If the attempt fails, an`IllegalArgumentException`is thrown. It accepts many syntaxes; in particular, it recognizes the IETF standard date syntax: "Sat, 12 Aug 1995 13:30:00 GMT". It also understands the continental U.S. time-zone abbreviations, but for general use, a time-zone offset should be used: "Sat, 12 Aug 1995 13:30:00 GMT+0430" (4 hours, 30 minutes west of the Greenwich meridian). If no time zone is specified, the local time zone is assumed. GMT and UTC are considered equivalent. The string`s`is processed from left to right, looking for data of interest. Any material in`s`that is within the ASCII parenthesis characters`(`and`)`is ignored. Parentheses may be nested. Otherwise, the only characters permitted within`s`are these ASCII characters: ```kotlin abcdefghijklmnopqrstuvwxyz ABCDEFGHIJKLMNOPQRSTUVWXYZ 0123456789,+-:/ ``` and whitespace characters. A consecutive sequence of decimal digits is treated as a decimal number: - If a number is preceded by`+`or`-`and a year has already been recognized, then the number is a time-zone offset. If the number is less than 24, it is an offset measured in hours. Otherwise, it is regarded as an offset in minutes, expressed in 24-hour time format without punctuation. A preceding`-`means a westward offset. Time zone offsets are always relative to UTC (Greenwich). Thus, for example,`-5`occurring in the string would mean "five hours west of Greenwich" and`+0430`would mean "four hours and thirty minutes east of Greenwich." It is permitted for the string to specify`GMT`,`UT`, or`UTC`redundantly-for example,`GMT-5`or`utc+0430`. - The number is regarded as a year number if one of the following conditions is true: - The number is equal to or greater than 70 and followed by a space, comma, slash, or end of string - The number is less than 70, and both a month and a day of the month have already been recognized If the recognized year number is less than 100, it is interpreted as an abbreviated year relative to a century of which dates are within 80 years before and 19 years after the time when the Date class is initialized. After adjusting the year number, 1900 is subtracted from it. For example, if the current year is 1999 then years in the range 19 to 99 are assumed to mean 1919 to 1999, while years from 0 to 18 are assumed to mean 2000 to 2018. Note that this is slightly different from the interpretation of years less than 100 that is used in [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#). - If the number is followed by a colon, it is regarded as an hour, unless an hour has already been recognized, in which case it is regarded as a minute. - If the number is followed by a slash, it is regarded as a month (it is decreased by 1 to produce a number in the range`0`to`11`), unless a month has already been recognized, in which case it is regarded as a day of the month. - If the number is followed by whitespace, a comma, a hyphen, or end of string, then if an hour has been recognized but not a minute, it is regarded as a minute; otherwise, if a minute has been recognized but not a second, it is regarded as a second; otherwise, it is regarded as a day of the month. A consecutive sequence of letters is regarded as a word and treated as follows: - A word that matches`AM`, ignoring case, is ignored (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - A word that matches`PM`, ignoring case, adds`12`to the hour (but the parse fails if an hour has not been recognized or is less than`1`or greater than`12`). - Any word that matches any prefix of`SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY`, or`SATURDAY`, ignoring case, is ignored. For example,`sat, Friday, TUE`, and`Thurs`are ignored. - Otherwise, any word that matches any prefix of`JANUARY, FEBRUARY, MARCH, APRIL, MAY, JUNE, JULY, AUGUST, SEPTEMBER, OCTOBER, NOVEMBER`, or`DECEMBER`, ignoring case, and considering them in the order given here, is recognized as specifying a month and is converted to a number (`0`to`11`). For example,`aug, Sept, april`, and`NOV`are recognized as months. So is`Ma`, which is recognized as`MARCH`, not`MAY`. - Any word that matches`GMT, UT`, or`UTC`, ignoring case, is treated as referring to UTC. - Any word that matches`EST, CST, MST`, or`PST`, ignoring case, is recognized as referring to the time zone in North America that is five, six, seven, or eight hours west of Greenwich, respectively. Any word that matches`EDT, CDT, MDT`, or`PDT`, ignoring case, is recognized as referring to the same time zone, respectively, during daylight saving time. Once the entire string s has been scanned, it is converted to a time result in one of two ways. If a time zone or time-zone offset has been recognized, then the year, month, day of month, hour, minute, and second are interpreted in UTC and then the time-zone offset is applied. Otherwise, the year, month, day of month, hour, minute, and second are interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](https://developer.android.com/reference/kotlin/java/util/Date.html#setDate(kotlin.Int))`(`date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the day of the month of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified day of the month, with the year, month, hour, minute, and second the same as before, as interpreted in the local time zone. If the date was April 30, for example, and the date is set to 31, then it will be treated as if it were on May 1, because April has only 30 days. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHours](https://developer.android.com/reference/kotlin/java/util/Date.html#setHours(kotlin.Int))`(`hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the hour of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified hour of the day, with the year, month, date, minute, and second the same as before, as interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinutes](https://developer.android.com/reference/kotlin/java/util/Date.html#setMinutes(kotlin.Int))`(`minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the minutes of this`Date`object to the specified value. This`Date`object is modified so that it represents a point in time within the specified minute of the hour, with the year, month, date, hour, and second the same as before, as interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonth](https://developer.android.com/reference/kotlin/java/util/Date.html#setMonth(kotlin.Int))`(`month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the month of this date to the specified value. This`Date`object is modified so that it represents a point in time within the specified month, with the year, date, hour, minute, and second the same as before, as interpreted in the local time zone. If the date was October 31, for example, and the month is set to June, then the new date will be treated as if it were on July 1, because June has only 30 days. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSeconds](https://developer.android.com/reference/kotlin/java/util/Date.html#setSeconds(kotlin.Int))`(`seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the seconds of this`Date`to the specified value. This`Date`object is modified so that it represents a point in time within the specified second of the minute, with the year, month, date, hour, and minute the same as before, as interpreted in the local time zone. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYear](https://developer.android.com/reference/kotlin/java/util/Date.html#setYear(kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the year of this`Date`object to be the specified value plus 1900. This`Date`object is modified so that it represents a point in time within the specified year, with the month, date, hour, minute, and second the same as before, as interpreted in the local time zone. (Of course, if the date was February 29, for example, and the year is set to a non-leap year, then the new date will be treated as if it were on March 1.) <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toGMTString](https://developer.android.com/reference/kotlin/java/util/Date.html#toGMTString())`()` <br /> Creates a string representation of this`Date`object of the form: ```kotlin d mon yyyy hh:mm:ss GMT ``` where: - *d* is the day of the month (`1`through`31`), as one or two decimal digits. - *mon* is the month (`Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec`). - *yyyy*is the year, as four decimal digits. - *hh* is the hour of the day (`00`through`23`), as two decimal digits. - *mm* is the minute within the hour (`00`through`59`), as two decimal digits. - *ss* is the second within the minute (`00`through`61`), as two decimal digits. - *GMT* is exactly the ASCII letters "`GMT`" to indicate Greenwich Mean Time. <br /> The result does not depend on the local time zone. <br /> | | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)! | [toInstant](https://developer.android.com/reference/kotlin/java/util/Date.html#toInstant())`()` <br /> Converts this`Date`object to an`Instant`. The conversion creates an`Instant`that represents the same point on the time-line as this`Date`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocaleString](https://developer.android.com/reference/kotlin/java/util/Date.html#toLocaleString())`()` <br /> Creates a string representation of this`Date`object in an implementation-dependent form. The intent is that the form should be familiar to the user of the Java application, wherever it may happen to be running. The intent is comparable to that of the "`%c`" format supported by the`strftime()`function of ISO C. <br /> | ||

## Public constructors

### Timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timestamp(
    year: Int, 
    month: Int, 
    date: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    nano: Int)
```

**Deprecated:** *instead use the constructor`Timestamp(long millis)`*

Constructs a`Timestamp`object initialized with the given values.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year minus 1900 |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 11 |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):1 to 31 |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 59 |
| --- | --- |
| `nano` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 to 999,999,999 |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | if the nano argument is out of bounds |

### Timestamp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Timestamp(time: Long)
```

Constructs a`Timestamp`object using a milliseconds time value. The integral seconds are stored in the underlying date value; the fractional seconds are stored in the`nanos`field of the`Timestamp`object.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):milliseconds since January 1, 1970, 00:00:00 GMT. A negative number is the number of milliseconds before January 1, 1970, 00:00:00 GMT. |

**See Also**

- [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)

## Public methods

### after

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun after(ts: Timestamp!): Boolean
```

Indicates whether this`Timestamp`object is later than the given`Timestamp`object.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ts` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!:the`Timestamp`value to compare with |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`Timestamp`object is later;`false`otherwise |

### before

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun before(ts: Timestamp!): Boolean
```

Indicates whether this`Timestamp`object is earlier than the given`Timestamp`object.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ts` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!:the`Timestamp`value to compare with |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`Timestamp`object is earlier;`false`otherwise |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(ts: Timestamp!): Int
```

Compares this`Timestamp`object to the given`Timestamp`object.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `ts` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!:the`Timestamp`object to be compared to this`Timestamp`object |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if the two`Timestamp`objects are equal; a value less than`0`if this`Timestamp`object is before the given argument; and a value greater than`0`if this`Timestamp`object is after the given argument. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: Date!): Int
```

Compares this`Timestamp`object to the given`Date`object.

| Parameters ||
|---------------|--------------------------------------------------|
| `o` | the`Date`to be compared to this`Timestamp`object |
| `anotherDate` | the`Date`to be compared. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value`0`if this`Timestamp`object and the given object are equal; a value less than`0`if this`Timestamp`object is before the given argument; and a value greater than`0`if this`Timestamp`object is after the given argument. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`anotherDate`is null. |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Tests to see if this`Timestamp`object is equal to the given object. This version of the method`equals`has been added to fix the incorrect signature of`Timestamp.equals(Timestamp)`and to preserve backward compatibility with existing class files. Note: This method is not symmetric with respect to the`equals(Object)`method in the base class.

| Parameters ||
|-------|----------------------------------|
| `obj` | the object to compare with. |
| `ts` | the`Object`value to compare with |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given`Object`is an instance of a`Timestamp`that is equal to this`Timestamp`object;`false`otherwise |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(ts: Timestamp!): Boolean
```

Tests to see if this`Timestamp`object is equal to the given`Timestamp`object.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ts` | [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)!:the`Timestamp`value to compare with |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given`Timestamp`object is equal to this`Timestamp`object;`false`otherwise |

### getNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNanos(): Int
```

Gets this`Timestamp`object's`nanos`value.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this`Timestamp`object's fractional seconds component |

**See Also**

- [#setNanos](https://developer.android.com/reference/kotlin/java/sql/Timestamp#setNanos(kotlin.Int)) 

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTime(): Long
```

Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT represented by this`Timestamp`object.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of milliseconds since January 1, 1970, 00:00:00 GMT represented by this date. |

**See Also**

- [#setTime](https://developer.android.com/reference/kotlin/java/sql/Timestamp#setTime(kotlin.Long)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for this object. The result is the exclusive OR of the two halves of the primitive`long`value returned by the [Date.getTime](https://developer.android.com/reference/kotlin/java/util/Date.html#getTime())method. That is, the hash code is the value of the expression: 

```kotlin
<code>(int)(this.getTime()^(this.getTime() &gt;&gt;&gt; 32))
  </code>
```
The`hashCode`method uses the underlying`java.util.Date`implementation and therefore does not include nanos in its computation.

<br />

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNanos(n: Int): Unit
```

Sets this`Timestamp`object's`nanos`field to the given value.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new fractional seconds component |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given argument is greater than 999999999 or less than 0 |

**See Also**

- [#getNanos](https://developer.android.com/reference/kotlin/java/sql/Timestamp#getNanos()) 

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTime(time: Long): Unit
```

Sets this`Timestamp`object to represent a point in time that is time milliseconds after January 1, 1970 00:00:00 GMT.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the number of milliseconds. |

**See Also**

- [#getTime](https://developer.android.com/reference/kotlin/java/sql/Timestamp#getTime())
- [#Timestamp(long time)](https://developer.android.com/reference/kotlin/java/sql/Timestamp#Timestamp(kotlin.Long))
- [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Formats a timestamp in JDBC timestamp escape format.`yyyy-mm-dd hh:mm:ss.fffffffff`, where`ffffffffff`indicates nanoseconds.

<br />

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`object in`yyyy-mm-dd hh:mm:ss.fffffffff`format |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(s: String!): Timestamp!
```

Converts a`String`object in JDBC timestamp escape format to a`Timestamp`value.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:timestamp in format`yyyy-[m]m-[d]d hh:mm:ss[.f...]`. The fractional seconds may be omitted. The leading zero for`mm`and`dd`may also be omitted. |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------|
| [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp#)! | corresponding`Timestamp`value |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given argument does not have the format`yyyy-[m]m-[d]d hh:mm:ss[.f...]` |
