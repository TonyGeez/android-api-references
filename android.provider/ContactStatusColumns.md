# ContactsContract.ContactStatusColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactStatusColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.ContactStatusColumns "View this page in Java") 
| --- | --- |

```
protected interface ContactStatusColumns
```

| [android.provider.ContactsContract.ContactStatusColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts), [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions), [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions) | A*read-only*sub-directory of a single contact aggregate that contains all aggregation suggestions (other contacts). | | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_CHAT_CAPABILITY:kotlin.String) Contact Chat Capabilities. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_PRESENCE:kotlin.String) Contact presence status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_STATUS](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS:kotlin.String) Contact's latest status update. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_STATUS_ICON](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_ICON:kotlin.String) The resource ID of the icon for the source of contact status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_STATUS_LABEL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_LABEL:kotlin.String) The resource ID of the label describing the source of contact status, e. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_RES_PACKAGE:kotlin.String) The package containing resources for this status: label and icon. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_STATUS_TIMESTAMP](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_TIMESTAMP:kotlin.String) The absolute time in milliseconds when the latest status was inserted/updated. |

## Constants

### CONTACT_CHAT_CAPABILITY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_CHAT_CAPABILITY: String
```

Contact Chat Capabilities. See [StatusUpdates](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates) for individual definitions.

Type: NUMBER 

 Value: "contact_chat_capability"

### CONTACT_PRESENCE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_PRESENCE: String
```

Contact presence status. See [StatusUpdates](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates) for individual status definitions.

Type: NUMBER 

 Value: "contact_presence"

### CONTACT_STATUS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_STATUS: String
```

Contact's latest status update.

Type: TEXT 

 Value: "contact_status"

### CONTACT_STATUS_ICON

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_STATUS_ICON: String
```

The resource ID of the icon for the source of contact status. This resource is scoped by the [CONTACT_STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_RES_PACKAGE:kotlin.String).

Type: NUMBER 

 Value: "contact_status_icon"

### CONTACT_STATUS_LABEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_STATUS_LABEL: String
```

The resource ID of the label describing the source of contact status, e.g. "Google Talk". This resource is scoped by the [CONTACT_STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns#CONTACT_STATUS_RES_PACKAGE:kotlin.String).

Type: NUMBER 

 Value: "contact_status_label"

### CONTACT_STATUS_RES_PACKAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_STATUS_RES_PACKAGE: String
```

The package containing resources for this status: label and icon.

Type: TEXT 

 Value: "contact_status_res_package"

### CONTACT_STATUS_TIMESTAMP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_STATUS_TIMESTAMP: String
```

The absolute time in milliseconds when the latest status was inserted/updated.

Type: NUMBER 

 Value: "contact_status_ts"
