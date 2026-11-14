# TextWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextWatcher

Kotlin| [Java](TextWatcher.md) 
| --- | --- |

```
interface TextWatcher : NoCopySpan
```

| [android.text.TextWatcher](TextWatcher.md) |

| Known Direct Subclasses [AbsListView](../android.widget/AbsListView.md), [PasswordTransformationMethod](../android.text.method/PasswordTransformationMethod.md), [PhoneNumberFormattingTextWatcher](../android.telephony/PhoneNumberFormattingTextWatcher.md) |---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbsListView](../android.widget/AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [PasswordTransformationMethod](../android.text.method/PasswordTransformationMethod.md) | <br /> | | [PhoneNumberFormattingTextWatcher](../android.telephony/PhoneNumberFormattingTextWatcher.md) | Watches a [android.widget.TextView](../android.widget/TextView.md) and if a phone number is entered will format it. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ExpandableListView](../android.widget/ExpandableListView.md), [GridView](../android.widget/GridView.md), [ListView](../android.widget/ListView.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](../android.widget/ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [GridView](../android.widget/GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [ListView](../android.widget/ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

When an object of this type is attached to an Editable, its methods will be called when the text is changed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterTextChanged](TextWatcher.md))`(`s:` ` [Editable](Editable.md)!`)` This method is called to notify you that, somewhere within`s`, the text has been changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeTextChanged](TextWatcher.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that, within`s`, the`count`characters beginning at`start`are about to be replaced by new text with length`after`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTextChanged](TextWatcher.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `before:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called to notify you that, within`s`, the`count`characters beginning at`start`have just replaced old text that had length`before`. |
| --- | --- |

## Public methods

### afterTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun afterTextChanged(s: Editable!): Unit
```

This method is called to notify you that, somewhere within`s`, the text has been changed. It is legitimate to make further changes to`s`from this callback, but be careful not to get yourself into an infinite loop, because any changes you make will cause this method to be called again recursively. (You are not told where the change took place because other afterTextChanged() methods may already have made other changes and invalidated the offsets. But if you need to know here, you can use [Spannable.setSpan](Spannable.md))in [onTextChanged](TextWatcher.md))to mark your place and then look up from here where the span ended up. 

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
