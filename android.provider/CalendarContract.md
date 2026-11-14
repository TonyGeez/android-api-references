# CalendarContract

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarContract

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract "View this page in Java") 

```
class CalendarContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.CalendarContract](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#) |

The contract between the calendar provider and applications. Contains definitions for the supported URIs and data columns.

### Overview

CalendarContract defines the data model of calendar and event related information. This data is stored in a number of tables:

- The [Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars) table holds the calendar specific information. Each row in this table contains the details for a single calendar, such as the name, color, sync info, etc.
- The [Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events) table holds the event specific information. Each row in this table has the info for a single event. It contains information such as event title, location, start time, end time, etc. The event can occur one-time or can recur multiple times. Attendees, reminders, and extended properties are stored on separate tables and reference the [Events._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) to link them with the event.
- The [Instances](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Instances) table holds the start and end time for occurrences of an event. Each row in this table represents a single occurrence. For one-time events there will be a 1:1 mapping of instances to events. For recurring events, multiple rows will automatically be generated which correspond to multiple occurrences of that event.
- The [Attendees](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Attendees) table holds the event attendee or guest information. Each row represents a single guest of an event. It specifies the type of guest they are and their attendance response for the event.
- The [Reminders](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Reminders) table holds the alert/notification data. Each row represents a single alert for an event. An event can have multiple reminders. The number of reminders per event is specified in [Calendars.MAX_REMINDERS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns#MAX_REMINDERS:kotlin.String) which is set by the Sync Adapter that owns the given calendar. Reminders are specified in minutes before the event and have a type.
- The [ExtendedProperties](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedProperties) table holds opaque data fields used by the sync adapter. The provider takes no action with items in this table except to delete them when their related events are deleted.

Other tables include:

- [SyncState](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncState), which contains free-form data maintained by the sync adapters

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Attendees](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Attendees) Fields and helpers for interacting with Attendees. |
| abstract | [AttendeesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.AttendeesColumns) Columns from the Attendees table that other tables join into themselves. |
| | [CalendarAlerts](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlerts) Fields and helpers for accessing calendar alerts information. |
| abstract | [CalendarAlertsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarAlertsColumns) <br /> |
| | [CalendarCache](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarCache) CalendarCache stores some settings for calendar including the current time zone for the instances. |
| abstract | [CalendarCacheColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarCacheColumns) <br /> |
| abstract | [CalendarColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarColumns) Columns specific to the Calendars Uri that other Uris can query. |
| | [CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity) Class that represents a Calendar Entity. |
| abstract | [CalendarSyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns) Generic columns for use by sync adapters. |
| | [Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars) Constants and helpers for the Calendars table, which contains details for individual calendars. |
| | [Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) Fields for accessing colors available for a given account. |
| abstract | [ColorsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns) <br /> |
| | [EventDays](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventDays) Fields and helpers for querying for a list of days that contain events. |
| abstract | [EventDaysColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventDaysColumns) <br /> |
| | [Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events) Constants and helpers for the Events table, which contains details for individual events. |
| abstract | [EventsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns) Columns from the Events table that other tables join into themselves. |
| | [EventsEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsEntity) Class that represents an Event Entity. |
| | [ExtendedProperties](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedProperties) Fields for accessing the Extended Properties. |
| abstract | [ExtendedPropertiesColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ExtendedPropertiesColumns) <br /> |
| | [Instances](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Instances) Fields and helpers for interacting with Instances. |
| | [Reminders](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Reminders) Fields and helpers for accessing reminders for an event. |
| abstract | [RemindersColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.RemindersColumns) <br /> |
| abstract | [SyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns) Columns for Sync information used by Calendars and Events tables. |
| | [SyncState](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncState) A table provided for sync adapters to use for storing private sync state data. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE_LOCAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACCOUNT_TYPE_LOCAL:kotlin.String) A special account type for calendars not associated with any account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_EVENT_REMINDER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_EVENT_REMINDER:kotlin.String) Broadcast Action: This is the intent that gets fired when an alarm notification needs to be posted for a reminder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_HANDLE_CUSTOM_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_HANDLE_CUSTOM_EVENT:kotlin.String) Activity Action: Display the event to the user in the custom app as specified in [EventsColumns.CUSTOM_APP_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#CUSTOM_APP_PACKAGE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT:kotlin.String) Action used to help apps show calendar events in the managed profile. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#AUTHORITY:kotlin.String) This authority is used for writing to or querying from the calendar provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CALLER_IS_SYNCADAPTER](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#CALLER_IS_SYNCADAPTER:kotlin.String) An optional insert, update or delete URI parameter that allows the caller to specify that it is a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CUSTOM_APP_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_CUSTOM_APP_URI:kotlin.String) Intent Extras key: [EventsColumns.CUSTOM_APP_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#CUSTOM_APP_URI:kotlin.String) for the event in the [ACTION_HANDLE_CUSTOM_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_HANDLE_CUSTOM_EVENT:kotlin.String) intent |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_EVENT_ALL_DAY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ALL_DAY:kotlin.String) Intent Extras key: When creating an event, set this to true to create an all-day event by default |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_EVENT_BEGIN_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_BEGIN_TIME:kotlin.String) Intent Extras key: The start time of an event or an instance of a recurring event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_EVENT_END_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_END_TIME:kotlin.String) Intent Extras key: The end time of an event or an instance of a recurring event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ID:kotlin.String) Intent Extras key: An extra of type`long`holding the id of an event. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [startViewCalendarEventInManagedProfile](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#startViewCalendarEventInManagedProfile(android.content.Context,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Boolean,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `eventId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `startMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `allDay:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Starts an activity to view calendar events in the managed profile. |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#CONTENT_URI:android.net.Uri) The content:// style URL for the top-level calendar authority |

## Constants

### ACCOUNT_TYPE_LOCAL

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE_LOCAL: String
```

A special account type for calendars not associated with any account. Normally calendars that do not match an account on the device will be removed. Setting the account_type on a calendar to this will prevent it from being wiped if it does not match an existing account. 

 Value: "LOCAL"

**See Also**

- [android.provider.CalendarContract.SyncColumns#ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_TYPE:kotlin.String) 

### ACTION_EVENT_REMINDER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_EVENT_REMINDER: String
```

Broadcast Action: This is the intent that gets fired when an alarm notification needs to be posted for a reminder. 

 Value: "android.intent.action.EVENT_REMINDER"

### ACTION_HANDLE_CUSTOM_EVENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_HANDLE_CUSTOM_EVENT: String
```

Activity Action: Display the event to the user in the custom app as specified in [EventsColumns.CUSTOM_APP_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#CUSTOM_APP_PACKAGE:kotlin.String). The custom app will be started via [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))and it should call [Activity.setResult(int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#setResult(kotlin.Int))with [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int) or [Activity.RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int) to acknowledge whether the action was handled or not. The custom app should have an intent filter like the following: 

```kotlin
<intent-filter>
     <action android:name="android.provider.calendar.action.HANDLE_CUSTOM_EVENT" />
     <category android:name="android.intent.category.DEFAULT" />
     <data android:mimeType="vnd.android.cursor.item/event" />
  </intent-filter>
```

<br />

Input: [Intent.getData](https://developer.android.com/reference/kotlin/android/content/Intent.html#getData())has the event URI. The extra [EXTRA_EVENT_BEGIN_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_BEGIN_TIME:kotlin.String) has the start time of the instance. The extra [EXTRA_CUSTOM_APP_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_CUSTOM_APP_URI:kotlin.String) will have the [EventsColumns.CUSTOM_APP_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#CUSTOM_APP_URI:kotlin.String).

Output: [Activity.RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int) if this was handled; otherwise [Activity.RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int). 

 Value: "android.provider.calendar.action.HANDLE_CUSTOM_EVENT"

### ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT: String
```

Action used to help apps show calendar events in the managed profile. 

 Value: "android.provider.calendar.action.VIEW_MANAGED_PROFILE_CALENDAR_EVENT"

### AUTHORITY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

This authority is used for writing to or querying from the calendar provider. Note: This is set at first run and cannot be changed without breaking apps that access the provider. 

 Value: "com.android.calendar"

### CALLER_IS_SYNCADAPTER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLER_IS_SYNCADAPTER: String
```

An optional insert, update or delete URI parameter that allows the caller to specify that it is a sync adapter. The default value is false. If set to true, the modified row is not marked as "dirty" (needs to be synced) and when the provider calls [ContentResolver.notifyChange(android.net.Uri, android.database.ContentObserver, boolean)](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)), the third parameter "syncToNetwork" is set to false. Furthermore, if set to true, the caller must also include [Calendars.ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_NAME:kotlin.String) and [Calendars.ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_TYPE:kotlin.String) as query parameters. 

 Value: "caller_is_syncadapter"

**See Also**

- [android.net.Uri.Builder#appendQueryParameter(java.lang.String, java.lang.String)](https://developer.android.com/reference/kotlin/android/net/Uri.Builder.html#appendQueryParameter(kotlin.String,%20kotlin.String)) 

### EXTRA_CUSTOM_APP_URI

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CUSTOM_APP_URI: String
```

Intent Extras key: [EventsColumns.CUSTOM_APP_URI](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#CUSTOM_APP_URI:kotlin.String) for the event in the [ACTION_HANDLE_CUSTOM_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_HANDLE_CUSTOM_EVENT:kotlin.String) intent 

 Value: "customAppUri"

### EXTRA_EVENT_ALL_DAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_EVENT_ALL_DAY: String
```

Intent Extras key: When creating an event, set this to true to create an all-day event by default 

 Value: "allDay"

### EXTRA_EVENT_BEGIN_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_EVENT_BEGIN_TIME: String
```

Intent Extras key: The start time of an event or an instance of a recurring event. (milliseconds since epoch) 

 Value: "beginTime"

### EXTRA_EVENT_END_TIME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_EVENT_END_TIME: String
```

Intent Extras key: The end time of an event or an instance of a recurring event. (milliseconds since epoch) 

 Value: "endTime"

### EXTRA_EVENT_ID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_EVENT_ID: String
```

Intent Extras key: An extra of type`long`holding the id of an event. 

 Value: "id"

## Public methods

### startViewCalendarEventInManagedProfile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startViewCalendarEventInManagedProfile(
    context: Context, 
    eventId: Long, 
    startMs: Long, 
    endMs: Long, 
    allDay: Boolean, 
    flags: Int
): Boolean
```

Starts an activity to view calendar events in the managed profile. When this API is called, the system will attempt to start an activity in the managed profile with an intent targeting the same caller package. The intent will have its action set to [CalendarContract.ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACTION_VIEW_MANAGED_PROFILE_CALENDAR_EVENT:kotlin.String) and contain extras corresponding to the API's arguments. A calendar app intending to support cross-profile events viewing should handle this intent, parse the arguments and show the appropriate UI.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context. This value cannot be`null`. |
| `eventId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the id of the event to be viewed. Will be put into [EXTRA_EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ID:kotlin.String) field of the intent. |
| `startMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time of the event in milliseconds since epoch. Will be put into [EXTRA_EVENT_BEGIN_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_BEGIN_TIME:kotlin.String) field of the intent. |
| `endMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the end time of the event in milliseconds since epoch. Will be put into [EXTRA_EVENT_END_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_END_TIME:kotlin.String) field of the intent. |
| `allDay` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if the event is an all-day event. Will be put into [EXTRA_EVENT_ALL_DAY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ALL_DAY:kotlin.String) field of the intent. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags to be set on the intent via [Intent.setFlags](https://developer.android.com/reference/kotlin/android/content/Intent.html#setFlags(kotlin.Int)) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the activity is started successfully.`false`otherwise. |

**See Also**

- [#EXTRA_EVENT_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ID:kotlin.String)
- [#EXTRA_EVENT_BEGIN_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_BEGIN_TIME:kotlin.String)
- [#EXTRA_EVENT_END_TIME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_END_TIME:kotlin.String)
- [#EXTRA_EVENT_ALL_DAY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#EXTRA_EVENT_ALL_DAY:kotlin.String)

## Properties

### CONTENT_URI

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_URI: Uri!
```

The content:// style URL for the top-level calendar authority
