# DatePickerDialog.OnDateSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateSetListener

Kotlin| [Java](../android/app/DatePickerDialog.OnDateSetListener.md) 
| --- | --- |

```
interface OnDateSetListener
```

| [android.app.DatePickerDialog.OnDateSetListener](../android/app/DatePickerDialog.OnDateSetListener.md) |

The listener used to indicate the user has finished selecting a date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDateSet](../android/app/DatePickerDialog.OnDateSetListener.md))`(`view:` ` [DatePicker](../android.widget/DatePicker.md)!`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
| `view` | [DatePicker](../android.widget/DatePicker.md)!:the picker associated with the dialog |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected month (0-11 for compatibility with [Calendar.MONTH](../java.util/Calendar.md)) |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the selected day of the month (1-31, depending on month) |
