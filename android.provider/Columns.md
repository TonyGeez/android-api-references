# SyncStateContract.Columns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Columns

Kotlin| [Java](../android/provider/SyncStateContract.Columns.md) 
| --- | --- |

```
interface Columns : BaseColumns
```

| [android.provider.SyncStateContract.Columns](../android/provider/SyncStateContract.Columns.md) |

| Known Direct Subclasses [CalendarContract.ColorsColumns](../android/provider/CalendarContract.ColorsColumns.md), [CalendarContract.SyncState](../android/provider/CalendarContract.SyncState.md), [ContactsContract.ProfileSyncState](../android/provider/ContactsContract.ProfileSyncState.md), [ContactsContract.SyncState](../android/provider/ContactsContract.SyncState.md), [SyncStateContract.Constants](../android/provider/SyncStateContract.Constants.md) |----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [CalendarContract.ColorsColumns](../android/provider/CalendarContract.ColorsColumns.md) | <br /> | | [CalendarContract.SyncState](../android/provider/CalendarContract.SyncState.md) | A table provided for sync adapters to use for storing private sync state data. | | [ContactsContract.ProfileSyncState](../android/provider/ContactsContract.ProfileSyncState.md) | A table provided for sync adapters to use for storing private sync state data for the user's personal profile. | | [ContactsContract.SyncState](../android/provider/ContactsContract.SyncState.md) | A table provided for sync adapters to use for storing private sync state data for contacts. | | [SyncStateContract.Constants](../android/provider/SyncStateContract.Constants.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CalendarContract.Colors](../android/provider/CalendarContract.Colors.md) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [CalendarContract.Colors](../android/provider/CalendarContract.Colors.md) | Fields for accessing colors available for a given account. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](../android/provider/SyncStateContract.Columns.md) A reference to the name of the account to which this data belongs |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](../android/provider/SyncStateContract.Columns.md) A reference to the type of the account to which this data belongs |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](../android/provider/SyncStateContract.Columns.md) The sync data associated with this account. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [BaseColumns](../android/provider/BaseColumns.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](../android/provider/BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](../android/provider/BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ACCOUNT_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_NAME: String
```

A reference to the name of the account to which this data belongs

Type: STRING 

 Value: "account_name"

### ACCOUNT_TYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE: String
```

A reference to the type of the account to which this data belongs

Type: STRING 

 Value: "account_type"

### DATA

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA: String
```

The sync data associated with this account.

Type: NONE 

 Value: "data"
