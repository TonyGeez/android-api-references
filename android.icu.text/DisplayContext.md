# DisplayContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayContext

Kotlin| [Java](DisplayContext.md) 
| --- | --- |

```
class DisplayContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.icu.text.DisplayContext](DisplayContext.md)\> ||
| | ↳ | [android.icu.text.DisplayContext](DisplayContext.md) |

| Known Direct Subclasses [DisplayContext.CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](DisplayContext.md), [DisplayContext.CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](DisplayContext.md), [DisplayContext.CAPITALIZATION_FOR_STANDALONE](DisplayContext.md), [DisplayContext.CAPITALIZATION_FOR_UI_LIST_OR_MENU](DisplayContext.md), [DisplayContext.CAPITALIZATION_NONE](DisplayContext.md), [DisplayContext.DIALECT_NAMES](DisplayContext.md), [DisplayContext.LENGTH_FULL](DisplayContext.md), [DisplayContext.LENGTH_SHORT](DisplayContext.md), [DisplayContext.NO_SUBSTITUTE](DisplayContext.md), [DisplayContext.STANDARD_NAMES](DisplayContext.md), [DisplayContext.SUBSTITUTE](DisplayContext.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DisplayContext.CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](DisplayContext.md) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the beginning of a sentence. | | [DisplayContext.CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](DisplayContext.md) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the middle of a sentence. | | [DisplayContext.CAPITALIZATION_FOR_STANDALONE](DisplayContext.md) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for stand-alone usage such as an isolated name on a calendar page. | | [DisplayContext.CAPITALIZATION_FOR_UI_LIST_OR_MENU](DisplayContext.md) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for a user-interface list or menu item. | | [DisplayContext.CAPITALIZATION_NONE](DisplayContext.md) | A possible setting for CAPITALIZATION: The capitalization context to be used is unknown (this is the default value). | | [DisplayContext.DIALECT_NAMES](DisplayContext.md) | A possible setting for DIALECT_HANDLING: use dialect names, when generating a locale name, e. | | [DisplayContext.LENGTH_FULL](DisplayContext.md) | A possible setting for DISPLAY_LENGTH: use full names when generating a locale name, e. | | [DisplayContext.LENGTH_SHORT](DisplayContext.md) | A possible setting for DISPLAY_LENGTH: use short names when generating a locale name, e. | | [DisplayContext.NO_SUBSTITUTE](DisplayContext.md) | A possible setting for SUBSTITUTE_HANDLING: Returns a null value when no data is available. | | [DisplayContext.STANDARD_NAMES](DisplayContext.md) | A possible setting for DIALECT_HANDLING: use standard names when generating a locale name, e. | | [DisplayContext.SUBSTITUTE](DisplayContext.md) | A possible setting for SUBSTITUTE_HANDLING: Returns a fallback value (e.g., the input code) when no data is available. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Display context settings. Note, the specific numeric values are internal and may change.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------|
| | [Type](../android/icu/text/DisplayContext.Type.md) Type values for DisplayContext |

| Enum values ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](DisplayContext.md) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the beginning of a sentence. |
| [CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](DisplayContext.md) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the middle of a sentence. |
| [CAPITALIZATION_FOR_STANDALONE](DisplayContext.md) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for stand-alone usage such as an isolated name on a calendar page. |
| [CAPITALIZATION_FOR_UI_LIST_OR_MENU](DisplayContext.md) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for a user-interface list or menu item. |
| [CAPITALIZATION_NONE](DisplayContext.md) A possible setting for CAPITALIZATION: The capitalization context to be used is unknown (this is the default value). |
| [DIALECT_NAMES](DisplayContext.md) A possible setting for DIALECT_HANDLING: use dialect names, when generating a locale name, e. |
| [LENGTH_FULL](DisplayContext.md) A possible setting for DISPLAY_LENGTH: use full names when generating a locale name, e. |
| [LENGTH_SHORT](DisplayContext.md) A possible setting for DISPLAY_LENGTH: use short names when generating a locale name, e. |
| [NO_SUBSTITUTE](DisplayContext.md) A possible setting for SUBSTITUTE_HANDLING: Returns a null value when no data is available. |
| [STANDARD_NAMES](DisplayContext.md) A possible setting for DIALECT_HANDLING: use standard names when generating a locale name, e. |
| [SUBSTITUTE](DisplayContext.md) A possible setting for SUBSTITUTE_HANDLING: Returns a fallback value (e.g., the input code) when no data is available. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)! | [type](DisplayContext.md))`()` Get the Type part of the enum item (e.g. CAPITALIZATION) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [value](DisplayContext.md))`()` Get the value part of the enum item (e.g. CAPITALIZATION_FOR_STANDALONE) |

## Enum values

### CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE : DisplayContext
```

A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the beginning of a sentence. 

### CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE : DisplayContext
```

A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the middle of a sentence. 

### CAPITALIZATION_FOR_STANDALONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CAPITALIZATION_FOR_STANDALONE : DisplayContext
```

A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for stand-alone usage such as an isolated name on a calendar page. 

### CAPITALIZATION_FOR_UI_LIST_OR_MENU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CAPITALIZATION_FOR_UI_LIST_OR_MENU : DisplayContext
```

A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for a user-interface list or menu item. 

### CAPITALIZATION_NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CAPITALIZATION_NONE : DisplayContext
```

A possible setting for CAPITALIZATION: The capitalization context to be used is unknown (this is the default value). 

### DIALECT_NAMES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DIALECT_NAMES : DisplayContext
```

A possible setting for DIALECT_HANDLING: use dialect names, when generating a locale name, e.g. en_GB displays as 'British English'. 

### LENGTH_FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LENGTH_FULL : DisplayContext
```

A possible setting for DISPLAY_LENGTH: use full names when generating a locale name, e.g. "United States" for US. 

### LENGTH_SHORT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LENGTH_SHORT : DisplayContext
```

A possible setting for DISPLAY_LENGTH: use short names when generating a locale name, e.g. "U.S." for US. 

### NO_SUBSTITUTE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NO_SUBSTITUTE : DisplayContext
```

A possible setting for SUBSTITUTE_HANDLING: Returns a null value when no data is available. 

### STANDARD_NAMES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val STANDARD_NAMES : DisplayContext
```

A possible setting for DIALECT_HANDLING: use standard names when generating a locale name, e.g. en_GB displays as 'English (United Kingdom)'. 

### SUBSTITUTE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SUBSTITUTE : DisplayContext
```

A possible setting for SUBSTITUTE_HANDLING: Returns a fallback value (e.g., the input code) when no data is available. This is the default behavior.

## Public methods

### type

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun type(): DisplayContext.Type!
```

Get the Type part of the enum item (e.g. CAPITALIZATION) 

### value

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun value(): Int
```

Get the value part of the enum item (e.g. CAPITALIZATION_FOR_STANDALONE)
