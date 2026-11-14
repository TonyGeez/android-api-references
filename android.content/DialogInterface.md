# DialogInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DialogInterface

Kotlin| [Java](https://developer.android.com/reference/android/content/DialogInterface "View this page in Java") 
| --- | --- |

```
interface DialogInterface
```

| [android.content.DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface#) |

| Known Direct Subclasses [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog.html#), [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog.html#), [MockDialogInterface](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface.html#) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog.html#) | A subclass of Dialog that can display one, two or three buttons. | | [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog.html#) | Base class for Dialogs. | | [MockDialogInterface](https://developer.android.com/reference/kotlin/android/test/mock/MockDialogInterface.html#) | A mock [android.content.DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface#) class. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog.html#), [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#), [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#), [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#), [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#), [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog.html#), [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog.html#), [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) |-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog.html#) | A subclass of Dialog that can display one, two or three buttons. | | [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#) | Dialog for choosing accented characters related to a base character. | | [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#) | A simple dialog containing an [android.widget.DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#). | | [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#) | A simple dialog containing an [android.widget.DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#). | | [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation.html#) | Base class for presentations. | | [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog.html#) | A dialog showing a progress indicator and an optional text message or view. | | [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog.html#) | A dialog showing a progress indicator and an optional text message or view. | | [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) | A dialog that prompts the user for the time of day using a [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#). | | [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) | A dialog that prompts the user for the time of day using a [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface that defines a dialog-type class that can be shown, dismissed, or canceled, and may have buttons that can be clicked.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener) Interface used to allow the creator of a dialog to run some code when the dialog is canceled. |
| abstract | [OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener) Interface used to allow the creator of a dialog to run some code when an item on the dialog is clicked. |
| abstract | [OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener) Interface used to allow the creator of a dialog to run some code when the dialog is dismissed. |
| --- | --- |
| abstract | [OnKeyListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnKeyListener) Interface definition for a callback to be invoked when a key event is dispatched to this dialog. |
| abstract | [OnMultiChoiceClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnMultiChoiceClickListener) Interface used to allow the creator of a dialog to run some code when an item in a multi-choice dialog is clicked. |
| abstract | [OnShowListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnShowListener) Interface used to allow the creator of a dialog to run some code when the dialog is shown. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON1](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON1:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON2](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON2:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON3](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON3:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEGATIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_NEGATIVE:kotlin.Int) The identifier for the negative button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_NEUTRAL:kotlin.Int) The identifier for the neutral button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUTTON_POSITIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_POSITIVE:kotlin.Int) The identifier for the positive button. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/content/DialogInterface#cancel())`()` Cancels the dialog, invoking the [OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/content/DialogInterface#dismiss())`()` Dismisses the dialog, invoking the [OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener). |

## Constants

### BUTTON1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON1: Int
```

**Deprecated:** *Use [BUTTON_POSITIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_POSITIVE:kotlin.Int)* 

 Value: -1

### BUTTON2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON2: Int
```

**Deprecated:** *Use [BUTTON_NEGATIVE](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_NEGATIVE:kotlin.Int)* 

 Value: -2

### BUTTON3

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUTTON3: Int
```

**Deprecated:** *Use [BUTTON_NEUTRAL](https://developer.android.com/reference/kotlin/android/content/DialogInterface#BUTTON_NEUTRAL:kotlin.Int)* 

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

Cancels the dialog, invoking the [OnCancelListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnCancelListener).

The [OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener) may also be called if cancellation dismisses the dialog. 

### dismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun dismiss(): Unit
```

Dismisses the dialog, invoking the [OnDismissListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnDismissListener).
