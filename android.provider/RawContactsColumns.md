# ContactsContract.RawContactsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RawContactsColumns

Kotlin| [Java](../android/provider/ContactsContract.RawContactsColumns.md) 
| --- | --- |

```
protected interface RawContactsColumns
```

| [android.provider.ContactsContract.RawContactsColumns](../android/provider/ContactsContract.RawContactsColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md), [ContactsContract.RawContactsEntity](../android/provider/ContactsContract.RawContactsEntity.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | | [ContactsContract.RawContactsEntity](../android/provider/ContactsContract.RawContactsEntity.md) | Constants for the raw contacts entities table, which can be thought of as an outer join of the raw_contacts table with the data table. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACCOUNT_TYPE_AND_DATA_SET](../android/provider/ContactsContract.RawContactsColumns.md) A concatenation of the account type and data set (delimited by a forward slash) - if the data set is empty, this will be the same as the account type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AGGREGATION_MODE](../android/provider/ContactsContract.RawContactsColumns.md) The aggregation mode for this contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BACKUP_ID](../android/provider/ContactsContract.RawContactsColumns.md) Persistent unique id for each raw_contact within its account. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](../android/provider/ContactsContract.RawContactsColumns.md) A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_SET](../android/provider/ContactsContract.RawContactsColumns.md) The data set within the account that this row belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DELETED](../android/provider/ContactsContract.RawContactsColumns.md) The "deleted" flag: "0" by default, "1" if the row has been marked for deletion. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METADATA_DIRTY](../android/provider/ContactsContract.RawContactsColumns.md) Flag indicating that a raw contact's metadata has changed, and its metadata needs to be synchronized by the server. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_IS_READ_ONLY](../android/provider/ContactsContract.RawContactsColumns.md) The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_IS_USER_PROFILE](../android/provider/ContactsContract.RawContactsColumns.md) Flag that reflects whether this raw contact belongs to the user's personal profile entry. |
| --- | --- |

## Constants

### ACCOUNT_TYPE_AND_DATA_SET

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNT_TYPE_AND_DATA_SET: String
```

A concatenation of the account type and data set (delimited by a forward slash) - if the data set is empty, this will be the same as the account type. For applications that need to be aware of the data set, this can be used instead of account type to distinguish sets of data. This is never intended to be used for specifying accounts.

This column does \*not\* escape forward slashes in the account type or the data set. If this is an issue, consider using [ContactsContract.RawContacts.ACCOUNT_TYPE](../android/provider/ContactsContract.SyncColumns.md) and [ContactsContract.RawContacts.DATA_SET](../android/provider/ContactsContract.RawContactsColumns.md) directly. 

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

A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that this data belongs to.

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

The "deleted" flag: "0" by default, "1" if the row has been marked for deletion. When android.content.ContentResolver#delete is called on a raw contact, it is marked for deletion and removed from its aggregate contact. The sync adaptor deletes the raw contact on the server and then calls ContactResolver.delete once more, this time passing the [ContactsContract.CALLER_IS_SYNCADAPTER](../android/provider/ContactsContract.md) query parameter to finalize the data removal.

Type: INTEGER 

 Value: "deleted"

### METADATA_DIRTY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_DIRTY: String
```

**Deprecated:** *This column never actually worked since added. It will not supported as of Android version [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md).*

Flag indicating that a raw contact's metadata has changed, and its metadata needs to be synchronized by the server.

Type: INTEGER (boolean) 

 Value: "metadata_dirty"

### RAW_CONTACT_IS_READ_ONLY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_IS_READ_ONLY: String
```

The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. See [ContactsContract.CALLER_IS_SYNCADAPTER](../android/provider/ContactsContract.md).

Type: INTEGER 

 Value: "raw_contact_is_read_only"

### RAW_CONTACT_IS_USER_PROFILE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_IS_USER_PROFILE: String
```

Flag that reflects whether this raw contact belongs to the user's personal profile entry. 

 Value: "raw_contact_is_user_profile"
