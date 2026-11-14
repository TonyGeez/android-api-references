# DisplayContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayContext

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/DisplayContext "View this page in Java") 
| --- | --- |

```
class DisplayContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.icu.text.DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#)\> ||
| | ↳ | [android.icu.text.DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#) |

| Known Direct Subclasses [DisplayContext.CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE), [DisplayContext.CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE), [DisplayContext.CAPITALIZATION_FOR_STANDALONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_STANDALONE), [DisplayContext.CAPITALIZATION_FOR_UI_LIST_OR_MENU](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_UI_LIST_OR_MENU), [DisplayContext.CAPITALIZATION_NONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_NONE), [DisplayContext.DIALECT_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:DIALECT_NAMES), [DisplayContext.LENGTH_FULL](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_FULL), [DisplayContext.LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_SHORT), [DisplayContext.NO_SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:NO_SUBSTITUTE), [DisplayContext.STANDARD_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:STANDARD_NAMES), [DisplayContext.SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:SUBSTITUTE) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DisplayContext.CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the beginning of a sentence. | | [DisplayContext.CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the middle of a sentence. | | [DisplayContext.CAPITALIZATION_FOR_STANDALONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_STANDALONE) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for stand-alone usage such as an isolated name on a calendar page. | | [DisplayContext.CAPITALIZATION_FOR_UI_LIST_OR_MENU](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_UI_LIST_OR_MENU) | A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for a user-interface list or menu item. | | [DisplayContext.CAPITALIZATION_NONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_NONE) | A possible setting for CAPITALIZATION: The capitalization context to be used is unknown (this is the default value). | | [DisplayContext.DIALECT_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:DIALECT_NAMES) | A possible setting for DIALECT_HANDLING: use dialect names, when generating a locale name, e. | | [DisplayContext.LENGTH_FULL](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_FULL) | A possible setting for DISPLAY_LENGTH: use full names when generating a locale name, e. | | [DisplayContext.LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_SHORT) | A possible setting for DISPLAY_LENGTH: use short names when generating a locale name, e. | | [DisplayContext.NO_SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:NO_SUBSTITUTE) | A possible setting for SUBSTITUTE_HANDLING: Returns a null value when no data is available. | | [DisplayContext.STANDARD_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:STANDARD_NAMES) | A possible setting for DIALECT_HANDLING: use standard names when generating a locale name, e. | | [DisplayContext.SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:SUBSTITUTE) | A possible setting for SUBSTITUTE_HANDLING: Returns a fallback value (e.g., the input code) when no data is available. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Display context settings. Note, the specific numeric values are internal and may change.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------|
| | [Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type) Type values for DisplayContext |

| Enum values ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_BEGINNING_OF_SENTENCE) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the beginning of a sentence. |
| [CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_MIDDLE_OF_SENTENCE) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for the middle of a sentence. |
| [CAPITALIZATION_FOR_STANDALONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_STANDALONE) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for stand-alone usage such as an isolated name on a calendar page. |
| [CAPITALIZATION_FOR_UI_LIST_OR_MENU](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_FOR_UI_LIST_OR_MENU) A possible setting for CAPITALIZATION: The capitalization context if a date, date symbol or display name is to be formatted with capitalization appropriate for a user-interface list or menu item. |
| [CAPITALIZATION_NONE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:CAPITALIZATION_NONE) A possible setting for CAPITALIZATION: The capitalization context to be used is unknown (this is the default value). |
| [DIALECT_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:DIALECT_NAMES) A possible setting for DIALECT_HANDLING: use dialect names, when generating a locale name, e. |
| [LENGTH_FULL](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_FULL) A possible setting for DISPLAY_LENGTH: use full names when generating a locale name, e. |
| [LENGTH_SHORT](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:LENGTH_SHORT) A possible setting for DISPLAY_LENGTH: use short names when generating a locale name, e. |
| [NO_SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:NO_SUBSTITUTE) A possible setting for SUBSTITUTE_HANDLING: Returns a null value when no data is available. |
| [STANDARD_NAMES](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:STANDARD_NAMES) A possible setting for DIALECT_HANDLING: use standard names when generating a locale name, e. |
| [SUBSTITUTE](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#ENUM_VALUE:SUBSTITUTE) A possible setting for SUBSTITUTE_HANDLING: Returns a fallback value (e.g., the input code) when no data is available. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)! | [type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#type())`()` Get the Type part of the enum item (e.g. CAPITALIZATION) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [value](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext#value())`()` Get the value part of the enum item (e.g. CAPITALIZATION_FOR_STANDALONE) |

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
