# CalendarContract.SyncColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.SyncColumns "View this page in Java") 

```
protected interface SyncColumns : CalendarContract.CalendarSyncColumns
```

| [android.provider.CalendarContract.SyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#) |

| Known Direct Subclasses [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity), [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars), [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events), [CalendarContract.EventsEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsEntity) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity) | Class that represents a Calendar Entity. | | [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars) | Constants and helpers for the Calendars table, which contains details for individual calendars. | | [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.EventsEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsEntity) | Class that represents an Event Entity. | |

Columns for Sync information used by Calendars and Events tables. These have specific uses which are expected to be consistent by the app and sync adapter.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_NAME:kotlin.String) The account that was used to sync the entry to the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#ACCOUNT_TYPE:kotlin.String) The type of the account that was used to sync the entry to the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_PARTIALLY_UPDATE](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#CAN_PARTIALLY_UPDATE:kotlin.String) If set to 1 this causes events on this calendar to be duplicated with [Events.LAST_SYNCED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#LAST_SYNCED:kotlin.String) set to 1 whenever the event transitions from non-dirty to dirty. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELETED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#DELETED:kotlin.String) Whether the row has been deleted but not synced to the server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIRTY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#DIRTY:kotlin.String) Used to indicate that local, unsynced, changes are present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MUTATORS](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#MUTATORS:kotlin.String) Used in conjunction with [DIRTY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#DIRTY:kotlin.String) to indicate what packages wrote local changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ID](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#_SYNC_ID:kotlin.String) The unique ID for a row assigned by the sync source. |

| Inherited constants ||
|---|---|
| From class [CalendarSyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC1](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC1:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC10](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC10:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC2](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC2:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC3](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC3:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC4](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC4:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC5](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC5:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC6](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC6:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC7](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC7:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC8](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC8:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC9](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC9:kotlin.String) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | ||

## Constants

### ACCOUNT_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_NAME: String
```

The account that was used to sync the entry to the device. If the account_type is not [ACCOUNT_TYPE_LOCAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACCOUNT_TYPE_LOCAL:kotlin.String) then the name and type must match an account on the device or the calendar will be deleted.

Type: TEXT 

 Value: "account_name"

### ACCOUNT_TYPE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE: String
```

The type of the account that was used to sync the entry to the device. A type of [ACCOUNT_TYPE_LOCAL](https://developer.android.com/reference/kotlin/android/provider/CalendarContract#ACCOUNT_TYPE_LOCAL:kotlin.String) will keep this event form being deleted if there are no matching accounts on the device.

Type: TEXT 

 Value: "account_type"

### CAN_PARTIALLY_UPDATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAN_PARTIALLY_UPDATE: String
```

If set to 1 this causes events on this calendar to be duplicated with [Events.LAST_SYNCED](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsColumns#LAST_SYNCED:kotlin.String) set to 1 whenever the event transitions from non-dirty to dirty. The duplicated event will not be expanded in the instances table and will only show up in sync adapter queries of the events table. It will also be deleted when the originating event has its dirty flag cleared by the sync adapter.

Type: INTEGER (boolean) 

 Value: "canPartiallyUpdate"

### DELETED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELETED: String
```

Whether the row has been deleted but not synced to the server. A deleted row should be ignored.

Type: INTEGER (boolean) 

 Value: "deleted"

### DIRTY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRTY: String
```

Used to indicate that local, unsynced, changes are present.

Type: INTEGER (long) 

 Value: "dirty"

### MUTATORS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MUTATORS: String
```

Used in conjunction with [DIRTY](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns#DIRTY:kotlin.String) to indicate what packages wrote local changes.

Type: TEXT 

 Value: "mutators"

### _SYNC_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ID: String
```

The unique ID for a row assigned by the sync source. NULL if the row has never been synced. This is used as a reference id for exceptions along with [BaseColumns._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String).

Type: TEXT 

 Value: "_sync_id"
