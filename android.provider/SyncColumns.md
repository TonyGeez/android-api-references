# CalendarContract.SyncColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncColumns

Kotlin| [Java](../android/provider/CalendarContract.SyncColumns.md) 
| --- | --- |

```
protected interface SyncColumns : CalendarContract.CalendarSyncColumns
```

| [android.provider.CalendarContract.SyncColumns](../android/provider/CalendarContract.SyncColumns.md) |

| Known Direct Subclasses [CalendarContract.CalendarEntity](../android/provider/CalendarContract.CalendarEntity.md), [CalendarContract.Calendars](../android/provider/CalendarContract.Calendars.md), [CalendarContract.Events](../android/provider/CalendarContract.Events.md), [CalendarContract.EventsEntity](../android/provider/CalendarContract.EventsEntity.md) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [CalendarContract.CalendarEntity](../android/provider/CalendarContract.CalendarEntity.md) | Class that represents a Calendar Entity. | | [CalendarContract.Calendars](../android/provider/CalendarContract.Calendars.md) | Constants and helpers for the Calendars table, which contains details for individual calendars. | | [CalendarContract.Events](../android/provider/CalendarContract.Events.md) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.EventsEntity](../android/provider/CalendarContract.EventsEntity.md) | Class that represents an Event Entity. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns for Sync information used by Calendars and Events tables. These have specific uses which are expected to be consistent by the app and sync adapter.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](../android/provider/CalendarContract.SyncColumns.md) The account that was used to sync the entry to the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](../android/provider/CalendarContract.SyncColumns.md) The type of the account that was used to sync the entry to the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAN_PARTIALLY_UPDATE](../android/provider/CalendarContract.SyncColumns.md) If set to 1 this causes events on this calendar to be duplicated with [Events.LAST_SYNCED](../android/provider/CalendarContract.EventsColumns.md) set to 1 whenever the event transitions from non-dirty to dirty. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELETED](../android/provider/CalendarContract.SyncColumns.md) Whether the row has been deleted but not synced to the server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DIRTY](../android/provider/CalendarContract.SyncColumns.md) Used to indicate that local, unsynced, changes are present. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MUTATORS](../android/provider/CalendarContract.SyncColumns.md) Used in conjunction with [DIRTY](../android/provider/CalendarContract.SyncColumns.md) to indicate what packages wrote local changes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ID](../android/provider/CalendarContract.SyncColumns.md) The unique ID for a row assigned by the sync source. |

| Inherited constants ||
|---|---|
| From class [CalendarSyncColumns](../android/provider/CalendarContract.CalendarSyncColumns.md) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC1](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC10](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC2](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC3](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC4](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC5](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC6](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC7](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC8](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC9](../android/provider/CalendarContract.CalendarSyncColumns.md) <br /> Generic column for use by sync adapters. Column name. Type: TEXT <br /> | ||

## Constants

### ACCOUNT_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_NAME: String
```

The account that was used to sync the entry to the device. If the account_type is not [ACCOUNT_TYPE_LOCAL](CalendarContract.md) then the name and type must match an account on the device or the calendar will be deleted.

Type: TEXT 

 Value: "account_name"

### ACCOUNT_TYPE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE: String
```

The type of the account that was used to sync the entry to the device. A type of [ACCOUNT_TYPE_LOCAL](CalendarContract.md) will keep this event form being deleted if there are no matching accounts on the device.

Type: TEXT 

 Value: "account_type"

### CAN_PARTIALLY_UPDATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAN_PARTIALLY_UPDATE: String
```

If set to 1 this causes events on this calendar to be duplicated with [Events.LAST_SYNCED](../android/provider/CalendarContract.EventsColumns.md) set to 1 whenever the event transitions from non-dirty to dirty. The duplicated event will not be expanded in the instances table and will only show up in sync adapter queries of the events table. It will also be deleted when the originating event has its dirty flag cleared by the sync adapter.

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

Used in conjunction with [DIRTY](../android/provider/CalendarContract.SyncColumns.md) to indicate what packages wrote local changes.

Type: TEXT 

 Value: "mutators"

### _SYNC_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ID: String
```

The unique ID for a row assigned by the sync source. NULL if the row has never been synced. This is used as a reference id for exceptions along with [BaseColumns._ID](BaseColumns.md).

Type: TEXT 

 Value: "_sync_id"
