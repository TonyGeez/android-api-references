# DatePickerDialog.OnDateSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateSetListener

Kotlin| [Java](https://developer.android.com/reference/android/app/DatePickerDialog.OnDateSetListener "View this page in Java") 

```
interface OnDateSetListener
```

| [android.app.DatePickerDialog.OnDateSetListener](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.OnDateSetListener#) |

The listener used to indicate the user has finished selecting a date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDateSet](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.OnDateSetListener#onDateSet(android.widget.DatePicker,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`view:` ` [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#)!`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public methods

### onDateSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDateSet(
    view: DatePicker!, 
    year: Int, 
    month: Int, 
    dayOfMonth: Int
): Unit
```

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [DatePicker](https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#)!:the picker associated with the dialog |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected month (0-11 for compatibility with [Calendar.MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar.html#MONTH:kotlin.Int)) |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected day of the month (1-31, depending on month) |
