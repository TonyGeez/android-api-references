Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextStyle

```
class TextStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.time.format.TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#)\> ||
| | ↳ | [java.time.format.TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#) |

| Known Direct Subclasses [TextStyle.FULL](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL), [TextStyle.FULL_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL_STANDALONE), [TextStyle.NARROW](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW), [TextStyle.NARROW_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW_STANDALONE), [TextStyle.SHORT](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT), [TextStyle.SHORT_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT_STANDALONE) |---|---| | [TextStyle.FULL](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL) | Full text, typically the full description. | | [TextStyle.FULL_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL_STANDALONE) | Full text for stand-alone use, typically the full description. | | [TextStyle.NARROW](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW) | Narrow text, typically a single letter. | | [TextStyle.NARROW_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW_STANDALONE) | Narrow text for stand-alone use, typically a single letter. | | [TextStyle.SHORT](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT) | Short text, typically an abbreviation. | | [TextStyle.SHORT_STANDALONE](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT_STANDALONE) | Short text for stand-alone use, typically an abbreviation. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Enumeration of the style of text formatting and parsing.

Text styles define three sizes for the formatted text - 'full', 'short' and 'narrow'. Each of these three sizes is available in both 'standard' and 'stand-alone' variations.

The difference between the three sizes is obvious in most languages. For example, in English the 'full' month is 'January', the 'short' month is 'Jan' and the 'narrow' month is 'J'. Note that the narrow size is often not unique. For example, 'January', 'June' and 'July' all have the 'narrow' text 'J'.

The difference between the 'standard' and 'stand-alone' forms is trickier to describe as there is no difference in English. However, in other languages there is a difference in the word used when the text is used alone, as opposed to in a complete date. For example, the word used for a month when used alone in a date picker is different to the word used for month in association with a day and year in a date.

## Summary

| Enum values ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL` Full text, typically the full description. |
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:FULL_STANDALONE` Full text for stand-alone use, typically the full description. |
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW` Narrow text, typically a single letter. |
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:NARROW_STANDALONE` Narrow text for stand-alone use, typically a single letter. |
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT` Short text, typically an abbreviation. |
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#ENUM_VALUE:SHORT_STANDALONE` Short text for stand-alone use, typically an abbreviation. |

| Public methods ||
|---|---|
| [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#)! | `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#asNormal()()` Returns the normal style with the same size. |
| [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle#)! | `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#asStandalone()()` {@return the stand-alone style with the same size} |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#isStandalone()()` Returns true if the Style is a stand-alone style. |
| --- | --- |

## Enum values

### FULL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val FULL : TextStyle
```

Full text, typically the full description. For example, day-of-week Monday might output "Monday".

### FULL_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val FULL_STANDALONE : TextStyle
```

Full text for stand-alone use, typically the full description. For example, day-of-week Monday might output "Monday".

### NARROW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val NARROW : TextStyle
```

Narrow text, typically a single letter. For example, day-of-week Monday might output "M".

### NARROW_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val NARROW_STANDALONE : TextStyle
```

Narrow text for stand-alone use, typically a single letter. For example, day-of-week Monday might output "M".

### SHORT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SHORT : TextStyle
```

Short text, typically an abbreviation. For example, day-of-week Monday might output "Mon".

### SHORT_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
enum val SHORT_STANDALONE : TextStyle
```

Short text for stand-alone use, typically an abbreviation. For example, day-of-week Monday might output "Mon".

## Public methods

### asNormal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun asNormal(): TextStyle!
```

Returns the normal style with the same size.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/format/TextStyle#!` | the normal style with the same size |

### asStandalone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun asStandalone(): TextStyle!
```

{@return the stand-alone style with the same size}

### isStandalone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStandalone(): Boolean
```

Returns true if the Style is a stand-alone style.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the style is a stand-alone style. |
