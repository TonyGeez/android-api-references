# ContactsContract.ContactNameColumns

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactNameColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.ContactNameColumns "View this page in Java") 

```
protected interface ContactNameColumns
```

| [android.provider.ContactsContract.ContactNameColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts), [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup), [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile), [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | | [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) | Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. | |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |

Contact name and contact name metadata columns in the RawContacts table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE:kotlin.String) An alternative representation of the display name, such as "family name first" instead of "given name first" for Western names. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_PRIMARY:kotlin.String) The standard text shown as the contact's display name, based on the best available information for the contact (for example, it might be the email address if the name is not available). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME_SOURCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_SOURCE:kotlin.String) The kind of data that is used as the display name for the contact, such as structured name or email address. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME:kotlin.String) Pronunciation of the full name in the phonetic alphabet specified by [PHONETIC_NAME_STYLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME_STYLE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME_STYLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME_STYLE:kotlin.String) The phonetic alphabet used to represent the [PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SORT_KEY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#SORT_KEY_ALTERNATIVE:kotlin.String) Sort key based on the alternative representation of the full name, [DISPLAY_NAME_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SORT_KEY_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#SORT_KEY_PRIMARY:kotlin.String) Sort key that takes into account locale-based traditions for sorting names in address books. |

## Constants

### DISPLAY_NAME_ALTERNATIVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_ALTERNATIVE: String
```

An alternative representation of the display name, such as "family name first" instead of "given name first" for Western names. If an alternative is not available, the values should be the same as [DISPLAY_NAME_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_PRIMARY:kotlin.String).

A contacts provider is free to provide alternatives as necessary for its target market. For example the default Android Open Source Project contacts provider currently provides an alternative in a single case: if the display name is based on the structured name and the structured name follows the Western full name style, then the field contains the "family name first" version of the full name. Other cases may be added later. 

 Value: "display_name_alt"

### DISPLAY_NAME_PRIMARY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_PRIMARY: String
```

The standard text shown as the contact's display name, based on the best available information for the contact (for example, it might be the email address if the name is not available). The information actually used to compute the name is stored in [DISPLAY_NAME_SOURCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_SOURCE:kotlin.String).

A contacts provider is free to choose whatever representation makes most sense for its target market. For example in the default Android Open Source Project implementation, if the display name is based on the structured name and the structured name follows the Western full-name style, then this field contains the "given name first" version of the full name.

<br />

 Value: "display_name"

**See Also**

- [android.provider.ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE:kotlin.String) 

### DISPLAY_NAME_SOURCE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME_SOURCE: String
```

The kind of data that is used as the display name for the contact, such as structured name or email address. See [DisplayNameSources](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources). 

 Value: "display_name_source"

### PHONETIC_NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME: String
```

Pronunciation of the full name in the phonetic alphabet specified by [PHONETIC_NAME_STYLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME_STYLE:kotlin.String).

The value may be set manually by the user. This capability is of interest only in countries with commonly used phonetic alphabets, such as Japan and Korea. See [PhoneticNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle). 

 Value: "phonetic_name"

### PHONETIC_NAME_STYLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME_STYLE: String
```

The phonetic alphabet used to represent the [PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#PHONETIC_NAME:kotlin.String). See [PhoneticNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle). 

 Value: "phonetic_name_style"

### SORT_KEY_ALTERNATIVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SORT_KEY_ALTERNATIVE: String
```

Sort key based on the alternative representation of the full name, [DISPLAY_NAME_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_ALTERNATIVE:kotlin.String). Thus for Western names, it is the one using the "family name first" format. 

 Value: "sort_key_alt"

### SORT_KEY_PRIMARY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SORT_KEY_PRIMARY: String
```

Sort key that takes into account locale-based traditions for sorting names in address books. The default sort key is [DISPLAY_NAME_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns#DISPLAY_NAME_PRIMARY:kotlin.String). For Chinese names the sort key is the name's Pinyin spelling, and for Japanese names it is the Hiragana version of the phonetic name. 

 Value: "sort_key"
