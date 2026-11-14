# MetricAffectingSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MetricAffectingSpan

Kotlin| [Java](../android/text/style/MetricAffectingSpan.md) 
| --- | --- |

```
abstract class MetricAffectingSpan : CharacterStyle, UpdateLayout
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](../android/text/style/CharacterStyle.md) ||
| | ↳ | [android.text.style.MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) |

| Known Direct Subclasses [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md), [LocaleSpan](../android/text/style/LocaleSpan.md), [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md), [ReplacementSpan](../android/text/style/ReplacementSpan.md), [ScaleXSpan](../android/text/style/ScaleXSpan.md), [StyleSpan](../android/text/style/StyleSpan.md), [SubscriptSpan](../android/text/style/SubscriptSpan.md), [SuperscriptSpan](../android/text/style/SuperscriptSpan.md), [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md), [TypefaceSpan](../android/text/style/TypefaceSpan.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. | | [LocaleSpan](../android/text/style/LocaleSpan.md) | Changes the [Locale](../java/util/Locale.md) of the text to which the span is attached. | | [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](../android/text/style/ReplacementSpan.md) | <br /> | | [ScaleXSpan](../android/text/style/ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](../android/text/style/StyleSpan.md) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](../android/text/style/SubscriptSpan.md) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](../android/text/style/SuperscriptSpan.md) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. | | [TypefaceSpan](../android/text/style/TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md), [ImageSpan](../android/text/style/ImageSpan.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](../android/text/style/ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md)! | [getUnderlying](../android/text/style/MetricAffectingSpan.md))`()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](../android/text/style/CharacterStyle.md)), returns the underlying MetricAffectingSpan. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](../android/text/style/MetricAffectingSpan.md))`(`textPaint:` ` [TextPaint](../android/text/TextPaint.md)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |

| Inherited functions ||
|---|---|
| From class [CharacterStyle](../android/text/style/CharacterStyle.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](../android/text/style/CharacterStyle.md))`(`tp:` ` [TextPaint](../android/text/TextPaint.md)!`)` <br /> | | [CharacterStyle](../android/text/style/CharacterStyle.md)! | [wrap](../android/text/style/CharacterStyle.md))`(`cs:` ` [CharacterStyle](../android/text/style/CharacterStyle.md)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

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

Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](../android/text/style/CharacterStyle.md)), returns the underlying MetricAffectingSpan. 

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateMeasureState(textPaint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `textPaint` | [TextPaint](../android/text/TextPaint.md):the paint used for drawing the text This value cannot be`null`. |
