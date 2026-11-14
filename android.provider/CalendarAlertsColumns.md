# CalendarContract.CalendarAlertsColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarAlertsColumns

Kotlin | [Java](https://developer.android.com/reference/android/provider/CalendarContract.CalendarAlertsColumns "View this page in Java") 
| --- | --- |

```
protected interface CalendarAlertsColumns
```

| [android.provider.CalendarContract.CalendarAlertsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#) |

| Known Direct Subclasses [CalendarContract.CalendarAlerts](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlerts) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [CalendarContract.CalendarAlerts](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlerts) | Fields and helpers for accessing calendar alerts information. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALARM_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#ALARM_TIME:kotlin.String) The alarm time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BEGIN](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#BEGIN:kotlin.String) The start time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CREATION_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#CREATION_TIME:kotlin.String) The creation time of this database entry, in UTC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_SORT_ORDER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#DEFAULT_SORT_ORDER:kotlin.String) The default sort order for this alerts queries |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [END](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#END:kotlin.String) The end time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#EVENT_ID:kotlin.String) The event that the alert belongs to. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTES](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#MINUTES:kotlin.String) The number of minutes that this alarm precedes the start time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTIFY_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#NOTIFY_TIME:kotlin.String) The time that the notification was created by the Calendar app, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RECEIVED_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#RECEIVED_TIME:kotlin.String) The time that the alarm broadcast was received by the Calendar app, in UTC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE:kotlin.String) The state of this alert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISMISSED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_DISMISSED:kotlin.Int) Once the user has dismissed the notification the alert's state should be set to dismissed so it is not fired again. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FIRED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_FIRED:kotlin.Int) After a notification for an alert has been created it should be updated to fired. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SCHEDULED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_SCHEDULED:kotlin.Int) An alert begins in this state when it is first created. |

## Constants

### ALARM_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALARM_TIME: String
```

The alarm time of the event, in UTC. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "alarmTime"

### BEGIN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BEGIN: String
```

The start time of the event, in UTC. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "begin"

### CREATION_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATION_TIME: String
```

The creation time of this database entry, in UTC. Useful for debugging missed reminders. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "creationTime"

### DEFAULT_SORT_ORDER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_SORT_ORDER: String
```

The default sort order for this alerts queries 

 Value: "begin ASC,title ASC"

### END

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val END: String
```

The end time of the event, in UTC. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "end"

### EVENT_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ID: String
```

The event that the alert belongs to. Column name.

Type: INTEGER (foreign key to the Events table) 

 Value: "event_id"

### MINUTES

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MINUTES: String
```

The number of minutes that this alarm precedes the start time. Column name.

Type: INTEGER 

 Value: "minutes"

### NOTIFY_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_TIME: String
```

The time that the notification was created by the Calendar app, in UTC. Useful for debugging missed reminders. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "notifyTime"

### RECEIVED_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECEIVED_TIME: String
```

The time that the alarm broadcast was received by the Calendar app, in UTC. Useful for debugging missed reminders. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "receivedTime"

### STATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE: String
```

The state of this alert. It starts out as [STATE_SCHEDULED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_SCHEDULED:kotlin.Int), then when the alarm goes off, it changes to [STATE_FIRED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_FIRED:kotlin.Int), and then when the user dismisses the alarm it changes to [STATE_DISMISSED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns#STATE_DISMISSED:kotlin.Int). Column name.

Type: INTEGER 

 Value: "state"

### STATE_DISMISSED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISMISSED: Int
```

Once the user has dismissed the notification the alert's state should be set to dismissed so it is not fired again. 

 Value: 2

### STATE_FIRED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_FIRED: Int
```

After a notification for an alert has been created it should be updated to fired. 

 Value: 1

### STATE_SCHEDULED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SCHEDULED: Int
```

An alert begins in this state when it is first created. 

 Value: 0
