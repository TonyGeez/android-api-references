# SignStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignStyle

```
class SignStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.format.SignStyle](SignStyle.md)\> ||
| | ↳ | [java.time.format.SignStyle](SignStyle.md) |

| Known Direct Subclasses [SignStyle.ALWAYS](SignStyle.md), [SignStyle.EXCEEDS_PAD](SignStyle.md), [SignStyle.NEVER](SignStyle.md), [SignStyle.NORMAL](SignStyle.md), [SignStyle.NOT_NEGATIVE](SignStyle.md) |-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------| | [SignStyle.ALWAYS](SignStyle.md) | Style to always output the sign, where zero will output '+'. | | [SignStyle.EXCEEDS_PAD](SignStyle.md) | Style to always output the sign if the value exceeds the pad width. | | [SignStyle.NEVER](SignStyle.md) | Style to never output sign, only outputting the absolute value. | | [SignStyle.NORMAL](SignStyle.md) | Style to output the sign only if the value is negative. | | [SignStyle.NOT_NEGATIVE](SignStyle.md) | Style to block negative values, throwing an exception on printing. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration of ways to handle the positive/negative sign.

The formatting engine allows the positive and negative signs of numbers to be controlled using this enum. See [DateTimeFormatterBuilder](DateTimeFormatterBuilder.md) for usage.

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ALWAYS](SignStyle.md) Style to always output the sign, where zero will output '+'. |
| [EXCEEDS_PAD](SignStyle.md) Style to always output the sign if the value exceeds the pad width. |
| [NEVER](SignStyle.md) Style to never output sign, only outputting the absolute value. |
| [NORMAL](SignStyle.md) Style to output the sign only if the value is negative. |
| [NOT_NEGATIVE](SignStyle.md) Style to block negative values, throwing an exception on printing. |

## Enum values

### ALWAYS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ALWAYS : SignStyle
```

Style to always output the sign, where zero will output '+'.

In strict parsing, the absence of a sign will be rejected. In lenient parsing, any sign will be accepted, with the absence of a sign treated as a positive number. 

### EXCEEDS_PAD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val EXCEEDS_PAD : SignStyle
```

Style to always output the sign if the value exceeds the pad width. A negative value will always output the '-' sign.

In strict parsing, the sign will be rejected unless the pad width is exceeded. In lenient parsing, any sign will be accepted, with the absence of a sign treated as a positive number. 

### NEVER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NEVER : SignStyle
```

Style to never output sign, only outputting the absolute value.

In strict parsing, any sign will be rejected. In lenient parsing, any sign will be accepted unless the width is fixed. 

### NORMAL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NORMAL : SignStyle
```

Style to output the sign only if the value is negative.

In strict parsing, the negative sign will be accepted and the positive sign rejected. In lenient parsing, any sign will be accepted. 

### NOT_NEGATIVE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NOT_NEGATIVE : SignStyle
```

Style to block negative values, throwing an exception on printing.

In strict parsing, any sign will be rejected. In lenient parsing, any sign will be accepted unless the width is fixed.
