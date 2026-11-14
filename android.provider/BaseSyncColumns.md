# ContactsContract.BaseSyncColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseSyncColumns

Kotlin | [Java](../android/provider/ContactsContract.BaseSyncColumns.md) 
| --- | --- |

```
protected interface BaseSyncColumns
```

| [android.provider.ContactsContract.BaseSyncColumns](../android/provider/ContactsContract.BaseSyncColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.SyncColumns](../android/provider/ContactsContract.SyncColumns.md) |--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.SyncColumns](../android/provider/ContactsContract.SyncColumns.md) | Columns that appear when each row of a table belongs to a specific account, including sync information that an account may need. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.Groups](../android/provider/ContactsContract.Groups.md), [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) |--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.Groups](../android/provider/ContactsContract.Groups.md) | Constants for the groups table. | | [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Generic columns for use by sync adapters. The specific functions of these columns are private to the sync adapter. Other clients of the API should not attempt to either read or write this column.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC1](../android/provider/ContactsContract.BaseSyncColumns.md) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC2](../android/provider/ContactsContract.BaseSyncColumns.md) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC3](../android/provider/ContactsContract.BaseSyncColumns.md) Generic column for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC4](../android/provider/ContactsContract.BaseSyncColumns.md) Generic column for use by sync adapters. |

## Constants

### SYNC1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC1: String
```

Generic column for use by sync adapters. 

 Value: "sync1"

### SYNC2

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC2: String
```

Generic column for use by sync adapters. 

 Value: "sync2"

### SYNC3

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC3: String
```

Generic column for use by sync adapters. 

 Value: "sync3"

### SYNC4

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC4: String
```

Generic column for use by sync adapters. 

 Value: "sync4"
