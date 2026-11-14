# CharacterStyle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CharacterStyle

Kotlin| [Java](https://developer.android.com/reference/android/text/style/CharacterStyle "View this page in Java") 
| --- | --- |

```
abstract class CharacterStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#) |

| Known Direct Subclasses [BackgroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/BackgroundColorSpan), [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan), [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan), [MaskFilterSpan](https://developer.android.com/reference/kotlin/android/text/style/MaskFilterSpan), [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan), [StrikethroughSpan](https://developer.android.com/reference/kotlin/android/text/style/StrikethroughSpan), [SuggestionRangeSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionRangeSpan), [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan), [UnderlineSpan](https://developer.android.com/reference/kotlin/android/text/style/UnderlineSpan) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [BackgroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/BackgroundColorSpan) | Changes the background color of the text to which the span is attached. | | [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. | | [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan) | Changes the color of the text to which the span is attached. | | [MaskFilterSpan](https://developer.android.com/reference/kotlin/android/text/style/MaskFilterSpan) | Span that allows setting a [MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter.html#) to the text it's attached to. | | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. | | [StrikethroughSpan](https://developer.android.com/reference/kotlin/android/text/style/StrikethroughSpan) | A span that strikes through the text it's attached to. | | [SuggestionRangeSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionRangeSpan) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. | | [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan) | Holds suggestion candidates for the text enclosed in this span. | | [UnderlineSpan](https://developer.android.com/reference/kotlin/android/text/style/UnderlineSpan) | A span that underlines the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsoluteSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan), [DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan), [ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan), [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan), [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan), [ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan), [ScaleXSpan](https://developer.android.com/reference/kotlin/android/text/style/ScaleXSpan), [StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan), [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan), [SuperscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SuperscriptSpan), [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan), [TextLinks.TextLinkSpan](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan.html#), and 2 others. |-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan) | A span that changes the size of the text it's attached to. | | [DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. | | [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan) | Changes the [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) of the text to which the span is attached. | | [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan) | <br /> | | [ScaleXSpan](https://developer.android.com/reference/kotlin/android/text/style/ScaleXSpan) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SuperscriptSpan) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan) | Sets the text appearance using the given [TextAppearance](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance:kotlin.IntArray) attributes. | | [TextLinks.TextLinkSpan](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan.html#) | A ClickableSpan for a TextLink. | | [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan) | Span that updates the typeface of the text it's attached to. | | [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan) | Implementation of the [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan) that allows setting a url string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting extend this class. Most extend its subclass [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan), but simple ones may just implement [UpdateAppearance](https://developer.android.com/reference/kotlin/android/text/style/UpdateAppearance).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#CharacterStyle())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#getUnderlying())`()` Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying CharacterStyle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> |
| openstatic [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#)!`)` A given CharacterStyle can only applied to a single region of a given Spanned. |
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

Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying CharacterStyle. 

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
