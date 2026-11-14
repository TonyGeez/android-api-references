# DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateFormatSymbols

Kotlin| [Java](../android/icu/text/DateFormatSymbols.md) 
| --- | --- |

```
open class DateFormatSymbols : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) |

**\[icu enhancement\]** ICU's replacement for [java.text.DateFormatSymbols](../java/text/DateFormatSymbols.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

`DateFormatSymbols`is a public class for encapsulating localizable date-time formatting data, such as the names of the months, the names of the days of the week, and the time zone data.`DateFormat`and`SimpleDateFormat`both use`DateFormatSymbols`to encapsulate this information.

Typically you shouldn't use`DateFormatSymbols`directly. Rather, you are encouraged to create a date-time formatter with the`DateFormat`class's factory methods:`getTimeInstance`,`getDateInstance`, or`getDateTimeInstance`. These methods automatically create a`DateFormatSymbols`for the formatter so that you don't have to. After the formatter is created, you may modify its format pattern using the`setPattern`method. For more information about creating formatters using`DateFormat`'s factory methods, see [DateFormat](../android/icu/text/DateFormat.md).

If you decide to create a date-time formatter with a specific format pattern for a specific locale, you can do so with: 

```kotlin
new SimpleDateFormat(aPattern, new DateFormatSymbols(aLocale)).
  
```

`DateFormatSymbols`objects are clonable. When you obtain a`DateFormatSymbols`object, feel free to modify the date-time formatting data. For instance, you can replace the localized date-time format pattern characters with the ones that you feel easy to remember. Or you can change the representative cities to your favorite ones.

New`DateFormatSymbols`subclasses may be added to support`SimpleDateFormat`for date-time formatting for additional locales.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ABBREVIATED](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for width. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for context. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NARROW](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for width. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for width; only supported for weekdays. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDALONE](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for context. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WIDE](../android/icu/text/DateFormatSymbols.md) **\[icu\]**Constant for width. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`()` Constructs a DateFormatSymbols object by loading format data from resources for the default`FORMAT`locale. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`cal:` ` [Calendar](../android/icu/util/Calendar.md)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Returns the [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) object that should be used to format a calendar system's dates in the given locale. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`cal:` ` [Calendar](../android/icu/util/Calendar.md)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Returns the [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) object that should be used to format a calendar system's dates in the given locale. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Constructs a DateFormatSymbols object by loading format data from resources for the given ulocale. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`calendarClass:` ` [Class](../java/lang/Class.md)<out` ` [Calendar](../android/icu/util/Calendar.md)!>!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Variant of DateFormatSymbols(Calendar, ULocale) that takes the Calendar class instead of a Calendar instance. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`calendarClass:` ` [Class](../java/lang/Class.md)<out` ` [Calendar](../android/icu/util/Calendar.md)!>!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Variant of DateFormatSymbols(Calendar, Locale) that takes the Calendar class instead of a Calendar instance. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Constructs a DateFormatSymbols object by loading format data from resources for the given locale. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`bundle:` ` [ResourceBundle](../java/util/ResourceBundle.md)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Fetches a custom calendar's DateFormatSymbols out of the given resource bundle. |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md))`(`bundle:` ` [ResourceBundle](../java/util/ResourceBundle.md)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Fetches a custom calendar's DateFormatSymbols out of the given resource bundle. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/DateFormatSymbols.md))`()` Overrides clone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/DateFormatSymbols.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAmPmStrings](../android/icu/text/DateFormatSymbols.md))`()` Returns am/pm strings. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../android/icu/text/DateFormatSymbols.md))`()` Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEraNames](../android/icu/text/DateFormatSymbols.md))`()` **\[icu\]**Returns full era name strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getEras](../android/icu/text/DateFormatSymbols.md))`()` Returns abbreviated era strings. |
| --- | --- |
| openstatic [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | [getInstance](../android/icu/text/DateFormatSymbols.md))`()` Returns a DateFormatSymbols instance for the default locale. |
| openstatic [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | [getInstance](../android/icu/text/DateFormatSymbols.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a DateFormatSymbols instance for the given locale. |
| openstatic [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | [getInstance](../android/icu/text/DateFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Returns a DateFormatSymbols instance for the given locale. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalPatternChars](../android/icu/text/DateFormatSymbols.md))`()` Returns localized date-time pattern characters. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getMonths](../android/icu/text/DateFormatSymbols.md))`()` Returns month strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getMonths](../android/icu/text/DateFormatSymbols.md))`(`context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns month strings. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getNarrowEras](../android/icu/text/DateFormatSymbols.md))`()` **\[icu\]**Returns narrow era name strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getQuarters](../android/icu/text/DateFormatSymbols.md))`(`context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Returns quarter strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getShortMonths](../android/icu/text/DateFormatSymbols.md))`()` Returns short month strings. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getShortWeekdays](../android/icu/text/DateFormatSymbols.md))`()` Returns abbreviated weekday strings; for example: "Sun", "Mon", etc. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getWeekdays](../android/icu/text/DateFormatSymbols.md))`()` Returns wide weekday strings. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getWeekdays](../android/icu/text/DateFormatSymbols.md))`(`context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns weekday strings. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getYearNames](../android/icu/text/DateFormatSymbols.md))`(`context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns cyclic year name strings if the calendar has them, for example: "jia-zi", "yi-chou", etc. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getZodiacNames](../android/icu/text/DateFormatSymbols.md))`(`context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns calendar zodiac name strings if the calendar has them, for example: "Rat", "Ox", "Tiger", etc. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getZoneStrings](../android/icu/text/DateFormatSymbols.md))`()` Returns time zone strings. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/text/DateFormatSymbols.md))`()` Override hashCode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAmPmStrings](../android/icu/text/DateFormatSymbols.md))`(`newAmpms:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets am/pm strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEraNames](../android/icu/text/DateFormatSymbols.md))`(`newEraNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` **\[icu\]**Sets full era name strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEras](../android/icu/text/DateFormatSymbols.md))`(`newEras:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets abbreviated era strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocalPatternChars](../android/icu/text/DateFormatSymbols.md))`(`newLocalPatternChars:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets localized date-time pattern characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonths](../android/icu/text/DateFormatSymbols.md))`(`newMonths:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets month strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonths](../android/icu/text/DateFormatSymbols.md))`(`newMonths:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets month strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNarrowEras](../android/icu/text/DateFormatSymbols.md))`(`newNarrowEras:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` **\[icu\]**Sets narrow era name strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQuarters](../android/icu/text/DateFormatSymbols.md))`(`newQuarters:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **\[icu\]**Sets quarter strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShortMonths](../android/icu/text/DateFormatSymbols.md))`(`newShortMonths:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets short month strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShortWeekdays](../android/icu/text/DateFormatSymbols.md))`(`newAbbrevWeekdays:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets abbreviated weekday strings; for example: "Sun", "Mon", etc. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWeekdays](../android/icu/text/DateFormatSymbols.md))`(`newWeekdays:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets wide weekday strings. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWeekdays](../android/icu/text/DateFormatSymbols.md))`(`newWeekdays:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets weekday strings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYearNames](../android/icu/text/DateFormatSymbols.md))`(`yearNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets cyclic year name strings, for example: "jia-zi", "yi-chou", etc. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZodiacNames](../android/icu/text/DateFormatSymbols.md))`(`zodiacNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `context:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets calendar zodiac name strings, for example: "Rat", "Ox", "Tiger", etc. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZoneStrings](../android/icu/text/DateFormatSymbols.md))`(`newZoneStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` Sets time zone strings. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initializeData](../android/icu/text/DateFormatSymbols.md))`(`desiredLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Initializes format symbols for the locale and calendar type |

## Constants

### ABBREVIATED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ABBREVIATED: Int
```

**\[icu\]**Constant for width. 

 Value: 0

### FORMAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT: Int
```

**\[icu\]**Constant for context. 

 Value: 0

### NARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NARROW: Int
```

**\[icu\]**Constant for width. 

 Value: 2

### SHORT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHORT: Int
```

**\[icu\]**Constant for width; only supported for weekdays. 

 Value: 3

### STANDALONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDALONE: Int
```

**\[icu\]**Constant for context. 

 Value: 1

### WIDE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDE: Int
```

**\[icu\]**Constant for width. 

 Value: 1

## Public constructors

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols()
```

Constructs a DateFormatSymbols object by loading format data from resources for the default`FORMAT`locale.

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resources for the default locale cannot be found or cannot be loaded. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    cal: Calendar!, 
    locale: ULocale!)
```

Returns the [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) object that should be used to format a calendar system's dates in the given locale.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cal` | [Calendar](../android/icu/util/Calendar.md)!:The calendar system whose date format symbols are desired. |
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:The ulocale whose symbols are desired. |

**See Also**

- [android.icu.text.DateFormatSymbols#DateFormatSymbols(java.util.Locale)](../android/icu/text/DateFormatSymbols.md)) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    cal: Calendar!, 
    locale: Locale!)
```

Returns the [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) object that should be used to format a calendar system's dates in the given locale.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cal` | [Calendar](../android/icu/util/Calendar.md)!:The calendar system whose date format symbols are desired. |
| `locale` | [Locale](../java/util/Locale.md)!:The locale whose symbols are desired. |

**See Also**

- [android.icu.text.DateFormatSymbols#DateFormatSymbols(java.util.Locale)](../android/icu/text/DateFormatSymbols.md)) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(locale: ULocale!)
```

**\[icu\]**Constructs a DateFormatSymbols object by loading format data from resources for the given ulocale.

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resources for the specified locale cannot be found or cannot be loaded. |

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    calendarClass: Class<out Calendar!>!, 
    locale: ULocale!)
```

Variant of DateFormatSymbols(Calendar, ULocale) that takes the Calendar class instead of a Calendar instance. 
**See Also**

- [#DateFormatSymbols(Calendar, Locale)](../android/icu/text/DateFormatSymbols.md)) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    calendarClass: Class<out Calendar!>!, 
    locale: Locale!)
```

Variant of DateFormatSymbols(Calendar, Locale) that takes the Calendar class instead of a Calendar instance. 
**See Also**

- [#DateFormatSymbols(Calendar, Locale)](../android/icu/text/DateFormatSymbols.md)) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(locale: Locale!)
```

Constructs a DateFormatSymbols object by loading format data from resources for the given locale.

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | if the resources for the specified locale cannot be found or cannot be loaded. |

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    bundle: ResourceBundle!, 
    locale: ULocale!)
```

Fetches a custom calendar's DateFormatSymbols out of the given resource bundle. Symbols that are not overridden are inherited from the default DateFormatSymbols for the locale. 
**See Also**

- [android.icu.text.DateFormatSymbols#DateFormatSymbols(java.util.Locale)](../android/icu/text/DateFormatSymbols.md)) 

### DateFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateFormatSymbols(
    bundle: ResourceBundle!, 
    locale: Locale!)
```

Fetches a custom calendar's DateFormatSymbols out of the given resource bundle. Symbols that are not overridden are inherited from the default DateFormatSymbols for the locale. 
**See Also**

- [android.icu.text.DateFormatSymbols#DateFormatSymbols(java.util.Locale)](../android/icu/text/DateFormatSymbols.md))

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides clone.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Overrides equals.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAmPmStrings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAmPmStrings(): Array<String!>!
```

Returns am/pm strings. For example: "AM" and "PM".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the weekday strings. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.**\[icu\] Note:** Unlike`java.text.DateFormatSymbols#getAvailableLocales`, this method simply returns the array of`Locale`s available in this class. ICU does not support`DateFormatSymbolsProvider`introduced in Java 6 or its equivalent implementation for now.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | An array of`Locale`s for which localized`DateFormatSymbols`instances are available. |

### getEraNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEraNames(): Array<String!>!
```

**\[icu\]**Returns full era name strings. For example: "Anno Domini" and "Before Christ".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the era strings. |

### getEras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEras(): Array<String!>!
```

Returns abbreviated era strings. For example: "AD" and "BC".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the era strings. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): DateFormatSymbols!
```

Returns a DateFormatSymbols instance for the default locale.**\[icu\] Note:** Unlike`java.text.DateFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DateFormatSymbols()`. ICU does not support`DateFormatSymbolsProvider`introduced in Java 6 or its equivalent implementation for now.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------|
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | A DateFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): DateFormatSymbols!
```

**\[icu\]** Returns a DateFormatSymbols instance for the given locale.**\[icu\] Note:** Unlike`java.text.DateFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DateFormatSymbols(locale)`. ICU does not support`DateFormatSymbolsProvider`introduced in Java 6 or its equivalent implementation for now.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------|
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | A DateFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): DateFormatSymbols!
```

Returns a DateFormatSymbols instance for the given locale.**\[icu\] Note:** Unlike`java.text.DateFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DateFormatSymbols(locale)`. ICU does not support`DateFormatSymbolsProvider`introduced in Java 6 or its equivalent implementation for now.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------|
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md)! | A DateFormatSymbols instance. |

### getLocalPatternChars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPatternChars(): String!
```

Returns localized date-time pattern characters. For example: 'u', 't', etc.

Note: ICU no longer provides localized date-time pattern characters for a locale starting ICU 3.8. This method returns the non-localized date-time pattern characters unless user defined localized data is set by setLocalPatternChars.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized date-time pattern characters. |

### getMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonths(): Array<String!>!
```

Returns month strings. For example: "January", "February", etc.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the month strings. |

### getMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonths(
    context: Int, 
    width: Int
): Array<String!>!
```

Returns month strings. For example: "January", "February", etc.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month context, FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width or the returned month string, either WIDE, ABBREVIATED, or NARROW. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the month strings. |

### getNarrowEras

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNarrowEras(): Array<String!>!
```

**\[icu\]**Returns narrow era name strings. For example: "A" and "B".

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the narrow era strings. |

### getQuarters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuarters(
    context: Int, 
    width: Int
): Array<String!>!
```

**\[icu\]**Returns quarter strings. For example: "1st Quarter", "2nd Quarter", etc.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The quarter context, FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width or the returned quarter string, WIDE, NARROW, or ABBREVIATED. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the quarter strings. |

### getShortMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShortMonths(): Array<String!>!
```

Returns short month strings. For example: "Jan", "Feb", etc.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the short month strings. |

### getShortWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShortWeekdays(): Array<String!>!
```

Returns abbreviated weekday strings; for example: "Sun", "Mon", etc. (Note: the method name is misleading; it does not get the CLDR-style "short" weekday strings, e.g. "Su", "Mo", etc.)

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the abbreviated weekday strings. Use`Calendar.SUNDAY`,`Calendar.MONDAY`, etc. to index the result array. |

### getWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeekdays(): Array<String!>!
```

Returns wide weekday strings. For example: "Sunday", "Monday", etc.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the weekday strings. Use`Calendar.SUNDAY`,`Calendar.MONDAY`, etc. to index the result array. |

### getWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeekdays(
    context: Int, 
    width: Int
): Array<String!>!
```

Returns weekday strings. For example: "Sunday", "Monday", etc.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Formatting context, either FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Width of strings to be returned, either WIDE, ABBREVIATED, SHORT, or NARROW |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the weekday strings. Use`Calendar.SUNDAY`,`Calendar.MONDAY`, etc. to index the result array. |

### getYearNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYearNames(
    context: Int, 
    width: Int
): Array<String!>!
```

Returns cyclic year name strings if the calendar has them, for example: "jia-zi", "yi-chou", etc.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The usage context: FORMAT, STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The requested name width: WIDE, ABBREVIATED, SHORT, NARROW. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The year name strings, or null if they are not available for this calendar. |

### getZodiacNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZodiacNames(
    context: Int, 
    width: Int
): Array<String!>!
```

Returns calendar zodiac name strings if the calendar has them, for example: "Rat", "Ox", "Tiger", etc.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The usage context: FORMAT, STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The requested name width: WIDE, ABBREVIATED, SHORT, NARROW. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The zodiac name strings, or null if they are not available for this calendar. |

### getZoneStrings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZoneStrings(): Array<Array<String!>!>!
```

Returns time zone strings.

The array returned by this API is a two dimensional String array and each row contains at least following strings:

- ZoneStrings\[n\]\[0\] - System time zone ID
- ZoneStrings\[n\]\[1\] - Long standard time display name
- ZoneStrings\[n\]\[2\] - Short standard time display name
- ZoneStrings\[n\]\[3\] - Long daylight saving time display name
- ZoneStrings\[n\]\[4\] - Short daylight saving time display name

When a localized display name is not available, the corresponding array element will be`null`.

**Note** : ICU implements the time zone display name formatting algorithm specified by [UTS#35 Unicode Locale Data Markup Language(LDML)](http://www.unicode.org/reports/tr35/). The algorithm supports historic display name changes and various different types of names not available in [java.text.DateFormatSymbols#getZoneStrings()](../java/text/DateFormatSymbols.md)). For accessing the full set of time zone string data used by ICU implementation, you should use [TimeZoneNames](../android/icu/text/TimeZoneNames.md) APIs instead.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | the time zone strings. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Override hashCode. Generates a hash code for the DateFormatSymbols object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setAmPmStrings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAmPmStrings(newAmpms: Array<String!>!): Unit
```

Sets am/pm strings. For example: "AM" and "PM".

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newAmpms` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new ampm strings. |

### setEraNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEraNames(newEraNames: Array<String!>!): Unit
```

**\[icu\]**Sets full era name strings. For example: "Anno Domini" and "Before Christ".

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newEraNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new era strings. |

### setEras

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEras(newEras: Array<String!>!): Unit
```

Sets abbreviated era strings. For example: "AD" and "BC".

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newEras` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new era strings. |

### setLocalPatternChars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocalPatternChars(newLocalPatternChars: String!): Unit
```

Sets localized date-time pattern characters. For example: 'u', 't', etc.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `newLocalPatternChars` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new localized date-time pattern characters. |

### setMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonths(newMonths: Array<String!>!): Unit
```

Sets month strings. For example: "January", "February", etc.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newMonths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new month strings. |

### setMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonths(
    newMonths: Array<String!>!, 
    context: Int, 
    width: Int
): Unit
```

Sets month strings. For example: "January", "February", etc.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newMonths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new month strings. |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The formatting context, FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the month string, either WIDE, ABBREVIATED, or NARROW. |
| --- | --- |

### setNarrowEras

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNarrowEras(newNarrowEras: Array<String!>!): Unit
```

**\[icu\]**Sets narrow era name strings. For example: "A" and "B".

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newNarrowEras` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new narrow era strings. |

### setQuarters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setQuarters(
    newQuarters: Array<String!>!, 
    context: Int, 
    width: Int
): Unit
```

**\[icu\]**Sets quarter strings. For example: "1st Quarter", "2nd Quarter", etc.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newQuarters` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new quarter strings. |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The formatting context, FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the quarter string, WIDE, NARROW, or ABBREVIATED. |
| --- | --- |

### setShortMonths

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShortMonths(newShortMonths: Array<String!>!): Unit
```

Sets short month strings. For example: "Jan", "Feb", etc.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newShortMonths` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new short month strings. |

### setShortWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShortWeekdays(newAbbrevWeekdays: Array<String!>!): Unit
```

Sets abbreviated weekday strings; for example: "Sun", "Mon", etc. (Note: the method name is misleading; it does not set the CLDR-style "short" weekday strings, e.g. "Su", "Mo", etc.)

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newAbbrevWeekdays` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new abbreviated weekday strings. The array should be indexed by`Calendar.SUNDAY`,`Calendar.MONDAY`, etc. |

### setWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWeekdays(newWeekdays: Array<String!>!): Unit
```

Sets wide weekday strings. For example: "Sunday", "Monday", etc.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newWeekdays` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the new weekday strings. The array should be indexed by`Calendar.SUNDAY`,`Calendar.MONDAY`, etc. |

### setWeekdays

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWeekdays(
    newWeekdays: Array<String!>!, 
    context: Int, 
    width: Int
): Unit
```

Sets weekday strings. For example: "Sunday", "Monday", etc.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newWeekdays` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The new weekday strings. |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The formatting context, FORMAT or STANDALONE. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the strings, either WIDE, ABBREVIATED, SHORT, or NARROW. |
| --- | --- |

### setYearNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setYearNames(
    yearNames: Array<String!>!, 
    context: Int, 
    width: Int
): Unit
```

Sets cyclic year name strings, for example: "jia-zi", "yi-chou", etc.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `yearNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The new cyclic year name strings. |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The usage context: FORMAT, STANDALONE (currently only FORMAT is supported). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The name width: WIDE, ABBREVIATED, NARROW (currently only ABBREVIATED is supported). |
| --- | --- |

### setZodiacNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setZodiacNames(
    zodiacNames: Array<String!>!, 
    context: Int, 
    width: Int
): Unit
```

Sets calendar zodiac name strings, for example: "Rat", "Ox", "Tiger", etc.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `zodiacNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The new zodiac name strings. |
| `context` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The usage context: FORMAT, STANDALONE (currently only FORMAT is supported). |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The name width: WIDE, ABBREVIATED, NARROW (currently only ABBREVIATED is supported). |
| --- | --- |

### setZoneStrings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setZoneStrings(newZoneStrings: Array<Array<String!>!>!): Unit
```

Sets time zone strings.

**Note** : [SimpleDateFormat](../android/icu/text/SimpleDateFormat.md) no longer uses the zone strings stored in a`DateFormatSymbols`. Therefore, the time zone strings set by this method have no effects in an instance of`SimpleDateFormat`for formatting time zones. If you want to customize time zone display names formatted by`SimpleDateFormat`, you should customize [TimeZoneFormat](../android/icu/text/TimeZoneFormat.md) and set the instance by [SimpleDateFormat.setTimeZoneFormat(TimeZoneFormat)](../android/icu/text/SimpleDateFormat.md))instead.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newZoneStrings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:the new time zone strings. |

## Protected methods

### initializeData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun initializeData(
    desiredLocale: ULocale!, 
    type: String!
): Unit
```

Initializes format symbols for the locale and calendar type

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `desiredLocale` | [ULocale](../android/icu/util/ULocale.md)!:The locale whose symbols are desired. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The calendar type whose date format symbols are desired. |
