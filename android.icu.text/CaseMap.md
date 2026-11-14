# CaseMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaseMap

Kotlin| [Java](CaseMap.md) 
| --- | --- |

```
abstract class CaseMap
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.CaseMap](CaseMap.md) |

| Known Direct Subclasses [CaseMap.Fold](../android/icu/text/CaseMap.Fold.md), [CaseMap.Lower](../android/icu/text/CaseMap.Lower.md), [CaseMap.Title](../android/icu/text/CaseMap.Title.md), [CaseMap.Upper](../android/icu/text/CaseMap.Upper.md) |------------------------------------------------------------------------------------------------|-----------------------------------| | [CaseMap.Fold](../android/icu/text/CaseMap.Fold.md) | Case folding options and methods. | | [CaseMap.Lower](../android/icu/text/CaseMap.Lower.md) | Lowercasing options and methods. | | [CaseMap.Title](../android/icu/text/CaseMap.Title.md) | Titlecasing options and methods. | | [CaseMap.Upper](../android/icu/text/CaseMap.Upper.md) | Uppercasing options and methods. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Low-level case mapping options and methods. Immutable. "Setters" return instances with the union of the current and new options set. This class is not intended for public subclassing.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Fold](../android/icu/text/CaseMap.Fold.md) Case folding options and methods. |
| | [Lower](../android/icu/text/CaseMap.Lower.md) Lowercasing options and methods. |
| | [Title](../android/icu/text/CaseMap.Title.md) Titlecasing options and methods. |
| --- | --- |
| | [Upper](../android/icu/text/CaseMap.Upper.md) Uppercasing options and methods. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CaseMap.Fold](../android/icu/text/CaseMap.Fold.md)! | [fold](CaseMap.md))`()` <br /> |
| abstract [CaseMap](CaseMap.md)! | [omitUnchangedText](CaseMap.md))`()` Returns an instance that behaves like this one but omits unchanged text when case-mapping with [Edits](Edits.md). |
| openstatic [CaseMap.Lower](../android/icu/text/CaseMap.Lower.md)! | [toLower](CaseMap.md))`()` <br /> |
| --- | --- |
| openstatic [CaseMap.Title](../android/icu/text/CaseMap.Title.md)! | [toTitle](CaseMap.md))`()` <br /> |
| openstatic [CaseMap.Upper](../android/icu/text/CaseMap.Upper.md)! | [toUpper](CaseMap.md))`()` <br /> |

## Public methods

### fold

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fold(): CaseMap.Fold!
```

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| [CaseMap.Fold](../android/icu/text/CaseMap.Fold.md)! | Case folding object with default options. |

### omitUnchangedText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun omitUnchangedText(): CaseMap!
```

Returns an instance that behaves like this one but omits unchanged text when case-mapping with [Edits](Edits.md).

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------|
| [CaseMap](CaseMap.md)! | an options object with this option. |

### toLower

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toLower(): CaseMap.Lower!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Lower](../android/icu/text/CaseMap.Lower.md)! | Lowercasing object with default options. |

### toTitle

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toTitle(): CaseMap.Title!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Title](../android/icu/text/CaseMap.Title.md)! | Titlecasing object with default options. |

### toUpper

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toUpper(): CaseMap.Upper!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------|
| [CaseMap.Upper](../android/icu/text/CaseMap.Upper.md)! | Uppercasing object with default options. |
