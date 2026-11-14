# DatePicker.OnDateChangedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateChangedListener

Kotlin| [Java](../android/widget/DatePicker.OnDateChangedListener.md) 
| --- | --- |

```
interface OnDateChangedListener
```

| [android.widget.DatePicker.OnDateChangedListener](../android/widget/DatePicker.OnDateChangedListener.md) |

| Known Direct Subclasses [DatePickerDialog](../android/app/DatePickerDialog.md) |-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------| | [DatePickerDialog](../android/app/DatePickerDialog.md) | A simple dialog containing an [android.widget.DatePicker](../android/widget/DatePicker.md). | |
| --- | --- | --- | --- | --- | --- | --- |

The callback used to indicate the user changed the date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDateChanged](../android/widget/DatePicker.OnDateChangedListener.md))`(`view:` ` [DatePicker](../android/widget/DatePicker.md)!`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `monthOfYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon a date change. |

## Public methods

### onDateChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDateChanged(
    view: DatePicker!, 
    year: Int, 
    monthOfYear: Int, 
    dayOfMonth: Int
): Unit
```

Called upon a date change.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [DatePicker](../android/widget/DatePicker.md)!:The view associated with this listener. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year that was set. |
| `monthOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month that was set (0-11) for compatibility with [java.util.Calendar](../java/util/Calendar.md). |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month that was set. |
