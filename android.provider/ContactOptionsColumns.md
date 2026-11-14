# ContactsContract.ContactOptionsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactOptionsColumns

Kotlin| [Java](../android/provider/ContactsContract.ContactOptionsColumns.md) 
| --- | --- |

```
protected interface ContactOptionsColumns
```

| [android.provider.ContactsContract.ContactOptionsColumns](../android/provider/ContactsContract.ContactOptionsColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md), [ContactsContract.Contacts.AggregationSuggestions](../android/provider/ContactsContract.Contacts.AggregationSuggestions.md), [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md), [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md), [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.AggregationSuggestions](../android/provider/ContactsContract.Contacts.AggregationSuggestions.md) | A*read-only*sub-directory of a single contact aggregate that contains all aggregation suggestions (other contacts). | | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | | [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns of [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md) that track the user's preferences for, or interactions with, the contact.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_RINGTONE](../android/provider/ContactsContract.ContactOptionsColumns.md) URI for a custom ringtone associated with the contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_TIME_CONTACTED](../android/provider/ContactsContract.ContactOptionsColumns.md) The last time a contact was contacted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PINNED](../android/provider/ContactsContract.ContactOptionsColumns.md) The position at which the contact is pinned. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEND_TO_VOICEMAIL](../android/provider/ContactsContract.ContactOptionsColumns.md) Whether the contact should always be sent to voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STARRED](../android/provider/ContactsContract.ContactOptionsColumns.md) Is the contact starred? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TIMES_CONTACTED](../android/provider/ContactsContract.ContactOptionsColumns.md) The number of times a contact has been contacted. |
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

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). This column always contains 0.*

The last time a contact was contacted.

**Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](../guide/topics/providers/contacts-provider.md) page.

Type: INTEGER 

 Value: "last_time_contacted"

### PINNED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PINNED: String
```

The position at which the contact is pinned. If [PinnedPositions.UNPINNED](../android/provider/ContactsContract.PinnedPositions.md), the contact is not pinned. Also see [PinnedPositions](../android/provider/ContactsContract.PinnedPositions.md).

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

**Deprecated:** *Contacts affinity information is no longer supported as of Android version [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). This column always contains 0.*

The number of times a contact has been contacted.

**Caution:** If you publish your app to the Google Play Store, this field is obsolete, regardless of Android version. For more information, see the [Contacts Provider](../guide/topics/providers/contacts-provider.md) page.

Type: INTEGER 

 Value: "times_contacted"
