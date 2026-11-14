# UpdateLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UpdateLayout

Kotlin| [Java](../android/text/style/UpdateLayout.md) 
| --- | --- |

```
interface UpdateLayout : UpdateAppearance
```

| [android.text.style.UpdateLayout](../android/text/style/UpdateLayout.md) |

| Known Direct Subclasses [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md), [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md), [ImageSpan](../android/text/style/ImageSpan.md), [LocaleSpan](../android/text/style/LocaleSpan.md), [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md), [ReplacementSpan](../android/text/style/ReplacementSpan.md), [ScaleXSpan](../android/text/style/ScaleXSpan.md), [StyleSpan](../android/text/style/StyleSpan.md), [SubscriptSpan](../android/text/style/SubscriptSpan.md), [SuperscriptSpan](../android/text/style/SuperscriptSpan.md), [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md), [TypefaceSpan](../android/text/style/TypefaceSpan.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. | | [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](../android/text/style/ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [LocaleSpan](../android/text/style/LocaleSpan.md) | Changes the [Locale](../java/util/Locale.md) of the text to which the span is attached. | | [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](../android/text/style/ReplacementSpan.md) | <br /> | | [ScaleXSpan](../android/text/style/ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](../android/text/style/StyleSpan.md) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](../android/text/style/SubscriptSpan.md) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](../android/text/style/SuperscriptSpan.md) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. | | [TypefaceSpan](../android/text/style/TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting in a way that triggers a text layout update when one is added or removed must implement this interface. This interface also includes [UpdateAppearance](../android/text/style/UpdateAppearance.md) since such a change implicitly also impacts the appearance.

## Summary
