Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReplacementTransformationMethod

Kotlin | [Java](https://developer.android.com/reference/android/text/method/ReplacementTransformationMethod "View this page in Java")

```
abstract class ReplacementTransformationMethod : TransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.method.ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#) |

| Known Direct Subclasses [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod), [SingleLineTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/SingleLineTransformationMethod) |---|---| | [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). | | [SingleLineTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/SingleLineTransformationMethod) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. | |

This transformation method causes the characters in the `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal()` array to be replaced by the corresponding characters in the `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement()` array.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#ReplacementTransformationMethod()()` <br /> |

| Public methods ||
|---|---|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getTransformation(kotlin.CharSequence,%20android.view.View)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, v: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal()` replaced by ones from `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#onFocusChanged(android.view.View,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, sourceText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, focused: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, previouslyFocusedRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` This method is called when the TextView that uses this TransformationMethod gains or loses focus. |

| Protected methods ||
|---|---|
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal()()` Returns the list of characters that are to be replaced by other characters when displayed. |
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement()()` Returns a parallel array of replacement characters for the ones that are to be replaced. |

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

Returns a CharSequence that will mirror the contents of the source CharSequence but with the characters in `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal()` replaced by ones from `https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement()`.

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
