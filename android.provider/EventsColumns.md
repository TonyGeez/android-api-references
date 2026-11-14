# CalendarContract.EventsColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventsColumns

Kotlin| [Java](../android/provider/CalendarContract.EventsColumns.md) 
| --- | --- |

```
protected interface EventsColumns
```

| [android.provider.CalendarContract.EventsColumns](../android/provider/CalendarContract.EventsColumns.md) |

| Known Direct Subclasses [CalendarContract.Attendees](../android/provider/CalendarContract.Attendees.md), [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md), [CalendarContract.Events](../android/provider/CalendarContract.Events.md), [CalendarContract.EventsEntity](../android/provider/CalendarContract.EventsEntity.md), [CalendarContract.ExtendedProperties](../android/provider/CalendarContract.ExtendedProperties.md), [CalendarContract.Instances](../android/provider/CalendarContract.Instances.md), [CalendarContract.Reminders](../android/provider/CalendarContract.Reminders.md) |--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------| | [CalendarContract.Attendees](../android/provider/CalendarContract.Attendees.md) | Fields and helpers for interacting with Attendees. | | [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md) | Fields and helpers for accessing calendar alerts information. | | [CalendarContract.Events](../android/provider/CalendarContract.Events.md) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.EventsEntity](../android/provider/CalendarContract.EventsEntity.md) | Class that represents an Event Entity. | | [CalendarContract.ExtendedProperties](../android/provider/CalendarContract.ExtendedProperties.md) | Fields for accessing the Extended Properties. | | [CalendarContract.Instances](../android/provider/CalendarContract.Instances.md) | Fields and helpers for interacting with Instances. | | [CalendarContract.Reminders](../android/provider/CalendarContract.Reminders.md) | Fields and helpers for accessing reminders for an event. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns from the Events table that other tables join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_CONFIDENTIAL](../android/provider/CalendarContract.EventsColumns.md) Confidential is not used by the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_DEFAULT](../android/provider/CalendarContract.EventsColumns.md) Default access is controlled by the server and will be treated as public on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCESS_LEVEL](../android/provider/CalendarContract.EventsColumns.md) Defines how the event shows up for others when the calendar is shared. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_PRIVATE](../android/provider/CalendarContract.EventsColumns.md) Private shares the event as a free/busy slot with no details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS_PUBLIC](../android/provider/CalendarContract.EventsColumns.md) Public makes the contents visible to anyone with access to the calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALL_DAY](../android/provider/CalendarContract.EventsColumns.md) Is the event all day (time zone independent). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AVAILABILITY](../android/provider/CalendarContract.EventsColumns.md) If this event counts as busy time or is still free time that can be scheduled over. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_BUSY](../android/provider/CalendarContract.EventsColumns.md) Indicates that this event takes up time and will conflict with other events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_FREE](../android/provider/CalendarContract.EventsColumns.md) Indicates that this event is free time and will not conflict with other events. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABILITY_TENTATIVE](../android/provider/CalendarContract.EventsColumns.md) Indicates that the owner's availability may change, but should be considered busy time that will conflict. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_ID](../android/provider/CalendarContract.EventsColumns.md) The [Calendars._ID](BaseColumns.md) of the calendar the event belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_INVITE_OTHERS](../android/provider/CalendarContract.EventsColumns.md) Whether the user can invite others to the event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_APP_PACKAGE](../android/provider/CalendarContract.EventsColumns.md) The package name of the custom app that can provide a richer experience for the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_APP_URI](../android/provider/CalendarContract.EventsColumns.md) The URI used by the custom app for the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DESCRIPTION](../android/provider/CalendarContract.EventsColumns.md) The description of the event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_COLOR](../android/provider/CalendarContract.EventsColumns.md) This will be [EVENT_COLOR](../android/provider/CalendarContract.EventsColumns.md) if it is not null; otherwise, this will be [Calendars.CALENDAR_COLOR](../android/provider/CalendarContract.CalendarColumns.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DTEND](../android/provider/CalendarContract.EventsColumns.md) The time the event ends in UTC millis since epoch. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DTSTART](../android/provider/CalendarContract.EventsColumns.md) The time the event starts in UTC millis since epoch. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DURATION](../android/provider/CalendarContract.EventsColumns.md) The duration of the event in RFC2445 format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_COLOR](../android/provider/CalendarContract.EventsColumns.md) A secondary color for the individual event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_COLOR_KEY](../android/provider/CalendarContract.EventsColumns.md) A secondary color key for the individual event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_END_TIMEZONE](../android/provider/CalendarContract.EventsColumns.md) The timezone for the end time of the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_LOCATION](../android/provider/CalendarContract.EventsColumns.md) Where the event takes place. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EVENT_TIMEZONE](../android/provider/CalendarContract.EventsColumns.md) The timezone for the event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXDATE](../android/provider/CalendarContract.EventsColumns.md) The recurrence exception dates for the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXRULE](../android/provider/CalendarContract.EventsColumns.md) The recurrence exception rule for the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GUESTS_CAN_INVITE_OTHERS](../android/provider/CalendarContract.EventsColumns.md) Whether guests can invite other guests. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GUESTS_CAN_MODIFY](../android/provider/CalendarContract.EventsColumns.md) Whether guests can modify the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GUESTS_CAN_SEE_GUESTS](../android/provider/CalendarContract.EventsColumns.md) Whether guests can see the list of attendees. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_ALARM](../android/provider/CalendarContract.EventsColumns.md) Whether the event has an alarm or not. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_ATTENDEE_DATA](../android/provider/CalendarContract.EventsColumns.md) Whether the event has attendee information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_EXTENDED_PROPERTIES](../android/provider/CalendarContract.EventsColumns.md) Whether the event has extended properties or not. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_ORGANIZER](../android/provider/CalendarContract.EventsColumns.md) Are we the organizer of this event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_DATE](../android/provider/CalendarContract.EventsColumns.md) The last date this event repeats on, or NULL if it never ends. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_SYNCED](../android/provider/CalendarContract.EventsColumns.md) Used to indicate that a row is not a real event but an original copy of a locally modified event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ORGANIZER](../android/provider/CalendarContract.EventsColumns.md) Email of the organizer (owner) of the event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ORIGINAL_ALL_DAY](../android/provider/CalendarContract.EventsColumns.md) The allDay status (true or false) of the original recurring event for which this event is an exception. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ORIGINAL_ID](../android/provider/CalendarContract.EventsColumns.md) The [Events._ID](BaseColumns.md) of the original recurring event for which this event is an exception. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ORIGINAL_INSTANCE_TIME](../android/provider/CalendarContract.EventsColumns.md) The original instance time of the recurring event for which this event is an exception. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ORIGINAL_SYNC_ID](../android/provider/CalendarContract.EventsColumns.md) The _sync_id of the original recurring event for which this event is an exception. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RDATE](../android/provider/CalendarContract.EventsColumns.md) The recurrence dates for the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RRULE](../android/provider/CalendarContract.EventsColumns.md) The recurrence rule for the event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SELF_ATTENDEE_STATUS](../android/provider/CalendarContract.EventsColumns.md) This is a copy of the attendee status for the owner of this event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS](../android/provider/CalendarContract.EventsColumns.md) The event status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_CANCELED](../android/provider/CalendarContract.EventsColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_CONFIRMED](../android/provider/CalendarContract.EventsColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_TENTATIVE](../android/provider/CalendarContract.EventsColumns.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA1](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA10](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA2](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA3](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA4](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA5](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA6](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA7](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA8](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_DATA9](../android/provider/CalendarContract.EventsColumns.md) This column is available for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TITLE](../android/provider/CalendarContract.EventsColumns.md) The title of the event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [UID_2445](../android/provider/CalendarContract.EventsColumns.md) The UID for events added from the RFC 2445 iCalendar format. |

## Constants

### ACCESS_CONFIDENTIAL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_CONFIDENTIAL: Int
```

Confidential is not used by the app. 

 Value: 1

### ACCESS_DEFAULT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_DEFAULT: Int
```

Default access is controlled by the server and will be treated as public on the device. 

 Value: 0

### ACCESS_LEVEL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_LEVEL: String
```

Defines how the event shows up for others when the calendar is shared. Column name.

Type: INTEGER (One of [ACCESS_DEFAULT](../android/provider/CalendarContract.EventsColumns.md), ...) 

 Value: "accessLevel"

### ACCESS_PRIVATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_PRIVATE: Int
```

Private shares the event as a free/busy slot with no details. 

 Value: 2

### ACCESS_PUBLIC

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS_PUBLIC: Int
```

Public makes the contents visible to anyone with access to the calendar. 

 Value: 3

### ALL_DAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_DAY: String
```

Is the event all day (time zone independent). Column name.

Type: INTEGER (boolean) 

 Value: "allDay"

### AVAILABILITY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY: String
```

If this event counts as busy time or is still free time that can be scheduled over. Column name.

Type: INTEGER (One of [AVAILABILITY_BUSY](../android/provider/CalendarContract.EventsColumns.md), [AVAILABILITY_FREE](../android/provider/CalendarContract.EventsColumns.md), [AVAILABILITY_TENTATIVE](../android/provider/CalendarContract.EventsColumns.md)) 

 Value: "availability"

### AVAILABILITY_BUSY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_BUSY: Int
```

Indicates that this event takes up time and will conflict with other events. 

 Value: 0

### AVAILABILITY_FREE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_FREE: Int
```

Indicates that this event is free time and will not conflict with other events. 

 Value: 1

### AVAILABILITY_TENTATIVE

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABILITY_TENTATIVE: Int
```

Indicates that the owner's availability may change, but should be considered busy time that will conflict. 

 Value: 2

### CALENDAR_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_ID: String
```

The [Calendars._ID](BaseColumns.md) of the calendar the event belongs to. Column name.

Type: INTEGER 

 Value: "calendar_id"

### CAN_INVITE_OTHERS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAN_INVITE_OTHERS: String
```

Whether the user can invite others to the event. The GUESTS_CAN_INVITE_OTHERS is a setting that applies to an arbitrary guest, while CAN_INVITE_OTHERS indicates if the user can invite others (either through GUESTS_CAN_INVITE_OTHERS or because the user has modify access to the event). Column name.

Type: INTEGER (boolean, readonly) 

 Value: "canInviteOthers"

### CUSTOM_APP_PACKAGE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUSTOM_APP_PACKAGE: String
```

The package name of the custom app that can provide a richer experience for the event. See the ACTION TYPE [CalendarContract.ACTION_HANDLE_CUSTOM_EVENT](CalendarContract.md) for details. Column name.

Type: TEXT 

 Value: "customAppPackage"

### CUSTOM_APP_URI

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUSTOM_APP_URI: String
```

The URI used by the custom app for the event. Column name.

Type: TEXT 

 Value: "customAppUri"

### DESCRIPTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DESCRIPTION: String
```

The description of the event. Column name.

Type: TEXT 

 Value: "description"

### DISPLAY_COLOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_COLOR: String
```

This will be [EVENT_COLOR](../android/provider/CalendarContract.EventsColumns.md) if it is not null; otherwise, this will be [Calendars.CALENDAR_COLOR](../android/provider/CalendarContract.CalendarColumns.md). Read-only value. To modify, write to [EVENT_COLOR](../android/provider/CalendarContract.EventsColumns.md) or [Calendars.CALENDAR_COLOR](../android/provider/CalendarContract.CalendarColumns.md) directly.

Type: INTEGER 

 Value: "displayColor"

### DTEND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DTEND: String
```

The time the event ends in UTC millis since epoch. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "dtend"

### DTSTART

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DTSTART: String
```

The time the event starts in UTC millis since epoch. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "dtstart"

### DURATION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DURATION: String
```

The duration of the event in RFC2445 format. Column name.

Type: TEXT (duration in RFC2445 format) 

 Value: "duration"

### EVENT_COLOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_COLOR: String
```

A secondary color for the individual event. This should only be updated by the sync adapter for a given account.

Type: INTEGER 

 Value: "eventColor"

### EVENT_COLOR_KEY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_COLOR_KEY: String
```

A secondary color key for the individual event. NULL or an empty string are reserved for indicating that the event does not use a key for looking up the color. The provider will update [EVENT_COLOR](../android/provider/CalendarContract.EventsColumns.md) automatically when a valid key is written to this column. The key must reference an existing row of the [Colors](../android/provider/CalendarContract.Colors.md) table. @see Colors

Type: TEXT 

 Value: "eventColor_index"

### EVENT_END_TIMEZONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_END_TIMEZONE: String
```

The timezone for the end time of the event. Column name.

Type: TEXT 

 Value: "eventEndTimezone"

### EVENT_LOCATION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_LOCATION: String
```

Where the event takes place. Column name.

Type: TEXT 

 Value: "eventLocation"

### EVENT_TIMEZONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_TIMEZONE: String
```

The timezone for the event. Column name.

Type: TEXT 

 Value: "eventTimezone"

### EXDATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXDATE: String
```

The recurrence exception dates for the event. Column name.

Type: TEXT 

 Value: "exdate"

### EXRULE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXRULE: String
```

The recurrence exception rule for the event. Column name.

Type: TEXT 

 Value: "exrule"

### GUESTS_CAN_INVITE_OTHERS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GUESTS_CAN_INVITE_OTHERS: String
```

Whether guests can invite other guests. Column name.

Type: INTEGER (boolean) 

 Value: "guestsCanInviteOthers"

### GUESTS_CAN_MODIFY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GUESTS_CAN_MODIFY: String
```

Whether guests can modify the event. Column name.

Type: INTEGER (boolean) 

 Value: "guestsCanModify"

### GUESTS_CAN_SEE_GUESTS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GUESTS_CAN_SEE_GUESTS: String
```

Whether guests can see the list of attendees. Column name.

Type: INTEGER (boolean) 

 Value: "guestsCanSeeGuests"

### HAS_ALARM

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAS_ALARM: String
```

Whether the event has an alarm or not. Column name.

Type: INTEGER (boolean) 

 Value: "hasAlarm"

### HAS_ATTENDEE_DATA

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAS_ATTENDEE_DATA: String
```

Whether the event has attendee information. True if the event has full attendee data, false if the event has information about self only. Column name.

Type: INTEGER (boolean) 

 Value: "hasAttendeeData"

### HAS_EXTENDED_PROPERTIES

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAS_EXTENDED_PROPERTIES: String
```

Whether the event has extended properties or not. Column name.

Type: INTEGER (boolean) 

 Value: "hasExtendedProperties"

### IS_ORGANIZER

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_ORGANIZER: String
```

Are we the organizer of this event. If this column is not explicitly set, the provider will return 1 if [ORGANIZER](../android/provider/CalendarContract.EventsColumns.md) is equal to [Calendars.OWNER_ACCOUNT](../android/provider/CalendarContract.CalendarColumns.md). Column name.

Type: STRING 

 Value: "isOrganizer"

### LAST_DATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_DATE: String
```

The last date this event repeats on, or NULL if it never ends. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "lastDate"

### LAST_SYNCED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_SYNCED: String
```

Used to indicate that a row is not a real event but an original copy of a locally modified event. A copy is made when an event changes from non-dirty to dirty and the event is on a calendar with [Calendars.CAN_PARTIALLY_UPDATE](../android/provider/CalendarContract.SyncColumns.md) set to 1. This copy does not get expanded in the instances table and is only visible in queries made by a sync adapter. The copy gets removed when the event is changed back to non-dirty by a sync adapter.

Type: INTEGER (boolean) 

 Value: "lastSynced"

### ORGANIZER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORGANIZER: String
```

Email of the organizer (owner) of the event. Column name.

Type: STRING 

 Value: "organizer"

### ORIGINAL_ALL_DAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGINAL_ALL_DAY: String
```

The allDay status (true or false) of the original recurring event for which this event is an exception. Column name.

Type: INTEGER (boolean) 

 Value: "originalAllDay"

### ORIGINAL_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGINAL_ID: String
```

The [Events._ID](BaseColumns.md) of the original recurring event for which this event is an exception. Column name.

Type: TEXT 

 Value: "original_id"

### ORIGINAL_INSTANCE_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGINAL_INSTANCE_TIME: String
```

The original instance time of the recurring event for which this event is an exception. Column name.

Type: INTEGER (long; millis since epoch) 

 Value: "originalInstanceTime"

### ORIGINAL_SYNC_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIGINAL_SYNC_ID: String
```

The _sync_id of the original recurring event for which this event is an exception. The provider should keep the original_id in sync when this is updated. Column name.

Type: TEXT 

 Value: "original_sync_id"

### RDATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RDATE: String
```

The recurrence dates for the event. Column name.

Type: TEXT 

 Value: "rdate"

### RRULE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RRULE: String
```

The recurrence rule for the event. Column name.

Type: TEXT 

 Value: "rrule"

### SELF_ATTENDEE_STATUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SELF_ATTENDEE_STATUS: String
```

This is a copy of the attendee status for the owner of this event. This field is copied here so that we can efficiently filter out events that are declined without having to look in the Attendees table. Column name.

Type: INTEGER (int) 

 Value: "selfAttendeeStatus"

### STATUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS: String
```

The event status. Column name.

Type: INTEGER (one of [STATUS_TENTATIVE](../android/provider/CalendarContract.EventsColumns.md)...) 

 Value: "eventStatus"

### STATUS_CANCELED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_CANCELED: Int
```  

 Value: 2

### STATUS_CONFIRMED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_CONFIRMED: Int
```  

 Value: 1

### STATUS_TENTATIVE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_TENTATIVE: Int
```  

 Value: 0

### SYNC_DATA1

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA1: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data1"

### SYNC_DATA10

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA10: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data10"

### SYNC_DATA2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA2: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data2"

### SYNC_DATA3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA3: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data3"

### SYNC_DATA4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA4: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data4"

### SYNC_DATA5

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA5: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data5"

### SYNC_DATA6

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA6: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data6"

### SYNC_DATA7

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA7: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data7"

### SYNC_DATA8

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA8: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data8"

### SYNC_DATA9

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_DATA9: String
```

This column is available for use by sync adapters. Column name.

Type: TEXT 

 Value: "sync_data9"

### TITLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLE: String
```

The title of the event. Column name.

Type: TEXT 

 Value: "title"

### UID_2445

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UID_2445: String
```

The UID for events added from the RFC 2445 iCalendar format. Column name.

Type: TEXT 

 Value: "uid2445"
