# CalendarContract.CalendarColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarColumns

Kotlin| [Java](../android/provider/CalendarContract.CalendarColumns.md) 
| --- | --- |

```
protected interface CalendarColumns
```

| [android.provider.CalendarContract.CalendarColumns](../android/provider/CalendarContract.CalendarColumns.md) |

| Known Direct Subclasses [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md), [CalendarContract.CalendarEntity](../android/provider/CalendarContract.CalendarEntity.md), [CalendarContract.Calendars](../android/provider/CalendarContract.Calendars.md), [CalendarContract.Events](../android/provider/CalendarContract.Events.md), [CalendarContract.Instances](../android/provider/CalendarContract.Instances.md) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [CalendarContract.CalendarAlerts](../android/provider/CalendarContract.CalendarAlerts.md) | Fields and helpers for accessing calendar alerts information. | | [CalendarContract.CalendarEntity](../android/provider/CalendarContract.CalendarEntity.md) | Class that represents a Calendar Entity. | | [CalendarContract.Calendars](../android/provider/CalendarContract.Calendars.md) | Constants and helpers for the Calendars table, which contains details for individual calendars. | | [CalendarContract.Events](../android/provider/CalendarContract.Events.md) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.Instances](../android/provider/CalendarContract.Instances.md) | Fields and helpers for interacting with Instances. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns specific to the Calendars Uri that other Uris can query.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_ATTENDEE_TYPES](../android/provider/CalendarContract.CalendarColumns.md) A comma separated list of attendee types supported for this calendar in the format "#,#,#". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_AVAILABILITY](../android/provider/CalendarContract.CalendarColumns.md) A comma separated list of availability types supported for this calendar in the format "#,#,#". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_REMINDERS](../android/provider/CalendarContract.CalendarColumns.md) A comma separated list of reminder methods supported for this calendar in the format "#,#,#". |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_ACCESS_LEVEL](../android/provider/CalendarContract.CalendarColumns.md) The level of access that the user has for the calendar |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_COLOR](../android/provider/CalendarContract.CalendarColumns.md) The color of the calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_COLOR_KEY](../android/provider/CalendarContract.CalendarColumns.md) A key for looking up a color from the [Colors](../android/provider/CalendarContract.Colors.md) table. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_DISPLAY_NAME](../android/provider/CalendarContract.CalendarColumns.md) The display name of the calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_TIME_ZONE](../android/provider/CalendarContract.CalendarColumns.md) The time zone the calendar is associated with. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_CONTRIBUTOR](../android/provider/CalendarContract.CalendarColumns.md) Full access to modify the calendar, but not the access control settings |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_EDITOR](../android/provider/CalendarContract.CalendarColumns.md) Full access to modify the calendar, but not the access control settings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_FREEBUSY](../android/provider/CalendarContract.CalendarColumns.md) Can only see free/busy information about the calendar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_NONE](../android/provider/CalendarContract.CalendarColumns.md) Cannot access the calendar |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_OVERRIDE](../android/provider/CalendarContract.CalendarColumns.md) not used |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_OWNER](../android/provider/CalendarContract.CalendarColumns.md) Full access to the calendar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_READ](../android/provider/CalendarContract.CalendarColumns.md) Can read all event details |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_RESPOND](../android/provider/CalendarContract.CalendarColumns.md) Can reply yes/no/maybe to an event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_ROOT](../android/provider/CalendarContract.CalendarColumns.md) Domain admin |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_MODIFY_TIME_ZONE](../android/provider/CalendarContract.CalendarColumns.md) Can the organizer modify the time zone of the event? Column name. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_ORGANIZER_RESPOND](../android/provider/CalendarContract.CalendarColumns.md) Can the organizer respond to the event? If no, the status of the organizer should not be shown by the UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_PRIMARY](../android/provider/CalendarContract.CalendarColumns.md) Is this the primary calendar for this account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_REMINDERS](../android/provider/CalendarContract.CalendarColumns.md) The maximum number of reminders allowed for an event. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [OWNER_ACCOUNT](../android/provider/CalendarContract.CalendarColumns.md) The owner account for this calendar, based on the calendar feed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EVENTS](../android/provider/CalendarContract.CalendarColumns.md) Is this calendar synced and are its events stored on the device? 0 - Do not sync this calendar or store events for this calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VISIBLE](../android/provider/CalendarContract.CalendarColumns.md) Is the calendar selected to be displayed? 0 - do not show events associated with this calendar. |
| --- | --- |

## Constants

### ALLOWED_ATTENDEE_TYPES

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_ATTENDEE_TYPES: String
```

A comma separated list of attendee types supported for this calendar in the format "#,#,#". Valid types are [Attendees.TYPE_NONE](../android/provider/CalendarContract.AttendeesColumns.md), [Attendees.TYPE_OPTIONAL](../android/provider/CalendarContract.AttendeesColumns.md), [Attendees.TYPE_REQUIRED](../android/provider/CalendarContract.AttendeesColumns.md), [Attendees.TYPE_RESOURCE](../android/provider/CalendarContract.AttendeesColumns.md). Setting this field to only [Attendees.TYPE_NONE](../android/provider/CalendarContract.AttendeesColumns.md) should be used to indicate that changing the attendee type is not supported. 

 Value: "allowedAttendeeTypes"

### ALLOWED_AVAILABILITY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_AVAILABILITY: String
```

A comma separated list of availability types supported for this calendar in the format "#,#,#". Valid types are [Events.AVAILABILITY_BUSY](../android/provider/CalendarContract.EventsColumns.md), [Events.AVAILABILITY_FREE](../android/provider/CalendarContract.EventsColumns.md), [Events.AVAILABILITY_TENTATIVE](../android/provider/CalendarContract.EventsColumns.md). Setting this field to only [Events.AVAILABILITY_BUSY](../android/provider/CalendarContract.EventsColumns.md) should be used to indicate that changing the availability is not supported. 

 Value: "allowedAvailability"

### ALLOWED_REMINDERS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_REMINDERS: String
```

A comma separated list of reminder methods supported for this calendar in the format "#,#,#". Valid types are [Reminders.METHOD_DEFAULT](../android/provider/CalendarContract.RemindersColumns.md), [Reminders.METHOD_ALERT](../android/provider/CalendarContract.RemindersColumns.md), [Reminders.METHOD_EMAIL](../android/provider/CalendarContract.RemindersColumns.md), [Reminders.METHOD_SMS](../android/provider/CalendarContract.RemindersColumns.md), [Reminders.METHOD_ALARM](../android/provider/CalendarContract.RemindersColumns.md). Column name.

Type: TEXT 

 Value: "allowedReminders"

### CALENDAR_ACCESS_LEVEL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_ACCESS_LEVEL: String
```

The level of access that the user has for the calendar

Type: INTEGER (one of the values below) 

 Value: "calendar_access_level"

### CALENDAR_COLOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_COLOR: String
```

The color of the calendar. This should only be updated by the sync adapter, not other apps, as changing a calendar's color can adversely affect its display.

Type: INTEGER (color value) 

 Value: "calendar_color"

### CALENDAR_COLOR_KEY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_COLOR_KEY: String
```

A key for looking up a color from the [Colors](../android/provider/CalendarContract.Colors.md) table. NULL or an empty string are reserved for indicating that the calendar does not use a key for looking up the color. The provider will update [CALENDAR_COLOR](../android/provider/CalendarContract.CalendarColumns.md) automatically when a valid key is written to this column. The key must reference an existing row of the [Colors](../android/provider/CalendarContract.Colors.md) table. @see Colors

Type: TEXT 

 Value: "calendar_color_index"

### CALENDAR_DISPLAY_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_DISPLAY_NAME: String
```

The display name of the calendar. Column name.

Type: TEXT 

 Value: "calendar_displayName"

### CALENDAR_TIME_ZONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALENDAR_TIME_ZONE: String
```

The time zone the calendar is associated with.

Type: TEXT 

 Value: "calendar_timezone"

### CAL_ACCESS_CONTRIBUTOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_CONTRIBUTOR: Int
```

Full access to modify the calendar, but not the access control settings 

 Value: 500

### CAL_ACCESS_EDITOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_EDITOR: Int
```

Full access to modify the calendar, but not the access control settings 

 Value: 600

### CAL_ACCESS_FREEBUSY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_FREEBUSY: Int
```

Can only see free/busy information about the calendar 

 Value: 100

### CAL_ACCESS_NONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_NONE: Int
```

Cannot access the calendar 

 Value: 0

### CAL_ACCESS_OVERRIDE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_OVERRIDE: Int
```

not used 

 Value: 400

### CAL_ACCESS_OWNER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_OWNER: Int
```

Full access to the calendar 

 Value: 700

### CAL_ACCESS_READ

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_READ: Int
```

Can read all event details 

 Value: 200

### CAL_ACCESS_RESPOND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_RESPOND: Int
```

Can reply yes/no/maybe to an event 

 Value: 300

### CAL_ACCESS_ROOT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_ACCESS_ROOT: Int
```

Domain admin 

 Value: 800

### CAN_MODIFY_TIME_ZONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAN_MODIFY_TIME_ZONE: String
```

Can the organizer modify the time zone of the event? Column name.

Type: INTEGER (boolean) 

 Value: "canModifyTimeZone"

### CAN_ORGANIZER_RESPOND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAN_ORGANIZER_RESPOND: String
```

Can the organizer respond to the event? If no, the status of the organizer should not be shown by the UI. Defaults to 1. Column name.

Type: INTEGER (boolean) 

 Value: "canOrganizerRespond"

### IS_PRIMARY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_PRIMARY: String
```

Is this the primary calendar for this account. If this column is not explicitly set, the provider will return 1 if [Calendars.ACCOUNT_NAME](../android/provider/CalendarContract.SyncColumns.md) is equal to [Calendars.OWNER_ACCOUNT](../android/provider/CalendarContract.CalendarColumns.md). 

 Value: "isPrimary"

### MAX_REMINDERS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_REMINDERS: String
```

The maximum number of reminders allowed for an event. Column name.

Type: INTEGER 

 Value: "maxReminders"

### OWNER_ACCOUNT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OWNER_ACCOUNT: String
```

The owner account for this calendar, based on the calendar feed. This will be different from the _SYNC_ACCOUNT for delegated calendars. Column name.

Type: String 

 Value: "ownerAccount"

### SYNC_EVENTS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EVENTS: String
```

Is this calendar synced and are its events stored on the device? 0 - Do not sync this calendar or store events for this calendar. 1 - Sync down events for this calendar.

Type: INTEGER (boolean) 

 Value: "sync_events"

### VISIBLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VISIBLE: String
```

Is the calendar selected to be displayed? 0 - do not show events associated with this calendar. 1 - show events associated with this calendar

Type: INTEGER (boolean) 

 Value: "visible"
