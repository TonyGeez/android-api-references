# SyncStateContract.Columns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Columns

Kotlin| [Java](https://developer.android.com/reference/android/provider/SyncStateContract.Columns "View this page in Java") 
| --- | --- |

```
interface Columns : BaseColumns
```

| [android.provider.SyncStateContract.Columns](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#) |

| Known Direct Subclasses [CalendarContract.ColorsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns), [CalendarContract.SyncState](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncState), [ContactsContract.ProfileSyncState](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ProfileSyncState), [ContactsContract.SyncState](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncState), [SyncStateContract.Constants](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Constants) |----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [CalendarContract.ColorsColumns](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.ColorsColumns) | <br /> | | [CalendarContract.SyncState](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.SyncState) | A table provided for sync adapters to use for storing private sync state data. | | [ContactsContract.ProfileSyncState](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ProfileSyncState) | A table provided for sync adapters to use for storing private sync state data for the user's personal profile. | | [ContactsContract.SyncState](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncState) | A table provided for sync adapters to use for storing private sync state data for contacts. | | [SyncStateContract.Constants](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Constants) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CalendarContract.Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------| | [CalendarContract.Colors](https://developer.android.com/reference/kotlin/android/provider/CalendarContract.Colors) | Fields for accessing colors available for a given account. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_NAME](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_NAME:kotlin.String) A reference to the name of the account to which this data belongs |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#ACCOUNT_TYPE:kotlin.String) A reference to the type of the account to which this data belongs |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](https://developer.android.com/reference/kotlin/android/provider/SyncStateContract.Columns#DATA:kotlin.String) The sync data associated with this account. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

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
