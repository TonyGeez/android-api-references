Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReplacementTransformationMethod

Kotlin | [Java](ReplacementTransformationMethod.md)
| --- | --- |

```
abstract class ReplacementTransformationMethod : TransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.ReplacementTransformationMethod](ReplacementTransformationMethod.md) |

| Known Direct Subclasses [HideReturnsTransformationMethod](HideReturnsTransformationMethod.md), [SingleLineTransformationMethod](SingleLineTransformationMethod.md) |---|---| | [HideReturnsTransformationMethod](HideReturnsTransformationMethod.md) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). | | [SingleLineTransformationMethod](SingleLineTransformationMethod.md) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This transformation method causes the characters in the getOriginal array to be replaced by the corresponding characters in the getReplacement array.

## Summary

| Public constructors ||
|---|---|
| ReplacementTransformationMethod <br /> |

| Public methods ||
|---|---|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getTransformation Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in getOriginal replaced by ones from getReplacement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onFocusChanged This method is called when the TextView that uses this TransformationMethod gains or loses focus. |

| Protected methods ||
|---|---|
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | getOriginal Returns the list of characters that are to be replaced by other characters when displayed. |
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | getReplacement Returns a parallel array of replacement characters for the ones that are to be replaced. |

## Public constructors

### ReplacementTransformationMethod

```
ReplacementTransformationMethod()
```

## Public methods

### getTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransformation(
    source: CharSequence!, 
    v: View!
): CharSequence!
```

Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in getOriginal replaced by ones from getReplacement.

### onFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onFocusChanged(
    view: View!, 
    sourceText: CharSequence!, 
    focused: Boolean, 
    direction: Int, 
    previouslyFocusedRect: Rect!
): Unit
```

This method is called when the TextView that uses this TransformationMethod gains or loses focus.

## Protected methods

### getOriginal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getOriginal(): CharArray!
```

Returns the list of characters that are to be replaced by other characters when displayed.

### getReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getReplacement(): CharArray!
```

Returns a parallel array of replacement characters for the ones that are to be replaced.
