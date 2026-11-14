# CharacterStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterStyle

Kotlin| [Java](../android/text/style/CharacterStyle.md) 
| --- | --- |

```
abstract class CharacterStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.CharacterStyle](../android/text/style/CharacterStyle.md) |

| Known Direct Subclasses [BackgroundColorSpan](../android/text/style/BackgroundColorSpan.md), [ClickableSpan](../android/text/style/ClickableSpan.md), [ForegroundColorSpan](../android/text/style/ForegroundColorSpan.md), [MaskFilterSpan](../android/text/style/MaskFilterSpan.md), [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md), [StrikethroughSpan](../android/text/style/StrikethroughSpan.md), [SuggestionRangeSpan](../android/text/style/SuggestionRangeSpan.md), [SuggestionSpan](../android/text/style/SuggestionSpan.md), [UnderlineSpan](../android/text/style/UnderlineSpan.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [BackgroundColorSpan](../android/text/style/BackgroundColorSpan.md) | Changes the background color of the text to which the span is attached. | | [ClickableSpan](../android/text/style/ClickableSpan.md) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. | | [ForegroundColorSpan](../android/text/style/ForegroundColorSpan.md) | Changes the color of the text to which the span is attached. | | [MaskFilterSpan](../android/text/style/MaskFilterSpan.md) | Span that allows setting a [MaskFilter](../android/graphics/MaskFilter.md) to the text it's attached to. | | [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. | | [StrikethroughSpan](../android/text/style/StrikethroughSpan.md) | A span that strikes through the text it's attached to. | | [SuggestionRangeSpan](../android/text/style/SuggestionRangeSpan.md) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. | | [SuggestionSpan](../android/text/style/SuggestionSpan.md) | Holds suggestion candidates for the text enclosed in this span. | | [UnderlineSpan](../android/text/style/UnderlineSpan.md) | A span that underlines the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md), [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md), [ImageSpan](../android/text/style/ImageSpan.md), [LocaleSpan](../android/text/style/LocaleSpan.md), [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md), [ReplacementSpan](../android/text/style/ReplacementSpan.md), [ScaleXSpan](../android/text/style/ScaleXSpan.md), [StyleSpan](../android/text/style/StyleSpan.md), [SubscriptSpan](../android/text/style/SubscriptSpan.md), [SuperscriptSpan](../android/text/style/SuperscriptSpan.md), [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md), [TextLinks.TextLinkSpan](../android/view/textclassifier/TextLinks.TextLinkSpan.md), and 2 others. |-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. | | [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](../android/text/style/ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [LocaleSpan](../android/text/style/LocaleSpan.md) | Changes the [Locale](../java/util/Locale.md) of the text to which the span is attached. | | [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](../android/text/style/ReplacementSpan.md) | <br /> | | [ScaleXSpan](../android/text/style/ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](../android/text/style/StyleSpan.md) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](../android/text/style/SubscriptSpan.md) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](../android/text/style/SuperscriptSpan.md) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. | | [TextLinks.TextLinkSpan](../android/view/textclassifier/TextLinks.TextLinkSpan.md) | A ClickableSpan for a TextLink. | | [TypefaceSpan](../android/text/style/TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. | | [URLSpan](../android/text/style/URLSpan.md) | Implementation of the [ClickableSpan](../android/text/style/ClickableSpan.md) that allows setting a url string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting extend this class. Most extend its subclass [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md), but simple ones may just implement [UpdateAppearance](../android/text/style/UpdateAppearance.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [CharacterStyle](../android/text/style/CharacterStyle.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharacterStyle](../android/text/style/CharacterStyle.md)! | [getUnderlying](../android/text/style/CharacterStyle.md))`()` Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](../android/text/style/CharacterStyle.md)), returns the underlying CharacterStyle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](../android/text/style/CharacterStyle.md))`(`tp:` ` [TextPaint](../android/text/TextPaint.md)!`)` <br /> |
| openstatic [CharacterStyle](../android/text/style/CharacterStyle.md)! | [wrap](../android/text/style/CharacterStyle.md))`(`cs:` ` [CharacterStyle](../android/text/style/CharacterStyle.md)!`)` A given CharacterStyle can only applied to a single region of a given Spanned. |
| --- | --- |

## Public constructors

### CharacterStyle

```
CharacterStyle()
```

## Public methods

### getUnderlying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnderlying(): CharacterStyle!
```

Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](../android/text/style/CharacterStyle.md)), returns the underlying CharacterStyle. 

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun updateDrawState(tp: TextPaint!): Unit
```  

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(cs: CharacterStyle!): CharacterStyle!
```

A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict.
