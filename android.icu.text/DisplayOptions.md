# DisplayOptions

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayOptions

Kotlin| [Java](../android/icu/text/DisplayOptions.md) 
| --- | --- |

```
class DisplayOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DisplayOptions](../android/icu/text/DisplayOptions.md) |

Represents all the display options that are supported by CLDR such as grammatical case, noun class, ... etc. It currently supports enums, but may be extended in the future to have other types of data. It replaces a DisplayContext\[\] as a method parameter.

NOTE: This class is Immutable, and uses a Builder interface.

For example:`DisplayOptions x = DisplayOptions.builder() .setNounClass(NounClass.DATIVE) .setPluralCategory(PluralCategory.FEW) .build(); `

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/icu/text/DisplayOptions.Builder.md) Responsible for building`DisplayOptions`. |
| | [Capitalization](../android/icu/text/DisplayOptions.Capitalization.md) Represents all the capitalization options. |
| | [DisplayLength](../android/icu/text/DisplayOptions.DisplayLength.md) Represents all the display lengths. |
| --- | --- |
| | [GrammaticalCase](../android/icu/text/DisplayOptions.GrammaticalCase.md) Represents all the grammatical cases that are supported by CLDR. |
| | [NameStyle](../android/icu/text/DisplayOptions.NameStyle.md) Represents all the name styles. |
| | [NounClass](../android/icu/text/DisplayOptions.NounClass.md) Represents all the grammatical noun classes that are supported by CLDR. |
| --- | --- |
| | [PluralCategory](../android/icu/text/DisplayOptions.PluralCategory.md) Standard CLDR plural category constants. |
| | [SubstituteHandling](../android/icu/text/DisplayOptions.SubstituteHandling.md) Represents all the substitute handlings. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DisplayOptions.Builder](../android/icu/text/DisplayOptions.Builder.md)! | [builder](../android/icu/text/DisplayOptions.md))`()` Creates a builder with the`UNDEFINED`value for all the parameters. |
| [DisplayOptions.Builder](../android/icu/text/DisplayOptions.Builder.md)! | [copyToBuilder](../android/icu/text/DisplayOptions.md))`()` Creates a builder with the same parameters from this object. |
| [DisplayOptions.Capitalization](../android/icu/text/DisplayOptions.Capitalization.md)! | [getCapitalization](../android/icu/text/DisplayOptions.md))`()` Gets the capitalization. |
| --- | --- |
| [DisplayOptions.DisplayLength](../android/icu/text/DisplayOptions.DisplayLength.md)! | [getDisplayLength](../android/icu/text/DisplayOptions.md))`()` Gets the display length. |
| [DisplayOptions.GrammaticalCase](../android/icu/text/DisplayOptions.GrammaticalCase.md)! | [getGrammaticalCase](../android/icu/text/DisplayOptions.md))`()` Gets the grammatical case. |
| [DisplayOptions.NameStyle](../android/icu/text/DisplayOptions.NameStyle.md)! | [getNameStyle](../android/icu/text/DisplayOptions.md))`()` Gets the name style. |
| --- | --- |
| [DisplayOptions.NounClass](../android/icu/text/DisplayOptions.NounClass.md)! | [getNounClass](../android/icu/text/DisplayOptions.md))`()` Gets the noun class. |
| [DisplayOptions.PluralCategory](../android/icu/text/DisplayOptions.PluralCategory.md)! | [getPluralCategory](../android/icu/text/DisplayOptions.md))`()` Gets the plural category. |
| [DisplayOptions.SubstituteHandling](../android/icu/text/DisplayOptions.SubstituteHandling.md)! | [getSubstituteHandling](../android/icu/text/DisplayOptions.md))`()` Gets the substitute handling. |
| --- | --- |

## Public methods

### builder

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun builder(): DisplayOptions.Builder!
```

Creates a builder with the`UNDEFINED`value for all the parameters.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|---------|
| [DisplayOptions.Builder](../android/icu/text/DisplayOptions.Builder.md)! | Builder |

### copyToBuilder

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyToBuilder(): DisplayOptions.Builder!
```

Creates a builder with the same parameters from this object.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|---------|
| [DisplayOptions.Builder](../android/icu/text/DisplayOptions.Builder.md)! | Builder |

### getCapitalization

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapitalization(): DisplayOptions.Capitalization!
```

Gets the capitalization.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------|
| [DisplayOptions.Capitalization](../android/icu/text/DisplayOptions.Capitalization.md)! | Capitalization |

### getDisplayLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLength(): DisplayOptions.DisplayLength!
```

Gets the display length.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|---------------|
| [DisplayOptions.DisplayLength](../android/icu/text/DisplayOptions.DisplayLength.md)! | DisplayLength |

### getGrammaticalCase

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrammaticalCase(): DisplayOptions.GrammaticalCase!
```

Gets the grammatical case.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------|
| [DisplayOptions.GrammaticalCase](../android/icu/text/DisplayOptions.GrammaticalCase.md)! | GrammaticalCase |

### getNameStyle

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameStyle(): DisplayOptions.NameStyle!
```

Gets the name style.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------|
| [DisplayOptions.NameStyle](../android/icu/text/DisplayOptions.NameStyle.md)! | NameStyle |

### getNounClass

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNounClass(): DisplayOptions.NounClass!
```

Gets the noun class.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------|
| [DisplayOptions.NounClass](../android/icu/text/DisplayOptions.NounClass.md)! | NounClass |

### getPluralCategory

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPluralCategory(): DisplayOptions.PluralCategory!
```

Gets the plural category.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------|
| [DisplayOptions.PluralCategory](../android/icu/text/DisplayOptions.PluralCategory.md)! | PluralCategory |

### getSubstituteHandling

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubstituteHandling(): DisplayOptions.SubstituteHandling!
```

Gets the substitute handling.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [DisplayOptions.SubstituteHandling](../android/icu/text/DisplayOptions.SubstituteHandling.md)! | SubstituteHandling |
