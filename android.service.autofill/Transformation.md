# Transformation

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformation

Kotlin| [Java](../android/service/autofill/Transformation.md) 
| --- | --- |

```
interface Transformation
```

| [android.service.autofill.Transformation](../android/service/autofill/Transformation.md) |

| Known Direct Subclasses [CharSequenceTransformation](../android/service/autofill/CharSequenceTransformation.md), [DateTransformation](../android/service/autofill/DateTransformation.md), [ImageTransformation](../android/service/autofill/ImageTransformation.md) |----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequenceTransformation](../android/service/autofill/CharSequenceTransformation.md) | Replaces a [TextView](../android/widget/TextView.md) child of a [CustomDescription](../android/service/autofill/CustomDescription.md) with the contents of one or more regular expressions (regexs). | | [DateTransformation](../android/service/autofill/DateTransformation.md) | Replaces a [TextView](../android/widget/TextView.md) child of a [CustomDescription](../android/service/autofill/CustomDescription.md) with the contents of a field that is expected to have a [date value](../android/view/autofill/AutofillValue.md)). | | [ImageTransformation](../android/service/autofill/ImageTransformation.md) | Replaces the content of a child [ImageView](../android/widget/ImageView.md) of a [presentation template](../android/widget/RemoteViews.md) with the first image that matches a regular expression (regex). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Helper class used to change a child view of a [presentation](../android/widget/RemoteViews.md) at runtime, using the values of fields contained in the screen.

Typically used by [CustomDescription](../android/service/autofill/CustomDescription.md) to provide a customized autofill save UI.

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary
