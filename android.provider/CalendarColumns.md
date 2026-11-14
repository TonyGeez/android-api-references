# CalendarContract.CalendarColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.CalendarColumns "View this page in Java") 

```
protected interface CalendarColumns
```

| [android.provider.CalendarContract.CalendarColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#) |

| Known Direct Subclasses [CalendarContract.CalendarAlerts](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlerts), [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity), [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars), [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events), [CalendarContract.Instances](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Instances) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [CalendarContract.CalendarAlerts](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlerts) | Fields and helpers for accessing calendar alerts information. | | [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity) | Class that represents a Calendar Entity. | | [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars) | Constants and helpers for the Calendars table, which contains details for individual calendars. | | [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.Instances](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Instances) | Fields and helpers for interacting with Instances. | |

Columns specific to the Calendars Uri that other Uris can query.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_ATTENDEE_TYPES](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#ALLOWED_ATTENDEE_TYPES:kotlin.String) A comma separated list of attendee types supported for this calendar in the format "#,#,#". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_AVAILABILITY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#ALLOWED_AVAILABILITY:kotlin.String) A comma separated list of availability types supported for this calendar in the format "#,#,#". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ALLOWED_REMINDERS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#ALLOWED_REMINDERS:kotlin.String) A comma separated list of reminder methods supported for this calendar in the format "#,#,#". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_ACCESS_LEVEL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_ACCESS_LEVEL:kotlin.String) The level of access that the user has for the calendar |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_COLOR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_COLOR:kotlin.String) The color of the calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_COLOR_KEY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_COLOR_KEY:kotlin.String) A key for looking up a color from the [Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) table. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_DISPLAY_NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_DISPLAY_NAME:kotlin.String) The display name of the calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALENDAR_TIME_ZONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_TIME_ZONE:kotlin.String) The time zone the calendar is associated with. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_CONTRIBUTOR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_CONTRIBUTOR:kotlin.Int) Full access to modify the calendar, but not the access control settings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_EDITOR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_EDITOR:kotlin.Int) Full access to modify the calendar, but not the access control settings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_FREEBUSY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_FREEBUSY:kotlin.Int) Can only see free/busy information about the calendar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_NONE:kotlin.Int) Cannot access the calendar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_OVERRIDE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_OVERRIDE:kotlin.Int) not used |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_OWNER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_OWNER:kotlin.Int) Full access to the calendar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_READ](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_READ:kotlin.Int) Can read all event details |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_RESPOND](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_RESPOND:kotlin.Int) Can reply yes/no/maybe to an event |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAL_ACCESS_ROOT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAL_ACCESS_ROOT:kotlin.Int) Domain admin |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_MODIFY_TIME_ZONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAN_MODIFY_TIME_ZONE:kotlin.String) Can the organizer modify the time zone of the event? Column name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_ORGANIZER_RESPOND](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CAN_ORGANIZER_RESPOND:kotlin.String) Can the organizer respond to the event? If no, the status of the organizer should not be shown by the UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#IS_PRIMARY:kotlin.String) Is this the primary calendar for this account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_REMINDERS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#MAX_REMINDERS:kotlin.String) The maximum number of reminders allowed for an event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [OWNER_ACCOUNT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#OWNER_ACCOUNT:kotlin.String) The owner account for this calendar, based on the calendar feed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EVENTS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#SYNC_EVENTS:kotlin.String) Is this calendar synced and are its events stored on the device? 0 - Do not sync this calendar or store events for this calendar. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VISIBLE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#VISIBLE:kotlin.String) Is the calendar selected to be displayed? 0 - do not show events associated with this calendar. |

## Constants

### ALLOWED_ATTENDEE_TYPES

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_ATTENDEE_TYPES: String
```

A comma separated list of attendee types supported for this calendar in the format "#,#,#". Valid types are [Attendees.TYPE_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_NONE:kotlin.Int), [Attendees.TYPE_OPTIONAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_OPTIONAL:kotlin.Int), [Attendees.TYPE_REQUIRED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_REQUIRED:kotlin.Int), [Attendees.TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_RESOURCE:kotlin.Int). Setting this field to only [Attendees.TYPE_NONE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns#TYPE_NONE:kotlin.Int) should be used to indicate that changing the attendee type is not supported. 

 Value: "allowedAttendeeTypes"

### ALLOWED_AVAILABILITY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_AVAILABILITY: String
```

A comma separated list of availability types supported for this calendar in the format "#,#,#". Valid types are [Events.AVAILABILITY_BUSY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#AVAILABILITY_BUSY:kotlin.Int), [Events.AVAILABILITY_FREE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#AVAILABILITY_FREE:kotlin.Int), [Events.AVAILABILITY_TENTATIVE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#AVAILABILITY_TENTATIVE:kotlin.Int). Setting this field to only [Events.AVAILABILITY_BUSY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#AVAILABILITY_BUSY:kotlin.Int) should be used to indicate that changing the availability is not supported. 

 Value: "allowedAvailability"

### ALLOWED_REMINDERS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALLOWED_REMINDERS: String
```

A comma separated list of reminder methods supported for this calendar in the format "#,#,#". Valid types are [Reminders.METHOD_DEFAULT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_DEFAULT:kotlin.Int), [Reminders.METHOD_ALERT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALERT:kotlin.Int), [Reminders.METHOD_EMAIL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_EMAIL:kotlin.Int), [Reminders.METHOD_SMS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_SMS:kotlin.Int), [Reminders.METHOD_ALARM](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns#METHOD_ALARM:kotlin.Int). Column name.

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

A key for looking up a color from the [Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) table. NULL or an empty string are reserved for indicating that the calendar does not use a key for looking up the color. The provider will update [CALENDAR_COLOR](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#CALENDAR_COLOR:kotlin.String) automatically when a valid key is written to this column. The key must reference an existing row of the [Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) table. @see Colors

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

Is this the primary calendar for this account. If this column is not explicitly set, the provider will return 1 if [Calendars.ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_NAME:kotlin.String) is equal to [Calendars.OWNER_ACCOUNT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#OWNER_ACCOUNT:kotlin.String). 

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
