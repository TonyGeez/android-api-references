# CalendarContract.CalendarSyncColumns

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalendarSyncColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/CalendarContract.CalendarSyncColumns "View this page in Java") 
| --- | --- |

```
protected interface CalendarSyncColumns
```

| [android.provider.CalendarContract.CalendarSyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#) |

| Known Direct Subclasses [CalendarContract.SyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns) |------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------| | [CalendarContract.SyncColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncColumns) | Columns for Sync information used by Calendars and Events tables. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity), [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars), [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events), [CalendarContract.EventsEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsEntity) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [CalendarContract.CalendarEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarEntity) | Class that represents a Calendar Entity. | | [CalendarContract.Calendars](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Calendars) | Constants and helpers for the Calendars table, which contains details for individual calendars. | | [CalendarContract.Events](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Events) | Constants and helpers for the Events table, which contains details for individual events. | | [CalendarContract.EventsEntity](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.EventsEntity) | Class that represents an Event Entity. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Generic columns for use by sync adapters. The specific functions of these columns are private to the sync adapter. Other clients of the API should not attempt to either read or write this column. These columns are editable as part of the Calendars Uri, but can only be read if accessed through any other Uri.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC1](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC1:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC10](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC10:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC2](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC2:kotlin.String) Generic column for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC3](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC3:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC4](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC4:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC5](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC5:kotlin.String) Generic column for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC6](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC6:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC7](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC7:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC8](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC8:kotlin.String) Generic column for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CAL_SYNC9](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.CalendarSyncColumns#CAL_SYNC9:kotlin.String) Generic column for use by sync adapters. |

## Constants

### CAL_SYNC1

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC1: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync1"

### CAL_SYNC10

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC10: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync10"

### CAL_SYNC2

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC2: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync2"

### CAL_SYNC3

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC3: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync3"

### CAL_SYNC4

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC4: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync4"

### CAL_SYNC5

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC5: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync5"

### CAL_SYNC6

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC6: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync6"

### CAL_SYNC7

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC7: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync7"

### CAL_SYNC8

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC8: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync8"

### CAL_SYNC9

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAL_SYNC9: String
```

Generic column for use by sync adapters. Column name.

Type: TEXT 

 Value: "cal_sync9"
