# CaseMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaseMap

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/CaseMap "View this page in Java") 

```
abstract class CaseMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.CaseMap](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#) |

| Known Direct Subclasses [CaseMap.Fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Fold), [CaseMap.Lower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Lower), [CaseMap.Title](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Title), [CaseMap.Upper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Upper) |------------------------------------------------------------------------------------------------|-----------------------------------| | [CaseMap.Fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Fold) | Case folding options and methods. | | [CaseMap.Lower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Lower) | Lowercasing options and methods. | | [CaseMap.Title](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Title) | Titlecasing options and methods. | | [CaseMap.Upper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Upper) | Uppercasing options and methods. | |

Low-level case mapping options and methods. Immutable. "Setters" return instances with the union of the current and new options set. This class is not intended for public subclassing.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Fold) Case folding options and methods. |
| | [Lower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Lower) Lowercasing options and methods. |
| | [Title](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Title) Titlecasing options and methods. |
| | [Upper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Upper) Uppercasing options and methods. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CaseMap.Fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Fold)! | [fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#fold())`()` <br /> |
| abstract [CaseMap](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#)! | [omitUnchangedText](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#omitUnchangedText())`()` Returns an instance that behaves like this one but omits unchanged text when case-mapping with [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits). |
| openstatic [CaseMap.Lower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Lower)! | [toLower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#toLower())`()` <br /> |
| openstatic [CaseMap.Title](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Title)! | [toTitle](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#toTitle())`()` <br /> |
| openstatic [CaseMap.Upper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Upper)! | [toUpper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#toUpper())`()` <br /> |

## Public methods

### fold

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fold(): CaseMap.Fold!
```

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| [CaseMap.Fold](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Fold)! | Case folding object with default options. |

### omitUnchangedText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun omitUnchangedText(): CaseMap!
```

Returns an instance that behaves like this one but omits unchanged text when case-mapping with [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits).

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------|
| [CaseMap](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap#)! | an options object with this option. |

### toLower

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toLower(): CaseMap.Lower!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Lower](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Lower)! | Lowercasing object with default options. |

### toTitle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toTitle(): CaseMap.Title!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Title](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Title)! | Titlecasing object with default options. |

### toUpper

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toUpper(): CaseMap.Upper!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Upper](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap.Upper)! | Uppercasing object with default options. |
