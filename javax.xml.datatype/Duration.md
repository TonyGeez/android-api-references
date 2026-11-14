# Duration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Duration

```
abstract class Duration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.datatype.Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#) |

Immutable representation of a time span as defined in the W3C XML Schema 1.0 specification.

A Duration object represents a period of Gregorian time, which consists of six fields (years, months, days, hours, minutes, and seconds) plus a sign (+/-) field.

The first five fields have non-negative (\>=0) integers or null (which represents that the field is not set), and the seconds field has a non-negative decimal or null. A negative sign indicates a negative duration.

This class provides a number of methods that make it easy to use for the duration datatype of XML Schema 1.0 with the errata.

## Order relationship

Duration objects only have partial order, where two values A and B maybe either:

1. A\<B (A is shorter than B)
2. A\>B (A is longer than B)
3. A==B (A and B are of the same duration)
4. A\<\>B (Comparison between A and B is indeterminate)

For example, 30 days cannot be meaningfully compared to one month. The [compare(javax.xml.datatype.Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#compare(javax.xml.datatype.Duration))method implements this relationship.

See the [isLongerThan(javax.xml.datatype.Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isLongerThan(javax.xml.datatype.Duration))method for details about the order relationship among`Duration`objects.

## Operations over Duration

This class provides a set of basic arithmetic operations, such as addition, subtraction and multiplication. Because durations don't have total order, an operation could fail for some combinations of operations. For example, you cannot subtract 15 days from 1 month. See the javadoc of those methods for detailed conditions where this could happen.

Also, division of a duration by a number is not provided because the`Duration`class can only deal with finite precision decimal numbers. For example, one cannot represent 1 sec divided by 3.

However, you could substitute a division by 3 with multiplying by numbers such as 0.3 or 0.333.

## Range of allowed values

Because some operations of`Duration`rely on [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) even though [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#) can hold very large or very small values, some of the methods may not work correctly on such`Duration`s. The impacted methods document their dependency on [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#Duration())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [add](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#add(javax.xml.datatype.Duration))`(`rhs:` ` [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!`)` Computes a new duration whose value is`this+rhs`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTo](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Calendar))`(`calendar:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Adds this duration to a [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTo](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Adds this duration to a [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#compare(javax.xml.datatype.Duration))`(`duration:` ` [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!`)` Partial order relation comparison with this`Duration`instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this duration object has the same duration as another`Duration`object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDays](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getDays())`()` Obtains the value of the DAYS field as an integer value, or 0 if not present. |
| --- | --- |
| abstract [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getField](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getField(javax.xml.datatype.DatatypeConstants.Field))`(`field:` ` [DatatypeConstants.Field](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants.Field)!`)` Gets the value of a field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHours](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getHours())`()` Obtains the value of the HOURS field as an integer value, or 0 if not present. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinutes](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getMinutes())`()` Obtains the value of the MINUTES field as an integer value, or 0 if not present. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonths](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getMonths())`()` Obtains the value of the MONTHS field as an integer value, or 0 if not present. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSeconds](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getSeconds())`()` Obtains the value of the SECONDS field as an integer value, or 0 if not present. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSign](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getSign())`()` Returns the sign of this duration in -1,0, or 1. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeInMillis](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getTimeInMillis(java.util.Calendar))`(`startInstant:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Returns the length of the duration in milliseconds. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeInMillis](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getTimeInMillis(java.util.Date))`(`startInstant:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Returns the length of the duration in milliseconds. |
| open [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | [getXMLSchemaType](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getXMLSchemaType())`()` Return the name of the XML Schema date/time type that this instance maps to. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYears](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())`()` Get the years value of this`Duration`as an`int`or`0`if not present. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#hashCode())`()` Returns a hash code consistent with the definition of the equals method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLongerThan](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isLongerThan(javax.xml.datatype.Duration))`(`duration:` ` [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!`)` Checks if this duration object is strictly longer than another`Duration`object. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSet](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isSet(javax.xml.datatype.DatatypeConstants.Field))`(`field:` ` [DatatypeConstants.Field](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants.Field)!`)` Checks if a field is set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShorterThan](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isShorterThan(javax.xml.datatype.Duration))`(`duration:` ` [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!`)` Checks if this duration object is strictly shorter than another`Duration`object. |
| open [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [multiply](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#multiply(kotlin.Int))`(`factor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Computes a new duration whose value is`factor`times longer than the value of this duration. |
| --- | --- |
| abstract [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [multiply](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#multiply(java.math.BigDecimal))`(`factor:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Computes a new duration whose value is`factor`times longer than the value of this duration. |
| abstract [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [negate](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#negate())`()` Returns a new`Duration`object whose value is`-this`. |
| abstract [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [normalizeWith](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#normalizeWith(java.util.Calendar))`(`startTimeInstant:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!`)` Converts the years and months fields into the days field by using a specific time instant as the reference point. |
| --- | --- |
| open [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | [subtract](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#subtract(javax.xml.datatype.Duration))`(`rhs:` ` [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!`)` Computes a new duration whose value is`this-rhs`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#toString())`()` Returns a`String`representation of this`Duration``Object`. |

## Public constructors

### Duration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Duration()
```

## Public methods

### add

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(rhs: Duration!): Duration!
```

Computes a new duration whose value is`this+rhs`.

For example, 

```kotlin
"1 day" + "-3 days" = "-2 days"
  "1 year" + "1 day" = "1 year and 1 day"
  "-(1 hour,50 minutes)" + "-20 minutes" = "-(1 hours,70 minutes)"
  "15 hours" + "-3 days" = "-(2 days,9 hours)"
  "1 year" + "-1 day" = IllegalStateException
  
```

Since there's no way to meaningfully subtract 1 day from 1 month, there are cases where the operation fails in [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

Formally, the computation is defined as follows.

Firstly, we can assume that two`Duration`s to be added are both positive without losing generality (i.e.,`(-X)+Y=Y-X`,`X+(-Y)=X-Y`,`(-X)+(-Y)=-(X+Y)`)

Addition of two positive`Duration`s are simply defined as field by field addition where missing fields are treated as 0.

A field of the resulting`Duration`will be unset if and only if respective fields of two input`Duration`s are unset.

Note that`lhs.add(rhs)`will be always successful if`lhs.signum()*rhs.signum()!=-1`or both of them are normalized.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!:`Duration`to add to this`Duration` |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | non-null valid Duration object. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the rhs parameter is null. |
| `java.lang.IllegalStateException` | If two durations cannot be meaningfully added. For example, adding negative one day to one month causes this exception. |

**See Also**

- [#subtract(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#subtract(javax.xml.datatype.Duration)) 

### addTo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addTo(calendar: Calendar!): Unit
```

Adds this duration to a [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) object.

Calls [java.util.Calendar#add(int,int)](https://developer.android.com/reference/kotlin/java/util/Calendar.html#add(kotlin.Int,%20kotlin.Int))in the order of YEARS, MONTHS, DAYS, HOURS, MINUTES, SECONDS, and MILLISECONDS if those fields are present. Because the [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) class uses int to hold values, there are cases where this method won't work correctly (for example if values of fields exceed the range of int.)

Also, since this duration class is a Gregorian duration, this method will not work correctly if the given [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) object is based on some other calendar systems.

Any fractional parts of this`Duration`object beyond milliseconds will be simply ignored. For example, if this duration is "P1.23456S", then 1 is added to SECONDS, 234 is added to MILLISECONDS, and the rest will be unused.

Note that because [Calendar.add(int, int)](https://developer.android.com/reference/kotlin/java/util/Calendar.html#add(kotlin.Int,%20kotlin.Int))is using int,`Duration`with values beyond the range of int in its fields will cause overflow/underflow to the given [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#). [XMLGregorianCalendar.add(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/XMLGregorianCalendar#add(javax.xml.datatype.Duration))provides the same basic operation as this method while avoiding the overflow/underflow issues.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `calendar` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:A calendar object whose value will be modified. |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the calendar parameter is null. |

### addTo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTo(date: Date!): Unit
```

Adds this duration to a [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) object.

The given date is first converted into a [java.util.GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#), then the duration is added exactly like the [addTo(java.util.Calendar)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Calendar))method.

The updated time instant is then converted back into a [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) object and used to update the given [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#) object.

This somewhat redundant computation is necessary to unambiguously determine the duration of months and years.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:A date object whose value will be modified. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the date parameter is null. |

### compare

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compare(duration: Duration!): Int
```

Partial order relation comparison with this`Duration`instance.

Comparison result must be in accordance with [W3C XML Schema 1.0 Part 2, Section 3.2.7.6.2,*Order relation on duration*](http://www.w3.org/TR/xmlschema-2/#duration-order).

Return:

- [DatatypeConstants.LESSER](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#LESSER:kotlin.Int) if this`Duration`is shorter than`duration`parameter
- [DatatypeConstants.EQUAL](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#EQUAL:kotlin.Int) if this`Duration`is equal to`duration`parameter
- [DatatypeConstants.GREATER](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GREATER:kotlin.Int) if this`Duration`is longer than`duration`parameter
- [DatatypeConstants.INDETERMINATE](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#INDETERMINATE:kotlin.Int) if a conclusive partial order relation cannot be determined

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!:to compare |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the relationship between`this``Duration`and`duration`parameter as [DatatypeConstants.LESSER](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#LESSER:kotlin.Int), [DatatypeConstants.EQUAL](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#EQUAL:kotlin.Int), [DatatypeConstants.GREATER](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#GREATER:kotlin.Int) or [DatatypeConstants.INDETERMINATE](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#INDETERMINATE:kotlin.Int). |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the underlying implementation cannot reasonably process the request, e.g. W3C XML Schema allows for arbitrarily large/small/precise values, the request may be beyond the implementations capability. |
| `java.lang.NullPointerException` | if`duration`is`null`. |

**See Also**

- [#isShorterThan(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isShorterThan(javax.xml.datatype.Duration))
- [#isLongerThan(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isLongerThan(javax.xml.datatype.Duration)) 

### equals

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Checks if this duration object has the same duration as another`Duration`object.

For example, "P1D" (1 day) is equal to "PT24H" (24 hours).

Duration X is equal to Y if and only if time instant t+X and t+Y are the same for all the test time instants specified in the section 3.2.6.2 of the XML Schema 1.0 specification.

Note that there are cases where two`Duration`s are "incomparable" to each other, like one month and 30 days. For example, 

```kotlin
!new Duration("P1M").isShorterThan(new Duration("P30D"))
  !new Duration("P1M").isLongerThan(new Duration("P30D"))
  !new Duration("P1M").equals(new Duration("P30D"))
  
```

| Parameters ||
|------------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `duration` | A non-null valid`Duration`object. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this duration is the same length as`duration`.`false`if`duration`is not a`Duration`object, is`null`, or its length is different from this duration. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the underlying implementation cannot reasonably process the request, e.g. W3C XML Schema allows for arbitrarily large/small/precise values, the request may be beyond the implementations capability. |

**See Also**

- [#compare(Duration duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#compare(javax.xml.datatype.Duration)) 

### getDays

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDays(): Int
```

Obtains the value of the DAYS field as an integer value, or 0 if not present. This method works just like [getYears()](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())except that this method works on the DAYS field.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Days of this`Duration`. |

### getField

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getField(field: DatatypeConstants.Field!): Number!
```

Gets the value of a field. Fields of a duration object may contain arbitrary large value. Therefore this method is designed to return a [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) object. In case of YEARS, MONTHS, DAYS, HOURS, and MINUTES, the returned number will be a non-negative integer. In case of seconds, the returned number may be a non-negative decimal value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [DatatypeConstants.Field](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants.Field)!:one of the six Field constants (YEARS,MONTHS,DAYS,HOURS, MINUTES, or SECONDS.) |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | If the specified field is present, this method returns a non-null non-negative [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) object that represents its value. If it is not present, return null. For YEARS, MONTHS, DAYS, HOURS, and MINUTES, this method returns a [java.math.BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#) object. For SECONDS, this method returns a [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#). |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | If the`field`is`null`. |

### getHours

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHours(): Int
```

Obtains the value of the HOURS field as an integer value, or 0 if not present. This method works just like [getYears()](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())except that this method works on the HOURS field.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Hours of this`Duration`. |

### getMinutes

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinutes(): Int
```

Obtains the value of the MINUTES field as an integer value, or 0 if not present. This method works just like [getYears()](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())except that this method works on the MINUTES field.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Minutes of this`Duration`. |

### getMonths

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonths(): Int
```

Obtains the value of the MONTHS field as an integer value, or 0 if not present. This method works just like [getYears()](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())except that this method works on the MONTHS field.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Months of this`Duration`. |

### getSeconds

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSeconds(): Int
```

Obtains the value of the SECONDS field as an integer value, or 0 if not present. This method works just like [getYears()](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getYears())except that this method works on the SECONDS field.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | seconds in the integer value. The fraction of seconds will be discarded (for example, if the actual value is 2.5, this method returns 2) |

### getSign

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSign(): Int
```

Returns the sign of this duration in -1,0, or 1.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | -1 if this duration is negative, 0 if the duration is zero, and 1 if the duration is positive. |

### getTimeInMillis

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeInMillis(startInstant: Calendar!): Long
```

Returns the length of the duration in milliseconds.

If the seconds field carries more digits than millisecond order, those will be simply discarded (or in other words, rounded to zero.) For example, for any Calendar value`x`, 

```kotlin
<code>new Duration("PT10.00099S").getTimeInMills(x) == 10000</code>.
  <code>new Duration("-PT10.00099S").getTimeInMills(x) == -10000</code>.
  
```

Note that this method uses the [addTo(java.util.Calendar)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Calendar))method, which may work incorrectly with`Duration`objects with very large values in its fields. See the [addTo(java.util.Calendar)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Calendar))method for details.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startInstant` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:The length of a month/year varies. The`startInstant`is used to disambiguate this variance. Specifically, this method returns the difference between`startInstant`and`startInstant+duration` |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | milliseconds between`startInstant`and`startInstant`plus this`Duration` |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if`startInstant`parameter is null. |

### getTimeInMillis

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeInMillis(startInstant: Date!): Long
```

Returns the length of the duration in milliseconds.

If the seconds field carries more digits than millisecond order, those will be simply discarded (or in other words, rounded to zero.) For example, for any`Date`value`x`, 

```kotlin
<code>new Duration("PT10.00099S").getTimeInMills(x) == 10000</code>.
  <code>new Duration("-PT10.00099S").getTimeInMills(x) == -10000</code>.
  
```

Note that this method uses the [addTo(java.util.Date)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Date))method, which may work incorrectly with`Duration`objects with very large values in its fields. See the [addTo(java.util.Date)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#addTo(java.util.Date))method for details.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startInstant` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:The length of a month/year varies. The`startInstant`is used to disambiguate this variance. Specifically, this method returns the difference between`startInstant`and`startInstant+duration`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | milliseconds between`startInstant`and`startInstant`plus this`Duration` |

| Exceptions ||
|----------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | If the startInstant parameter is null. |

**See Also**

- [#getTimeInMillis(Calendar)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getTimeInMillis(java.util.Calendar)) 

### getXMLSchemaType

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getXMLSchemaType(): QName!
```

Return the name of the XML Schema date/time type that this instance maps to. Type is computed based on fields that are set, i.e. [isSet(javax.xml.datatype.DatatypeConstants.Field)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isSet(javax.xml.datatype.DatatypeConstants.Field))==`true`.

| Required fields for XML Schema 1.0 Date/Time Datatypes. *(timezone is optional for all date/time datatypes)* |||||||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|-------|-----|------|--------|--------|
| Datatype | year | month | day | hour | minute | second |
| [DatatypeConstants.DURATION](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION:javax.xml.namespace.QName) | X | X | X | X | X | X |
| [DatatypeConstants.DURATION_DAYTIME](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION_DAYTIME:javax.xml.namespace.QName) | | | X | X | X | X |
| --- | --- | --- | --- | --- | --- | --- |
| [DatatypeConstants.DURATION_YEARMONTH](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION_YEARMONTH:javax.xml.namespace.QName) | X | X | | | | |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [QName](https://developer.android.com/reference/kotlin/javax/xml/namespace/QName.html#)! | one of the following constants: [DatatypeConstants.DURATION](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION:javax.xml.namespace.QName), [DatatypeConstants.DURATION_DAYTIME](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION_DAYTIME:javax.xml.namespace.QName) or [DatatypeConstants.DURATION_YEARMONTH](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants#DURATION_YEARMONTH:javax.xml.namespace.QName). |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the combination of set fields does not match one of the XML Schema date/time datatypes. |

### getYears

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYears(): Int
```

Get the years value of this`Duration`as an`int`or`0`if not present.

`getYears()`is a convenience method for [getField(DatatypeConstants.YEARS)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getField(javax.xml.datatype.DatatypeConstants.Field)).

As the return value is an`int`, an incorrect value will be returned for`Duration`s with years that go beyond the range of an`int`. Use [getField(DatatypeConstants.YEARS)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#getField(javax.xml.datatype.DatatypeConstants.Field))to avoid possible loss of precision.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | If the years field is present, return its value as an`int`, else return`0`. |

### hashCode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hashCode(): Int
```

Returns a hash code consistent with the definition of the equals method.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

**See Also**

- [java.lang.Object#hashCode()](https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()) 

### isLongerThan

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLongerThan(duration: Duration!): Boolean
```

Checks if this duration object is strictly longer than another`Duration`object.

Duration X is "longer" than Y if and only if X\>Y as defined in the section 3.2.6.2 of the XML Schema 1.0 specification.

For example, "P1D" (one day) \> "PT12H" (12 hours) and "P2Y" (two years) \> "P23M" (23 months).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!:`Duration`to test this`Duration`against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the duration represented by this object is longer than the given duration. false otherwise. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the underlying implementation cannot reasonably process the request, e.g. W3C XML Schema allows for arbitrarily large/small/precise values, the request may be beyond the implementations capability. |
| `java.lang.NullPointerException` | If`duration`is null. |

**See Also**

- [#isShorterThan(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isShorterThan(javax.xml.datatype.Duration))
- [#compare(Duration duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#compare(javax.xml.datatype.Duration)) 

### isSet

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSet(field: DatatypeConstants.Field!): Boolean
```

Checks if a field is set. A field of a duration object may or may not be present. This method can be used to test if a field is present.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [DatatypeConstants.Field](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConstants.Field)!:one of the six Field constants (YEARS,MONTHS,DAYS,HOURS, MINUTES, or SECONDS.) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the field is present. false if not. |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | If the field parameter is null. |

### isShorterThan

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShorterThan(duration: Duration!): Boolean
```

Checks if this duration object is strictly shorter than another`Duration`object.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!:`Duration`to test this`Duration`against. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`duration`parameter is shorter than this`Duration`, else`false`. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the underlying implementation cannot reasonably process the request, e.g. W3C XML Schema allows for arbitrarily large/small/precise values, the request may be beyond the implementations capability. |
| `java.lang.NullPointerException` | if`duration`is null. |

**See Also**

- [#isLongerThan(Duration duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#isLongerThan(javax.xml.datatype.Duration))
- [#compare(Duration duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#compare(javax.xml.datatype.Duration)) 

### multiply

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(factor: Int): Duration!
```

Computes a new duration whose value is`factor`times longer than the value of this duration.

This method is provided for the convenience. It is functionally equivalent to the following code: 

```kotlin
multiply(new BigDecimal(String.valueOf(factor)))
  
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `factor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Factor times longer of new`Duration`to create. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | New`Duration`that is`factor`times longer than this`Duration`. |

**See Also**

- [#multiply(BigDecimal)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#multiply(java.math.BigDecimal)) 

### multiply

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun multiply(factor: BigDecimal!): Duration!
```

Computes a new duration whose value is`factor`times longer than the value of this duration.

For example, 

```kotlin
"P1M" (1 month) * "12" = "P12M" (12 months)
  "PT1M" (1 min) * "0.3" = "PT18S" (18 seconds)
  "P1M" (1 month) * "1.5" = IllegalStateException
  
```

Since the`Duration`class is immutable, this method doesn't change the value of this object. It simply computes a new Duration object and returns it.

The operation will be performed field by field with the precision of [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#). Since all the fields except seconds are restricted to hold integers, any fraction produced by the computation will be carried down toward the next lower unit. For example, if you multiply "P1D" (1 day) with "0.5", then it will be 0.5 day, which will be carried down to "PT12H" (12 hours). When fractions of month cannot be meaningfully carried down to days, or year to months, this will cause an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) to be thrown. For example if you multiple one month by 0.5.

To avoid [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#), use the [normalizeWith(java.util.Calendar)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#normalizeWith(java.util.Calendar))method to remove the years and months fields.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `factor` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!:to multiply by |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | returns a non-null valid`Duration`object |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------|
| `java.lang.IllegalStateException` | if operation produces fraction in the months field. |
| `java.lang.NullPointerException` | if the`factor`parameter is`null`. |

### negate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun negate(): Duration!
```

Returns a new`Duration`object whose value is`-this`.

Since the`Duration`class is immutable, this method doesn't change the value of this object. It simply computes a new Duration object and returns it.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | always return a non-null valid`Duration`object. |

### normalizeWith

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalizeWith(startTimeInstant: Calendar!): Duration!
```

Converts the years and months fields into the days field by using a specific time instant as the reference point.

For example, duration of one month normalizes to 31 days given the start time instance "July 8th 2003, 17:40:32".

Formally, the computation is done as follows:

1. the given Calendar object is cloned
2. the years, months and days fields will be added to the [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#) object by using the [Calendar.add(int,int)](https://developer.android.com/reference/kotlin/java/util/Calendar.html#add(kotlin.Int,%20kotlin.Int))method
3. the difference between the two Calendars in computed in milliseconds and converted to days, if a remainder occurs due to Daylight Savings Time, it is discarded
4. the computed days, along with the hours, minutes and seconds fields of this duration object is used to construct a new Duration object.

Note that since the Calendar class uses`int`to hold the value of year and month, this method may produce an unexpected result if this duration object holds a very large value in the years or months fields.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------|
| `startTimeInstant` | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#)!:`Calendar`reference point. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | `Duration`of years and months of this`Duration`as days. |

| Exceptions ||
|----------------------------------|--------------------------------------------|
| `java.lang.NullPointerException` | If the startTimeInstant parameter is null. |

### subtract

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subtract(rhs: Duration!): Duration!
```

Computes a new duration whose value is`this-rhs`.

For example: 

```kotlin
"1 day" - "-3 days" = "4 days"
  "1 year" - "1 day" = IllegalStateException
  "-(1 hour,50 minutes)" - "-20 minutes" = "-(1hours,30 minutes)"
  "15 hours" - "-3 days" = "3 days and 15 hours"
  "1 year" - "-1 day" = "1 year and 1 day"
  
```

Since there's no way to meaningfully subtract 1 day from 1 month, there are cases where the operation fails in [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

Formally the computation is defined as follows. First, we can assume that two`Duration`s are both positive without losing generality. (i.e.,`(-X)-Y=-(X+Y)`,`X-(-Y)=X+Y`,`(-X)-(-Y)=-(X-Y)`)

Then two durations are subtracted field by field. If the sign of any non-zero field F is different from the sign of the most significant field, 1 (if F is negative) or -1 (otherwise) will be borrowed from the next bigger unit of F.

This process is repeated until all the non-zero fields have the same sign.

If a borrow occurs in the days field (in other words, if the computation needs to borrow 1 or -1 month to compensate days), then the computation fails by throwing an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)!:`Duration`to subtract from this`Duration`. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Duration](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#)! | New`Duration`created from subtracting`rhs`from this`Duration`. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If two durations cannot be meaningfully subtracted. For example, subtracting one day from one month causes this exception. |
| `java.lang.NullPointerException` | If the rhs parameter is null. |

**See Also**

- [#add(Duration)](https://developer.android.com/reference/kotlin/javax/xml/datatype/Duration#add(javax.xml.datatype.Duration)) 

### toString

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a`String`representation of this`Duration``Object`.

The result is formatted according to the XML Schema 1.0 specification and can be always parsed back later into the equivalent`Duration``Object`by [DatatypeFactory.newDuration(String lexicalRepresentation)](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeFactory#newDuration(kotlin.String)).

Formally, the following holds for any`Duration``Object`x: 

```kotlin
new Duration(x.toString()).equals(x)
  
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A non-`null`valid`String`representation of this`Duration`. |
