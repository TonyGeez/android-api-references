# CalendarView.OnDateChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/CalendarView.OnDateChangeListener "View this page in Java") 

```
interface OnDateChangeListener
```

| [android.widget.CalendarView.OnDateChangeListener](https://developer.android.com/reference/kotlin/android/widget/CalendarView.OnDateChangeListener#) |

The callback used to indicate the user changes the date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSelectedDayChange](https://developer.android.com/reference/kotlin/android/widget/CalendarView.OnDateChangeListener#onSelectedDayChange(android.widget.CalendarView,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`view:` ` [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView)`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon change of the selected day. |

## Public methods

### onSelectedDayChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSelectedDayChange(
    view: CalendarView, 
    year: Int, 
    month: Int, 
    dayOfMonth: Int
): Unit
```

Called upon change of the selected day.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [CalendarView](https://developer.android.com/reference/kotlin/android/widget/CalendarView):The view associated with this listener. This value cannot be`null`. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year that was set. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month that was set \[0-11\]. |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month that was set. |
