# DialogInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DialogInterface

Kotlin| [Java](../android/content/DialogInterface.md) 
| --- | --- |

```
interface DialogInterface
```

| [android.content.DialogInterface](../android/content/DialogInterface.md) |

| Known Direct Subclasses [AlertDialog](../android/app/AlertDialog.md), [Dialog](../android/app/Dialog.md), [MockDialogInterface](../android/test/mock/MockDialogInterface.md) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [AlertDialog](../android/app/AlertDialog.md) | A subclass of Dialog that can display one, two or three buttons. | | [Dialog](../android/app/Dialog.md) | Base class for Dialogs. | | [MockDialogInterface](../android/test/mock/MockDialogInterface.md) | A mock [android.content.DialogInterface](../android/content/DialogInterface.md) class. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AlertDialog](../android/app/AlertDialog.md), [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md), [DatePickerDialog](../android/app/DatePickerDialog.md), [DatePickerDialog](../android/app/DatePickerDialog.md), [Presentation](../android/app/Presentation.md), [ProgressDialog](../android/app/ProgressDialog.md), [ProgressDialog](../android/app/ProgressDialog.md), [TimePickerDialog](../android/app/TimePickerDialog.md) [TimePickerDialog](../android/app/TimePickerDialog.md) |-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [AlertDialog](../android/app/AlertDialog.md) | A subclass of Dialog that can display one, two or three buttons. | | [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. | | [DatePickerDialog](../android/app/DatePickerDialog.md) | A simple dialog containing an [android.widget.DatePicker](../android/widget/DatePicker.md). | | [DatePickerDialog](../android/app/DatePickerDialog.md) | A simple dialog containing an [android.widget.DatePicker](../android/widget/DatePicker.md). | | [Presentation](../android/app/Presentation.md) | Base class for presentations. | | [ProgressDialog](../android/app/ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. | | [ProgressDialog](../android/app/ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](../android/app/TimePickerDialog.md) | A dialog that prompts the user for the time of day using a [TimePicker](../android/widget/TimePicker.md). | | [TimePickerDialog](../android/app/TimePickerDialog.md) | A dialog that prompts the user for the time of day using a [TimePicker](../android/widget/TimePicker.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface that defines a dialog-type class that can be shown, dismissed, or canceled, and may have buttons that can be clicked.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnCancelListener](../android/content/DialogInterface.OnCancelListener.md) Interface used to allow the creator of a dialog to run some code when the dialog is canceled. |
| abstract | [OnClickListener](../android/content/DialogInterface.OnClickListener.md) Interface used to allow the creator of a dialog to run some code when an item on the dialog is clicked. |
| abstract | [OnDismissListener](../android/content/DialogInterface.OnDismissListener.md) Interface used to allow the creator of a dialog to run some code when the dialog is dismissed. |
| --- | --- |
| abstract | [OnKeyListener](../android/content/DialogInterface.OnKeyListener.md) Interface definition for a callback to be invoked when a key event is dispatched to this dialog. |
| abstract | [OnMultiChoiceClickListener](../android/content/DialogInterface.OnMultiChoiceClickListener.md) Interface used to allow the creator of a dialog to run some code when an item in a multi-choice dialog is clicked. |
| abstract | [OnShowListener](../android/content/DialogInterface.OnShowListener.md) Interface used to allow the creator of a dialog to run some code when the dialog is shown. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](../android/content/DialogInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](../android/content/DialogInterface.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](../android/content/DialogInterface.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](../android/content/DialogInterface.md) The identifier for the negative button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](../android/content/DialogInterface.md) The identifier for the neutral button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](../android/content/DialogInterface.md) The identifier for the positive button. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/content/DialogInterface.md))`()` Cancels the dialog, invoking the [OnCancelListener](../android/content/DialogInterface.OnCancelListener.md). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](../android/content/DialogInterface.md))`()` Dismisses the dialog, invoking the [OnDismissListener](../android/content/DialogInterface.OnDismissListener.md). |

## Constants

### BUTTON1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON1: Int
```

**Deprecated:** *Use [BUTTON_POSITIVE](../android/content/DialogInterface.md)* 

 Value: -1

### BUTTON2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON2: Int
```

**Deprecated:** *Use [BUTTON_NEGATIVE](../android/content/DialogInterface.md)* 

 Value: -2

### BUTTON3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON3: Int
```

**Deprecated:** *Use [BUTTON_NEUTRAL](../android/content/DialogInterface.md)* 

 Value: -3

### BUTTON_NEGATIVE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_NEGATIVE: Int
```

The identifier for the negative button. 

 Value: -2

### BUTTON_NEUTRAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_NEUTRAL: Int
```

The identifier for the neutral button. 

 Value: -3

### BUTTON_POSITIVE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON_POSITIVE: Int
```

The identifier for the positive button. 

 Value: -1

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Cancels the dialog, invoking the [OnCancelListener](../android/content/DialogInterface.OnCancelListener.md).

The [OnDismissListener](../android/content/DialogInterface.OnDismissListener.md) may also be called if cancellation dismisses the dialog. 

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dismiss(): Unit
```

Dismisses the dialog, invoking the [OnDismissListener](../android/content/DialogInterface.OnDismissListener.md).
