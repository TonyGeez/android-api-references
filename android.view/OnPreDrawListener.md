# ViewTreeObserver.OnPreDrawListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreDrawListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewTreeObserver.OnPreDrawListener "View this page in Java") 
| --- | --- |

```
interface OnPreDrawListener
```

| [android.view.ViewTreeObserver.OnPreDrawListener](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnPreDrawListener#) |

| Known Direct Subclasses [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) |------------------------------------------------------------------------------------------|----------------------------------------------------------| | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) | A user interface element that displays text to the user. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#), [Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [CheckBox](https://developer.android.com/reference/kotlin/android/widget/CheckBox.html#), [CheckedTextView](https://developer.android.com/reference/kotlin/android/widget/CheckedTextView.html#), [Chronometer](https://developer.android.com/reference/kotlin/android/widget/Chronometer.html#), [CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), [DigitalClock](https://developer.android.com/reference/kotlin/android/widget/DigitalClock.html#), [EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#), [ExtractEditText](https://developer.android.com/reference/kotlin/android/inputmethodservice/ExtractEditText.html#), [MultiAutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.html#), [RadioButton](https://developer.android.com/reference/kotlin/android/widget/RadioButton.html#), [Switch](https://developer.android.com/reference/kotlin/android/widget/Switch.html#), and 2 others. |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#) | An editable text view that shows completion suggestions automatically while the user is typing. | | [Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#) | A user interface element the user can tap or click to perform an action. | | [CheckBox](https://developer.android.com/reference/kotlin/android/widget/CheckBox.html#) | A checkbox is a specific type of two-states button that can be either checked or unchecked. | | [CheckedTextView](https://developer.android.com/reference/kotlin/android/widget/CheckedTextView.html#) | An extension to [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) that supports the [Checkable](https://developer.android.com/reference/kotlin/android/widget/Checkable.html#) interface and displays. | | [Chronometer](https://developer.android.com/reference/kotlin/android/widget/Chronometer.html#) | Class that implements a simple timer. | | [CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#) | A button with two states, checked and unchecked. | | [DigitalClock](https://developer.android.com/reference/kotlin/android/widget/DigitalClock.html#) | Like AnalogClock, but digital. | | [EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#) | A user interface element for entering and modifying text. | | [ExtractEditText](https://developer.android.com/reference/kotlin/android/inputmethodservice/ExtractEditText.html#) | \* Specialization of [EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#) for showing and interacting with the extracted text in a full-screen input method. | | [MultiAutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.html#) | An editable text view, extending [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.html#), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. | | [RadioButton](https://developer.android.com/reference/kotlin/android/widget/RadioButton.html#) | A radio button is a two-states button that can be either checked or unchecked. | | [Switch](https://developer.android.com/reference/kotlin/android/widget/Switch.html#) | A Switch is a two-state toggle widget. | | [TextClock](https://developer.android.com/reference/kotlin/android/widget/TextClock.html#) | `TextClock`can display the current date and/or time as a formatted string. | | [ToggleButton](https://developer.android.com/reference/kotlin/android/widget/ToggleButton.html#) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the view tree is about to be drawn.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreDraw](https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.OnPreDrawListener#onPreDraw())`()` Callback method to be invoked when the view tree is about to be drawn. |

## Public methods

### onPreDraw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreDraw(): Boolean
```

Callback method to be invoked when the view tree is about to be drawn. At this point, all views in the tree have been measured and given a frame. Clients can use this to adjust their scroll bounds or even to request a new layout before drawing occurs.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true to proceed with the current drawing pass, or false to cancel. |

**See Also**

- [android.view.View#onMeasure](https://developer.android.com/reference/kotlin/android/view/View#onMeasure(kotlin.Int,%20kotlin.Int))
- [android.view.View#onLayout](https://developer.android.com/reference/kotlin/android/view/View#onLayout(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- [android.view.View#onDraw](https://developer.android.com/reference/kotlin/android/view/View#onDraw(android.graphics.Canvas))
