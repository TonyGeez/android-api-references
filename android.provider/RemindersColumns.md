# CalendarContract.RemindersColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemindersColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.RemindersColumns "View this page in Java") 
| --- | --- |

```
protected interface RemindersColumns
```

| [android.provider.CalendarContract.RemindersColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#) |

| Known Direct Subclasses [CalendarContract.Reminders](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Reminders) |--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------| | [CalendarContract.Reminders](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Reminders) | Fields and helpers for accessing reminders for an event. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#EVENT_ID:kotlin.String) The event the reminder belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METHOD](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD:kotlin.String) The alarm method, as set on the server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_ALARM](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALARM:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_ALERT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALERT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_DEFAULT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_DEFAULT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_EMAIL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_EMAIL:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METHOD_SMS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_SMS:kotlin.Int) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTES](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#MINUTES:kotlin.String) The minutes prior to the event that the alarm should ring. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTES_DEFAULT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#MINUTES_DEFAULT:kotlin.Int) Passing this as a minutes value will use the default reminder minutes. |
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

The alarm method, as set on the server. [METHOD_DEFAULT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_DEFAULT:kotlin.Int), [METHOD_ALERT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALERT:kotlin.Int), [METHOD_EMAIL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_EMAIL:kotlin.Int), [METHOD_SMS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_SMS:kotlin.Int) and [METHOD_ALARM](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALARM:kotlin.Int) are possible values; the device will only process [METHOD_DEFAULT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_DEFAULT:kotlin.Int) and [METHOD_ALERT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALERT:kotlin.Int) reminders (the other types are simply stored so we can send the same reminder info back to the server when we make changes). 

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
