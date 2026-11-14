# ContactsContract.ContactsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.ContactsColumns "View this page in Java") 

```
protected interface ContactsColumns
```

| [android.provider.ContactsContract.ContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts), [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions), [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup), [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.AggregationSuggestions](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.AggregationSuggestions) | A*read-only*sub-directory of a single contact aggregate that contains all aggregation suggestions (other contacts). | | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |

Columns of [ContactsContract.Contacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts) that refer to intrinsic properties of the contact, as opposed to the user-specified options found in [ContactOptionsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_LAST_UPDATED_TIMESTAMP](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#CONTACT_LAST_UPDATED_TIMESTAMP:kotlin.String) Timestamp (milliseconds since epoch) of when this contact was last updated. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#DISPLAY_NAME:kotlin.String) The display name for the contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_PHONE_NUMBER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#HAS_PHONE_NUMBER:kotlin.String) An indicator of whether this contact has at least one phone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IN_DEFAULT_DIRECTORY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#IN_DEFAULT_DIRECTORY:kotlin.String) Flag that reflects whether the contact exists inside the default directory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IN_VISIBLE_GROUP](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#IN_VISIBLE_GROUP:kotlin.String) Flag that reflects the [Groups.GROUP_VISIBLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.GroupsColumns#GROUP_VISIBLE:kotlin.String) state of any [CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) for this contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_USER_PROFILE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#IS_USER_PROFILE:kotlin.String) Flag that reflects whether this contact represents the user's personal profile entry. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOOKUP_KEY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#LOOKUP_KEY:kotlin.String) An opaque value that contains hints on how to find the contact if its row id changed as a result of a sync or aggregation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME_RAW_CONTACT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#NAME_RAW_CONTACT_ID:kotlin.String) Reference to the row in the RawContacts table holding the contact name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_FILE_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_FILE_ID:kotlin.String) Photo file ID of the full-size photo. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_ID:kotlin.String) Reference to the row in the data table holding the photo. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_THUMBNAIL_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_THUMBNAIL_URI:kotlin.String) A URI that can be used to retrieve a thumbnail of the contact's photo. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String) A URI that can be used to retrieve the contact's full-size photo. |

## Constants

### CONTACT_LAST_UPDATED_TIMESTAMP

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_LAST_UPDATED_TIMESTAMP: String
```

Timestamp (milliseconds since epoch) of when this contact was last updated. This includes updates to all data associated with this contact including raw contacts. Any modification (including deletes and inserts) of underlying contact data are also reflected in this timestamp. 

 Value: "contact_last_updated_timestamp"

### DISPLAY_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME: String
```

The display name for the contact.

Type: TEXT 

 Value: "display_name"

### HAS_PHONE_NUMBER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAS_PHONE_NUMBER: String
```

An indicator of whether this contact has at least one phone number. "1" if there is at least one phone number, "0" otherwise.

Type: INTEGER 

 Value: "has_phone_number"

### IN_DEFAULT_DIRECTORY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IN_DEFAULT_DIRECTORY: String
```

Flag that reflects whether the contact exists inside the default directory. Ie, whether the contact is designed to only be visible outside search. 

 Value: "in_default_directory"

### IN_VISIBLE_GROUP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IN_VISIBLE_GROUP: String
```

Flag that reflects the [Groups.GROUP_VISIBLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.GroupsColumns#GROUP_VISIBLE:kotlin.String) state of any [CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) for this contact. 

 Value: "in_visible_group"

### IS_USER_PROFILE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_USER_PROFILE: String
```

Flag that reflects whether this contact represents the user's personal profile entry. 

 Value: "is_user_profile"

### LOOKUP_KEY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOOKUP_KEY: String
```

An opaque value that contains hints on how to find the contact if its row id changed as a result of a sync or aggregation. 

 Value: "lookup"

### NAME_RAW_CONTACT_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME_RAW_CONTACT_ID: String
```

Reference to the row in the RawContacts table holding the contact name.

Type: INTEGER REFERENCES raw_contacts(_id) 

 Value: "name_raw_contact_id"

### PHOTO_FILE_ID

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_FILE_ID: String
```

Photo file ID of the full-size photo. If present, this will be used to populate [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String). The ID can also be used with [ContactsContract.DisplayPhoto.CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayPhoto#CONTENT_URI:android.net.Uri) to create a URI to the photo. If this is present, [PHOTO_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_ID:kotlin.String) is also guaranteed to be populated.

Type: INTEGER 

 Value: "photo_file_id"

### PHOTO_ID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_ID: String
```

Reference to the row in the data table holding the photo. A photo can be referred to either by ID (this field) or by URI (see [PHOTO_THUMBNAIL_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_THUMBNAIL_URI:kotlin.String) and [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String)). If PHOTO_ID is null, consult [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String) or [PHOTO_THUMBNAIL_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_THUMBNAIL_URI:kotlin.String), which is a more generic mechanism for referencing the contact photo, especially for contacts returned by non-local directories (see [Directory](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Directory)).

Type: INTEGER REFERENCES data(_id) 

 Value: "photo_id"

### PHOTO_THUMBNAIL_URI

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_THUMBNAIL_URI: String
```

A URI that can be used to retrieve a thumbnail of the contact's photo. A photo can be referred to either by a URI (this field or [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String)) or by ID (see [PHOTO_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_ID:kotlin.String)). If PHOTO_ID is not null, PHOTO_URI and PHOTO_THUMBNAIL_URI shall not be null (but not necessarily vice versa). If the content provider does not differentiate between full-size photos and thumbnail photos, PHOTO_THUMBNAIL_URI and [PHOTO_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_URI:kotlin.String) can contain the same value, but either both shall be null or both not null.

Type: TEXT 

 Value: "photo_thumb_uri"

### PHOTO_URI

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_URI: String
```

A URI that can be used to retrieve the contact's full-size photo. If PHOTO_FILE_ID is not null, this will be populated with a URI based off [ContactsContract.DisplayPhoto.CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayPhoto#CONTENT_URI:android.net.Uri). Otherwise, this will be populated with the same value as [PHOTO_THUMBNAIL_URI](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_THUMBNAIL_URI:kotlin.String). A photo can be referred to either by a URI (this field) or by ID (see [PHOTO_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns#PHOTO_ID:kotlin.String)). If either PHOTO_FILE_ID or PHOTO_ID is not null, PHOTO_URI and PHOTO_THUMBNAIL_URI shall not be null (but not necessarily vice versa). Thus using PHOTO_URI is a more robust method of retrieving contact photos.

Type: TEXT 

 Value: "photo_uri"
