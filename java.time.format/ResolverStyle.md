# ResolverStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResolverStyle

```
class ResolverStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.format.ResolverStyle](ResolverStyle.md)\> ||
| | ↳ | [java.time.format.ResolverStyle](ResolverStyle.md) |

| Known Direct Subclasses [ResolverStyle.LENIENT](ResolverStyle.md), [ResolverStyle.SMART](ResolverStyle.md), [ResolverStyle.STRICT](ResolverStyle.md) |---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [ResolverStyle.LENIENT](ResolverStyle.md) | Style to resolve dates and times leniently. | | [ResolverStyle.SMART](ResolverStyle.md) | Style to resolve dates and times in a smart, or intelligent, manner. | | [ResolverStyle.STRICT](ResolverStyle.md) | Style to resolve dates and times strictly. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration of different ways to resolve dates and times.

Parsing a text string occurs in two phases. Phase 1 is a basic text parse according to the fields added to the builder. Phase 2 resolves the parsed field-value pairs into date and/or time objects. This style is used to control how phase 2, resolving, happens.

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LENIENT](ResolverStyle.md) Style to resolve dates and times leniently. |
| [SMART](ResolverStyle.md) Style to resolve dates and times in a smart, or intelligent, manner. |
| [STRICT](ResolverStyle.md) Style to resolve dates and times strictly. |

## Enum values

### LENIENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LENIENT : ResolverStyle
```

Style to resolve dates and times leniently.

Using lenient resolution will resolve the values in an appropriate lenient manner. Individual fields will interpret this differently.

For example, lenient mode allows the month in the ISO calendar system to be outside the range 1 to 12. For example, month 15 is treated as being 3 months after month 12. 

### SMART

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SMART : ResolverStyle
```

Style to resolve dates and times in a smart, or intelligent, manner.

Using smart resolution will perform the sensible default for each field, which may be the same as strict, the same as lenient, or a third behavior. Individual fields will interpret this differently.

For example, resolving year-month and day-of-month in the ISO calendar system using smart mode will ensure that the day-of-month is from 1 to 31, converting any value beyond the last valid day-of-month to be the last valid day-of-month. 

### STRICT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val STRICT : ResolverStyle
```

Style to resolve dates and times strictly.

Using strict resolution will ensure that all parsed values are within the outer range of valid values for the field. Individual fields may be further processed for strictness.

For example, resolving year-month and day-of-month in the ISO calendar system using strict mode will ensure that the day-of-month is valid for the year-month, rejecting invalid values.
