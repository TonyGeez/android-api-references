# MetricAffectingSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MetricAffectingSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/MetricAffectingSpan "View this page in Java") 
| --- | --- |

```
abstract class MetricAffectingSpan : CharacterStyle, UpdateLayout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) ||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#) |

| Known Direct Subclasses [AbsoluteSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan), [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan), [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan), [ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan), [ScaleXSpan](https://developer.android.com/reference/kotlin/android/text/style/ScaleXSpan), [StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan), [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan), [SuperscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SuperscriptSpan), [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan), [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan) | A span that changes the size of the text it's attached to. | | [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan) | Changes the [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) of the text to which the span is attached. | | [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan) | <br /> | | [ScaleXSpan](https://developer.android.com/reference/kotlin/android/text/style/ScaleXSpan) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SuperscriptSpan) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan) | Sets the text appearance using the given [TextAppearance](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance:kotlin.IntArray) attributes. | | [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan) | Span that updates the typeface of the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan), [ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#MetricAffectingSpan())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#updateMeasureState(android.text.TextPaint))`(`textPaint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |

| Inherited functions ||
|---|---|
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### MetricAffectingSpan

```
MetricAffectingSpan()
```

## Public methods

### getUnderlying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnderlying(): MetricAffectingSpan!
```

Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. 

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateMeasureState(textPaint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `textPaint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):the paint used for drawing the text This value cannot be`null`. |
