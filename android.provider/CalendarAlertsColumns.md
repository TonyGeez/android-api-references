# CalendarContract.CalendarAlertsColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarAlertsColumns

Kotlin | [Java](../android/provider/CalendarContract.CalendarAlertsColumns.md) 
| --- | --- |

```
protected interface CalendarAlertsColumns
```

| [android.provider.CalendarContract.CalendarAlertsColumns](../android/provider/CalendarContract.CalendarAlertsColumns.md) |

| Known Direct Subclasses [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md) | Fields and helpers for accessing calendar alerts information. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALARM_TIME](../android/provider/CalendarContract.CalendarAlertsColumns.md) The alarm time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BEGIN](../android/provider/CalendarContract.CalendarAlertsColumns.md) The start time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CREATION_TIME](../android/provider/CalendarContract.CalendarAlertsColumns.md) The creation time of this database entry, in UTC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_SORT_ORDER](../android/provider/CalendarContract.CalendarAlertsColumns.md) The default sort order for this alerts queries |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [END](../android/provider/CalendarContract.CalendarAlertsColumns.md) The end time of the event, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_ID](../android/provider/CalendarContract.CalendarAlertsColumns.md) The event that the alert belongs to. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MINUTES](../android/provider/CalendarContract.CalendarAlertsColumns.md) The number of minutes that this alarm precedes the start time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTIFY_TIME](../android/provider/CalendarContract.CalendarAlertsColumns.md) The time that the notification was created by the Calendar app, in UTC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RECEIVED_TIME](../android/provider/CalendarContract.CalendarAlertsColumns.md) The time that the alarm broadcast was received by the Calendar app, in UTC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATE](../android/provider/CalendarContract.CalendarAlertsColumns.md) The state of this alert. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISMISSED](../android/provider/CalendarContract.CalendarAlertsColumns.md) Once the user has dismissed the notification the alert's state should be set to dismissed so it is not fired again. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FIRED](../android/provider/CalendarContract.CalendarAlertsColumns.md) After a notification for an alert has been created it should be updated to fired. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SCHEDULED](../android/provider/CalendarContract.CalendarAlertsColumns.md) An alert begins in this state when it is first created. |

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

The state of this alert. It starts out as [STATE_SCHEDULED](../android/provider/CalendarContract.CalendarAlertsColumns.md), then when the alarm goes off, it changes to [STATE_FIRED](../android/provider/CalendarContract.CalendarAlertsColumns.md), and then when the user dismisses the alarm it changes to [STATE_DISMISSED](../android/provider/CalendarContract.CalendarAlertsColumns.md). Column name.

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
