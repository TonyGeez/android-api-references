# TimePicker.OnTimeChangedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimeChangedListener

Kotlin| [Java](../android/widget/TimePicker.OnTimeChangedListener.md) 
| --- | --- |

```
interface OnTimeChangedListener
```

| [android.widget.TimePicker.OnTimeChangedListener](../android/widget/TimePicker.OnTimeChangedListener.md) |

| Known Direct Subclasses [TimePickerDialog](../android.app/TimePickerDialog.md) |-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [TimePickerDialog](../android.app/TimePickerDialog.md) | A dialog that prompts the user for the time of day using a [TimePicker](TimePicker.md). | |
| --- | --- | --- | --- | --- | --- | --- |

The callback interface used to indicate the time has been adjusted.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimeChanged](../android/widget/TimePicker.OnTimeChangedListener.md))`(`view:` ` [TimePicker](TimePicker.md)!`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
| `view` | [TimePicker](TimePicker.md)!:The view associated with this listener. |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current hour. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current minute. |
| --- | --- |
