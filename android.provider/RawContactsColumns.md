# ContactsContract.RawContactsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RawContactsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.RawContactsColumns "View this page in Java") 
| --- | --- |

```
protected interface RawContactsColumns
```

| [android.provider.ContactsContract.RawContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts), [ContactsContract.RawContactsEntity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsEntity) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | | [ContactsContract.RawContactsEntity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsEntity) | Constants for the raw contacts entities table, which can be thought of as an outer join of the raw_contacts table with the data table. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE_AND_DATA_SET](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#ACCOUNT_TYPE_AND_DATA_SET:kotlin.String) A concatenation of the account type and data set (delimited by a forward slash) - if the data set is empty, this will be the same as the account type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AGGREGATION_MODE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#AGGREGATION_MODE:kotlin.String) The aggregation mode for this contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BACKUP_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#BACKUP_ID:kotlin.String) Persistent unique id for each raw_contact within its account. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#CONTACT_ID:kotlin.String) A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_SET](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#DATA_SET:kotlin.String) The data set within the account that this row belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELETED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#DELETED:kotlin.String) The "deleted" flag: "0" by default, "1" if the row has been marked for deletion. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METADATA_DIRTY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#METADATA_DIRTY:kotlin.String) Flag indicating that a raw contact's metadata has changed, and its metadata needs to be synchronized by the server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_IS_READ_ONLY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#RAW_CONTACT_IS_READ_ONLY:kotlin.String) The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_IS_USER_PROFILE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#RAW_CONTACT_IS_USER_PROFILE:kotlin.String) Flag that reflects whether this raw contact belongs to the user's personal profile entry. |
| --- | --- |

## Constants

### ACCOUNT_TYPE_AND_DATA_SET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE_AND_DATA_SET: String
```

A concatenation of the account type and data set (delimited by a forward slash) - if the data set is empty, this will be the same as the account type. For applications that need to be aware of the data set, this can be used instead of account type to distinguish sets of data. This is never intended to be used for specifying accounts.

This column does \*not\* escape forward slashes in the account type or the data set. If this is an issue, consider using [ContactsContract.RawContacts.ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns#ACCOUNT_TYPE:kotlin.String) and [ContactsContract.RawContacts.DATA_SET](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns#DATA_SET:kotlin.String) directly. 

 Value: "account_type_and_data_set"

### AGGREGATION_MODE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AGGREGATION_MODE: String
```

The aggregation mode for this contact.

Type: INTEGER 

 Value: "aggregation_mode"

### BACKUP_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BACKUP_ID: String
```

Persistent unique id for each raw_contact within its account. This id is provided by its own data source, and can be used to backup metadata to the server. This should be unique within each set of account_name/account_type/data_set 

 Value: "backup_id"

### CONTACT_ID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_ID: String
```

A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to.

Type: INTEGER 

 Value: "contact_id"

### DATA_SET

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_SET: String
```

The data set within the account that this row belongs to. This allows multiple sync adapters for the same account type to distinguish between each others' data. This is empty by default, and is completely optional. It only needs to be populated if multiple sync adapters are entering distinct data for the same account type and account name.

Type: TEXT 

 Value: "data_set"

### DELETED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELETED: String
```

The "deleted" flag: "0" by default, "1" if the row has been marked for deletion. When android.content.ContentResolver#delete is called on a raw contact, it is marked for deletion and removed from its aggregate contact. The sync adaptor deletes the raw contact on the server and then calls ContactResolver.delete once more, this time passing the [ContactsContract.CALLER_IS_SYNCADAPTER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract#CALLER_IS_SYNCADAPTER:kotlin.String) query parameter to finalize the data removal.

Type: INTEGER 

 Value: "deleted"

### METADATA_DIRTY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_DIRTY: String
```

**Deprecated:** *This column never actually worked since added. It will not supported as of Android version [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int).*

Flag indicating that a raw contact's metadata has changed, and its metadata needs to be synchronized by the server.

Type: INTEGER (boolean) 

 Value: "metadata_dirty"

### RAW_CONTACT_IS_READ_ONLY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_IS_READ_ONLY: String
```

The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. See [ContactsContract.CALLER_IS_SYNCADAPTER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract#CALLER_IS_SYNCADAPTER:kotlin.String).

Type: INTEGER 

 Value: "raw_contact_is_read_only"

### RAW_CONTACT_IS_USER_PROFILE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_IS_USER_PROFILE: String
```

Flag that reflects whether this raw contact belongs to the user's personal profile entry. 

 Value: "raw_contact_is_user_profile"
