# TimePicker.OnTimeChangedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimeChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/TimePicker.OnTimeChangedListener "View this page in Java") 
| --- | --- |

```
interface OnTimeChangedListener
```

| [android.widget.TimePicker.OnTimeChangedListener](https://developer.android.com/reference/kotlin/android/widget/TimePicker.OnTimeChangedListener#) |

| Known Direct Subclasses [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) |-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.html#) | A dialog that prompts the user for the time of day using a [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker). | |
| --- | --- | --- | --- | --- | --- | --- |

The callback interface used to indicate the time has been adjusted.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimeChanged](https://developer.android.com/reference/kotlin/android/widget/TimePicker.OnTimeChangedListener#onTimeChanged(android.widget.TimePicker,%20kotlin.Int,%20kotlin.Int))`(`view:` ` [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker)!`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public methods

### onTimeChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTimeChanged(
    view: TimePicker!, 
    hourOfDay: Int, 
    minute: Int
): Unit
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| `view` | [TimePicker](https://developer.android.com/reference/kotlin/android/widget/TimePicker)!:The view associated with this listener. |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current hour. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current minute. |
| --- | --- |
