# CalendarView.OnDateChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDateChangeListener

Kotlin| [Java](../android/widget/CalendarView.OnDateChangeListener.md) 
| --- | --- |

```
interface OnDateChangeListener
```

| [android.widget.CalendarView.OnDateChangeListener](../android/widget/CalendarView.OnDateChangeListener.md) |

The callback used to indicate the user changes the date.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSelectedDayChange](../android/widget/CalendarView.OnDateChangeListener.md))`(`view:` ` [CalendarView](../android/widget/CalendarView.md)`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon change of the selected day. |

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
| `view` | [CalendarView](../android/widget/CalendarView.md):The view associated with this listener. This value cannot be`null`. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year that was set. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month that was set \[0-11\]. |
| --- | --- |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month that was set. |
