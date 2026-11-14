# TextWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextWatcher

Kotlin| [Java](https://developer.android.com/reference/android/text/TextWatcher "View this page in Java") 

```
interface TextWatcher : NoCopySpan
```

| [android.text.TextWatcher](https://developer.android.com/reference/kotlin/android/text/TextWatcher#) |

| Known Direct Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#), [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod), [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher.html#) |---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView.html#) | Base class that can be used to implement virtualized lists of items. | | [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod) | <br /> | | [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher.html#) | Watches a [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) and if a phone number is entered will format it. | |

| Known Indirect Subclasses [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#), [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#), [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView.html#) | A view that shows items in a vertically scrolling two-level list. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView.html#) | A view that shows items in two-dimensional scrolling grid. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |

When an object of this type is attached to an Editable, its methods will be called when the text is changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterTextChanged](https://developer.android.com/reference/kotlin/android/text/TextWatcher#afterTextChanged(android.text.Editable))`(`s:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable)!`)` This method is called to notify you that, somewhere within`s`, the text has been changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeTextChanged](https://developer.android.com/reference/kotlin/android/text/TextWatcher#beforeTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that, within`s`, the`count`characters beginning at`start`are about to be replaced by new text with length`after`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTextChanged](https://developer.android.com/reference/kotlin/android/text/TextWatcher#onTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `before:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that, within`s`, the`count`characters beginning at`start`have just replaced old text that had length`before`. |

## Public methods

### afterTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun afterTextChanged(s: Editable!): Unit
```

This method is called to notify you that, somewhere within`s`, the text has been changed. It is legitimate to make further changes to`s`from this callback, but be careful not to get yourself into an infinite loop, because any changes you make will cause this method to be called again recursively. (You are not told where the change took place because other afterTextChanged() methods may already have made other changes and invalidated the offsets. But if you need to know here, you can use [Spannable.setSpan](https://developer.android.com/reference/kotlin/android/text/Spannable#setSpan(kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))in [onTextChanged](https://developer.android.com/reference/kotlin/android/text/TextWatcher#onTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))to mark your place and then look up from here where the span ended up. 

### beforeTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun beforeTextChanged(
    s: CharSequence!, 
    start: Int, 
    count: Int, 
    after: Int
): Unit
```

This method is called to notify you that, within`s`, the`count`characters beginning at`start`are about to be replaced by new text with length`after`. It is an error to attempt to make changes to`s`from this callback. 

### onTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTextChanged(
    s: CharSequence!, 
    start: Int, 
    before: Int, 
    count: Int
): Unit
```

This method is called to notify you that, within`s`, the`count`characters beginning at`start`have just replaced old text that had length`before`. It is an error to attempt to make changes to`s`from this callback.
