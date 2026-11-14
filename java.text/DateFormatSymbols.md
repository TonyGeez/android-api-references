# DateFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateFormatSymbols

```
open class DateFormatSymbols : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.DateFormatSymbols](../java/text/DateFormatSymbols.md) |

`DateFormatSymbols`is a public class for encapsulating localizable date-time formatting data, such as the names of the months, the names of the days of the week, and the time zone data.`SimpleDateFormat`uses`DateFormatSymbols`to encapsulate this information.

Typically you shouldn't use`DateFormatSymbols`directly. Rather, you are encouraged to create a date-time formatter with the`DateFormat`class's factory methods:`getTimeInstance`,`getDateInstance`, or`getDateTimeInstance`. These methods automatically create a`DateFormatSymbols`for the formatter so that you don't have to. After the formatter is created, you may modify its format pattern using the`setPattern`method. For more information about creating formatters using`DateFormat`'s factory methods, see [DateFormat](../java/text/DateFormat.md).

If you decide to create a date-time formatter with a specific format pattern for a specific locale, you can do so with: 

```kotlin
new SimpleDateFormat(aPattern, DateFormatSymbols.getInstance(aLocale)).
  
```

`DateFormatSymbols`objects are cloneable. When you obtain a`DateFormatSymbols`object, feel free to modify the date-time formatting data. For instance, you can replace the localized date-time format pattern characters with the ones that you feel easy to remember. Or you can change the representative cities to your favorite ones.

New`DateFormatSymbols`subclasses may be added to support`SimpleDateFormat`for date-time formatting for additional locales.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateFormatSymbols](../java/text/DateFormatSymbols.md))`()` Construct a DateFormatSymbols object by loading format data from resources for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| [DateFormatSymbols](../java/text/DateFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Construct a DateFormatSymbols object by loading format data from resources for the given locale. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/DateFormatSymbols.md))`()` Overrides Cloneable |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/DateFormatSymbols.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Override equals |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAmPmStrings](../java/text/DateFormatSymbols.md))`()` Gets ampm strings. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../java/text/DateFormatSymbols.md))`()` Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEras](../java/text/DateFormatSymbols.md))`()` Gets era strings. |
| static [DateFormatSymbols](../java/text/DateFormatSymbols.md)! | [getInstance](../java/text/DateFormatSymbols.md))`()` Gets the`DateFormatSymbols`instance for the default locale. |
| --- | --- |
| static [DateFormatSymbols](../java/text/DateFormatSymbols.md)! | [getInstance](../java/text/DateFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Gets the`DateFormatSymbols`instance for the specified locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalPatternChars](../java/text/DateFormatSymbols.md))`()` Gets localized date-time pattern characters. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getMonths](../java/text/DateFormatSymbols.md))`()` Gets month strings. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getShortMonths](../java/text/DateFormatSymbols.md))`()` Gets short month strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getShortWeekdays](../java/text/DateFormatSymbols.md))`()` Gets short weekday strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getWeekdays](../java/text/DateFormatSymbols.md))`()` Gets weekday strings. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getZoneStrings](../java/text/DateFormatSymbols.md))`()` Gets time zone strings. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/text/DateFormatSymbols.md))`()` Override hashCode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAmPmStrings](../java/text/DateFormatSymbols.md))`(`newAmpms:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets ampm strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEras](../java/text/DateFormatSymbols.md))`(`newEras:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets era strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalPatternChars](../java/text/DateFormatSymbols.md))`(`newLocalPatternChars:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets localized date-time pattern characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonths](../java/text/DateFormatSymbols.md))`(`newMonths:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets month strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShortMonths](../java/text/DateFormatSymbols.md))`(`newShortMonths:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets short month strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShortWeekdays](../java/text/DateFormatSymbols.md))`(`newShortWeekdays:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets short weekday strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWeekdays](../java/text/DateFormatSymbols.md))`(`newWeekdays:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets weekday strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZoneStrings](../java/text/DateFormatSymbols.md))`(`newZoneStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` Sets time zone strings. |

## Public constructors

### DateFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols()
```

Construct a DateFormatSymbols object by loading format data from resources for the default [FORMAT](../java/util/Locale.Category.md) locale. It is recommended that the [getInstance](../java/text/DateFormatSymbols.md))method is used instead.

This is equivalent to calling [DateFormatSymbols(Locale.getDefault(Locale.Category.FORMAT))](../java/text/DateFormatSymbols.md)).

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resources for the default locale cannot be found or cannot be loaded. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols#getInstance()>
- [java.util.Locale#getDefault(java.util.Locale.Category)](../java/util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### DateFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(locale: Locale!)
```

Construct a DateFormatSymbols object by loading format data from resources for the given locale. It is recommended that the [getInstance](../java/text/DateFormatSymbols.md))method is used instead.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the desired locale |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resources for the specified locale cannot be found or cannot be loaded. |

**See Also**

- [#getInstance(Locale)](../java/text/DateFormatSymbols.md))

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides Cloneable

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Override equals

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAmPmStrings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAmPmStrings(): Array<String!>!
```

Gets ampm strings. For example: "AM" and "PM".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the ampm strings. |

### getAvailableLocales

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. It must contain at least a`Locale`instance equal to [Locale.US](../java/util/Locale.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | An array of locales for which localized`DateFormatSymbols`instances are available. |

### getEras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEras(): Array<String!>!
```

Gets era strings. For example: "AD" and "BC".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the era strings. |

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): DateFormatSymbols!
```

Gets the`DateFormatSymbols`instance for the default locale.

This is equivalent to calling [getInstance(Locale.getDefault(Locale.Category.FORMAT))](../java/text/DateFormatSymbols.md)).

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------|
| [DateFormatSymbols](../java/text/DateFormatSymbols.md)! | a`DateFormatSymbols`instance. |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](../java/util/Locale.md))
- [java.util.Locale.Category#FORMAT](../java/util/Locale.Category.md) 

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): DateFormatSymbols!
```

Gets the`DateFormatSymbols`instance for the specified locale.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the given locale. |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------|
| [DateFormatSymbols](../java/text/DateFormatSymbols.md)! | a`DateFormatSymbols`instance. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### getLocalPatternChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPatternChars(): String!
```

Gets localized date-time pattern characters. For example: 'u', 't', etc.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized date-time pattern characters. |

### getMonths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonths(): Array<String!>!
```

Gets month strings. For example: "January", "February", etc. An array with either 12 or 13 elements will be returned depending on whether or not [Calendar.UNDECIMBER](../java/util/Calendar.md) is supported. Use [Calendar.JANUARY](../java/util/Calendar.md), [Calendar.FEBRUARY](../java/util/Calendar.md), etc. to index the result array.

If the language requires different forms for formatting and stand-alone usages, this method returns month names in the formatting form. For example, the preferred month name for January in the Czech language is*ledna* in the formatting form, while it is*leden* in the stand-alone form. This method returns`"ledna"`in this case. Refer to the [Calendar Elements in the Unicode Locale Data Markup Language (LDML) specification](http://unicode.org/reports/tr35/#Calendar_Elements) for more details.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the month strings. |

### getShortMonths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShortMonths(): Array<String!>!
```

Gets short month strings. For example: "Jan", "Feb", etc. An array with either 12 or 13 elements will be returned depending on whether or not [Calendar.UNDECIMBER](../java/util/Calendar.md) is supported. Use [Calendar.JANUARY](../java/util/Calendar.md), [Calendar.FEBRUARY](../java/util/Calendar.md), etc. to index the result array.

If the language requires different forms for formatting and stand-alone usages, this method returns short month names in the formatting form. For example, the preferred abbreviation for January in the Catalan language is*de gen.* in the formatting form, while it is*gen.* in the stand-alone form. This method returns`"de gen."`in this case. Refer to the [Calendar Elements in the Unicode Locale Data Markup Language (LDML) specification](http://unicode.org/reports/tr35/#Calendar_Elements) for more details.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the short month strings. |

### getShortWeekdays

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShortWeekdays(): Array<String!>!
```

Gets short weekday strings. For example: "Sun", "Mon", etc.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the short weekday strings. Use [Calendar.SUNDAY](../java/util/Calendar.md), [Calendar.MONDAY](../java/util/Calendar.md), etc. to index the result array. |

### getWeekdays

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeekdays(): Array<String!>!
```

Gets weekday strings. For example: "Sunday", "Monday", etc.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the weekday strings. Use [Calendar.SUNDAY](../java/util/Calendar.md), [Calendar.MONDAY](../java/util/Calendar.md), etc. to index the result array. |

### getZoneStrings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZoneStrings(): Array<Array<String!>!>!
```

Gets time zone strings. Use of this method is discouraged; use [TimeZone.getDisplayName()](../java/util/TimeZone.md))instead.

The value returned is a two-dimensional array of strings of size*n* by*m* , where*m* is at least 5. Each of the*n* rows is an entry containing the localized names for a single`TimeZone`. Each such row contains (with`i`ranging from 0..*n*-1):

- `zoneStrings[i][0]`- time zone ID
- `zoneStrings[i][1]`- long name of zone in standard time
- `zoneStrings[i][2]`- short name of zone in standard time
- `zoneStrings[i][3]`- long name of zone in daylight saving time
- `zoneStrings[i][4]`- short name of zone in daylight saving time

The zone ID is*not* localized; it's one of the valid IDs of the [TimeZone](../java/util/TimeZone.md) class that are not [custom IDs](../java/util/TimeZone.md). All other entries are localized names. If a zone does not implement daylight saving time, the daylight saving time names should not be used.

If [setZoneStrings](../java/text/DateFormatSymbols.md))has been called on this`DateFormatSymbols`instance, then the strings provided by that call are returned. Otherwise, the returned array contains names provided by the runtime.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | the time zone strings. |

**See Also**

- [#setZoneStrings(String[][])](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols#setZoneStrings(kotlin.Array)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Override hashCode. Generates a hash code for the DateFormatSymbols object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setAmPmStrings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAmPmStrings(newAmpms: Array<String!>!): Unit
```

Sets ampm strings. For example: "AM" and "PM".

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newAmpms` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new ampm strings. |

### setEras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEras(newEras: Array<String!>!): Unit
```

Sets era strings. For example: "AD" and "BC".

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newEras` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new era strings. |

### setLocalPatternChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocalPatternChars(newLocalPatternChars: String!): Unit
```

Sets localized date-time pattern characters. For example: 'u', 't', etc.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `newLocalPatternChars` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new localized date-time pattern characters. |

### setMonths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonths(newMonths: Array<String!>!): Unit
```

Sets month strings. For example: "January", "February", etc.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newMonths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new month strings. The array should be indexed by [Calendar.JANUARY](../java/util/Calendar.md), [Calendar.FEBRUARY](../java/util/Calendar.md), etc. |

### setShortMonths

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShortMonths(newShortMonths: Array<String!>!): Unit
```

Sets short month strings. For example: "Jan", "Feb", etc.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newShortMonths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new short month strings. The array should be indexed by [Calendar.JANUARY](../java/util/Calendar.md), [Calendar.FEBRUARY](../java/util/Calendar.md), etc. |

### setShortWeekdays

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShortWeekdays(newShortWeekdays: Array<String!>!): Unit
```

Sets short weekday strings. For example: "Sun", "Mon", etc.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newShortWeekdays` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new short weekday strings. The array should be indexed by [Calendar.SUNDAY](../java/util/Calendar.md), [Calendar.MONDAY](../java/util/Calendar.md), etc. |

### setWeekdays

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWeekdays(newWeekdays: Array<String!>!): Unit
```

Sets weekday strings. For example: "Sunday", "Monday", etc.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newWeekdays` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new weekday strings. The array should be indexed by [Calendar.SUNDAY](../java/util/Calendar.md), [Calendar.MONDAY](../java/util/Calendar.md), etc. |

### setZoneStrings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setZoneStrings(newZoneStrings: Array<Array<String!>!>!): Unit
```

Sets time zone strings. The argument must be a two-dimensional array of strings of size*n* by*m* , where*m* is at least 5. Each of the*n* rows is an entry containing the localized names for a single`TimeZone`. Each such row contains (with`i`ranging from 0..*n*-1):

- `zoneStrings[i][0]`- time zone ID
- `zoneStrings[i][1]`- long name of zone in standard time
- `zoneStrings[i][2]`- short name of zone in standard time
- `zoneStrings[i][3]`- long name of zone in daylight saving time
- `zoneStrings[i][4]`- short name of zone in daylight saving time

The zone ID is*not* localized; it's one of the valid IDs of the [TimeZone](../java/util/TimeZone.md) class that are not [custom IDs](../java/util/TimeZone.md). All other entries are localized names.

<br />

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newZoneStrings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:the new time zone strings. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the length of any row in`newZoneStrings`is less than 5 |
| `java.lang.NullPointerException` | if`newZoneStrings`is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols#getZoneStrings()>
