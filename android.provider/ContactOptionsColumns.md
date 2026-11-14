# ContactsContract.ContactOptionsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactOptionsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.ContactOptionsColumns "View this page in Java") 
| --- | --- |

```
protected interface ContactOptionsColumns
```

| [android.provider.ContactsContract.ContactOptionsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts), [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions), [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup), [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile), [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions) | A*read-only*sub-directory of a single contact aggregate that contains all aggregation suggestions (other contacts). | | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | | [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns of [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) that track the user's preferences for, or interactions with, the contact.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_RINGTONE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#CUSTOM_RINGTONE:kotlin.String) URI for a custom ringtone associated with the contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_TIME_CONTACTED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#LAST_TIME_CONTACTED:kotlin.String) The last time a contact was contacted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PINNED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#PINNED:kotlin.String) The position at which the contact is pinned. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEND_TO_VOICEMAIL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#SEND_TO_VOICEMAIL:kotlin.String) Whether the contact should always be sent to voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STARRED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#STARRED:kotlin.String) Is the contact starred? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TIMES_CONTACTED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns#TIMES_CONTACTED:kotlin.String) The number of times a contact has been contacted. |
| --- | --- |

## Constants

### CUSTOM_RINGTONE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUSTOM_RINGTONE: String
```

URI for a custom ringtone associated with the contact. If null or missing, the default ringtone is used.

Type: TEXT (URI to the ringtone) 

 Value: "custom_ringtone"

### LAST_TIME_CONTACTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_TIME_CONTACTED: String
```

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). This column always contains 0.*

The last time a contact was contacted.

**Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](https://developer.android.com/reference/kotlin/guide/topics/providers/contacts-provider#ObsoleteData) page.

Type: INTEGER 

 Value: "last_time_contacted"

### PINNED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PINNED: String
```

The position at which the contact is pinned. If [PinnedPositions.UNPINNED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PinnedPositions#UNPINNED:kotlin.Int), the contact is not pinned. Also see [PinnedPositions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PinnedPositions).

Type: INTEGER 

 Value: "pinned"

### SEND_TO_VOICEMAIL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEND_TO_VOICEMAIL: String
```

Whether the contact should always be sent to voicemail. If missing, defaults to false.

Type: INTEGER (0 for false, 1 for true) 

 Value: "send_to_voicemail"

### STARRED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STARRED: String
```

Is the contact starred?

Type: INTEGER (boolean) 

 Value: "starred"

### TIMES_CONTACTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMES_CONTACTED: String
```

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). This column always contains 0.*

The number of times a contact has been contacted.

**Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](https://developer.android.com/reference/kotlin/guide/topics/providers/contacts-provider#ObsoleteData) page.

Type: INTEGER 

 Value: "times_contacted"
