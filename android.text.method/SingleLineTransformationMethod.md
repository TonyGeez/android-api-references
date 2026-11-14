# SingleLineTransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SingleLineTransformationMethod

Kotlin| [Java](SingleLineTransformationMethod.md) 
| --- | --- |

```
open class SingleLineTransformationMethod : ReplacementTransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.method.ReplacementTransformationMethod](ReplacementTransformationMethod.md) ||
| | ↳ | [android.text.method.SingleLineTransformationMethod](SingleLineTransformationMethod.md) |

This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SingleLineTransformationMethod](SingleLineTransformationMethod.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [SingleLineTransformationMethod](SingleLineTransformationMethod.md)! | [getInstance](SingleLineTransformationMethod.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getOriginal](SingleLineTransformationMethod.md))`()` The characters to be replaced are \\n and \\r. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getReplacement](SingleLineTransformationMethod.md))`()` The character \\n is replaced with is space; the character \\r is replaced with is FEFF (zero width space). |

| Inherited functions ||
|---|---|
| From class [ReplacementTransformationMethod](ReplacementTransformationMethod.md) |------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](ReplacementTransformationMethod.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `v:` ` [View](../android.view/View.md)!`)` <br /> Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in [getOriginal](ReplacementTransformationMethod.md))replaced by ones from [getReplacement](ReplacementTransformationMethod.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](ReplacementTransformationMethod.md))`(`view:` ` [View](../android.view/View.md)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](../android.graphics/Rect.md)!`)` <br /> | ||

## Public constructors

### SingleLineTransformationMethod

```
SingleLineTransformationMethod()
```

## Public methods

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): SingleLineTransformationMethod!
```

## Protected methods

### getOriginal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getOriginal(): CharArray!
```

The characters to be replaced are \\n and \\r. 

### getReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getReplacement(): CharArray!
```

The character \\n is replaced with is space; the character \\r is replaced with is FEFF (zero width space).
