# TimePickerDialog.OnTimeSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnTimeSetListener

Kotlin| [Java](../android/app/TimePickerDialog.OnTimeSetListener.md) 
| --- | --- |

```
interface OnTimeSetListener
```

| [android.app.TimePickerDialog.OnTimeSetListener](../android/app/TimePickerDialog.OnTimeSetListener.md) |

The callback interface used to indicate the user is done filling in the time (e.g. they clicked on the 'OK' button).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTimeSet](../android/app/TimePickerDialog.OnTimeSetListener.md))`(`view:` ` [TimePicker](../android.widget/TimePicker.md)!`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the user is done setting a new time and the dialog has closed. |

## Public methods

### onTimeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTimeSet(
    view: TimePicker!, 
    hourOfDay: Int, 
    minute: Int
): Unit
```

Called when the user is done setting a new time and the dialog has closed.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [TimePicker](../android.widget/TimePicker.md)!:the view associated with this listener |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the hour that was set |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minute that was set |
| --- | --- |
