# HideReturnsTransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HideReturnsTransformationMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/HideReturnsTransformationMethod "View this page in Java") 

```
open class HideReturnsTransformationMethod : ReplacementTransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.text.method.ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod) ||
| | ↳ | [android.text.method.HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#) |

This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#HideReturnsTransformationMethod())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#getInstance())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getOriginal](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#getOriginal())`()` The character to be replaced is \\r. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getReplacement](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod#getReplacement())`()` The character that \\r is replaced with is \\uFEFF. |

| Inherited functions ||
|---|---|
| From class [ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod) |------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getTransformation(kotlin.CharSequence,%20android.view.View))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in [getOriginal](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal())replaced by ones from [getReplacement](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#onFocusChanged(android.view.View,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` <br /> | ||

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
