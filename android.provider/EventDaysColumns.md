# CalendarContract.EventDaysColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventDaysColumns

Kotlin| [Java](../android/provider/CalendarContract.EventDaysColumns.md) 
| --- | --- |

```
protected interface EventDaysColumns
```

| [android.provider.CalendarContract.EventDaysColumns](../android/provider/CalendarContract.EventDaysColumns.md) |

| Known Direct Subclasses [CalendarContract.EventDays](../android/provider/CalendarContract.EventDays.md) |--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------| | [CalendarContract.EventDays](../android/provider/CalendarContract.EventDays.md) | Fields and helpers for querying for a list of days that contain events. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ENDDAY](../android/provider/CalendarContract.EventDaysColumns.md) The Julian ending day number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STARTDAY](../android/provider/CalendarContract.EventDaysColumns.md) The Julian starting day number. |

## Constants

### ENDDAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENDDAY: String
```

The Julian ending day number. Column name.

Type: INTEGER (int) 

 Value: "endDay"

### STARTDAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STARTDAY: String
```

The Julian starting day number. Column name.

Type: INTEGER (int) 

 Value: "startDay"
