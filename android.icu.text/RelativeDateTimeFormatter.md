# RelativeDateTimeFormatter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RelativeDateTimeFormatter

Kotlin| [Java](../android/icu/text/RelativeDateTimeFormatter.md) 
| --- | --- |

```
class RelativeDateTimeFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md) |

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
| | [AbsoluteUnit](../android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit.md) Represents an absolute unit. |
| | [Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md) Represents a direction for an absolute unit e. |
| | [FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md) Represents the result of a formatting operation of a relative datetime. |
| --- | --- |
| | [RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md) Represents the unit for formatting a relative date. |
| | [RelativeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeUnit.md) Represents the unit for formatting a relative date. |
| | [Style](../android/icu/text/RelativeDateTimeFormatter.Style.md) The formatting style |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [combineDateAndTime](../android/icu/text/RelativeDateTimeFormatter.md))`(`relativeDateString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `timeString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Combines a relative date string and a time string in this object's locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/RelativeDateTimeFormatter.md))`(`direction:` ` [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!`, `unit:` ` [RelativeDateTimeFormatter.AbsoluteUnit](../android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit.md)!`)` Formats a relative date without a quantity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/RelativeDateTimeFormatter.md))`(`quantity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `direction:` ` [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!`, `unit:` ` [RelativeDateTimeFormatter.RelativeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeUnit.md)!`)` Formats a relative date with a quantity such as "in 5 days" or "3 months ago". |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/RelativeDateTimeFormatter.md))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumeric](../android/icu/text/RelativeDateTimeFormatter.md))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e. |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | [formatNumericToValue](../android/icu/text/RelativeDateTimeFormatter.md))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a numeric style, e. |
| --- | --- |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | [formatToValue](../android/icu/text/RelativeDateTimeFormatter.md))`(`direction:` ` [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!`, `unit:` ` [RelativeDateTimeFormatter.AbsoluteUnit](../android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit.md)!`)` Formats a relative date without a quantity. |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | [formatToValue](../android/icu/text/RelativeDateTimeFormatter.md))`(`quantity:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `direction:` ` [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!`, `unit:` ` [RelativeDateTimeFormatter.RelativeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeUnit.md)!`)` Formats a relative date with a quantity such as "in 5 days" or "3 months ago". |
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | [formatToValue](../android/icu/text/RelativeDateTimeFormatter.md))`(`offset:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `unit:` ` [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!`)` Format a combination of RelativeDateTimeUnit and numeric offset using a text style if possible, e. |
| --- | --- |
| [DisplayContext](../android/icu/text/DisplayContext.md)! | [getCapitalizationContext](../android/icu/text/RelativeDateTimeFormatter.md))`()` Return capitalization context. |
| [RelativeDateTimeFormatter.Style](../android/icu/text/RelativeDateTimeFormatter.Style.md)! | [getFormatStyle](../android/icu/text/RelativeDateTimeFormatter.md))`()` Return style |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`()` Returns a RelativeDateTimeFormatter for the default locale. |
| --- | --- |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Returns a RelativeDateTimeFormatter for a particular locale. |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `nf:` ` [NumberFormat](../android/icu/text/NumberFormat.md)!`)` Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object. |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `nf:` ` [NumberFormat](../android/icu/text/NumberFormat.md)!`, `style:` ` [RelativeDateTimeFormatter.Style](../android/icu/text/RelativeDateTimeFormatter.Style.md)!`, `capitalizationContext:` ` [DisplayContext](../android/icu/text/DisplayContext.md)!`)` Returns a RelativeDateTimeFormatter for a particular locale that uses a particular NumberFormat object, style, and capitalization context |
| --- | --- |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](../java/util/Locale.md). |
| static [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | [getInstance](../android/icu/text/RelativeDateTimeFormatter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `nf:` ` [NumberFormat](../android/icu/text/NumberFormat.md)!`)` Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](../java/util/Locale.md) that uses a particular NumberFormat object. |
| [NumberFormat](../android/icu/text/NumberFormat.md)! | [getNumberFormat](../android/icu/text/RelativeDateTimeFormatter.md))`()` Returns a copy of the NumberFormat this object is using. |
| --- | --- |

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
| `direction` | [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!:NEXT, LAST, THIS, etc. |
| `unit` | [RelativeDateTimeFormatter.AbsoluteUnit](../android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit.md)!:e.g SATURDAY, DAY, MONTH |

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
| `quantity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The numerical amount e.g 5. This value is formatted according to this object's [NumberFormat](../android/icu/text/NumberFormat.md) object. |
| `direction` | [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!:NEXT means a future relative date; LAST means a past relative date. |
| `unit` | [RelativeDateTimeFormatter.RelativeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeUnit.md)!:the unit e.g day? month? year? |
| --- | --- |

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
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

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
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

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
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | The formatted string (may be empty in case of error) |

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
| `direction` | [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!:NEXT, LAST, THIS, etc. |
| `unit` | [RelativeDateTimeFormatter.AbsoluteUnit](../android/icu/text/RelativeDateTimeFormatter.AbsoluteUnit.md)!:e.g SATURDAY, DAY, MONTH |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | the formatted string. If direction has a value that is documented as not being fully supported in every locale (for example NEXT_2 or LAST_2) then this function may return null to signal that no formatted string is available. |

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
| `quantity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The numerical amount e.g 5. This value is formatted according to this object's [NumberFormat](../android/icu/text/NumberFormat.md) object. |
| `direction` | [RelativeDateTimeFormatter.Direction](../android/icu/text/RelativeDateTimeFormatter.Direction.md)!:NEXT means a future relative date; LAST means a past relative date. |
| `unit` | [RelativeDateTimeFormatter.RelativeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeUnit.md)!:the unit e.g day? month? year? |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | the formatted relative datetime |

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
| `unit` | [RelativeDateTimeFormatter.RelativeDateTimeUnit](../android/icu/text/RelativeDateTimeFormatter.RelativeDateTimeUnit.md)!:The unit to use when formatting the relative date, e.g. RelativeDateTimeUnit.WEEK, RelativeDateTimeUnit.FRIDAY. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [RelativeDateTimeFormatter.FormattedRelativeDateTime](../android/icu/text/RelativeDateTimeFormatter.FormattedRelativeDateTime.md)! | The formatted string (may be empty in case of error) |

### getCapitalizationContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapitalizationContext(): DisplayContext!
```

Return capitalization context.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [DisplayContext](../android/icu/text/DisplayContext.md)! | The capitalization context. |

### getFormatStyle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormatStyle(): RelativeDateTimeFormatter.Style!
```

Return style

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [RelativeDateTimeFormatter.Style](../android/icu/text/RelativeDateTimeFormatter.Style.md)! | The formatting style. |

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
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | An instance of RelativeDateTimeFormatter. |

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
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale |
| `nf` | [NumberFormat](../android/icu/text/NumberFormat.md)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | An instance of RelativeDateTimeFormatter. |

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
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale |
| `nf` | [NumberFormat](../android/icu/text/NumberFormat.md)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. May be null. |
| `style` | [RelativeDateTimeFormatter.Style](../android/icu/text/RelativeDateTimeFormatter.Style.md)!:the style. |
| --- | --- |
| `capitalizationContext` | [DisplayContext](../android/icu/text/DisplayContext.md)!:the capitalization context. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](../java/util/Locale.md).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the [java.util.Locale](../java/util/Locale.md). |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | An instance of RelativeDateTimeFormatter. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    locale: Locale!, 
    nf: NumberFormat!
): RelativeDateTimeFormatter!
```

Returns a RelativeDateTimeFormatter for a particular [java.util.Locale](../java/util/Locale.md) that uses a particular NumberFormat object.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the [java.util.Locale](../java/util/Locale.md) |
| `nf` | [NumberFormat](../android/icu/text/NumberFormat.md)!:the number format object. It is defensively copied to ensure thread-safety and immutability of this class. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md)! | An instance of RelativeDateTimeFormatter. |

### getNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNumberFormat(): NumberFormat!
```

Returns a copy of the NumberFormat this object is using.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | A copy of the NumberFormat. |
