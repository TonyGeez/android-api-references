# ContactsContract.DataUsageStatColumns

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataUsageStatColumns

Kotlin| [Java](../android/provider/ContactsContract.DataUsageStatColumns.md) 
| --- | --- |

```
protected interface DataUsageStatColumns
```

| [android.provider.ContactsContract.DataUsageStatColumns](../android/provider/ContactsContract.DataUsageStatColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns in the Data_Usage_Stat table

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_TIME_USED](../android/provider/ContactsContract.DataUsageStatColumns.md) The last time (in milliseconds) this [Data](../android/provider/ContactsContract.Data.md) was used. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TIMES_USED](../android/provider/ContactsContract.DataUsageStatColumns.md) The number of times the referenced [Data](../android/provider/ContactsContract.Data.md) has been used. |

## Constants

### LAST_TIME_USED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_TIME_USED: String
```

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). This column always contains 0.*

***Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](../guide/topics/providers/contacts-provider.md) page.*

<br />

The last time (in milliseconds) this [Data](../android/provider/ContactsContract.Data.md) was used. 

 Value: "last_time_used"

### TIMES_USED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMES_USED: String
```

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). This column always contains 0.*

***Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](../guide/topics/providers/contacts-provider.md) page.*

<br />

The number of times the referenced [Data](../android/provider/ContactsContract.Data.md) has been used. 

 Value: "times_used"
