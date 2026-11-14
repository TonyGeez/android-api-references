# CharacterStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterStyle

Kotlin| [Java](CharacterStyle.md) 
| --- | --- |

```
abstract class CharacterStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.CharacterStyle](CharacterStyle.md) |

| Known Direct Subclasses [BackgroundColorSpan](BackgroundColorSpan.md), [ClickableSpan](ClickableSpan.md), [ForegroundColorSpan](ForegroundColorSpan.md), [MaskFilterSpan](MaskFilterSpan.md), [MetricAffectingSpan](MetricAffectingSpan.md), [StrikethroughSpan](StrikethroughSpan.md), [SuggestionRangeSpan](SuggestionRangeSpan.md), [SuggestionSpan](SuggestionSpan.md), [UnderlineSpan](UnderlineSpan.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [BackgroundColorSpan](BackgroundColorSpan.md) | Changes the background color of the text to which the span is attached. | | [ClickableSpan](ClickableSpan.md) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. | | [ForegroundColorSpan](ForegroundColorSpan.md) | Changes the color of the text to which the span is attached. | | [MaskFilterSpan](MaskFilterSpan.md) | Span that allows setting a [MaskFilter](../android.graphics/MaskFilter.md) to the text it's attached to. | | [MetricAffectingSpan](MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. | | [StrikethroughSpan](StrikethroughSpan.md) | A span that strikes through the text it's attached to. | | [SuggestionRangeSpan](SuggestionRangeSpan.md) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. | | [SuggestionSpan](SuggestionSpan.md) | Holds suggestion candidates for the text enclosed in this span. | | [UnderlineSpan](UnderlineSpan.md) | A span that underlines the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsoluteSizeSpan](AbsoluteSizeSpan.md), [DynamicDrawableSpan](DynamicDrawableSpan.md), [ImageSpan](ImageSpan.md), [LocaleSpan](LocaleSpan.md), [RelativeSizeSpan](RelativeSizeSpan.md), [ReplacementSpan](ReplacementSpan.md), [ScaleXSpan](ScaleXSpan.md), [StyleSpan](StyleSpan.md), [SubscriptSpan](SubscriptSpan.md), [SuperscriptSpan](SuperscriptSpan.md), [TextAppearanceSpan](TextAppearanceSpan.md), [TextLinks.TextLinkSpan](../android/view/textclassifier/TextLinks.TextLinkSpan.md), and 2 others. |-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. | | [DynamicDrawableSpan](DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [LocaleSpan](LocaleSpan.md) | Changes the [Locale](../java.util/Locale.md) of the text to which the span is attached. | | [RelativeSizeSpan](RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](ReplacementSpan.md) | <br /> | | [ScaleXSpan](ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](StyleSpan.md) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](SubscriptSpan.md) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](SuperscriptSpan.md) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. | | [TextLinks.TextLinkSpan](../android/view/textclassifier/TextLinks.TextLinkSpan.md) | A ClickableSpan for a TextLink. | | [TypefaceSpan](TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. | | [URLSpan](URLSpan.md) | Implementation of the [ClickableSpan](ClickableSpan.md) that allows setting a url string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting extend this class. Most extend its subclass [MetricAffectingSpan](MetricAffectingSpan.md), but simple ones may just implement [UpdateAppearance](UpdateAppearance.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [CharacterStyle](CharacterStyle.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharacterStyle](CharacterStyle.md)! | [getUnderlying](CharacterStyle.md))`()` Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](CharacterStyle.md)), returns the underlying CharacterStyle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](CharacterStyle.md))`(`tp:` ` [TextPaint](../android.text/TextPaint.md)!`)` <br /> |
| openstatic [CharacterStyle](CharacterStyle.md)! | [wrap](CharacterStyle.md))`(`cs:` ` [CharacterStyle](CharacterStyle.md)!`)` A given CharacterStyle can only applied to a single region of a given Spanned. |
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

Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](CharacterStyle.md)), returns the underlying CharacterStyle. 

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
