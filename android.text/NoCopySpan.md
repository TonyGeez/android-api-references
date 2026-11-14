# NoCopySpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoCopySpan

Kotlin| [Java](https://developer.android.com/reference/android/text/NoCopySpan "View this page in Java") 

```
interface NoCopySpan
```

| [android.text.NoCopySpan](https://developer.android.com/reference/kotlin/android/text/NoCopySpan#) |

| Known Direct Subclasses [NoCopySpan.Concrete](https://developer.android.com/reference/kotlin/android/text/NoCopySpan.Concrete), [SpanWatcher](https://developer.android.com/reference/kotlin/android/text/SpanWatcher), [TextWatcher](https://developer.android.com/reference/kotlin/android/text/TextWatcher) |--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NoCopySpan.Concrete](https://developer.android.com/reference/kotlin/android/text/NoCopySpan.Concrete) | Convenience equivalent for when you would just want a new Object() for a span but want it to be no-copy. | | [SpanWatcher](https://developer.android.com/reference/kotlin/android/text/SpanWatcher) | When an object of this type is attached to a Spannable, its methods will be called to notify it that other markup objects have been added, changed, or removed. | | [TextWatcher](https://developer.android.com/reference/kotlin/android/text/TextWatcher) | When an object of this type is attached to an Editable, its methods will be called when the text is changed. | |

| Known Indirect Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#), [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#), [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener), [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod), [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher.html#), [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) |---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) | Base class that can be used to implement virtualized lists of items. | | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) | A view that shows items in a vertically scrolling two-level list. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) | A view that shows items in two-dimensional scrolling grid. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod) | <br /> | | [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher.html#) | Watches a [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) and if a phone number is entered will format it. | | [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) | This is the key listener for typing normal text. | |

This interface should be added to a span object that should not be copied into a new Spanned when performing a slice or copy operation on the original Spanned it was placed in.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Concrete](https://developer.android.com/reference/kotlin/android/text/NoCopySpan.Concrete) Convenience equivalent for when you would just want a new Object() for a span but want it to be no-copy. |
