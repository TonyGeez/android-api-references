# Transformation

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformation

Kotlin| [Java](Transformation.md) 
| --- | --- |

```
interface Transformation
```

| [android.service.autofill.Transformation](Transformation.md) |

| Known Direct Subclasses [CharSequenceTransformation](CharSequenceTransformation.md), [DateTransformation](DateTransformation.md), [ImageTransformation](ImageTransformation.md) |----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequenceTransformation](CharSequenceTransformation.md) | Replaces a [TextView](../android.widget/TextView.md) child of a [CustomDescription](CustomDescription.md) with the contents of one or more regular expressions (regexs). | | [DateTransformation](DateTransformation.md) | Replaces a [TextView](../android.widget/TextView.md) child of a [CustomDescription](CustomDescription.md) with the contents of a field that is expected to have a [date value](../android.view.autofill/AutofillValue.md)). | | [ImageTransformation](ImageTransformation.md) | Replaces the content of a child [ImageView](../android.widget/ImageView.md) of a [presentation template](../android.widget/RemoteViews.md) with the first image that matches a regular expression (regex). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Helper class used to change a child view of a [presentation](../android.widget/RemoteViews.md) at runtime, using the values of fields contained in the screen.

Typically used by [CustomDescription](CustomDescription.md) to provide a customized autofill save UI.

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary
