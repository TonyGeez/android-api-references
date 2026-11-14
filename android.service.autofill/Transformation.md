# Transformation

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transformation

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/Transformation "View this page in Java") 
| --- | --- |

```
interface Transformation
```

| [android.service.autofill.Transformation](https://developer.android.com/reference/kotlin/android/service/autofill/Transformation#) |

| Known Direct Subclasses [CharSequenceTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/CharSequenceTransformation), [DateTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/DateTransformation), [ImageTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/ImageTransformation) |----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequenceTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/CharSequenceTransformation) | Replaces a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) child of a [CustomDescription](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription) with the contents of one or more regular expressions (regexs). | | [DateTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/DateTransformation) | Replaces a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) child of a [CustomDescription](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription) with the contents of a field that is expected to have a [date value](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#forDate(kotlin.Long)). | | [ImageTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/ImageTransformation) | Replaces the content of a child [ImageView](https://developer.android.com/reference/kotlin/android/widget/ImageView.html#) of a [presentation template](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) with the first image that matches a regular expression (regex). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Helper class used to change a child view of a [presentation](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) at runtime, using the values of fields contained in the screen.

Typically used by [CustomDescription](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription) to provide a customized autofill save UI.

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary
