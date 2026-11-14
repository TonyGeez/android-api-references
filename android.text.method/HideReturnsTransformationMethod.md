# HideReturnsTransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HideReturnsTransformationMethod

Kotlin| [Java](HideReturnsTransformationMethod.md) 
| --- | --- |

```
open class HideReturnsTransformationMethod : ReplacementTransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.method.ReplacementTransformationMethod](ReplacementTransformationMethod.md) ||
| | ↳ | [android.text.method.HideReturnsTransformationMethod](HideReturnsTransformationMethod.md) |

This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HideReturnsTransformationMethod](HideReturnsTransformationMethod.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [HideReturnsTransformationMethod](HideReturnsTransformationMethod.md)! | [getInstance](HideReturnsTransformationMethod.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getOriginal](HideReturnsTransformationMethod.md))`()` The character to be replaced is \\r. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getReplacement](HideReturnsTransformationMethod.md))`()` The character that \\r is replaced with is \\uFEFF. |

| Inherited functions ||
|---|---|
| From class [ReplacementTransformationMethod](ReplacementTransformationMethod.md) |------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](ReplacementTransformationMethod.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `v:` ` [View](../android.view/View.md)!`)` <br /> Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in [getOriginal](ReplacementTransformationMethod.md))replaced by ones from [getReplacement](ReplacementTransformationMethod.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](ReplacementTransformationMethod.md))`(`view:` ` [View](../android.view/View.md)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](../android.graphics/Rect.md)!`)` <br /> | ||

## Public constructors

### HideReturnsTransformationMethod

```
HideReturnsTransformationMethod()
```

## Public methods

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): HideReturnsTransformationMethod!
```

## Protected methods

### getOriginal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getOriginal(): CharArray!
```

The character to be replaced is \\r. 

### getReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getReplacement(): CharArray!
```

The character that \\r is replaced with is \\uFEFF.
