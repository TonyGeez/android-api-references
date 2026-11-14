Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLGregorianCalendar

```
abstract class XMLGregorianCalendar : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.datatype.XMLGregorianCalendar](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#) |

Representation for W3C XML Schema 1.0 date/time datatypes. Specifically, these date/time datatypes are [`dateTime`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#DATETIME), [`time`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#TIME), [`date`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#DATE), [`gYearMonth`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#GYEARMONTH), [`gMonthDay`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#GMONTHDAY), [`gYear`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#GYEAR) [`gMonth`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#GMONTH) and [`gDay`](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#GDAY) defined in the XML Namespace `"http://www.w3.org/2001/XMLSchema"`. These datatypes are normatively defined in [W3C XML Schema 1.0 Part 2, Section 3.2.7-14](http://www.w3.org/TR/xmlschema-2/#dateTime).

The table below defines the mapping between XML Schema 1.0 date/time datatype fields and this class' fields. It also summarizes the value constraints for the date and time fields defined in [W3C XML Schema 1.0 Part 2, Appendix D, *ISO 8601 Date and Time Formats*](http://www.w3.org/TR/xmlschema-2/#isoformats).

| Date/Time Datatype Field Mapping Between XML Schema 1.0 and Java Representation |||
| --- | --- | --- |
| XML Schema 1.0 datatype field | Related XMLGregorianCalendar Accessor(s) | Value Range |
|---|---|---|
| year | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getYear()` + `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEon()` or `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()` | `getYear()` is a value between -(10\^9-1) to (10\^9)-1 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEon()` is high order year value in billion of years. `getEon()` has values greater than or equal to (10\^9) or less than or equal to -(10\^9). A value of null indicates field is undefined. Given that [XML Schema 1.0 errata](http://www.w3.org/2001/05/xmlschema-errata#e2-63) states that the year zero will be a valid lexical value in a future version of XML Schema, this class allows the year field to be set to zero. Otherwise, the year field value is handled exactly as described in the errata and \[ISO-8601-1988\]. Note that W3C XML Schema 1.0 validation does not allow for the year field to have a value of zero. |
| month | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMonth()` | 1 to 12 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` |
| day | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getDay()` | Independent of month, max range is 1 to 31 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. The normative value constraint stated relative to month field's value is in [W3C XML Schema 1.0 Part 2, Appendix D](http://www.w3.org/TR/xmlschema-2/#isoformats). |
| --- | --- | --- |
| hour | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getHour()` | 0 to 24 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. For a value of 24, the minute and second field must be zero per [XML Schema Errata](http://www.w3.org/2001/05/xmlschema-errata#e2-45). |
| minute | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMinute()` | 0 to 59 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` |
| second | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()` + `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMillisecond()`/1000 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()` + `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()` from 0 to 60 or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. *(Note: 60 only allowable for leap second.)* `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()` allows for infinite precision over the range from 0.0 to 1.0 when the `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()` is defined. `FractionalSecond` is optional and has a value of `null` when it is undefined. `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMillisecond()` is the convenience millisecond precision of value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`. |
| --- | --- | --- |
| timezone | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getTimezone()` | Number of minutes or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. Value range from -14 hours (-14 \* 60 minutes) to 14 hours (14 \* 60 minutes). |

All maximum value space constraints listed for the fields in the table above are checked by factory methods, @{link DatatypeFactory}, setter methods and parse methods of this class. `IllegalArgumentException` is thrown when a parameter's value is outside the value constraint for the field or if the composite values constitute an invalid XMLGregorianCalendar instance (for example, if the 31st of June is specified).

The following operations are defined for this class:

- accessors/mutators for independent date/time fields
- conversion between this class and W3C XML Schema 1.0 lexical representation, `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toString()`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar(kotlin.String)`
- conversion between this class and `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toGregorianCalendar(java.util.TimeZone,%20java.util.Locale,%20javax.xml.datatype.XMLGregorianCalendar)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory`
- partial order relation comparator method, `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#compare(javax.xml.datatype.XMLGregorianCalendar)`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#equals(kotlin.Any)` defined relative to `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#compare(javax.xml.datatype.XMLGregorianCalendar)`.
- addition operation with `https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration` instance as defined in [W3C XML Schema 1.0 Part 2, Appendix E, *Adding durations to dateTimes*](http://www.w3.org/TR/xmlschema-2/#adding-durations-to-dateTimes).

<br />

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#XMLGregorianCalendar()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#add(javax.xml.datatype.Duration)(duration: https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration!)` Add `duration` to this instance. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#clear()()` Unset all fields to undefined. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#clone()()` Creates and returns a copy of this object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#compare(javax.xml.datatype.XMLGregorianCalendar)(xmlGregorianCalendar: https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#!)` Compare two instances of W3C XML Schema 1. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether parameter `obj` is "equal to" this one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getDay()()` Return day in month or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. |
| --- | --- |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEon()()` Return high order component for XML Schema 1. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()()` Return XML Schema 1. |
| abstract [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()()` Return fractional seconds. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getHour()()` Return hours or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMillisecond()()` Return millisecond precision of `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMinute()()` Return minutes or . |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMonth()()` Return number of month or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()()` Return seconds or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. |
| abstract [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getTimeZone(kotlin.Int)(defaultZoneoffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a `java.util.TimeZone` for this class. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getTimezone()()` Return timezone offset in minutes or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` if this optional field is not defined. |
| abstract [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getXMLSchemaType()()` Return the name of the XML Schema date/time type that this instance maps to. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getYear()()` Return low order component for XML Schema 1. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#hashCode()()` Returns a hash code consistent with the definition of the equals method. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#isValid()()` Validate instance by `getXMLSchemaType()` constraints. |
| abstract [XMLGregorianCalendar](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#normalize()()` Normalize this instance to UTC. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#reset()()` Reset this `XMLGregorianCalendar` to its original values. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setDay(kotlin.Int)(day: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set days in month. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setFractionalSecond(java.math.BigDecimal)(fractional: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` Set fractional seconds. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setHour(kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set hours. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setMillisecond(kotlin.Int)(millisecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set milliseconds. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setMinute(kotlin.Int)(minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set minutes. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setMonth(kotlin.Int)(month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set month. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setSecond(kotlin.Int)(second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set seconds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set time as one unit. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, millisecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set time as one unit, including optional milliseconds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.math.BigDecimal)(hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fractional: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` Set time as one unit, including the optional infinite precision fractional seconds. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTimezone(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the number of minutes in the timezone offset. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set year of XSD `dateTime` year field. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setYear(java.math.BigInteger)(year: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!)` Set low and high order component of XSD `dateTime` year field. |
| abstract [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toGregorianCalendar()()` Convert this `XMLGregorianCalendar` to a `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#`. |
| --- | --- |
| abstract [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toGregorianCalendar(java.util.TimeZone,%20java.util.Locale,%20javax.xml.datatype.XMLGregorianCalendar)(timezone: https://developer.android.com/reference/kotlin/java/util/TimeZone.html#!, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!, defaults: https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#!)` Convert this `XMLGregorianCalendar` along with provided parameters to a `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#` instance. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toString()()` Returns a `String` representation of this `XMLGregorianCalendar` `Object`. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toXMLFormat()()` Return the lexical representation of `this` instance. |
| --- | --- |

## Public constructors

### XMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
XMLGregorianCalendar()
```

## Public methods

### add

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(duration: Duration!): Unit
```

Add `duration` to this instance.

The computation is specified in [XML Schema 1.0 Part 2, Appendix E, *Adding durations to dateTimes*\>](http://www.w3.org/TR/xmlschema-2/#adding-durations-to-dateTimes). [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldsmapping) defines the mapping from XML Schema 1.0 `dateTime` fields to this class' representation of those fields.

| Parameters ||
|---|---|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration)!: Duration to add to this `XMLGregorianCalendar`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | when `duration` parameter is `null`. |

### clear

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clear(): Unit
```

Unset all fields to undefined.

Set all int fields to `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` and reference fields to null.

### clone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | copy of this `Object` |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compare

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compare(xmlGregorianCalendar: XMLGregorianCalendar!): Int
```

Compare two instances of W3C XML Schema 1.0 date/time datatypes according to partial order relation defined in [W3C XML Schema 1.0 Part 2, Section 3.2.7.3, *Order relation on dateTime*](http://www.w3.org/TR/xmlschema-2/#dateTime-order).

`xsd:dateTime` datatype field mapping to accessors of this class are defined in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping).

| Parameters ||
|---|---|
| `xmlGregorianCalendar` | [XMLGregorianCalendar](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#)!: Instance of `XMLGregorianCalendar` to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The relationship between `this` `XMLGregorianCalendar` and the specified `xmlGregorianCalendar` as `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#LESSER:kotlin.Int`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#EQUAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GREATER:kotlin.Int` or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#INDETERMINATE:kotlin.Int`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `xmlGregorianCalendar` is null. |

### equals

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether parameter `obj` is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` when `obj` is an instance of `XMLGregorianCalendar` and `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#compare(javax.xml.datatype.XMLGregorianCalendar)` returns `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#EQUAL:kotlin.Int`, otherwise `false`. |

### getDay

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDay(): Int
```

Return day in month or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

<br />

Value constraints for this value are summarized in [day field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-day).
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setDay(kotlin.Int)`

### getEon

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEon(): BigInteger!
```

Return high order component for XML Schema 1.0 dateTime datatype field for `year`. `null` if this optional part of the year field is not defined.

Value constraints for this value are summarized in [year field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-year).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | eon of this `XMLGregorianCalendar`. The value returned is an integer multiple of 10\^9. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getYear()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()`

### getEonAndYear

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEonAndYear(): BigInteger!
```

Return XML Schema 1.0 dateTime datatype field for `year`.

Value constraints for this value are summarized in [year field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-year).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | sum of `eon` and `BigInteger.valueOf(year)` when both fields are defined. When only `year` is defined, return it. When both `eon` and `year` are not defined, return `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEon()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getYear()`

### getFractionalSecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFractionalSecond(): BigDecimal!
```

Return fractional seconds.

`null` is returned when this optional field is not defined.

Value constraints are detailed in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second).

This optional field can only have a defined value when the xs:dateTime second field, represented by `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()`, does not return `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!` | fractional seconds of this `XMLGregorianCalendar`. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.math.BigDecimal)`

### getHour

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getHour(): Int
```

Return hours or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. Returns `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` if this field is not defined.

Value constraints for this value are summarized in [hour field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-hour).
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getMillisecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMillisecond(): Int
```

Return millisecond precision of `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`.

This method represents a convenience accessor to infinite precision fractional second value returned by `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`. The returned value is the rounded down to milliseconds value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`. When `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()` returns `null`, this method must return `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

Value constraints for this value are summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Millisecond of this `XMLGregorianCalendar`. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getMinute

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMinute(): Int
```

Return minutes or .

<br />

Returns `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` if this field is not defined.

Value constraints for this value are summarized in [minute field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-minute).
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMonth(): Int
```

Return number of month or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

Value constraints for this value are summarized in [month field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-month).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | year of this `XMLGregorianCalendar`. |

### getSecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSecond(): Int
```

Return seconds or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

Returns `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` if this field is not defined. When this field is not defined, the optional xs:dateTime fractional seconds field, represented by `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()` and `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMillisecond()`, must not be defined.

Value constraints for this value are summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Second of this `XMLGregorianCalendar`. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMillisecond()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getTimeZone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTimeZone(defaultZoneoffset: Int): TimeZone!
```

Returns a `java.util.TimeZone` for this class.

If timezone field is defined for this instance, returns TimeZone initialized with custom timezone id of zoneoffset. If timezone field is undefined, try the defaultZoneoffset that was passed in. If defaultZoneoffset is FIELD_UNDEFINED, return default timezone for this host. (Same default as java.util.GregorianCalendar).

| Parameters ||
|---|---|
| `defaultZoneoffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): default zoneoffset if this zoneoffset is `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#!` | TimeZone for this. |

### getTimezone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTimezone(): Int
```

Return timezone offset in minutes or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` if this optional field is not defined.

Value constraints for this value are summarized in [timezone field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-timezone).
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTimezone(kotlin.Int)`

### getXMLSchemaType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getXMLSchemaType(): QName!
```

Return the name of the XML Schema date/time type that this instance maps to. Type is computed based on fields that are set.

| Required fields for XML Schema 1.0 Date/Time Datatypes. *(timezone is optional for all date/time datatypes)* |||||||
|---|---|---|---|---|---|---|
| Datatype | year | month | day | hour | minute | second |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DATETIME:javax.xml.namespace.QName` | X | X | X | X | X | X |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DATE:javax.xml.namespace.QName` | X | X | X | | | |
| --- | --- | --- | --- | --- | --- | --- |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#TIME:javax.xml.namespace.QName` | | | | X | X | X |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GYEARMONTH:javax.xml.namespace.QName` | X | X | | | | |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GMONTHDAY:javax.xml.namespace.QName` | | X | X | | | |
| --- | --- | --- | --- | --- | --- | --- |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GYEAR:javax.xml.namespace.QName` | X | | | | | |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GMONTH:javax.xml.namespace.QName` | | X | | | | |
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GDAY:javax.xml.namespace.QName` | | | X | | | |
| --- | --- | --- | --- | --- | --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#!` | One of the following class constants: `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DATETIME:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#TIME:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DATE:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GYEARMONTH:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GMONTHDAY:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GYEAR:javax.xml.namespace.QName`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GMONTH:javax.xml.namespace.QName` or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GDAY:javax.xml.namespace.QName`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the combination of set fields does not match one of the eight defined XML Schema builtin date/time datatypes. |

### getYear

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getYear(): Int
```

Return low order component for XML Schema 1.0 dateTime datatype field for `year` or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

Value constraints for this value are summarized in [year field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-year).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | year of this `XMLGregorianCalendar`. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEon()`
- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()`

### hashCode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code consistent with the definition of the equals method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | hash code of this object. |

### isValid

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isValid(): Boolean
```

Validate instance by `getXMLSchemaType()` constraints.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if data values are valid. |

### normalize

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun normalize(): XMLGregorianCalendar!
```

Normalize this instance to UTC.

2000-03-04T23:00:00+03:00 normalizes to 2000-03-04T20:00:00Z

Implements W3C XML Schema Part 2, Section 3.2.7.3 (A).

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#!` | `this` `XMLGregorianCalendar` normalized to UTC. |

### reset

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun reset(): Unit
```

Reset this `XMLGregorianCalendar` to its original values.

`XMLGregorianCalendar` is reset to the same values as when it was created with `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar()`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar(kotlin.String)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar(java.math.BigInteger,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.math.BigDecimal,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendar(java.util.GregorianCalendar)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendarDate(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendarTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendarTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.math.BigDecimal,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newXMLGregorianCalendarTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`.

`reset()` is designed to allow the reuse of existing `XMLGregorianCalendar`s thus saving resources associated with the creation of new `XMLGregorianCalendar`s.

### setDay

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setDay(day: Int): Unit
```

Set days in month.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [day field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-day). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `day` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setFractionalSecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setFractionalSecond(fractional: BigDecimal!): Unit
```

Set fractional seconds.

Unset this field by invoking the setter with a parameter value of `null`.

| Parameters ||
|---|---|
| `fractional` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!: value constraints summarized in [fractional field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-fractional). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `fractional` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setHour

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setHour(hour: Int): Unit
```

Set hours.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [hour field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-hour). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `hour` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setMillisecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setMillisecond(millisecond: Int): Unit
```

Set milliseconds.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `millisecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [millisecond field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-millisecond). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `millisecond` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setMinute

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setMinute(minute: Int): Unit
```

Set minutes.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [minute field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-minute). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `minute` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setMonth(month: Int): Unit
```

Set month.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [month field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-month). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `month` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setSecond

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSecond(second: Int): Unit
```

Set seconds.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `second` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTime(
    hour: Int, 
    minute: Int, 
    second: Int
): Unit
```

Set time as one unit.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [hour field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-hour). |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [minute field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-minute). |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second). |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#setTime(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.math.BigDecimal)`

### setTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTime(
    hour: Int, 
    minute: Int, 
    second: Int, 
    millisecond: Int
): Unit
```

Set time as one unit, including optional milliseconds.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [hour field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-hour). |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [minute field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-minute). |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second). |
| --- | --- |
| `millisecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int` indicates this optional field is not set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTime(
    hour: Int, 
    minute: Int, 
    second: Int, 
    fractional: BigDecimal!
): Unit
```

Set time as one unit, including the optional infinite precision fractional seconds.

| Parameters ||
|---|---|
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [hour field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-hour). |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [minute field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-minute). |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [second field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-second). |
| --- | --- |
| `fractional` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!: value of `null` indicates this optional field is not set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setTimezone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setTimezone(offset: Int): Unit
```

Set the number of minutes in the timezone offset.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints summarized in [timezone field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-timezone). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `offset` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### setYear

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setYear(year: Int): Unit
```

Set year of XSD `dateTime` year field.

Unset this field by invoking the setter with a parameter value of `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`.

Note: if the absolute value of the `year` parameter is less than 10\^9, the eon component of the XSD year field is set to `null` by this method.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value constraints are summarized in [year field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-year). If year is `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#FIELD_UNDEFINED:kotlin.Int`, then eon is set to `null`. |

### setYear

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setYear(year: BigInteger!): Unit
```

Set low and high order component of XSD `dateTime` year field.

Unset this field by invoking the setter with a parameter value of `null`.

| Parameters ||
|---|---|
| `year` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!: value constraints summarized in [year field of date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefield-year). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `year` parameter is outside value constraints for the field as specified in [date/time field mapping table](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#datetimefieldmapping). |

### toGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toGregorianCalendar(): GregorianCalendar!
```

Convert this `XMLGregorianCalendar` to a `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#`.

When `this` instance has an undefined field, this conversion relies on the `java.util.GregorianCalendar` default for its corresponding field. A notable difference between XML Schema 1.0 date/time datatypes and `java.util.GregorianCalendar` is that Timezone value is optional for date/time datatypes and it is a required field for `java.util.GregorianCalendar`. See javadoc for `java.util.TimeZone.getDefault()` on how the default is determined. To explicitly specify the `TimeZone` instance, see `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toGregorianCalendar(java.util.TimeZone,%20java.util.Locale,%20javax.xml.datatype.XMLGregorianCalendar)`.

| Field by Field Conversion from this class to `java.util.GregorianCalendar` ||
|---|---|
| `java.util.GregorianCalendar` field | `javax.xml.datatype.XMLGregorianCalendar` field |
| `ERA` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()``.signum() < 0 ? GregorianCalendar.BC : GregorianCalendar.AD` |
| `YEAR` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getEonAndYear()``.abs().intValue()`*\** |
| --- | --- |
| `MONTH` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMonth()` - `https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#JANUARY:kotlin.Int` + `https://developer.android.com/reference/kotlin/java/util/Calendar.html#JANUARY:kotlin.Int` |
| `DAY_OF_MONTH` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getDay()` |
| `HOUR_OF_DAY` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getHour()` |
| --- | --- |
| `MINUTE` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getMinute()` |
| `SECOND` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getSecond()` |
| `MILLISECOND` | get millisecond order from `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getFractionalSecond()`*\** |
| --- | --- |
| `GregorianCalendar.setTimeZone(TimeZone)` | `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getTimezone()` formatted into Custom timezone id |

*\** designates possible loss of precision during the conversion due to source datatype having higher precision than target datatype.

To ensure consistency in conversion implementations, the new `GregorianCalendar` should be instantiated in following manner.

- Using `timeZone` value as defined above, create a new `java.util.GregorianCalendar(timeZone,Locale.getDefault())`.
- Initialize all GregorianCalendar fields by calling {(@link GegorianCalendar#clear()}.
- Obtain a pure Gregorian Calendar by invoking `GregorianCalendar.setGregorianChange( new Date(Long.MIN_VALUE))`.
- Its fields ERA, YEAR, MONTH, DAY_OF_MONTH, HOUR_OF_DAY, MINUTE, SECOND and MILLISECOND are set using the method `Calendar.set(int,int)`

<br />

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toGregorianCalendar(java.util.TimeZone,%20java.util.Locale,%20javax.xml.datatype.XMLGregorianCalendar)`

### toGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toGregorianCalendar(
    timezone: TimeZone!, 
    aLocale: Locale!, 
    defaults: XMLGregorianCalendar!
): GregorianCalendar!
```

Convert this `XMLGregorianCalendar` along with provided parameters to a `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#` instance.

Since XML Schema 1.0 date/time datetypes has no concept of timezone ids or daylight savings timezone ids, this conversion operation allows the user to explicitly specify one with `timezone` parameter.

To compute the return value's `TimeZone` field,

- when parameter `timeZone` is non-null, it is the timezone field.
- else when `this.getTimezone() != FIELD_UNDEFINED`, create a `java.util.TimeZone` with a custom timezone id using the `this.getTimezone()`.
- else when `defaults.getTimezone() != FIELD_UNDEFINED`, create a `java.util.TimeZone` with a custom timezone id using `defaults.getTimezone()`.
- else use the `GregorianCalendar` default timezone value for the host is defined as specified by `java.util.TimeZone.getDefault()`.

<br />

To ensure consistency in conversion implementations, the new `GregorianCalendar` should be instantiated in following manner.

- Create a new `java.util.GregorianCalendar(TimeZone, Locale)` with TimeZone set as specified above and the `Locale` parameter.
- Initialize all GregorianCalendar fields by calling `https://developer.android.com/reference/kotlin/java/util/Calendar.html#clear()`
- Obtain a pure Gregorian Calendar by invoking `GregorianCalendar.setGregorianChange( new Date(Long.MIN_VALUE))`.
- Its fields ERA, YEAR, MONTH, DAY_OF_MONTH, HOUR_OF_DAY, MINUTE, SECOND and MILLISECOND are set using the method `Calendar.set(int,int)`

<br />

| Parameters ||
|---|---|
| `timezone` | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#)!: provide Timezone. `null` is a legal value. |
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: provide explicit Locale. Use default GregorianCalendar locale if value is `null`. |
| `defaults` | [XMLGregorianCalendar](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#)!: provide default field values to use when corresponding field for this instance is FIELD_UNDEFINED or null. If `defaults`is `null` or a field within the specified `defaults` is undefined, just use `java.util.GregorianCalendar` defaults. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#!` | a java.util.GregorianCalendar conversion of this instance. |

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a `String` representation of this `XMLGregorianCalendar` `Object`.

The result is a lexical representation generated by `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toXMLFormat()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A non-`null` valid `String` representation of this `XMLGregorianCalendar`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the combination of set fields does not match one of the eight defined XML Schema builtin date/time datatypes. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#toXMLFormat()`

### toXMLFormat

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toXMLFormat(): String!
```

Return the lexical representation of `this` instance. The format is specified in [XML Schema 1.0 Part 2, Section 3.2.\[7-14\].1, *Lexical Representation*".](http://www.w3.org/TR/xmlschema-2/#dateTime-order)

Specific target lexical representation format is determined by `https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#getXMLSchemaType()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | XML, as `String`, representation of this `XMLGregorianCalendar` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the combination of set fields does not match one of the eight defined XML Schema builtin date/time datatypes. |
