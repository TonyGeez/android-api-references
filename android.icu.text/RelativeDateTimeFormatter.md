# RelativeDateTimeFormatter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RelativeDateTimeFormatter

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/RelativeDateTimeFormatter "View this page in Java") 

```
class RelativeDateTimeFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#) |

Formats simple relative dates. There are two types of relative dates that it handles:

- relative dates with a quantity e.g "in 5 days"
- relative dates without a quantity e.g "next Tuesday"

<br />

This API is very basic and is intended to be a building block for more fancy APIs. The caller tells it exactly what to display in a locale independent way. While this class automatically provides the correct plural forms, the grammatical form is otherwise as neutral as possible. It is the caller's responsibility to handle cut-off logic such as deciding between displaying "in 7 days" or "in 1 week." This API supports relative dates involving one single unit. This API does not support relative dates involving compound units. e.g "in 5 days and 4 hours" nor does it support parsing. This class is both immutable and thread-safe.

Here are some examples of use: 

```kotlin
RelativeDateTimeFormatter fmt = RelativeDateTimeFormatter.getInstance();
  fmt.format(1, Direction.NEXT, RelativeUnit.DAYS); // "in 1 day"
  fmt.format(3, Direction.NEXT, RelativeUnit.DAYS); // "in 3 days"
  fmt.format(3.2, Direction.LAST, RelativeUnit.YEARS); // "3.2 years ago"
 
  fmt.format(Direction.LAST, AbsoluteUnit.SUNDAY); // "last Sunday"
  fmt.format(Direction.THIS, AbsoluteUnit.SUNDAY); // "this Sunday"
  fmt.format(Direction.NEXT, AbsoluteUnit.SUNDAY); // "next Sunday"
  fmt.format(Direction.PLAIN, AbsoluteUnit.SUNDAY); // "Sunday"
 
  fmt.format(Direction.LAST, AbsoluteUnit.DAY); // "yesterday"
  fmt.format(Direction.THIS, AbsoluteUnit.DAY); // "today"
  fmt.format(Direction.NEXT, AbsoluteUnit.DAY); // "tomorrow"
 
  fmt.format(Direction.PLAIN, AbsoluteUnit.NOW); // "now"
  
```

The Style parameter allows selection of different length styles: LONG ("3 seconds ago"), SHORT ("3 sec. ago"), NARROW ("3s ago"). In the future, we may add more forms, such as relative day periods ("yesterday afternoon"), etc.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AbsoluteUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit) Represents an absolute unit. |
| | [Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction) Represents a direction for an absolute unit e. |
| | [FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime) Represents the result of a formatting operation of a relative datetime. |
| | [RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit) Represents the unit for formatting a relative date. |
| | [RelativeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeUnit) Represents the unit for formatting a relative date. |
| | [Style](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Style) The formatting style |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [combineDateAndTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#combineDateAndTime(kotlin.String,%20kotlin.String))`(`relativeDateString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `timeString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Combines a relative date string and a time string in this object's locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#format(android.icu.text.RelativeDateTimeFormatter.Direction,%20android.icu.text.RelativeDateTimeFormatter.AbsoluteUnit))`(`direction:` ` [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!`, `unit:` ` [RelativeDateTimeFormatter.AbsoluteUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit)!`)` Formats a relative date without a quantity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#format(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.Direction,%20android.icu.text.RelativeDateTimeFormatter.RelativeUnit))`(`quantity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `direction:` ` [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!`, `unit:` ` [RelativeDateTimeFormatter.RelativeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeUnit)!`)` Formats a relative date with a quantity such as "in 5 days" or "3 months ago". |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#format(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.RelativeDateTimeUnit))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumeric](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#formatNumeric(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.RelativeDateTimeUnit))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e. |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | [formatNumericToValue](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#formatNumericToValue(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.RelativeDateTimeUnit))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e. |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | [formatToValue](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#formatToValue(android.icu.text.RelativeDateTimeFormatter.Direction,%20android.icu.text.RelativeDateTimeFormatter.AbsoluteUnit))`(`direction:` ` [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!`, `unit:` ` [RelativeDateTimeFormatter.AbsoluteUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit)!`)` Formats a relative date without a quantity. |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | [formatToValue](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#formatToValue(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.Direction,%20android.icu.text.RelativeDateTimeFormatter.RelativeUnit))`(`quantity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `direction:` ` [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!`, `unit:` ` [RelativeDateTimeFormatter.RelativeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeUnit)!`)` Formats a relative date with a quantity such as "in 5 days" or "3 months ago". |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | [formatToValue](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#formatToValue(kotlin.Double,%20android.icu.text.RelativeDateTimeFormatter.RelativeDateTimeUnit))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e. |
| [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | [getCapitalizationContext](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getCapitalizationContext())`()` Return capitalization context. |
| [RelativeDateTimeFormatter.Style](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Style)! | [getFormatStyle](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getFormatStyle())`()` Return style |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance())`()` Returns a RelativeDateTimeFormatter for the default locale. |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns a RelativeDateTimeFormatter for a particular locale. |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance(android.icu.util.ULocale,%20android.icu.text.NumberFormat))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `nf:` ` [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!`)` Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object. |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance(android.icu.util.ULocale,%20android.icu.text.NumberFormat,%20android.icu.text.RelativeDateTimeFormatter.Style,%20android.icu.text.DisplayContext))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `nf:` ` [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!`, `style:` ` [RelativeDateTimeFormatter.Style](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Style)!`, `capitalizationContext:` ` [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!`)` Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object, style, and capitalization context |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| static [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getInstance(java.util.Locale,%20android.icu.text.NumberFormat))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `nf:` ` [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!`)` Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) that uses a particular NumberFormat object. |
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | [getNumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#getNumberFormat())`()` Returns a copy of the NumberFormat this object is using. |

## Public methods

### combineDateAndTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun combineDateAndTime(
    relativeDateString: String!, 
    timeString: String!
): String!
```

Combines a relative date string and a time string in this object's locale. This is done with the same date-time separator used for the default calendar in this locale.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------|
| `relativeDateString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the relative date e.g 'yesterday' |
| `timeString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the time e.g '3:45' |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the date and time concatenated according to the default calendar in this locale e.g 'yesterday, 3:45' |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    direction: RelativeDateTimeFormatter.Direction!, 
    unit: RelativeDateTimeFormatter.AbsoluteUnit!
): String!
```

Formats a relative date without a quantity. This method returns a String. To get more information about the formatting result, use formatToValue().

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!:NEXT, LAST, THIS, etc. |
| `unit` | [RelativeDateTimeFormatter.AbsoluteUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit)!:e.g SATURDAY, DAY, MONTH |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted string. If direction has a value that is documented as not being fully supported in every locale (for example NEXT_2 or LAST_2) then this function may return null to signal that no formatted string is available. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the direction is incompatible with unit this can occur with NOW which can only take PLAIN. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    quantity: Double, 
    direction: RelativeDateTimeFormatter.Direction!, 
    unit: RelativeDateTimeFormatter.RelativeUnit!
): String!
```

Formats a relative date with a quantity such as "in 5 days" or "3 months ago". This method returns a String. To get more information about the formatting result, use formatToValue().

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quantity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The numerical amount e.g 5. This value is formatted according to this object's [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat) object. |
| `direction` | [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!:NEXT means a future relative date; LAST means a past relative date. |
| `unit` | [RelativeDateTimeFormatter.RelativeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeUnit)!:the unit e.g day? month? year? |

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted string |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if direction is something other than NEXT or LAST. |

### format

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    offset: Double, 
    unit: RelativeDateTimeFormatter.RelativeDateTimeUnit!
): String!
```

Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e.g. "last week", "this week", "next week", "yesterday", "tomorrow". Falls back to numeric style if no appropriate text term is available for the specified offset in the object's locale. This method returns a String. To get more information about the formatting result, use formatToValue().

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The signed offset for the specified field. |
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The formatted string (may be empty in case of error) |

### formatNumeric

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatNumeric(
    offset: Double, 
    unit: RelativeDateTimeFormatter.RelativeDateTimeUnit!
): String!
```

Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e.g. "1 week ago", "in 1 week", "5 weeks ago", "in 5 weeks". This method returns a String. To get more information about the formatting result, use formatNumericToValue().

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The signed offset for the specified unit. This will be formatted according to this object's NumberFormat object. |
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The formatted string (may be empty in case of error) |

### formatNumericToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatNumericToValue(
    offset: Double, 
    unit: RelativeDateTimeFormatter.RelativeDateTimeUnit!
): RelativeDateTimeFormatter.FormattedRelativeDateTime!
```

Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e.g. "1 week ago", "in 1 week", "5 weeks ago", "in 5 weeks". This method returns a FormattedRelativeDateTime, which exposes more information than the String returned by formatNumeric().

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The signed offset for the specified unit. This will be formatted according to this object's NumberFormat object. |
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | The formatted string (may be empty in case of error) |

### formatToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatToValue(
    direction: RelativeDateTimeFormatter.Direction!, 
    unit: RelativeDateTimeFormatter.AbsoluteUnit!
): RelativeDateTimeFormatter.FormattedRelativeDateTime!
```

Formats a relative date without a quantity. This method returns a FormattedRelativeDateTime, which exposes more information than the String returned by format().

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!:NEXT, LAST, THIS, etc. |
| `unit` | [RelativeDateTimeFormatter.AbsoluteUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit)!:e.g SATURDAY, DAY, MONTH |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | the formatted string. If direction has a value that is documented as not being fully supported in every locale (for example NEXT_2 or LAST_2) then this function may return null to signal that no formatted string is available. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the direction is incompatible with unit this can occur with NOW which can only take PLAIN. |

### formatToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatToValue(
    quantity: Double, 
    direction: RelativeDateTimeFormatter.Direction!, 
    unit: RelativeDateTimeFormatter.RelativeUnit!
): RelativeDateTimeFormatter.FormattedRelativeDateTime!
```

Formats a relative date with a quantity such as "in 5 days" or "3 months ago". This method returns a FormattedRelativeDateTime, which exposes more information than the String returned by format().

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quantity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The numerical amount e.g 5. This value is formatted according to this object's [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat) object. |
| `direction` | [RelativeDateTimeFormatter.Direction](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Direction)!:NEXT means a future relative date; LAST means a past relative date. |
| `unit` | [RelativeDateTimeFormatter.RelativeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeUnit)!:the unit e.g day? month? year? |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | the formatted relative datetime |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if direction is something other than NEXT or LAST. |

### formatToValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun formatToValue(
    offset: Double, 
    unit: RelativeDateTimeFormatter.RelativeDateTimeUnit!
): RelativeDateTimeFormatter.FormattedRelativeDateTime!
```

Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e.g. "last week", "this week", "next week", "yesterday", "tomorrow". Falls back to numeric style if no appropriate text term is available for the specified offset in the object's locale. This method returns a FormattedRelativeDateTime, which exposes more information than the String returned by format().

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The signed offset for the specified field. |
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime)! | The formatted string (may be empty in case of error) |

### getCapitalizationContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapitalizationContext(): DisplayContext!
```

Return capitalization context.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | The capitalization context. |

### getFormatStyle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormatStyle(): RelativeDateTimeFormatter.Style!
```

Return style

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [RelativeDateTimeFormatter.Style](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Style)! | The formatting style. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for the default locale. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: ULocale!): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular locale.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | An instance of RelativeDateTimeFormatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: ULocale!, 
    nf: NumberFormat!
): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale |
| `nf` | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | An instance of RelativeDateTimeFormatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: ULocale!, 
    nf: NumberFormat!, 
    style: RelativeDateTimeFormatter.Style!, 
    capitalizationContext: DisplayContext!
): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object, style, and capitalization context

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale |
| `nf` | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. May be null. |
| `style` | [RelativeDateTimeFormatter.Style](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter.Style)!:the style. |
| `capitalizationContext` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!:the capitalization context. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | An instance of RelativeDateTimeFormatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: Locale!, 
    nf: NumberFormat!
): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) that uses a particular NumberFormat object.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) |
| `nf` | [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter#)! | An instance of RelativeDateTimeFormatter. |

### getNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNumberFormat(): NumberFormat!
```

Returns a copy of the NumberFormat this object is using.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat)! | A copy of the NumberFormat. |
