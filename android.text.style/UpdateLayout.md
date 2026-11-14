# UpdateLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UpdateLayout

Kotlin| [Java](UpdateLayout.md) 
| --- | --- |

```
interface UpdateLayout : UpdateAppearance
```

| [android.text.style.UpdateLayout](UpdateLayout.md) |

| Known Direct Subclasses [MetricAffectingSpan](MetricAffectingSpan.md) |--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsoluteSizeSpan](AbsoluteSizeSpan.md), [DynamicDrawableSpan](DynamicDrawableSpan.md), [ImageSpan](ImageSpan.md), [LocaleSpan](LocaleSpan.md), [RelativeSizeSpan](RelativeSizeSpan.md), [ReplacementSpan](ReplacementSpan.md), [ScaleXSpan](ScaleXSpan.md), [StyleSpan](StyleSpan.md), [SubscriptSpan](SubscriptSpan.md), [SuperscriptSpan](SuperscriptSpan.md), [TextAppearanceSpan](TextAppearanceSpan.md), [TypefaceSpan](TypefaceSpan.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsoluteSizeSpan](AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. | | [DynamicDrawableSpan](DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [ImageSpan](ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. | | [LocaleSpan](LocaleSpan.md) | Changes the [Locale](../java.util/Locale.md) of the text to which the span is attached. | | [RelativeSizeSpan](RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. | | [ReplacementSpan](ReplacementSpan.md) | <br /> | | [ScaleXSpan](ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. | | [StyleSpan](StyleSpan.md) | Span that allows setting the style of the text it's attached to. | | [SubscriptSpan](SubscriptSpan.md) | The span that moves the position of the text baseline lower. | | [SuperscriptSpan](SuperscriptSpan.md) | The span that moves the position of the text baseline higher. | | [TextAppearanceSpan](TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. | | [TypefaceSpan](TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The classes that affect character-level text formatting in a way that triggers a text layout update when one is added or removed must implement this interface. This interface also includes [UpdateAppearance](UpdateAppearance.md) since such a change implicitly also impacts the appearance.

## Summary
