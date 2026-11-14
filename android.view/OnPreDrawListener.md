# ViewTreeObserver.OnPreDrawListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreDrawListener

Kotlin| [Java](../android/view/ViewTreeObserver.OnPreDrawListener.md) 
| --- | --- |

```
interface OnPreDrawListener
```

| [android.view.ViewTreeObserver.OnPreDrawListener](../android/view/ViewTreeObserver.OnPreDrawListener.md) |

| Known Direct Subclasses [TextView](../android.widget/TextView.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------| | [TextView](../android.widget/TextView.md) | A user interface element that displays text to the user. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AutoCompleteTextView](../android.widget/AutoCompleteTextView.md), [Button](../android.widget/Button.md), [CheckBox](../android.widget/CheckBox.md), [CheckedTextView](../android.widget/CheckedTextView.md), [Chronometer](../android.widget/Chronometer.md), [CompoundButton](../android.widget/CompoundButton.md), [DigitalClock](../android.widget/DigitalClock.md), [EditText](../android.widget/EditText.md), [ExtractEditText](../android.inputmethodservice/ExtractEditText.md), [MultiAutoCompleteTextView](../android.widget/MultiAutoCompleteTextView.md), [RadioButton](../android.widget/RadioButton.md), [Switch](../android.widget/Switch.md), and 2 others. |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AutoCompleteTextView](../android.widget/AutoCompleteTextView.md) | An editable text view that shows completion suggestions automatically while the user is typing. | | [Button](../android.widget/Button.md) | A user interface element the user can tap or click to perform an action. | | [CheckBox](../android.widget/CheckBox.md) | A checkbox is a specific type of two-states button that can be either checked or unchecked. | | [CheckedTextView](../android.widget/CheckedTextView.md) | An extension to [TextView](../android.widget/TextView.md) that supports the [Checkable](../android.widget/Checkable.md) interface and displays. | | [Chronometer](../android.widget/Chronometer.md) | Class that implements a simple timer. | | [CompoundButton](../android.widget/CompoundButton.md) | A button with two states, checked and unchecked. | | [DigitalClock](../android.widget/DigitalClock.md) | Like AnalogClock, but digital. | | [EditText](../android.widget/EditText.md) | A user interface element for entering and modifying text. | | [ExtractEditText](../android.inputmethodservice/ExtractEditText.md) | \* Specialization of [EditText](../android.widget/EditText.md) for showing and interacting with the extracted text in a full-screen input method. | | [MultiAutoCompleteTextView](../android.widget/MultiAutoCompleteTextView.md) | An editable text view, extending [AutoCompleteTextView](../android.widget/AutoCompleteTextView.md), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. | | [RadioButton](../android.widget/RadioButton.md) | A radio button is a two-states button that can be either checked or unchecked. | | [Switch](../android.widget/Switch.md) | A Switch is a two-state toggle widget. | | [TextClock](../android.widget/TextClock.md) | `TextClock`can display the current date and/or time as a formatted string. | | [ToggleButton](../android.widget/ToggleButton.md) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the view tree is about to be drawn.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreDraw](../android/view/ViewTreeObserver.OnPreDrawListener.md))`()` Callback method to be invoked when the view tree is about to be drawn. |

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

- [android.view.View#onMeasure](View.md))
- [android.view.View#onLayout](View.md))
- [android.view.View#onDraw](View.md))
