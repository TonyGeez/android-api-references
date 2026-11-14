# ContactsContract.ContactNameColumns

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactNameColumns

Kotlin| [Java](../android/provider/ContactsContract.ContactNameColumns.md) 
| --- | --- |

```
protected interface ContactNameColumns
```

| [android.provider.ContactsContract.ContactNameColumns](../android/provider/ContactsContract.ContactNameColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md), [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md), [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md), [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | | [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Contact name and contact name metadata columns in the RawContacts table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_ALTERNATIVE](../android/provider/ContactsContract.ContactNameColumns.md) An alternative representation of the display name, such as "family name first" instead of "given name first" for Western names. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_PRIMARY](../android/provider/ContactsContract.ContactNameColumns.md) The standard text shown as the contact's display name, based on the best available information for the contact (for example, it might be the email address if the name is not available). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_SOURCE](../android/provider/ContactsContract.ContactNameColumns.md) The kind of data that is used as the display name for the contact, such as structured name or email address. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME](../android/provider/ContactsContract.ContactNameColumns.md) Pronunciation of the full name in the phonetic alphabet specified by [PHONETIC_NAME_STYLE](../android/provider/ContactsContract.ContactNameColumns.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME_STYLE](../android/provider/ContactsContract.ContactNameColumns.md) The phonetic alphabet used to represent the [PHONETIC_NAME](../android/provider/ContactsContract.ContactNameColumns.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SORT_KEY_ALTERNATIVE](../android/provider/ContactsContract.ContactNameColumns.md) Sort key based on the alternative representation of the full name, [DISPLAY_NAME_ALTERNATIVE](../android/provider/ContactsContract.ContactNameColumns.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SORT_KEY_PRIMARY](../android/provider/ContactsContract.ContactNameColumns.md) Sort key that takes into account locale-based traditions for sorting names in address books. |

## Constants

### DISPLAY_NAME_ALTERNATIVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_ALTERNATIVE: String
```

An alternative representation of the display name, such as "family name first" instead of "given name first" for Western names. If an alternative is not available, the values should be the same as [DISPLAY_NAME_PRIMARY](../android/provider/ContactsContract.ContactNameColumns.md).

A contacts provider is free to provide alternatives as necessary for its target market. For example the default Android Open Source Project contacts provider currently provides an alternative in a single case: if the display name is based on the structured name and the structured name follows the Western full name style, then the field contains the "family name first" version of the full name. Other cases may be added later. 

 Value: "display_name_alt"

### DISPLAY_NAME_PRIMARY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_PRIMARY: String
```

The standard text shown as the contact's display name, based on the best available information for the contact (for example, it might be the email address if the name is not available). The information actually used to compute the name is stored in [DISPLAY_NAME_SOURCE](../android/provider/ContactsContract.ContactNameColumns.md).

A contacts provider is free to choose whatever representation makes most sense for its target market. For example in the default Android Open Source Project implementation, if the display name is based on the structured name and the structured name follows the Western full-name style, then this field contains the "given name first" version of the full name.

<br />

 Value: "display_name"

**See Also**

- [android.provider.ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE](../android/provider/ContactsContract.ContactNameColumns.md) 

### DISPLAY_NAME_SOURCE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_SOURCE: String
```

The kind of data that is used as the display name for the contact, such as structured name or email address. See [DisplayNameSources](../android/provider/ContactsContract.DisplayNameSources.md). 

 Value: "display_name_source"

### PHONETIC_NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME: String
```

Pronunciation of the full name in the phonetic alphabet specified by [PHONETIC_NAME_STYLE](../android/provider/ContactsContract.ContactNameColumns.md).

The value may be set manually by the user. This capability is of interest only in countries with commonly used phonetic alphabets, such as Japan and Korea. See [PhoneticNameStyle](../android/provider/ContactsContract.PhoneticNameStyle.md). 

 Value: "phonetic_name"

### PHONETIC_NAME_STYLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME_STYLE: String
```

The phonetic alphabet used to represent the [PHONETIC_NAME](../android/provider/ContactsContract.ContactNameColumns.md). See [PhoneticNameStyle](../android/provider/ContactsContract.PhoneticNameStyle.md). 

 Value: "phonetic_name_style"

### SORT_KEY_ALTERNATIVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SORT_KEY_ALTERNATIVE: String
```

Sort key based on the alternative representation of the full name, [DISPLAY_NAME_ALTERNATIVE](../android/provider/ContactsContract.ContactNameColumns.md). Thus for Western names, it is the one using the "family name first" format. 

 Value: "sort_key_alt"

### SORT_KEY_PRIMARY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SORT_KEY_PRIMARY: String
```

Sort key that takes into account locale-based traditions for sorting names in address books. The default sort key is [DISPLAY_NAME_PRIMARY](../android/provider/ContactsContract.ContactNameColumns.md). For Chinese names the sort key is the name's Pinyin spelling, and for Japanese names it is the Hiragana version of the phonetic name. 

 Value: "sort_key"
