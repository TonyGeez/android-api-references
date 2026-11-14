# NoCopySpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoCopySpan

Kotlin| [Java](NoCopySpan.md) 
| --- | --- |

```
interface NoCopySpan
```

| [android.text.NoCopySpan](NoCopySpan.md) |

| Known Direct Subclasses [NoCopySpan.Concrete](../android/text/NoCopySpan.Concrete.md), [SpanWatcher](SpanWatcher.md), [TextWatcher](TextWatcher.md) |--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NoCopySpan.Concrete](../android/text/NoCopySpan.Concrete.md) | Convenience equivalent for when you would just want a new Object() for a span but want it to be no-copy. | | [SpanWatcher](SpanWatcher.md) | When an object of this type is attached to a Spannable, its methods will be called to notify it that other markup objects have been added, changed, or removed. | | [TextWatcher](TextWatcher.md) | When an object of this type is attached to an Editable, its methods will be called when the text is changed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbsListView](../android.widget/AbsListView.md), [ExpandableListView](../android.widget/ExpandableListView.md), [GridView](../android.widget/GridView.md), [ListView](../android.widget/ListView.md), [MultiTapKeyListener](../android.text.method/MultiTapKeyListener.md), [PasswordTransformationMethod](../android.text.method/PasswordTransformationMethod.md), [PhoneNumberFormattingTextWatcher](../android.telephony/PhoneNumberFormattingTextWatcher.md), [TextKeyListener](../android.text.method/TextKeyListener.md) |---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](../android.widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [ExpandableListView](../android.widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [GridView](../android.widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [ListView](../android.widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MultiTapKeyListener](../android.text.method/MultiTapKeyListener.md) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [PasswordTransformationMethod](../android.text.method/PasswordTransformationMethod.md) | <br /> | | [PhoneNumberFormattingTextWatcher](../android.telephony/PhoneNumberFormattingTextWatcher.md) | Watches a [android.widget.TextView](../android.widget/TextView.md) and if a phone number is entered will format it. | | [TextKeyListener](../android.text.method/TextKeyListener.md) | This is the key listener for typing normal text. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface should be added to a span object that should not be copied into a new Spanned when performing a slice or copy operation on the original Spanned it was placed in.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Concrete](../android/text/NoCopySpan.Concrete.md) Convenience equivalent for when you would just want a new Object() for a span but want it to be no-copy. |
