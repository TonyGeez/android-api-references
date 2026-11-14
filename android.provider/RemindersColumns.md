# CalendarContract.RemindersColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemindersColumns

Kotlin| [Java](../android/provider/CalendarContract.RemindersColumns.md) 
| --- | --- |

```
protected interface RemindersColumns
```

| [android.provider.CalendarContract.RemindersColumns](../android/provider/CalendarContract.RemindersColumns.md) |

| Known Direct Subclasses [CalendarContract.Reminders](../android/provider/CalendarContract.Reminders.md) |--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [CalendarContract.Reminders](../android/provider/CalendarContract.Reminders.md) | Fields and helpers for accessing reminders for an event. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](../android/provider/CalendarContract.RemindersColumns.md) The event the reminder belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METHOD](../android/provider/CalendarContract.RemindersColumns.md) The alarm method, as set on the server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_ALARM](../android/provider/CalendarContract.RemindersColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_ALERT](../android/provider/CalendarContract.RemindersColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_DEFAULT](../android/provider/CalendarContract.RemindersColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_EMAIL](../android/provider/CalendarContract.RemindersColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_SMS](../android/provider/CalendarContract.RemindersColumns.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTES](../android/provider/CalendarContract.RemindersColumns.md) The minutes prior to the event that the alarm should ring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTES_DEFAULT](../android/provider/CalendarContract.RemindersColumns.md) Passing this as a minutes value will use the default reminder minutes. |
| --- | --- |

## Constants

### EVENT_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ID: String
```

The event the reminder belongs to. Column name.

Type: INTEGER (foreign key to the Events table) 

 Value: "event_id"

### METHOD

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD: String
```

The alarm method, as set on the server. [METHOD_DEFAULT](../android/provider/CalendarContract.RemindersColumns.md), [METHOD_ALERT](../android/provider/CalendarContract.RemindersColumns.md), [METHOD_EMAIL](../android/provider/CalendarContract.RemindersColumns.md), [METHOD_SMS](../android/provider/CalendarContract.RemindersColumns.md) and [METHOD_ALARM](../android/provider/CalendarContract.RemindersColumns.md) are possible values; the device will only process [METHOD_DEFAULT](../android/provider/CalendarContract.RemindersColumns.md) and [METHOD_ALERT](../android/provider/CalendarContract.RemindersColumns.md) reminders (the other types are simply stored so we can send the same reminder info back to the server when we make changes). 

 Value: "method"

### METHOD_ALARM

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_ALARM: Int
```  

 Value: 4

### METHOD_ALERT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_ALERT: Int
```  

 Value: 1

### METHOD_DEFAULT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_DEFAULT: Int
```  

 Value: 0

### METHOD_EMAIL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_EMAIL: Int
```  

 Value: 2

### METHOD_SMS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METHOD_SMS: Int
```  

 Value: 3

### MINUTES

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTES: String
```

The minutes prior to the event that the alarm should ring. -1 specifies that we should use the default value for the system. Column name.

Type: INTEGER 

 Value: "minutes"

### MINUTES_DEFAULT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTES_DEFAULT: Int
```

Passing this as a minutes value will use the default reminder minutes. 

 Value: -1
