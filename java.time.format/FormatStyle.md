# FormatStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FormatStyle

```
class FormatStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.format.FormatStyle](FormatStyle.md)\> ||
| | ↳ | [java.time.format.FormatStyle](FormatStyle.md) |

| Known Direct Subclasses [FormatStyle.FULL](FormatStyle.md), [FormatStyle.LONG](FormatStyle.md), [FormatStyle.MEDIUM](FormatStyle.md), [FormatStyle.SHORT](FormatStyle.md) |---------------------------------------------------------------------------------------------------------------------|----------------------------------------| | [FormatStyle.FULL](FormatStyle.md) | Full text style, with the most detail. | | [FormatStyle.LONG](FormatStyle.md) | Long text style, with lots of detail. | | [FormatStyle.MEDIUM](FormatStyle.md) | Medium text style, with some detail. | | [FormatStyle.SHORT](FormatStyle.md) | Short text style, typically numeric. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration of the style of a localized date, time or date-time formatter.

These styles are used when obtaining a date-time style from configuration. See [DateTimeFormatter](DateTimeFormatter.md) and [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md) for usage.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FULL](FormatStyle.md) Full text style, with the most detail. |
| [LONG](FormatStyle.md) Long text style, with lots of detail. |
| [MEDIUM](FormatStyle.md) Medium text style, with some detail. |
| [SHORT](FormatStyle.md) Short text style, typically numeric. |

## Enum values

### FULL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FULL : FormatStyle
```

Full text style, with the most detail. For example, the format might be 'Tuesday, April 12, 1952 AD' or '3:30:42pm PST'. 

### LONG

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LONG : FormatStyle
```

Long text style, with lots of detail. For example, the format might be 'January 12, 1952'. 

### MEDIUM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MEDIUM : FormatStyle
```

Medium text style, with some detail. For example, the format might be 'Jan 12, 1952'. 

### SHORT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SHORT : FormatStyle
```

Short text style, typically numeric. For example, the format might be '12.13.52' or '3:30pm'.
