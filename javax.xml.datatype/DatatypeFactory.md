# DatatypeFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatatypeFactory

```
abstract class DatatypeFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.datatype.DatatypeFactory](DatatypeFactory.md) |

Factory that creates new`javax.xml.datatype``Object`s that map XML to/from Java`Object`s.

[newInstance()](DatatypeFactory.md))is used to create a new`DatatypeFactory`. The following implementation resolution mechanisms are used in the following order:

1. If the system property specified by [DATATYPEFACTORY_PROPERTY](DatatypeFactory.md), "`javax.xml.datatype.DatatypeFactory`", exists, a class with the name of the property's value is instantiated. Any Exception thrown during the instantiation process is wrapped as a [DatatypeConfigurationException](DatatypeConfigurationException.md).
2. If the file ${JAVA_HOME}/lib/jaxp.properties exists, it is loaded in a [java.util.Properties](../java.util/Properties.md)`Object`. The`Properties``Object `is then queried for the property as documented in the prior step and processed as documented in the prior step.
3. The services resolution mechanism is used, e.g.`META-INF/services/java.xml.datatype.DatatypeFactory`. Any Exception thrown during the instantiation process is wrapped as a [DatatypeConfigurationException](DatatypeConfigurationException.md).
4. The final mechanism is to attempt to instantiate the`Class`specified by [DATATYPEFACTORY_IMPLEMENTATION_CLASS](DatatypeFactory.md), "`javax.xml.datatype.DatatypeFactoryImpl`". Any Exception thrown during the instantiation process is wrapped as a [DatatypeConfigurationException](DatatypeConfigurationException.md).

Note that you must supply your own implementation (such as Xerces); Android does not ship with a default implementation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATATYPEFACTORY_PROPERTY](DatatypeFactory.md) Default property name as defined in JSR 206: Java(TM) API for XML Processing (JAXP) 1. |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DatatypeFactory](DatatypeFactory.md))`()` Protected constructor to prevent instantiation outside of package. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Duration](Duration.md)! | [newDuration](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `years:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `months:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `days:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtain a new instance of a`Duration`specifying the`Duration`as isPositive, years, months, days, hours, minutes, seconds. |
| abstract [Duration](Duration.md)! | [newDuration](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `years:` ` [BigInteger](../java.math/BigInteger.md)!`, `months:` ` [BigInteger](../java.math/BigInteger.md)!`, `days:` ` [BigInteger](../java.math/BigInteger.md)!`, `hours:` ` [BigInteger](../java.math/BigInteger.md)!`, `minutes:` ` [BigInteger](../java.math/BigInteger.md)!`, `seconds:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` Obtain a new instance of a`Duration`specifying the`Duration`as isPositive, years, months, days, hours, minutes, seconds. |
| abstract [Duration](Duration.md)! | [newDuration](DatatypeFactory.md))`(`lexicalRepresentation:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Obtain a new instance of a`Duration`specifying the`Duration`as its string representation, "PnYnMnDTnHnMnS", as defined in XML Schema 1. |
| --- | --- |
| abstract [Duration](Duration.md)! | [newDuration](DatatypeFactory.md))`(`durationInMilliSeconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Obtain a new instance of a`Duration`specifying the`Duration`as milliseconds. |
| open [Duration](Duration.md)! | [newDurationDayTime](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a`Duration`of type`xdt:dayTimeDuration`using the specified`day`,`hour`,`minute`and`second`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration). |
| open [Duration](Duration.md)! | [newDurationDayTime](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `day:` ` [BigInteger](../java.math/BigInteger.md)!`, `hour:` ` [BigInteger](../java.math/BigInteger.md)!`, `minute:` ` [BigInteger](../java.math/BigInteger.md)!`, `second:` ` [BigInteger](../java.math/BigInteger.md)!`)` Create a`Duration`of type`xdt:dayTimeDuration`using the specified`day`,`hour`,`minute`and`second`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration). |
| --- | --- |
| open [Duration](Duration.md)! | [newDurationDayTime](DatatypeFactory.md))`(`lexicalRepresentation:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a`Duration`of type`xdt:dayTimeDuration`by parsing its`String`representation, "*PnDTnHnMnS* ", [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration). |
| open [Duration](Duration.md)! | [newDurationDayTime](DatatypeFactory.md))`(`durationInMilliseconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a`Duration`of type`xdt:dayTimeDuration`using the specified milliseconds as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration). |
| open [Duration](Duration.md)! | [newDurationYearMonth](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a`Duration`of type`xdt:yearMonthDuration`using the specified`year`and`month`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthyDuration). |
| --- | --- |
| open [Duration](Duration.md)! | [newDurationYearMonth](DatatypeFactory.md))`(`isPositive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `year:` ` [BigInteger](../java.math/BigInteger.md)!`, `month:` ` [BigInteger](../java.math/BigInteger.md)!`)` Create a`Duration`of type`xdt:yearMonthDuration`using the specified`year`and`month`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthyDuration). |
| open [Duration](Duration.md)! | [newDurationYearMonth](DatatypeFactory.md))`(`lexicalRepresentation:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a`Duration`of type`xdt:yearMonthDuration`by parsing its`String`representation, "*PnYnM* ", [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthDuration). |
| open [Duration](Duration.md)! | [newDurationYearMonth](DatatypeFactory.md))`(`durationInMilliseconds:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Create a`Duration`of type`xdt:yearMonthDuration`using the specified milliseconds as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthDuration). |
| --- | --- |
| openstatic [DatatypeFactory](DatatypeFactory.md)! | [newInstance](DatatypeFactory.md))`()` Obtain a new instance of a`DatatypeFactory`. |
| openstatic [DatatypeFactory](DatatypeFactory.md)! | [newInstance](DatatypeFactory.md))`(`factoryClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` Returns an instance of the named implementation of`DatatypeFactory`. |
| abstract [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendar](DatatypeFactory.md))`()` Create a new instance of an`XMLGregorianCalendar`. |
| --- | --- |
| open [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendar](DatatypeFactory.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `millisecond:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor of value spaces that a`java.util.GregorianCalendar`instance would need to convert to an`XMLGregorianCalendar`instance. |
| abstract [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendar](DatatypeFactory.md))`(`lexicalRepresentation:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new XMLGregorianCalendar by parsing the String as a lexical representation. |
| abstract [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendar](DatatypeFactory.md))`(`year:` ` [BigInteger](../java.math/BigInteger.md)!`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fractionalSecond:` ` [BigDecimal](../java.math/BigDecimal.md)!`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor allowing for complete value spaces allowed by W3C XML Schema 1. |
| --- | --- |
| abstract [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendar](DatatypeFactory.md))`(`cal:` ` [GregorianCalendar](../java.util/GregorianCalendar.md)!`)` Create an`XMLGregorianCalendar`from a [GregorianCalendar](../java.util/GregorianCalendar.md). |
| open [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendarDate](DatatypeFactory.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Java representation of XML Schema builtin datatype`date`or`g*`. |
| open [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendarTime](DatatypeFactory.md))`(`hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Java instance of XML Schema builtin datatype`time`. |
| --- | --- |
| open [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendarTime](DatatypeFactory.md))`(`hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `milliseconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Java instance of XML Schema builtin datatype time. |
| open [XMLGregorianCalendar](XMLGregorianCalendar.md)! | [newXMLGregorianCalendarTime](DatatypeFactory.md))`(`hours:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minutes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `seconds:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fractionalSecond:` ` [BigDecimal](../java.math/BigDecimal.md)!`, `timezone:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Java instance of XML Schema builtin datatype time. |

| Properties ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [DATATYPEFACTORY_IMPLEMENTATION_CLASS](DatatypeFactory.md) Default implementation class name as defined in JSR 206: Java(TM) API for XML Processing (JAXP) 1. |

## Constants

### DATATYPEFACTORY_PROPERTY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATATYPEFACTORY_PROPERTY: String
```

Default property name as defined in JSR 206: Java(TM) API for XML Processing (JAXP) 1.3.

Default value is`javax.xml.datatype.DatatypeFactory`. 

 Value: "javax.xml.datatype.DatatypeFactory"

## Protected constructors

### DatatypeFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DatatypeFactory()
```

Protected constructor to prevent instantiation outside of package.

Use [newInstance()](DatatypeFactory.md))to create a`DatatypeFactory`.

## Public methods

### newDuration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDuration(
    isPositive: Boolean, 
    years: Int, 
    months: Int, 
    days: Int, 
    hours: Int, 
    minutes: Int, 
    seconds: Int
): Duration!
```

Obtain a new instance of a`Duration`specifying the`Duration`as isPositive, years, months, days, hours, minutes, seconds.

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |
| --- | --- |
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |
| --- | --- |
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of this`Duration` |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created from the specified values. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If values are not a valid representation of a`Duration`. |

**See Also**

- [#newDuration(
 * boolean isPositive,
 * BigInteger years,
 * BigInteger months,
 * BigInteger days,
 * BigInteger hours,
 * BigInteger minutes,
* BigDecimal seconds)](DatatypeFactory.md)) 

### newDuration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDuration(
    isPositive: Boolean, 
    years: BigInteger!, 
    months: BigInteger!, 
    days: BigInteger!, 
    hours: BigInteger!, 
    minutes: BigInteger!, 
    seconds: BigDecimal!
): Duration!
```

Obtain a new instance of a`Duration`specifying the`Duration`as isPositive, years, months, days, hours, minutes, seconds.

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

A`null`value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `years` | [BigInteger](../java.math/BigInteger.md)!:of this`Duration` |
| `months` | [BigInteger](../java.math/BigInteger.md)!:of this`Duration` |
| --- | --- |
| `days` | [BigInteger](../java.math/BigInteger.md)!:of this`Duration` |
| `hours` | [BigInteger](../java.math/BigInteger.md)!:of this`Duration` |
| `minutes` | [BigInteger](../java.math/BigInteger.md)!:of this`Duration` |
| --- | --- |
| `seconds` | [BigDecimal](../java.math/BigDecimal.md)!:of this`Duration` |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created from the specified values. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If values are not a valid representation of a`Duration`. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |

### newDuration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDuration(lexicalRepresentation: String!): Duration!
```

Obtain a new instance of a`Duration`specifying the`Duration`as its string representation, "PnYnMnDTnHnMnS", as defined in XML Schema 1.0 section 3.2.6.1.

XML Schema Part 2: Datatypes, 3.2.6 duration, defines`duration`as:
duration represents a duration of time. The value space of duration is a six-dimensional space where the coordinates designate the Gregorian year, month, day, hour, minute, and second components defined in Section 5.5.3.2 of \[ISO 8601\], respectively. These components are ordered in their significance by their order of appearance i.e. as year, month, day, hour, minute, and second.

All six values are set and available from the created [Duration](Duration.md)

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `lexicalRepresentation` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:`String`representation of a`Duration`. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created from parsing the`lexicalRepresentation`. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If`lexicalRepresentation`is not a valid representation of a`Duration`. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |
| `java.lang.NullPointerException` | if`lexicalRepresentation`is`null`. |
| --- | --- |

### newDuration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDuration(durationInMilliSeconds: Long): Duration!
```

Obtain a new instance of a`Duration`specifying the`Duration`as milliseconds.

XML Schema Part 2: Datatypes, 3.2.6 duration, defines`duration`as:
duration represents a duration of time. The value space of duration is a six-dimensional space where the coordinates designate the Gregorian year, month, day, hour, minute, and second components defined in Section 5.5.3.2 of \[ISO 8601\], respectively. These components are ordered in their significance by their order of appearance i.e. as year, month, day, hour, minute, and second.

All six values are set by computing their values from the specified milliseconds and are available using the`get`methods of the created [Duration](Duration.md). The values conform to and are defined by:

- ISO 8601:2000(E) Section 5.5.3.2 Alternative format
- [W3C XML Schema 1.0 Part 2, Appendix D, ISO 8601 Date and Time Formats](http://www.w3.org/TR/xmlschema-2/#isoformats)
- [XMLGregorianCalendar](XMLGregorianCalendar.md) Date/Time Datatype Field Mapping Between XML Schema 1.0 and Java Representation

The default start instance is defined by [GregorianCalendar](../java.util/GregorianCalendar.md)'s use of the start of the epoch: i.e., [java.util.Calendar#YEAR](../java.util/Calendar.md)= 1970, [java.util.Calendar#MONTH](../java.util/Calendar.md)= [java.util.Calendar#JANUARY](../java.util/Calendar.md), [java.util.Calendar#DATE](../java.util/Calendar.md)= 1, etc. This is important as there are variations in the Gregorian Calendar, e.g. leap years have different days in the month = [java.util.Calendar#FEBRUARY](../java.util/Calendar.md) so the result of [Duration.getMonths()](Duration.md))and [Duration.getDays()](Duration.md))can be influenced.

| Parameters ||
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| `durationInMilliSeconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Duration in milliseconds to create. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`representing`durationInMilliSeconds`. |

### newDurationDayTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationDayTime(
    isPositive: Boolean, 
    day: Int, 
    hour: Int, 
    minute: Int, 
    second: Int
): Duration!
```

Create a`Duration`of type`xdt:dayTimeDuration`using the specified`day`,`hour`,`minute`and`second`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration).

The datatype`xdt:dayTimeDuration`is a subtype of`xs:duration`whose lexical representation contains only day, hour, minute, and second components. This datatype resides in the namespace`http://www.w3.org/2003/11/xpath-datatypes`.

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Day of`Duration`. |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Hour of`Duration`. |
| --- | --- |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Minute of`Duration`. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Second of`Duration`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created with the specified`day`,`hour`,`minute`and`second`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any values would create an invalid`Duration`. |

### newDurationDayTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationDayTime(
    isPositive: Boolean, 
    day: BigInteger!, 
    hour: BigInteger!, 
    minute: BigInteger!, 
    second: BigInteger!
): Duration!
```

Create a`Duration`of type`xdt:dayTimeDuration`using the specified`day`,`hour`,`minute`and`second`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration).

The datatype`xdt:dayTimeDuration`is a subtype of`xs:duration`whose lexical representation contains only day, hour, minute, and second components. This datatype resides in the namespace`http://www.w3.org/2003/11/xpath-datatypes`.

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

A`null`value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `day` | [BigInteger](../java.math/BigInteger.md)!:Day of`Duration`. |
| `hour` | [BigInteger](../java.math/BigInteger.md)!:Hour of`Duration`. |
| --- | --- |
| `minute` | [BigInteger](../java.math/BigInteger.md)!:Minute of`Duration`. |
| `second` | [BigInteger](../java.math/BigInteger.md)!:Second of`Duration`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created with the specified`day`,`hour`,`minute`and`second`. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any values would create an invalid`Duration`. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |

### newDurationDayTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationDayTime(lexicalRepresentation: String!): Duration!
```

Create a`Duration`of type`xdt:dayTimeDuration`by parsing its`String`representation, "*PnDTnHnMnS* ", [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration).

The datatype`xdt:dayTimeDuration`is a subtype of`xs:duration`whose lexical representation contains only day, hour, minute, and second components. This datatype resides in the namespace`http://www.w3.org/2003/11/xpath-datatypes`.

All four values are set and available from the created [Duration](Duration.md)

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `lexicalRepresentation` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Lexical representation of a duration. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created using the specified`lexicalRepresentation`. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given string does not conform to the aforementioned specification. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |
| `java.lang.NullPointerException` | If`lexicalRepresentation`is`null`. |
| --- | --- |

### newDurationDayTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationDayTime(durationInMilliseconds: Long): Duration!
```

Create a`Duration`of type`xdt:dayTimeDuration`using the specified milliseconds as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:dayTimeDuration](http://www.w3.org/TR/xpath-datamodel#dt-dayTimeDuration).

The datatype`xdt:dayTimeDuration`is a subtype of`xs:duration`whose lexical representation contains only day, hour, minute, and second components. This datatype resides in the namespace`http://www.w3.org/2003/11/xpath-datatypes`.

All four values are set by computing their values from the specified milliseconds and are available using the`get`methods of the created [Duration](Duration.md). The values conform to and are defined by:

- ISO 8601:2000(E) Section 5.5.3.2 Alternative format
- [W3C XML Schema 1.0 Part 2, Appendix D, ISO 8601 Date and Time Formats](http://www.w3.org/TR/xmlschema-2/#isoformats)
- [XMLGregorianCalendar](XMLGregorianCalendar.md) Date/Time Datatype Field Mapping Between XML Schema 1.0 and Java Representation

The default start instance is defined by [GregorianCalendar](../java.util/GregorianCalendar.md)'s use of the start of the epoch: i.e., [java.util.Calendar#YEAR](../java.util/Calendar.md)= 1970, [java.util.Calendar#MONTH](../java.util/Calendar.md)= [java.util.Calendar#JANUARY](../java.util/Calendar.md), [java.util.Calendar#DATE](../java.util/Calendar.md)= 1, etc. This is important as there are variations in the Gregorian Calendar, e.g. leap years have different days in the month = [java.util.Calendar#FEBRUARY](../java.util/Calendar.md) so the result of [Duration.getDays()](Duration.md))can be influenced.

Any remaining milliseconds after determining the day, hour, minute and second are discarded.

| Parameters ||
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| `durationInMilliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Milliseconds of`Duration`to create. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created with the specified`durationInMilliseconds`. |

**See Also**

### newDurationYearMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationYearMonth(
    isPositive: Boolean, 
    year: Int, 
    month: Int
): Duration!
```

Create a`Duration`of type`xdt:yearMonthDuration`using the specified`year`and`month`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthyDuration).

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Year of`Duration`. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Month of`Duration`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created using the specified`year`and`month`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any values would create an invalid`Duration`. |

### newDurationYearMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationYearMonth(
    isPositive: Boolean, 
    year: BigInteger!, 
    month: BigInteger!
): Duration!
```

Create a`Duration`of type`xdt:yearMonthDuration`using the specified`year`and`month`as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthyDuration).

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

A`null`value indicates that field is not set.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isPositive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to`false`to create a negative duration. When the length of the duration is zero, this parameter will be ignored. |
| `year` | [BigInteger](../java.math/BigInteger.md)!:Year of`Duration`. |
| `month` | [BigInteger](../java.math/BigInteger.md)!:Month of`Duration`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created using the specified`year`and`month`. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any values would create an invalid`Duration`. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |

### newDurationYearMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationYearMonth(lexicalRepresentation: String!): Duration!
```

Create a`Duration`of type`xdt:yearMonthDuration`by parsing its`String`representation, "*PnYnM* ", [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthDuration).

The datatype`xdt:yearMonthDuration`is a subtype of`xs:duration`whose lexical representation contains only year and month components. This datatype resides in the namespace [javax.xml.XMLConstants#W3C_XPATH_DATATYPE_NS_URI](../javax.xml/XMLConstants.md).

Both values are set and available from the created [Duration](Duration.md)

The XML Schema specification states that values can be of an arbitrary size. Implementations may chose not to or be incapable of supporting arbitrarily large and/or small values. An [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md) will be thrown with a message indicating implementation limits if implementation capacities are exceeded.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `lexicalRepresentation` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Lexical representation of a duration. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created using the specified`lexicalRepresentation`. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the`lexicalRepresentation`does not conform to the specification. |
| `java.lang.UnsupportedOperationException` | If implementation cannot support requested values. |
| `java.lang.NullPointerException` | If`lexicalRepresentation`is`null`. |
| --- | --- |

### newDurationYearMonth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newDurationYearMonth(durationInMilliseconds: Long): Duration!
```

Create a`Duration`of type`xdt:yearMonthDuration`using the specified milliseconds as defined in [XQuery 1.0 and XPath 2.0 Data Model, xdt:yearMonthDuration](http://www.w3.org/TR/xpath-datamodel#dt-yearMonthDuration).

The datatype`xdt:yearMonthDuration`is a subtype of`xs:duration`whose lexical representation contains only year and month components. This datatype resides in the namespace [javax.xml.XMLConstants#W3C_XPATH_DATATYPE_NS_URI](../javax.xml/XMLConstants.md).

Both values are set by computing their values from the specified milliseconds and are available using the`get`methods of the created [Duration](Duration.md). The values conform to and are defined by:

- ISO 8601:2000(E) Section 5.5.3.2 Alternative format
- [W3C XML Schema 1.0 Part 2, Appendix D, ISO 8601 Date and Time Formats](http://www.w3.org/TR/xmlschema-2/#isoformats)
- [XMLGregorianCalendar](XMLGregorianCalendar.md) Date/Time Datatype Field Mapping Between XML Schema 1.0 and Java Representation

The default start instance is defined by [GregorianCalendar](../java.util/GregorianCalendar.md)'s use of the start of the epoch: i.e., [java.util.Calendar#YEAR](../java.util/Calendar.md)= 1970, [java.util.Calendar#MONTH](../java.util/Calendar.md)= [java.util.Calendar#JANUARY](../java.util/Calendar.md), [java.util.Calendar#DATE](../java.util/Calendar.md)= 1, etc. This is important as there are variations in the Gregorian Calendar, e.g. leap years have different days in the month = [java.util.Calendar#FEBRUARY](../java.util/Calendar.md) so the result of [Duration.getMonths()](Duration.md))can be influenced.

Any remaining milliseconds after determining the year and month are discarded.

| Parameters ||
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| `durationInMilliseconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Milliseconds of`Duration`to create. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Duration](Duration.md)! | New`Duration`created using the specified`durationInMilliseconds`. |

### newInstance

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): DatatypeFactory!
```

Obtain a new instance of a`DatatypeFactory`.

The implementation resolution mechanisms are [defined](DatatypeFactory.md) in this`Class`'s documentation.

Note that you must supply your own implementation (such as Xerces); Android does not ship with a default implementation.

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [DatatypeFactory](DatatypeFactory.md)! | New instance of a`DocumentBuilderFactory` |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------|
| `javax.xml.datatype.DatatypeConfigurationException` | If the implementation is not available or cannot be instantiated. |

### newInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    factoryClassName: String!, 
    classLoader: ClassLoader!
): DatatypeFactory!
```

Returns an instance of the named implementation of`DatatypeFactory`.

| Exceptions ||
|-----------------------------------------------------|-----------------------------------------------------------------|
| `javax.xml.datatype.DatatypeConfigurationException` | if`factoryClassName`is not available or cannot be instantiated. |

### newXMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLGregorianCalendar(): XMLGregorianCalendar!
```

Create a new instance of an`XMLGregorianCalendar`.

All date/time datatype fields set to [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) or null.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | New`XMLGregorianCalendar`with all date/time datatype fields set to [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) or null. |

### newXMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newXMLGregorianCalendar(
    year: Int, 
    month: Int, 
    day: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    millisecond: Int, 
    timezone: Int
): XMLGregorianCalendar!
```

Constructor of value spaces that a`java.util.GregorianCalendar`instance would need to convert to an`XMLGregorianCalendar`instance.

`XMLGregorianCalendar eon`and`fractionalSecond`are set to`null`

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| --- | --- |
| `millisecond` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from specified values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

### newXMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLGregorianCalendar(lexicalRepresentation: String!): XMLGregorianCalendar!
```

Create a new XMLGregorianCalendar by parsing the String as a lexical representation.

Parsing the lexical string representation is defined in[XML Schema 1.0 Part 2, Section 3.2.\[7-14\].1,*Lexical Representation*.](http://www.w3.org/TR/xmlschema-2/#dateTime-order)

The string representation may not have any leading and trailing whitespaces.

The parsing is done field by field so that the following holds for any lexically correct String x: 

```kotlin
newXMLGregorianCalendar(x).toXMLFormat().equals(x)
  
```

Except for the noted lexical/canonical representation mismatches listed in [XML Schema 1.0 errata, Section 3.2.7.2](http://www.w3.org/2001/05/xmlschema-errata#e2-45).

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lexicalRepresentation` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Lexical representation of one the eight XML Schema date/time datatypes. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from the`lexicalRepresentation`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the`lexicalRepresentation`is not a valid`XMLGregorianCalendar`. |
| `java.lang.NullPointerException` | If`lexicalRepresentation`is`null`. |

### newXMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLGregorianCalendar(
    year: BigInteger!, 
    month: Int, 
    day: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    fractionalSecond: BigDecimal!, 
    timezone: Int
): XMLGregorianCalendar!
```

Constructor allowing for complete value spaces allowed by W3C XML Schema 1.0 recommendation for xsd:dateTime and related builtin datatypes. Note that`year`parameter supports arbitrarily large numbers and fractionalSecond has infinite precision.

A`null`value indicates that field is not set.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `year` | [BigInteger](../java.math/BigInteger.md)!:of`XMLGregorianCalendar`to be created. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| --- | --- |
| `fractionalSecond` | [BigDecimal](../java.math/BigDecimal.md)!:of`XMLGregorianCalendar`to be created. |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from specified values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

### newXMLGregorianCalendar

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newXMLGregorianCalendar(cal: GregorianCalendar!): XMLGregorianCalendar!
```

Create an`XMLGregorianCalendar`from a [GregorianCalendar](../java.util/GregorianCalendar.md).

| Field by Field Conversion from [GregorianCalendar](../java.util/GregorianCalendar.md) to an [XMLGregorianCalendar](XMLGregorianCalendar.md) ||
| --- | --- |
| `java.util.GregorianCalendar`field | `javax.xml.datatype.XMLGregorianCalendar`field |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ERA == GregorianCalendar.BC ? -YEAR : YEAR` | [XMLGregorianCalendar.setYear(int year)](XMLGregorianCalendar.md)) |
| `MONTH + 1` | [XMLGregorianCalendar.setMonth(int month)](XMLGregorianCalendar.md)) |
| `DAY_OF_MONTH` | [XMLGregorianCalendar.setDay(int day)](XMLGregorianCalendar.md)) |
| --- | --- |
| `HOUR_OF_DAY, MINUTE, SECOND, MILLISECOND` | [XMLGregorianCalendar.setTime(int hour, int minute, int second, BigDecimal fractional)](XMLGregorianCalendar.md)) |
| `(ZONE_OFFSET + DST_OFFSET) / (60*1000)` *(in minutes)* | [XMLGregorianCalendar.setTimezone(int offset)](XMLGregorianCalendar.md))*\** |

*\** conversion loss of information. It is not possible to represent a`java.util.GregorianCalendar`daylight savings timezone id in the XML Schema 1.0 date/time datatype representation.

To compute the return value's`TimeZone`field,

- when`this.getTimezone() != FIELD_UNDEFINED`, create a`java.util.TimeZone`with a custom timezone id using the`this.getTimezone()`.
- else use the`GregorianCalendar`default timezone value for the host is defined as specified by`java.util.TimeZone.getDefault()`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cal` | [GregorianCalendar](../java.util/GregorianCalendar.md)!:`java.util.GregorianCalendar`used to create`XMLGregorianCalendar` |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from`java.util.GregorianCalendar` |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If`cal`is`null`. |

### newXMLGregorianCalendarDate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newXMLGregorianCalendarDate(
    year: Int, 
    month: Int, 
    day: Int, 
    timezone: Int
): XMLGregorianCalendar!
```

Create a Java representation of XML Schema builtin datatype`date`or`g*`.

For example, an instance of`gYear`can be created invoking this factory with`month`and`day`parameters set to [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md).

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of`XMLGregorianCalendar`to be created. |
| --- | --- |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset in minutes. [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) indicates optional field is not set. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from parameter values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

**See Also**

- [javax.xml.datatype.DatatypeConstants#FIELD_UNDEFINED](DatatypeConstants.md) 

### newXMLGregorianCalendarTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newXMLGregorianCalendarTime(
    hours: Int, 
    minutes: Int, 
    seconds: Int, 
    timezone: Int
): XMLGregorianCalendar!
```

Create a Java instance of XML Schema builtin datatype`time`.

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of hours |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of minutes |
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of seconds |
| --- | --- |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset in minutes. [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) indicates optional field is not set. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from parameter values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

**See Also**

- [javax.xml.datatype.DatatypeConstants#FIELD_UNDEFINED](DatatypeConstants.md) 

### newXMLGregorianCalendarTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newXMLGregorianCalendarTime(
    hours: Int, 
    minutes: Int, 
    seconds: Int, 
    milliseconds: Int, 
    timezone: Int
): XMLGregorianCalendar!
```

Create a Java instance of XML Schema builtin datatype time.

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of hours |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of minutes |
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of seconds |
| --- | --- |
| `milliseconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of milliseconds |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset in minutes. [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) indicates optional field is not set. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from parameter values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

**See Also**

- [javax.xml.datatype.DatatypeConstants#FIELD_UNDEFINED](DatatypeConstants.md) 

### newXMLGregorianCalendarTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newXMLGregorianCalendarTime(
    hours: Int, 
    minutes: Int, 
    seconds: Int, 
    fractionalSecond: BigDecimal!, 
    timezone: Int
): XMLGregorianCalendar!
```

Create a Java instance of XML Schema builtin datatype time.

A`null`value indicates that field is not set.

A [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) value indicates that field is not set.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of hours |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of minutes |
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of seconds |
| --- | --- |
| `fractionalSecond` | [BigDecimal](../java.math/BigDecimal.md)!:value of`null`indicates that this optional field is not set. |
| `timezone` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset in minutes. [DatatypeConstants.FIELD_UNDEFINED](DatatypeConstants.md) indicates optional field is not set. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [XMLGregorianCalendar](XMLGregorianCalendar.md)! | `XMLGregorianCalendar`created from parameter values. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If any individual parameter's value is outside the maximum value constraint for the field as determined by the Date/Time Data Mapping table in [XMLGregorianCalendar](XMLGregorianCalendar.md) or if the composite values constitute an invalid`XMLGregorianCalendar`instance as determined by [XMLGregorianCalendar.isValid()](XMLGregorianCalendar.md)). |

**See Also**

- [javax.xml.datatype.DatatypeConstants#FIELD_UNDEFINED](DatatypeConstants.md)

## Properties

### DATATYPEFACTORY_IMPLEMENTATION_CLASS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATATYPEFACTORY_IMPLEMENTATION_CLASS: String!
```

Default implementation class name as defined in JSR 206: Java(TM) API for XML Processing (JAXP) 1.3.

Default value is`org.apache.xerces.jaxp.datatype.DatatypeFactoryImpl`.
