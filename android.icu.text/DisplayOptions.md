# DisplayOptions

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayOptions

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/DisplayOptions "View this page in Java") 
| --- | --- |

```
class DisplayOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DisplayOptions](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#) |

Represents all the display options that are supported by CLDR such as grammatical case, noun class, ... etc. It currently supports enums, but may be extended in the future to have other types of data. It replaces a DisplayContext\[\] as a method parameter.

NOTE: This class is Immutable, and uses a Builder interface.

For example:`DisplayOptions x = DisplayOptions.builder() .setNounClass(NounClass.DATIVE) .setPluralCategory(PluralCategory.FEW) .build(); `

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Builder) Responsible for building`DisplayOptions`. |
| | [Capitalization](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Capitalization) Represents all the capitalization options. |
| | [DisplayLength](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.DisplayLength) Represents all the display lengths. |
| --- | --- |
| | [GrammaticalCase](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.GrammaticalCase) Represents all the grammatical cases that are supported by CLDR. |
| | [NameStyle](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NameStyle) Represents all the name styles. |
| | [NounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NounClass) Represents all the grammatical noun classes that are supported by CLDR. |
| --- | --- |
| | [PluralCategory](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.PluralCategory) Standard CLDR plural category constants. |
| | [SubstituteHandling](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.SubstituteHandling) Represents all the substitute handlings. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DisplayOptions.Builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Builder)! | [builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#builder())`()` Creates a builder with the`UNDEFINED`value for all the parameters. |
| [DisplayOptions.Builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Builder)! | [copyToBuilder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#copyToBuilder())`()` Creates a builder with the same parameters from this object. |
| [DisplayOptions.Capitalization](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Capitalization)! | [getCapitalization](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getCapitalization())`()` Gets the capitalization. |
| --- | --- |
| [DisplayOptions.DisplayLength](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.DisplayLength)! | [getDisplayLength](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getDisplayLength())`()` Gets the display length. |
| [DisplayOptions.GrammaticalCase](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.GrammaticalCase)! | [getGrammaticalCase](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getGrammaticalCase())`()` Gets the grammatical case. |
| [DisplayOptions.NameStyle](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NameStyle)! | [getNameStyle](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getNameStyle())`()` Gets the name style. |
| --- | --- |
| [DisplayOptions.NounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NounClass)! | [getNounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getNounClass())`()` Gets the noun class. |
| [DisplayOptions.PluralCategory](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.PluralCategory)! | [getPluralCategory](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getPluralCategory())`()` Gets the plural category. |
| [DisplayOptions.SubstituteHandling](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.SubstituteHandling)! | [getSubstituteHandling](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions#getSubstituteHandling())`()` Gets the substitute handling. |
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
| [DisplayOptions.Builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Builder)! | Builder |

### copyToBuilder

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun copyToBuilder(): DisplayOptions.Builder!
```

Creates a builder with the same parameters from this object.

| Return ||
|-------------------------------------------------------------------------------------------------------------------|---------|
| [DisplayOptions.Builder](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Builder)! | Builder |

### getCapitalization

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCapitalization(): DisplayOptions.Capitalization!
```

Gets the capitalization.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------|
| [DisplayOptions.Capitalization](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.Capitalization)! | Capitalization |

### getDisplayLength

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLength(): DisplayOptions.DisplayLength!
```

Gets the display length.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------|---------------|
| [DisplayOptions.DisplayLength](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.DisplayLength)! | DisplayLength |

### getGrammaticalCase

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGrammaticalCase(): DisplayOptions.GrammaticalCase!
```

Gets the grammatical case.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------|
| [DisplayOptions.GrammaticalCase](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.GrammaticalCase)! | GrammaticalCase |

### getNameStyle

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameStyle(): DisplayOptions.NameStyle!
```

Gets the name style.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------|
| [DisplayOptions.NameStyle](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NameStyle)! | NameStyle |

### getNounClass

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNounClass(): DisplayOptions.NounClass!
```

Gets the noun class.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------|
| [DisplayOptions.NounClass](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.NounClass)! | NounClass |

### getPluralCategory

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPluralCategory(): DisplayOptions.PluralCategory!
```

Gets the plural category.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------|
| [DisplayOptions.PluralCategory](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.PluralCategory)! | PluralCategory |

### getSubstituteHandling

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubstituteHandling(): DisplayOptions.SubstituteHandling!
```

Gets the substitute handling.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [DisplayOptions.SubstituteHandling](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.SubstituteHandling)! | SubstituteHandling |
