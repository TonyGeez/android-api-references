# DatePicker.OnDateChangedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/DatePicker.OnDateChangedListener "View this page in Java") 

```
interface OnDateChangedListener
```

| [android.widget.DatePicker.OnDateChangedListener](https://developer.android.com/reference/kotlin/android/widget/DatePicker.OnDateChangedListener#) |

| Known Direct Subclasses [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#) |-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------| | [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.html#) | A simple dialog containing an [android.widget.DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker). | |

The callback used to indicate the user changed the date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDateChanged](https://developer.android.com/reference/kotlin/android/widget/DatePicker.OnDateChangedListener#onDateChanged(android.widget.DatePicker,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`view:` ` [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker)!`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `monthOfYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon a date change. |

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
| `view` | [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker)!:The view associated with this listener. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year that was set. |
| `monthOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month that was set (0-11) for compatibility with [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#). |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month that was set. |
