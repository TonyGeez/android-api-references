# ContactsContract.BaseSyncColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseSyncColumns

Kotlin | [Java](https://developer.android.com/reference/android/provider/ContactsContract.BaseSyncColumns "View this page in Java") 

```
protected interface BaseSyncColumns
```

| [android.provider.ContactsContract.BaseSyncColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.SyncColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns) |--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.SyncColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns) | Columns that appear when each row of a table belongs to a specific account, including sync information that an account may need. | |

| Known Indirect Subclasses [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.Groups](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Groups), [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) |--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.Groups](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Groups) | Constants for the groups table. | | [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |

Generic columns for use by sync adapters. The specific functions of these columns are private to the sync adapter. Other clients of the API should not attempt to either read or write this column.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC1](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns#SYNC1:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC2](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns#SYNC2:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC3](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns#SYNC3:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC4](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns#SYNC4:kotlin.String) Generic column for use by sync adapters. |

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
